title: http传二进制流
date: 2017-06-16 11:04:18
categories: 【Http】
tags: [Http]
---
## {{ title }} ##

---

昨天和ios的同事联调，因为数据量大的缘故，我们选择gzip压缩。但是我这边的服务端始终无法解析ios发来的http请求。在排查后，推测可能是header中的content-type影响，最后发现ios在不指明content-type的情况下会默认传**"application/x-www-form-urlencoded"**类型，导致我这边会以x-www-form-urlencoded来解析参数。

当传输的是二进制流的时候，只需要指明content-type为**"application/octet-stream"**就可以了。


参考资料：
[HTTP Content-Type对照表](http://tool.oschina.net/commons)