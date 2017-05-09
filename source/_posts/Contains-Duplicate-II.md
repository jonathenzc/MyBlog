title: Contains Duplicate II
date: 2015-06-01 15:48:54
categories: 【LeetCode】
tags: [LeetCode, Array, Hash Table]
---
## {{ title }} ##

---

给定一个整数数组nums和一个整数k，找出在数组中是否存在两个不同的下标i和j，使得nums[i]和nums[j]相等且i和j的差值最多为k。

对于这个问题，我一开始用的是暴力搜索，结果超时了。之后看到问题的标签是Hash Table，心想应该用map来做。

我的方法是遍历数组，如果在map中没有找到表示这个数还没有出现过，那么存入map并记录这个数的下标。

如果找到了，返回这个数曾经出现的下标位置，接着判断这个数曾经和当前的位置的差值是否在正负k的范围内，如果在范围内，那么返回true；如果超出范围，更新这个数的位置。