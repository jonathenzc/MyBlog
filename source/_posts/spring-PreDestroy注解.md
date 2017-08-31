title: spring PreDestroy注解
date: 2017-08-31 17:42:47
categories: 【Spring Boot】
tags: [Spring Boot]
---
## {{ title }} ##

---

为某个方法加上PreDestroy的注解会在销毁bean之前调用该函数。我用这个注解的目的是为了当需要更新服务，发布新版本时，可以通过这个注解来把数据提前写入数据库。