title: Number Complement
date: 2017-01-15 20:24:21
categories: 【LeetCode】
tags: [LeetCode, Bit Manipulation]
---
## {{ title }} ##

---

一种可以用一个比原数大的二的幂来求，比如5的大一位的二次幂是8，那么异或后就是8-1-5=2，需要注意int的上限。

第二种做法是获取每个数位的异或。