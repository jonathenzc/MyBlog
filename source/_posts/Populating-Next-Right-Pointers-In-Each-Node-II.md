title: Populating Next Right Pointers In Each Node II
date: 2016-04-08 00:11:16
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

给定一颗二叉树，要将每层的节点指向右边的节点，如果右边没有节点，则指向NULL。

这道题目可以利用广搜，用队列存每层要访问的节点，其中每个节点再记录一下当前所在的层数，这样就可以知道何时可以指向NULL。