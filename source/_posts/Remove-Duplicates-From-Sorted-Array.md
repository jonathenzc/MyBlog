title: Remove Duplicates From Sorted Array
date: 2015-05-25 12:50:00
categories: 【LeetCode】
tags: [LeetCode, Array, Two Pointers]
---
## {{ title }} ##

---

问题是移除有序数组中的重复元素并返回新数组的长度，不能使用额外的空间。我的做法是从头开始扫，用一个指针指向需要填的位置，另一个指针寻找不同的元素，当找到不同元素时将这个元素放到需要填的指针。

题目的参数是vector，我一开始在想是不是得将不用的vector清空，但看了其他人的实现，似乎不用将之后的清空。