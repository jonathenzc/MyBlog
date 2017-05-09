title: Unique Path II
date: 2015-07-18 14:33:36
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Array]
---
## {{ title }} ##

---

这个问题和上一道问题很像，只是这次加入了限制，如果这个m*n中存在“障碍”，那么这个坐标是不能到达的。

所以我们只需要在动态规划的时候判断当前坐标是否为障碍，如果是障碍的话，d[i][j]就为0，为什么没有路径可以到达坐标。