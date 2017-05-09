title: Count Numbers With Unique Digits
date: 2016-07-05 10:55:43
categories: 【LeetCode】
tags: [LeetCode,Dynamic Programming, Backtracking, Math]
---
## {{ title }} ##

---

下面是数字位数与不同数位的数字个数的映射

1 10

2 9*9

3 9*9*8

4 9*9*8*7

也就是说numCnt(n) = 9*9*8...*(11-n)

最后再将之前的个位数加起来即可。 