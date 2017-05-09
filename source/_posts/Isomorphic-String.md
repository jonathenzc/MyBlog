title: Isomorphic String
date: 2015-04-30 23:18:21
categories: 【LeetCode】
tags: [LeetCode, Hash Table]
---
## {{ title }} ##

---

输入是两个字符串，问题是看这两个字符串s和t,如果t中的字符可以替换s中的字符，那么这两个字符串是同构的。

比如`egg`和`add`是同构的，e可以由a来替换，g可以由d来替换;

同理，`foo`和`bar`不同构，`paper`和`title`是同构的。

整体算法的思路挺简单的，就是建立一个映射，如果发现两个字符串无法互相映射，那么就不是同构字符串。