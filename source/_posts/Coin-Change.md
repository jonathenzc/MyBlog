title: Coin Change
date: 2016-08-17 23:45:51
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

用dp[i]表示对i进行找零的最小花费，那么dp[i] = min{dp[i-coins[j]],j遍历coins}，最终返回dp[amount]