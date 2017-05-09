title: Palindrome Linked List
date: 2015-07-12 14:38:34
categories: 【LeetCode】
tags: [LeetCode, Linked List, Two Pointers]
---
## {{ title }} ##

---

问题就是判断一个链表是否是回文链表。要求O(n)的时间，O(1)的空间。

我的方法是先找出链表的中间节点，我通过一个快节点和一个慢节点来获取中间节点。

接着将后半段的链表反向，即当前节点指向它的前一个节点。

最后再将前半段链表和后半段链表进行比较，得到该链表是否为回文链表。