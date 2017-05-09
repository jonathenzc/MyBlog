title: Merge k Sorted Lists
date: 2016-05-16 18:09:09
categories: 【LeetCode】
tags: [LeetCode, Linked List, Heap, Divide and Conquer]
---
## {{ title }} ##

---

对传入储存链表的容器进行遍历，对容器的i和i+1项进行两两归并，将归并后的链表头更新到容器的i+1项，最终返回容器的最后一个即可。