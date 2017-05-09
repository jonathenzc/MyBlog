title: Same Tree
date: 2015-05-27 21:56:21
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

问题是判断两棵树是否相同，就是两棵树的结构和节点上的值相同。我使用的方法和之前判断一棵树是否对称的方法一样，先判断两颗树的根节点是否同时为空节点，如果是，那么返回true，如果两个都是空，那么返回false，如果都不为空，那么进入迭代，判断两棵树的左子树是否相同且右子树是否相同，当两个情况都成立则返回true。