title: Perfect Square
date: 2016-06-08 16:47:52
categories: 【LeetCode】
tags: [LeetCode, Math, Dynamic Programming, Breadth-first Search]
---
## {{ title }} ##

---

问题是给定一个数num，求加和得到num的完全平方数最少的个数。

这道题目我用的是动态规划来求解，cnt[i]表示加和是i所需的完全平方数的个数的最小值，那么cnt[i] = min{cnt[i-squareSet[j]]}，即由其他完全平方数加和得到i的个数的最小值。