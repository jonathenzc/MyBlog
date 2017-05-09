title: Wiggle Subsequence
date: 2016-09-02 16:21:41
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Greedy]
---
## {{ title }} ##

---

这道题目我用两个数组dp和dir来实现动态规划的，

dp[i]表示以nums[i]结尾的wiggle序列的最大长度

dir[i]表示以nums[i]结尾的wiggle序列下一个数字是上升还是下降，1表示下一个数字应该上升，0表示都可以，-1表示下一个数字应该下降

dp[i]应该为（0...i-1）中能够组成最长wiggle序列的长度

比如

num   1 17 5 10 13 15 10 5 16 8

dp    1 2 3 4 4 4 5 5 6 7

dir   0 -1 1 -1 -1 -1 1 1 -1