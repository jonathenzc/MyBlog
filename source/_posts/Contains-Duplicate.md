title: Contains Duplicate
date: 2015-05-26 10:45:01
categories: 【LeetCode】
tags: [LeetCode, Array, Hash Table]
---
## {{ title }} ##

---

问题是找出一组数列中的元素是否包含相同的数，如果有返回true；如果没有则返回false。

这里我使用map来储存访问过的元素，如果在map中出现过，那么就返回true，如果访问结束也没有发现，那么就返回false。