title: "java.lang.IllegalArgumentException: Request header is too large"
date: 2016-06-02 17:26:48
categories: 【Java】
tags: [Java, Spring mvc]
---
## {{ title }} ##

---

遇到这个问题是因为http get的请求地址是有限的，只需要将get改成post即可。