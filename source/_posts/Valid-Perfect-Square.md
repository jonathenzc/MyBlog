title: Valid Perfect Square
date: 2016-07-05 12:13:47
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Math]
---
## {{ title }} ##

---

我一开始用减半求平方根，超时了，之后就用牛顿迭代法求平方根就过了。

后来看了discuss，其实一个平方数16 = 1+3+5+7，即n^2 = 1+3+5+...+(2n-1) = (1+2n-1)*n/2 = n^2