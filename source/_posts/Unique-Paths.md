title: Unique Paths
date: 2015-07-18 13:17:32
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Array]
---
## {{ title }} ##

--- 

问题就是给定m*n的空间，求从(0,0)坐标到(m-1,n-1)的路径数，只能向下或者向右走。

这道题目是典型的动态规划，设d[i][j]表示到(i-1,j-1)的路径数，在初始化的时候可以将第一行和第一列都初始化为1。

d[i][j]取决于d[i-1][j]+d[i][j-1]