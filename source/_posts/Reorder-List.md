title: Reorder List
date: 2016-05-17 23:48:30
categories: 【LeetCode】
tags: [LeetCode, Linked List]
---
## {{ title }} ##

---

给定一个链表L0->L1->...->Ln-1->Ln，将链表重新排序，改变成L0->Ln->L1->Ln-1...->L2->Ln-2。

这道题目可以这样做，先求出整个链表的中心节点Lmid，然后从这个中间节点到底进行逆转得到Ln->Ln-1->...->Lmid，最后对L0->L1->...Lmid和Ln->Ln-1->...Lmid进行归并。