title: IDEA + spring boot 热部署
date: 2017-05-25 18:00:34
categories: 【IDEA, Spring Boot】
tags: [IDEA, Spring Boot]
---
## {{ title }} ##

---

Spring Boot会直接通过Tomcat启动，如果前端文件我采用的是thymeleaf，如果我改一个前端文件想看效果，但是每次都起服务器太慢了，其实可以打快捷键ctrl+F9或者工具栏中的Build->Build Project也可以。会直接将Build目录下的改动添加进去。这样就完成了前端的热部署。

同时还要配置thymeleaf的内容

```yaml
server:
    port: 8081

spring:
    thymeleaf:
        mode: LEGACYHTML5
        cache: false
```