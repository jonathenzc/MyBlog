title: Divide Two Integers
date: 2016-05-21 22:38:57
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Math]
---
## {{ title }} ##

---

问题是不能使用乘除和取余操作来计算两整数相除的结果。

我们可以利用左右移的操作来计算，先用右移来得到该数的范围，接着减去该数后继续求它的范围，和二进制的计算很像。

需要注意的是输入的边界值，如果是INT_MIN和-1的输入，那么会溢出，返回的结果应该是INT_MAX.