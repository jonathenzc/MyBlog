title: Generate Parentheses
date: 2016-06-11 12:49:02
categories: 【LeetCode】
tags: [LeetCode, String, Backtracking]
---
## {{ title }} ##

---

我的方法是用递归回溯后来寻找成对的括号字符串，用left和right分别表示左括号、右括号使用的数量。

当right比left多的时候就不返回，因为这种情况非法；当left和right都为n，那么括号找到返回结果；没到，那么就当left<n时，在传入的字符串后塞入(;当right<n时，在传入的字符串后塞入）