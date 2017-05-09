title: Rotate List
date: 2016-05-18 16:15:15
categories: 【LeetCode】
tags: [LeetCode, Linked List, Two Pointers]
---
## {{ title }} ##

---

问题是给定一个链表，1->2->3->4->5->NULL,以及常数k。比如k=2，经过翻转得到4->5->1->2->3->NULL。

这道题目可以先得到整个链表的长度，同时得到最后一个节点a。由翻转的规律可以看到，头节点变成了第size-k+1个节点，那么我们可以再遍历一遍链表，得到新的头节点b以及它的前一个节点c。最后就是将a指向原来的头节点，c指向NULL，b变成新的头节点，再返回。