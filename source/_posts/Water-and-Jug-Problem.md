title: Water and Jug Problem
date: 2016-07-05 22:51:55
categories: 【LeetCode】
tags: [LeetCode, Math]
---
## {{ title }} ##

---

这道题目需要可以抽象成z = ax + by,那么这里需要用到一个定理，就是贝祖定理：若x和y是整数，那么存在整数a和b，使得ax+by = gcd(a,b)。

那么整道题目只需要判断一下z是否是gcd(x,y)的倍数即可。当然不能超过x+y