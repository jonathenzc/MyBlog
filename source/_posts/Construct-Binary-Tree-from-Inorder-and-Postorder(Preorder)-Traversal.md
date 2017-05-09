title: Construct Binary Tree from Inorder and Postorder(Preorder) Traversal
date: 2016-05-04 14:34:16
categories: 【LeetCode】
tags: [LeetCode, Tree, Array, Depth-first Search]
---
## {{ title }} ##

---

问题是给定经中序遍历和后序遍历后的字符串，问题是根据这两个顺序的字符串，给出正确的二叉树。

根据后序遍历的特点，我们发现后序遍历的最后一个字符就是二叉树的根节点。利用这个根节点去中序遍历的字符串中找出根节点所在的位置，那么由中序遍历的特点，我们知道中序遍历中根节点的左边是二叉树的左子树，右边是二叉树的右子树。

同样的，给定前序和中序也可以得到，前序的第一个字符是根节点。

那么知道前序和后序，能否重构这颗二叉树呢？答案是不行的，比如前序是ab，后序是ba，我们只能知道根节点是啊，但不知道b是a的左子树还是右子树。