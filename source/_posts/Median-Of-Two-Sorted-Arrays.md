title: Median Of Two Sorted Arrays
date: 2016-08-06 18:58:04
categories: 【LeetCode】
tags: [LeetCode, Array, Binary Search, Divide and Conquer]
---
## {{ title }} ##

---

我没有用分治的做法，用额外的空间来储存两个合并后的有序数组，如果是奇数就返回中间的；如果是偶数就返回两者之和。