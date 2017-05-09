title: Largest Divisible Subset
date: 2016-07-06 12:10:06
categories: 【LeetCode】
tags: [LeetCode, Math, Dynamic Programming]
---
## {{ title }} ##

---

这道题目可以用动态规划来实现:

dp[i]表示有序数组nums以nums[i]结尾的子数组中可分割最大子集和的大小是dp[i]。

那么dp[i+1] = max(dp[j]+1 如果nums[i+1] % nums[j] == 0,其中j表示0~i)

因为如果nums[i+1]可以被nums[j]整除的话，表示nums[i+1]和nums[j]可以组成可分割子集

问题是还要求出其中的集合，

这里可以用一个preEle的数组来储存以nums[i]结尾的分割子集的前一个元素的下标

比如序列：1 2 3 4 9 16 27 54 108 120

preEle的序列是

1 0

2 0

3 0

4 1

9 2

8 3

27 4

54 6

108 7

120 5