title: Populating Next Right Pointers in Each Node
date: 2015-08-13 14:19:25
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

问题是给定一个完美二叉树，每个树节点除了值、左右节点外，还有个next指针。如果当前结点没有右节点的话，next指向NULL，如果有的话，将指向右边的节点。

我的方法是用队列来储存节点，到节点数达到1，3，7，2n+1个的时候，将他们的next指向NULL。