title: Triangle
date: 2015-07-19 11:49:36
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Array]
---
## {{ title }} ##

---

给定一个三角形的矩阵，求从上到下最小的路径和，只能走与节点相邻的节点。

这道题目可以用动态规划来做，利用d[MaxSize]来记录，每行的路径和。那么d[i]就是d[i] + min(matrix[i-1][j],matrix[i-1][j+1])