title: House Robber II
date: 2015-07-20 12:15:05
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

问题是之前的House Robber类似，只是将房屋连成了环。这道题目可以这样来做，我们的动态规划还是原来的动态规划，但是可以求两种情况，一种第一个房屋的钱肯定抢走，那么dp[0]和dp[1]的初始状态就是nums[0]，那么只返回dp[size-2]因为最后一个元素不选取；另一种情况是第一个房屋的钱不抢走，直接抢第二个房屋，那么dp[0]和dp[1]的初始状态分别是0和nums[1]，最终返回dp[size-1]。

最后返回dp[size-2]和dp[size-1]的最大值。