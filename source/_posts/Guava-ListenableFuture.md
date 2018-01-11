title: Guava ListenableFuture
date: 2018-01-11 21:18:24
categories: 【java】
tags: [java, Guava]
---
## {{ title }} ##

---

原本搜到jdk1.8的completablefuture，想用join和get来实现一个多线程访问数据库的功能，但发现似乎allList.get()并不能像文档中说的那样等监听的线程都做完再继续执行下去。

最终选择用guava来实现，guava中的回调机制还是很不错的。下面是一个demo，生成10个线程，随机一个线程会挂，最终通过successfulAsList来等所有线程完成后再调用回调结果，太优雅了！

参考资料：

[Guava - 并行编程Futures](http://www.cnblogs.com/whitewolf/p/4113860.html)
[Guava中文](http://ifeve.com/google-guava-listenablefuture/)
[Guava英文](https://github.com/google/guava/wiki/ListenableFutureExplained)

```java
private final static int THREAD_CNT = 10;
public static void main(String[] args) throws Exception {
        ListeningExecutorService executorService = MoreExecutors.listeningDecorator(Executors.newFixedThreadPool(10));
        List<ListenableFuture<Object>> queries = Lists.newArrayList();
        int failedIndex = RandomUtils.nextInt(1, THREAD_CNT);
        for (int i = 1; i < THREAD_CNT; i++) {
            queries.add(testQuery(i, failedIndex, executorService));
        }
        ListenableFuture<List<Object>> successfulQueries = Futures.successfulAsList(queries); //allAsList
        // 绑定任务以及回调函数
        Futures.addCallback(successfulQueries, new FutureCallback<List<Object>>() {
            @Override
            public void onSuccess(List<Object> result) {
                System.out.println(result);
                System.out.println("任务执行成功，对任务进行操作。");
            }
            @Override
            public void onFailure(Throwable t) {
                System.out.println(t.toString());
                System.out.println("任务执行失败");
            }
        });
        executorService.shutdown();
    }
    private static ListenableFuture<Object> testQuery(int type, int failedIndex, ListeningExecutorService executorService) {
        // 执行任务
        ListenableFuture<Object> listenableFuture = executorService.submit(() -> {
            System.out.println("新任务。。。" + type);
            TimeUnit.SECONDS.sleep(type);
            if (type == failedIndex) {
                System.out.println("终止的线程是" + failedIndex);
                throw new RuntimeException();
            }
            return type + "";
        });
        return listenableFuture;
    }
```