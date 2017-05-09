title: Sort List
date: 2016-05-16 18:09:20
categories: 【LeetCode】
tags: [LeetCode, Linked List, Sort]
---
## {{ title }} ##

---

问题是对链表进行排序，时间复杂度是O(nlogn)，但只能使用固定的空间。

看到O(nlogn)，一开始想到的是用快排来实现，因为归并要用到额外的空间。但这道题目的数据会让快排的复杂度退化到N^2。仔细分析后，由于操作的是链表，所以在归并的时候不需要额外的空间。