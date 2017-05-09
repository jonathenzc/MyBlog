title: Combination Sum IV
date: 2016-07-31 12:29:58
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

这道题目如果像combination I II III那样的递归回溯的方法就会超时。我们换个思路用动态规划的方法来实现，用长度为target+1的数组来作为动态规划的状态数组dp。

dp[i]表示组成和为i的方法由多少种，那么dp[i] = sum(dp[i-nums[j]])，其中j为遍历nums的下标索引。

比如nums=[1,2,3], target=4。那么dp[4] = dp[4-1] + dp[4-2] + dp[4-3]。

在初始化时，如果i为nums中的元素，那么dp[i]为1。