title: Delete Node in a Linked List
date: 2015-07-15 10:11:49
categories: 【LeetCode】
tags: [LeetCode, Linked List]
---
## {{ title }} ##

---

问题是给定一个要删除的节点，将这个节点从链表中删除。乍一看问题并不难，但是题目只给出要删除的节点，并没有给整个链表的头节点。

所以这道题目可以这样做，将这个要删除的节点的val改成它下一个节点的val，接着将这个节点的next指向它的`next`的`next`。这样看，这个实现就需要保证它的next不为NULL，不然就不能指向`next`的`next`了，也就是说链表的最后一个节点是不能删的，题目中也提出这个被删除的节点不会是最后一个节点。