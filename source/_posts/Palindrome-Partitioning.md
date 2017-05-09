title: Palindrome Partitioning
date: 2016-07-27 11:40:27
categories: 【LeetCode】
tags: [LeetCode, Backtracking]
---
## {{ title }} ##

---

这道题目可以用回溯来做，判断0到i前的子串是否是回文子串，如果是，那么就判断i+1到结尾的子串是否是回文子串。每次要保留储存字符串的容器。