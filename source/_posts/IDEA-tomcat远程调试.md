title: IDEA tomcat远程调试
date: 2017-05-22 15:39:23
categories: 【IDEA】
tags: [IDEA, Tomcat]
---
## {{ title }} ##

---

需要在IDEA和远端的tomcat配置一下，原理就是远端tomcat监听一个端口用来远程调试。

IDEA下就是new一个remote的tomcat server，在‘Startup/Connection’下的debug配置端口号。

在远端的tomcat下的catalina.sh添加IDEA中的jpda设置，加在JPDA_OPTS后面。

在远端tomcat下启动catalina.sh jpda start

```shell
JPDA_OPTS="-agentlib:jdwp=transport=dt_socket,address=1043,suspend=n,server=y"
     
/usr/local/tomcat/bin/catalina.sh jpda start
```



参考资料：

[http://blog.csdn.net/mingjie1212/article/details/52281847](http://blog.csdn.net/mingjie1212/article/details/52281847)