title: Combination Sum
date: 2016-07-28 17:33:41
categories: 【LeetCode】
tags: [LeetCode, Array, Backtracking]
---
## {{ title }} ##

---

使用递归回溯，传入的是index，求得到的和，储存数列的矩阵。

如果和等于target，那么就压入矩阵。

如果不想等，那么就遍历candidates，如果和加上candidates的元素小于等于target时，才能递归访问。