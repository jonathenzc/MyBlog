title: Minimum Size Subarray Sum
date: 2016-08-02 00:19:44
categories: 【LeetCode】
tags: [LeetCode, Array, Two Pointers, Binary Search]

---
## {{ title }} ##

---

一开始把subarray看成不连续了，想直接排个序就可以了。

遍历数组，用left和right两个指针来记录subarray的长度，在循环中先找到一个候选的subarray，然后用left逐个减去元素，指导sum比s小。