title: 3Sum
date: 2016-07-10 19:42:02
categories: 【LeetCode】
tags: [LeetCode, Array, Two Pointers]
---
## {{ title }} ##

---

这道题目可以先使用2Sum的方法，就是先对数组排序，再用两个指针分别从头和尾来遍历，

如果两数和为target，那么就保留该结果，并将tail往前挪，head往后挪一位；

如果和大于target，说明tail指向的数大了，需要往前挪一位；

如果和小于target，说明head指向的数小了，需要往后挪一位；

那么3Sum也可以利用相同的方法，也是先排序，再从头开始取一个数，然后用target减去该数，用除去该数的集合和差来求2Sum。

这里需要注意的就是-2 0 0 2这样有重复数的情况，如果target是0，那么-2 0 2有两组，我们可以在遍历的时候去重。在求2Sum中也需要处理相同数的情况。


参考资料：

[http://blog.csdn.net/doc_sgl/article/details/12462151](http://blog.csdn.net/doc_sgl/article/details/12462151 "http://blog.csdn.net/doc_sgl/article/details/12462151")