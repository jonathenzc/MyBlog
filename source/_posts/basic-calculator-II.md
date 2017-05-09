title: basic calculator II
date: 2016-06-10 19:28:29
categories: 【LeetCode】
tags: [LeetCode, String]
---
## {{ title }} ##

---

整体思路和basic calculator一样，也是先转化成逆波兰表达式然后求解。

如果当前符号的优先级比栈中的符号优先级高，将当前符号压入栈中；当前符号优先级小于等于栈中的元素，那么弹栈。