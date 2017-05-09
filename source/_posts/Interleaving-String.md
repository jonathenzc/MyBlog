title: Interleaving String
date: 2016-06-20 19:55:12
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, String]
---
## {{ title }} ##

---

一开始我用回溯，结果超时了，看了解答是用动态规划来做。

dp[i][j]表示s3[0...i+j-1]能否被s1[0...i-1]和s2[0...j-1]交织组合起来。

那么dp[i][j]由(dp[i-1][j]和s1[i-1]==s3[i+j-1])或(dp[i][j-1]和s2[j-1]==s3[i+j-1])决定。