title: Subsets
date: 2016-07-10 09:48:38
categories: 【LeetCode】
tags: [LeetCode, Backtracking, Bit Manipulation]
---
## {{ title }} ##

---

我的方法是使用递归回溯的方法，每次传入函数的参数有一个当前集合，和刚刚压入集合的数字的下标。在函数开始时先压入当前集合，接着从下标的下一个开始遍历，调用该递归函数即可。

需要注意空集是任何集合的子集。