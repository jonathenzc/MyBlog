title: Remove Duplicate Letters
date: 2016-08-24 17:21:20
categories: 【LeetCode】
tags: [LeetCode, Stack, Greedy]
---
## {{ title }} ##

---

需要记录字符串中字符出现的个数，一个记录返回值的栈，以及一个数组来记录字符是否被添加进栈中。

遍历整个字符串，来决定当前字符的位置

出现的个数-1

如果当前字符没有被访问过，对栈顶的元素进行循环判断，如果栈顶元素的个数为0，说明该字符必须得加进返回值中，因为后面已经不再出现该字符；同时栈顶字符大于当前字符，那么当前字符需要与栈顶元素调整位置。

注意，字符串可以认为是字符类型的栈。