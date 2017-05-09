title: Search Insert Position
date: 2015-08-09 12:56:31
categories: 【LeetCode】
tags: [LeetCode, Array, Binary Search]
---
## {{ title }} ##

---

给定一个有序整数数组和一个整数，找出该数在这个数组中的位置。

比如：
[1,3,5,6], 5 → 2

[1,3,5,6], 2 → 1

[1,3,5,6], 7 → 4

[1,3,5,6], 0 → 0

这道题目我看到有序数组，就想到可以利用二分来找。唯一麻烦的就是要返回正确的下标索引。

我这里是将start设为0，end设为数组大小，判断条件是start<end就执行循环。mid是(start+end)/2。如果目标大于mid的话，start为mid+1；如果小于mid的话，end为mid。

这样的话在最终跳出循环的时候还要判断一下如果没有找到且mid<end的数，那么mid就加1。

最终返回的是mid