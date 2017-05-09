title: Subsets II
date: 2016-08-01 18:32:55
categories: 【LeetCode】
tags: [LeetCode, Array, Backtracking]
---
## {{ title }} ##

---

思路和combination sum II是一样的，先排序，再根据当前循环遍历的下标是否是第一个或者不是第一个且当前元素与前一个元素不同来进入递归。