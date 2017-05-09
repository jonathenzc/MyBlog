title: Search a 2D Matrix
date: 2016-06-03 17:05:56
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Array]
---
## {{ title }} ##

---

我的方法是先对第一列的数进行二分搜，找到位置i，当然由于二分的边界问题，我们找到位置后还要进行判断，如果target比matrix[i][0]大，那么i减1；如果直接和matrix[i][0]相等，那么就返回true。