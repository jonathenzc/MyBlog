title: Maximal Rectangle
date: 2016-07-10 15:17:36
categories: 【LeetCode】
tags: [LeetCode, Array, Hash Table, Stack, Dynamic Programming]
---
## {{ title }} ##

---

这道题目需要用到之前Largest Rectangle in Histogram的做法。维护一个大小为v[0].size()的数组height，该height将记录第i列的从第j行到第0行是1的高度。每次按行来更新该height数组。

比如输入的矩阵是这样的：

0 0 1 0 0 0

0 1 1 1 1 0

1 1 1 1 1 1

1 0 1 1 1 0

那么

在第0行时，height的内容是[0,0,1,0,0,0],

在第1行时，height的内容是[0,1,2,1,1,0],

在第2行时，height的内容是[1,2,3,2,2,1],

在第3行时，height的内容是[2,0,4,3,3,0]。

如果矩阵[i][j]是0，那么height[j]=0；如果是1，那么height[j]++

这样每次对height求Largest Rectangle in Histogram就可以找出最大矩形了。



