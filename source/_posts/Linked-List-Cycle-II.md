title: Linked List Cycle II
date: 2016-05-15 19:47:07
categories: 【LeetCode】
tags: [LeetCode, Linked List, Two Pointers]
---
## {{ title }} ##

---

题目是求出一个循环链表的的入口点。如果不是循环链表的话，返回NULL，而且要求不能使用额外的空间。

可以用Hash的方法，将访问过的链表都保存下来，如果发现该节点在HashMap中已经被记录过，那么就返回该节点。

那么如果不用额外的空间呢？

可以这样做，用快、慢节点来进行第一次相遇，如果相遇后，将两个指针分别指向链表的开头和相遇点的后一个节点，开始一个个地指下去。当两者相遇时，相遇的节点就是入口点，原理见参考资料。

参考资料：

[http://www.cnblogs.com/xudong-bupt/p/3667729.html](http://www.cnblogs.com/xudong-bupt/p/3667729.html "http://www.cnblogs.com/xudong-bupt/p/3667729.html")