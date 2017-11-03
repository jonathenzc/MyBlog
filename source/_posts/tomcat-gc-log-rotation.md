title: tomcat gc log rotation
date: 2017-11-03 16:17:38
categories: 【java】
tags: [java]
---
## {{ title }} ##

---

java启动时添加gc log的参数，如果从jvm启动后，一直没有结束，那么gc log会越来越大，我们可以通过rotation的方法来让新的gc log覆盖原来的内容。

参考资料：

[gc log rotation](https://blog.gceasy.io/2016/11/15/rotating-gc-log-files/)

