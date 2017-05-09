title: Path Sum
date: 2015-05-21 19:16:32
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

给定一个二叉树和一个整数，求在一条从根节点到叶子节点的路径上所有权值之和是否等于这个给定整数。如果有，那么返回True；没有，返回False。比如下面这样的二叉树，整数是22，有5->4->11->2这样的路径使得路径上权值之和为22。

<img src="/img/PathSum.png"  class="img-shadow img-center"/>

我的做法是对这棵树进行深搜，利用栈来实现对树的搜索。这里需要记录树的节点以及截止这个节点的权值和。