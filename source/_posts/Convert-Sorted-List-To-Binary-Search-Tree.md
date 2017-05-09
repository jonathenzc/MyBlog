title: Convert Sorted List To Binary Search Tree
date: 2016-05-18 22:20:59
categories: 【LeetCode】
tags: [LeetCode, Linked List, Depth-first Search]
---
## {{ title }} ##

---

问题是将一个排序的链表转化成二叉搜索树。

我的方法就是每次用龟兔赛跑的方法来得到链表的中间节点，然后将该中间节点的值作为当前子树的根节点。

该子树的左子树为[头节点，中间节点)，

该子树的右子树为[中间节点的下一个节点，尾节点)，都保持左闭右开的规则来构建。