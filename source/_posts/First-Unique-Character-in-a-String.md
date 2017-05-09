title: First Unique Character in a String
date: 2016-08-25 16:53:17
categories: 【LeetCode】
tags: [LeetCode]
---
## {{ title }} ##

---

我用map来储存之前访问过的char和个数的映射。如果当前字符和候选字符相同，那么就往候选字符后面寻找。