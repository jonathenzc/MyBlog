title: Binary Tree Zigzag Level Order Traversal
date: 2015-06-09 16:44:33
categories: 【LeetCode】
tags: [LeetCode, Tree, Breadth-first Search, Stack]
---
## {{ title }} ##

---

这道题目的问题要求和[Binary Tree Level Order Traversal](/2015/05/24/Binary-Tree-Level-Order-Traversal/)很像，只是这道题目访问树中节点的方法不是每排从左到右的访问，而是一个“Z字形”的方式再访问，比如下图

<img src="/img/BinaryTreeLevelOrder.png"  class="img-shadow img-center"/>

它的访问方式就是先访问3，接着是20、9，然后访问15、7。

这道题目我的做法就是在之前这道题目的基础上，每当偶数行的时候将vector逆转一下，就得到了“Z字形”的访问。