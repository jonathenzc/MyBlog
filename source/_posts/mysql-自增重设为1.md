title: mysql 自增重设为1
date: 2016-05-21 11:10:14
categories: 【Mysql】
tags: [Mysql]
---
## {{ title }} ##

---

我们经常会为mysql的表的主键设置为1，有时候为了测试，会往表中插入很多测试数据，主键也跟着自增。当我们想将这些测试数据清空后，再重新插入数据的时候发现主键仍然以之前的最大值进行自增。那么如何将表的主键重新设成从1开始自增的呢？

可以使用truncate table [你的表名]

参考资料：

[http://www.cnblogs.com/shangxia/p/4667363.html](http://www.cnblogs.com/shangxia/p/4667363.html "http://www.cnblogs.com/shangxia/p/4667363.html")