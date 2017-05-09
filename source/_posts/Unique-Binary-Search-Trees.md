title: Unique Binary Search Trees
date: 2015-07-18 15:38:17
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Trees]
---
## {{ title }} ##

---

这道题目是给定一个值n，求出有n个节点的二叉搜索树。

这道题目是用动态规划来做，设d[i]表示有i个节点的BST个数。0个节点的时候为1，1个节点的时候为1，2个节点的时候为2。

我们可以从左右子树的角度来思考问题，d[i]的值取决于左右子树可能的组合情况，比如求d[5]，那么左子树的节点可能为0到4，相应的右子树的节点可能为4到0，所以

d[5] = d[0]\*d[4]+d[1]\*d[3]+d[2]\*d[2]+d[3]\*d[1]+d[4]\*d[0]