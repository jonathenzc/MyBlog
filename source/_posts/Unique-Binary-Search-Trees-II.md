title: Unique Binary Search Trees II
date: 2016-08-16 19:47:26
categories: 【LeetCode】
tags: [LeetCode, Tree, Dynamic Programming]
---
## {{ title }} ##

---

利用递归获取start到end的所有节点的集合。用i遍历从start到end，每次获取（start,i-1）作为i节点的左子树，(i+1，end)作为i节点的右子树。