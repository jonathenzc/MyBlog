title: Binary Tree Maximum Path Sum
date: 2016-04-04 17:24:43
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

问题是给定一个二叉树，求出这棵树中一条路径，该路径上的值的和的最大值。

有这样四种情况来描述路径的值，

1. 当前节点+左子树
2. 当前节点+右子树
3. 当前节点
4. 当前节点+左子树+右子树

利用递归来寻找，先找出1,2,3种情况中，路径之和的最大值，接着将上一个比较的结果与第4种情况进行比较，得出全局的最大值。递归返回的是考虑有父亲节点连向当前节点的情况。
