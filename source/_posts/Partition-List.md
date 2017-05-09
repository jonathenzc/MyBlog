title: Partition List
date: 2016-05-15 22:01:01
categories: 【LeetCode】
tags: [LeetCode, Linked List, Two Pointers]
---
## {{ title }} ##

---

给定一个链表和一个数，调整链表的顺序，使得比x小的数都在比x大的数左边，调整后的相对位置和调整前一样。

一开始把这道题目看到快排中的划分了。我的方法是构建两个链表，分别是储存比x小的数smallList，和x大的数bigList。遍历链表，将小的数塞到smallList后，不比x小的数塞到bigList后。