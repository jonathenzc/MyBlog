title: UnsupportedClassVersionError
date: 2016-05-11 22:01:41
categories: 【Java】
tags: [Java]
---
## {{ title }} ##

---

今天在写java的时候报了UnsupportedClassVersionError的错误，java.lang.UnsupportedClassVersionError: Unsupported major.minor version 52.0，提示version 52.0，在网上查了资料后发现可能是引入的包需要用的jdk版本是1.8的，而我的jdk是1.7，所以跑不起来。只要将引入的包调整到jdk 1.7的版本就可以了。

参考资料是

[http://www.cnblogs.com/xing901022/p/4172410.html](http://www.cnblogs.com/xing901022/p/4172410.html "http://www.cnblogs.com/xing901022/p/4172410.html")