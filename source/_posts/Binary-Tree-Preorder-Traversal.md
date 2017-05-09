title: Binary Tree Preorder Traversal
date: 2015-08-10 11:47:00
categories: 【LeetCode】
tags: [LeetCode, Tree, Stack]
---
## {{ title }} ##

---

问题是对一颗二叉树进行前序遍历。

递归的方法比较简单：

1. 先访问头节点
2. 访问头节点的左子树
3. 访问头节点的右子树

这样就可以实现二叉树的前序遍历了。

迭代的方法利用栈：

在栈不为空的情况下，每次访问栈顶元素并弹栈，将栈顶节点的右子树压入栈中，接着压入左子树。