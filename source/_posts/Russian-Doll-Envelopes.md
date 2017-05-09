title: Russian Doll Envelopes
date: 2016-08-22 14:18:28
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Binary Search]
---
## {{ title }} ##

---

这道题目我先对pair的first进行排序，接着利用动态规划dp[i]表示最大的套娃为envelopes[i]所能套的娃的个数，那么dp[i]就取决于0~i中能被envelopes[i]套中的娃的个数。