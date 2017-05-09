title: Minimum Path Sum
date: 2015-07-19 12:14:42
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Array]
---
## {{ title }} ##

---

给定一个m*n的矩阵，填满了非负数（如果存在负数呢？可以抽象成图，接着利用BellmanFord来求），求从左上角到右下角的最短路径和是多少。

设d[i][j]表示到达grid[i][j]的最短路径和，那么d[i][j] = matrix[i][j] + min(d[i-1][j],d[i][j-1])