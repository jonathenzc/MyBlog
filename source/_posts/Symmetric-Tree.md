title: Symmetric Tree
date: 2015-05-26 18:24:27
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

这个问题是求一棵树是否是对称的，比如下面这颗树就是对称的。

<img src="/img/TrueSymmetricTree.png"  class="img-shadow img-center"/>

但这棵树就不是对称的。

<img src="/img/FalseSymmetricTree.png"  class="img-shadow img-center"/>

这道题目我使用递归来实现。

1. 先对根节点进行判断，如果为空，返回true；不为空，如果它的左右子树都为空，那么返回true。如果一个为空一个不为空，那么返回false。如果都不为空，判断这两颗左右子树是否对称(进入递归函数)
2. 进入递归函数，如果两节点中有一个为空另一个不为空，那么返回false，如果都不为空，判断两个节点的值是否相等，相等的话就进入迭代函数，判断左边的左边是否等于右边的右边且左边的右边等于右边的左边，如果等返回true，不等就返回false。