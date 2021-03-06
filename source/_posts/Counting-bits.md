title: Counting bits
date: 2016-03-25 14:20:50
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Bit Manipulation]
---
## {{ title }} ##

---

问题是给定一个数n，求范围内0 <= i <= n各个数二进制形式下的1的个数。

给定一个数i，求这个数1的个数，我们可以利用整除取余的方法得到1的个数，也可以利用位运算：将i与1按位与，那么就可以来判断最小位是否为1，接着再将该数左移1位直到0即可。

也就是说这道题目的上限是O(nlogn)的，每次计算一个数1的个数，logn的时间，总共有n个数，那么就是nlogn。

那么这道题目可以利用动态规划的方法，将时间复杂度变成O(n)，空间复杂度变成O(n)。

v[i] = v[i>>1] + i&1

这个方法就是说计算一个数的1的个数，我们可以利用之前去掉最小位的数的1的个数，再加上最小位是否为1。