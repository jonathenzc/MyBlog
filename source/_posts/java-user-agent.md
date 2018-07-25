title: java user agent
date: 2018-07-25 11:48:34
categories: 【Java】
tags: [Java]
---
## {{ title }} ##

---

依赖UserAgentUtils

```
<dependency>
    <groupId>nl.bitwalker</groupId>
    <artifactId>UserAgentUtils</artifactId>
    <version>1.2.4</version>
</dependency>
```

代码获取浏览器、操作系统等信息

```java
//获取浏览器信息
String ua = request.getHeader("User-Agent");
//转成UserAgent对象
UserAgent userAgent = UserAgent.parseUserAgentString(ua); 
//获取浏览器信息
Browser browser = userAgent.getBrowser();  
//获取系统信息
OperatingSystem os = userAgent.getOperatingSystem();
//系统名称
String system = os.getName();
//浏览器名称
String browserName = browser.getName();
```

参考资料：

[user agent js](https://github.com/fex-team/ua-device)

[user agent js demo](http://fex-team.github.io/ua-device/)

[user agent java](https://www.cnblogs.com/always-online/p/4846311.html)

[获得浏览器User-agent的方法](https://blog.csdn.net/a491857321/article/details/51775115)

[java 获取浏览器请求头获取浏览器、系统信息](https://www.sojson.com/blog/223.html)