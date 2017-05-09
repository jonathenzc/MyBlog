title: Linked List Cycle
date: 2015-08-07 13:20:21
categories: 【LeetCode】
tags: [LeetCode, Linked List, Two Pointers]
---
## {{ title }} ##

---

问题是从链表中查找是否存在环。我用的方法就是设置两个指针，一个慢指针，每次只指向下一个节点，另一个快指针，每次指向下一个节点的下一个节点，当两个指针指向的地址相同的时候，就能判断链表中是否存在环。

需要注意的是空指针的判断。