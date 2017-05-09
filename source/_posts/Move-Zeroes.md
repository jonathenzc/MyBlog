title: Move Zeroes
date: 2016-02-06 18:31:02
categories: 【LeetCode】
tags: [LeetCode, Array, Two Pointers]
---
## {{ title }} ##

---

给定一个数组，将数组中的0全部挪到数组的最后，其余的数保持原来数组中的顺序。

这道题目可以这样做，获取某数前的0的个数，将该数往前挪动0个数个位置，这样就可以保持原数组中数的顺序，最后再将0塞到数组的最后。