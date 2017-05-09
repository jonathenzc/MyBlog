title: Binary Tree Level Order Traversal II
date: 2015-05-24 22:20:38
categories: 【LeetCode】
tags: [LeetCode, Tree, Breadth-first Search]
---
## {{ title }} ##

---

问题的内容和上一道差不多，只是这次的顺序是从下往上。所以我这里使用栈来先存一下每一层的内容，接着将栈内的内容压入vector中。