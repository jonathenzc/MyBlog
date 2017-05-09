title: Missing Number
date: 2016-02-05 12:33:19
categories: 【LeetCode】
tags: [LeetCode, Array, Math, Bit Manipulation]
---
## {{ title }} ##

---

问题是给定一个包含n个不同数的数组，数组应该包括0到n中的所有数。需要找出缺少的数是哪个，比如数组是[0,1,2]，那么缺少3；[0,1,3]，那么缺少2。

这道题目可以用数学的方法求出应有的和为n*(n+1)/2，和现有的总和的差值，就是我们的缺失数。