title: Binary Search Tree Iterator
date: 2016-08-17 15:54:03
categories: 【LeetCode】
tags: [LeetCode, Tree, Stack, Design]
---
## {{ title }} ##

---

我一开始是用队列来中序储存整棵树，但是这样的空间复杂度是O(n)。但是实际上只需要O(h)的空间，用栈来储存树节点，在初始化时先把所有左边的节点压入栈中，在弹栈时再调用该函数来压入所有的左节点。