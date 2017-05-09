title: Number of Boomerangs
date: 2017-02-09 21:07:11
categories: 【LeetCode】
tags: [LeetCode, Hash Table]
---
## {{ title }} ##

---

这道题目我的方法是用O(N^2)+hash的方法来实现的。O(N^2)用来计算每个节点与其他节点的距离映射，在计算好当前节点与其他节点的距离后，遍历map，如果当前映射不为1，说明与该节点有两个距离的点，最后加上每个key的map[key]*(map[key]-1)。