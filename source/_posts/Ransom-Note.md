title: Ransom Note
date: 2016-08-14 19:26:03
categories: 【LeetCode】
tags: [LeetCode, String]
---
## {{ title }} ##

---

先对magazine构建一个<char,int>的映射，int用来记录magazine中字符的个数。

然后遍历ransomNote，如果发现字符的个数是0，那么就返回false，如果不是，那么就把个数-1。