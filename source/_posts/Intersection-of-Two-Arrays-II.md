title: Intersection of Two Arrays II
date: 2016-06-03 13:24:59
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Hash Table, Two Pointers,Sort]
---
## {{ title }} ##

---

我的方法是用map来记录一个数组中数字和它出现次数的映射，接着遍历另一个数组，如果找到数且出现次数不为0，那么出现次数减1,并将该数塞入结果集。