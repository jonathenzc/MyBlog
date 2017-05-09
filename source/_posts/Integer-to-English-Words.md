title: Integer to English Words
date: 2016-06-03 20:12:45
categories: 【LeetCode】
tags: [LeetCode, Math,String]
---
## {{ title }} ##

---

我的方法是先将输入通过整除10，取余10得到每位上的数，接着将数补全到10位（2^32-1是21亿），然后每3个数进行处理。