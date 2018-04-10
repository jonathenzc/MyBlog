title: python string set charactor
date: 2016-05-03 22:48:00
categories: 【Python】
tags: [Python]
---
## {{ title }} ##

---

因为python中的字符串是不可改变的，那么如何来改变一个python string的某一个字符呢？比如a="abcdefg",a[1] = e

可以通过list来改变

a = "abcdefg"
s = list(a)
s[1] = e
b = "".join(s)