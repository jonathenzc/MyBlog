title: Range Sum Query Immutable
date: 2016-08-17 23:22:42
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

一开始我是用一个二维数组来储存结果的，即dp[i][j]表示范围i到j的和。结果报了内存空间太大的错误，经改进，可以用一维数组来记录下标0到i的数的和，即dp[i+1]表示nums[0]+nums[1]+...+nums[i]的和。返回的时候就只需要返回dp[j+1]-dp[i]即可。