title: Guess Number Higher or Lower
date: 2016-07-17 16:53:49
categories: 【LeetCode】
tags: [LeetCode, Binary Search]
---
## {{ title }} ##

---

这道题目我就用常规的二分搜索来做，但是在碰到大数的时候会遇到问题，因为要找中间的数，那么中间的数是根据(start+end)，如果数很大的话就会越界。所以用long long来存这些变量即可。

(start+end)/2可以用start+(end-start)/2来处理