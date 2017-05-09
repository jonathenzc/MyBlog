title: Single Number II
date: 2015-08-17 23:03:42
categories: 【LeetCode】
tags: [LeetCode, Bit Manipulation]
---
## {{ title }} ##

---

问题是一个整数数组，里面只有一个元素出现了一次，其余的元素都出现了3次，现在需要找出这个只出现了一次的数。

我的方法是用map来存储出现过的数，键是数，值是出现的次数，最后遍历map找出出现次数是一个的数、