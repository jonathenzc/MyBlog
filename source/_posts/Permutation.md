title: Permutation
date: 2016-08-02 11:56:57
categories: 【LeetCode】
tags: [LeetCode, Backtracking]
---
## {{ title }} ##

---

我一开始是用一个nums大小的bool数组来储存该元素是否使用过，然后利用递归回溯来得到排列。

看了解答，发现可以用交换数字来得到排列。

比如一开始1 2 3，交换后面小的数，变成1 3 2.