title: Intersection of Two Arrays
date: 2016-06-03 13:12:31
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Hash Table, Two Pointers,Sort]
---
## {{ title }} ##

---

我的方法是先用map保存一个数组的数和出现次数，接着根据这个map去遍历另一个数组，如果在map中找到，且出现次数是1，那么就压入返回的结果集中。