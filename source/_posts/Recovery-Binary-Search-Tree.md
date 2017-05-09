title: Recovery Binary Search Tree
date: 2016-08-16 19:47:11
categories: 【LeetCode】
tags: [LeetCode, Tree, Depth-first Search]
---
## {{ title }} ##

---

可以利用中序遍历的方法来获取在顺序中不对的两个元素，因为中序遍历一个BST就是顺序排列的。当最终找到两个位置不对的节点，再交换两个节点即可。