title: Intellij开发Zookeeper
date: 2019-02-26 20:39:25
categories: 【IDEA】
tags: [IDEA]
---
## {{ title }} ##

---

用第一个链接中的话“没有一个项目的工具链像 ZooKeeper 这样陈旧，还在用 Ant 管理项目，用 Ivy 下载依赖，用 jute 定义 RPC……简直就是在逛古董店啊”

我起初是通过Open一个项目然后用Ant Build引入根目录的build.xml来构建依赖，但后来会卡住会报错。之后google了一下，发现其实可以先利用ant把zk源码转成eclipse项目，然后再用intellij导入eclipse项目。

总共就三个步骤：

1. 下载并安装ant环境，下载zookeeper源码；
2. 在zk根目录下输入ant eclipse（如果发现报错，将eclipse下载的地址更改一下即可，参考[Zookeeper 源码环境搭建](https://blog.csdn.net/zhangyuan19880606/article/details/51508294)）；
3. 通过intellij导入zookeeper项目；


参考资料：

[在 IntelliJ IDEA 中定制开发 ZooKeeper](https://yq.aliyun.com/articles/60105)

[Zookeeper源码 intellij idea 开发环境搭建](https://blog.csdn.net/fujianfafu/article/details/80307240)

[Zookeeper 源码环境搭建](https://blog.csdn.net/zhangyuan19880606/article/details/51508294)

[IntelliJ IDEA导入ZooKeeper源码](https://www.jianshu.com/p/5c410ced697d)