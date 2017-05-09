title: Top K Frequent Elements
date: 2016-05-08 15:38:45
categories: 【LeetCode】
tags: [LeetCode, Hash Table,Heap]
---
## {{ title }} ##

---

这个题目是求频率为前K的元素有多少个，比如[1,1,1,2,2,3]，如果k为2的话，那么返回[1,2]

这道题目我是利用求第k大的方法来实现的，首先遍历数列，得到该数和其频率的映射，然后对频率求第k大的数。