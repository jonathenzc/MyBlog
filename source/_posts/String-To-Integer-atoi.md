title: String To Integer(atoi)
date: 2015-05-17 00:18:33
categories: 【LeetCode】
tags: [LeetCode, Math, String]
---
## {{ title }} ##

---

问题就是将字符串转化成整数，实现一个atoi函数的功能。

1. 先找出第一个非空格字符
2. 处理符号问题
3. 接着每个数位进行处理
	1. 如果找到非数字字符，则返回0
	2. 检查是否会溢出