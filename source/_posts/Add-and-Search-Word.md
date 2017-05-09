title: Add and Search Word
date: 2016-06-19 17:21:40
categories: 【LeetCode】
tags: [LeetCode, Design, Backtracking, Trie]
---
## {{ title }} ##

---

我的做法是构建前缀树，然后addWord就调用Trie的insert函数，search的时候，如果当前字符是'.'，那么就把当前字符变成a到z然后枚举搜索。