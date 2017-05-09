title: Lowest Common Ancestor of a Binary Tree
date: 2016-04-06 16:54:53
categories: 【LeetCode】
tags: [LeetCode, Tree]
---
## {{ title }} ##

---

问题是给定一颗二叉树以及两个这棵树中的节点，求这两个节点的最小公共祖先。

这道题目我的做法是利用深搜记录这两个节点的路径，接着遍历这个路径，当找到第一个两条路径的不同节点时，返回前一个节点即可。