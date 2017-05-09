title: Combination Sum II
date: 2016-07-30 23:54:41
categories: 【LeetCode】
tags: [LeetCode, Array, Backtracking]
---
## {{ title }} ##

---

思路和Combination Sum一样，只是得先排个序，然后再每次递归前判断一下，当前循环遍历的下标是否是第一个或者不是第一个且当前元素与前一个元素不同，那么就可以进入递归。