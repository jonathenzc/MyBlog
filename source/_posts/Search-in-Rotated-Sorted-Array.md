title: Search in Rotated Sorted Array
date: 2016-08-07 23:26:51
categories: 【LeetCode】
tags: [LeetCode, Array, Binary Search]
---
## {{ title }} ##

---

先找到最小的元素下标，接着判断target和数组中最后一个数的大小，如果比最后一个数大，那么就从0左边的范围进行二分；如果小，那么就在右边进行二分查找。