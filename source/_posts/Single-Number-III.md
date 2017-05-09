title: Single Number III
date: 2015-08-19 18:01:47
categories: 【LeetCode】
tags: [LeetCode, Bit Manipulation]
---
## {{ title }} ##

---

给定一个正数数组，其中只有两个数是出现1次，其余的数都出现过2次。

我的方法和之前的方法一样，利用map来计算，键值对表示出现的数和它出现的次数。在第一次遍历的时候可以得到数和出现次数的映射，在进行第二次遍历的时候将出现次数为2次的数压入容器中。