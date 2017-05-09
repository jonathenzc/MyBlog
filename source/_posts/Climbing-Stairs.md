title: Climbing Stairs
date: 2015-06-01 14:54:04
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

问题是现在需要爬楼梯，需要`n`步可以爬到顶楼，每次只能爬`1`
步或者`2`步。那么总共有多少不同的方法可以爬到顶楼。

这里我利用动态规划来求解，设waysToTop[i]表示当需要i步可以爬到顶楼的方法数。那么waysToTop[i] = waysToTop[i-1] + waysToTop[i-2]，其中waysToTop[0]和waysToTop[1]的值为1。最终返回waysToTop[n]。