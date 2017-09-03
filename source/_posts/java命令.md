title: java命令
date: 2017-09-03 15:48:43
categories: 【java】
tags: [java]
---
## {{ title }} ##

---

# JPS #

jps（Java virtual machine Process Status）命令可以显示当前运行的java进程及其ID，它实现的机制就是在/tmp/下有多个以hsperfdata_{user}的目录，把这些目录里的java pid汇总起来。当然执行了jps后，会看到一个Jps的java pid，那是因为他也是个java命令。Jps的可执行程序在JAVA_HOME/bin目录下。

常用的参数是-l（输出完整的jar包），-m（输出传递给main函数的参数），-v（输出jvm的参数）

jps只能显示当前用户的，因为它是读tmp文件夹的。"ps -ef | grep java"的命令更加保险点。


参考资料：

[Java命令学习系列](http://www.hollischuang.com/archives/105)