title: js中为什么‘''== 0 为true
date: 2018-04-28 17:29:55
categories: 【jQuery】
tags: [jQuery]
---
## {{ title }} ##

---

javascript中为什么(''==0)和(' '==0)都为真。

两边类型不相同出现以下情况：

0为假即false

空值也或空格也为false

false==false恒成立
 
**只有两边类型相同时才可以真正对比是否完全一样**

比如"a"=="b"返回false

1==2返回false

另：如果真想判断空字符串和0是否相等，可以用(''===0)这样就是false了，

**即判断不相同类型的两个值可以用===**