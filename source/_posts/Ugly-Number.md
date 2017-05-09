title: Ugly Number
date: 2015-08-19 18:02:08
categories: 【LeetCode】
tags: [LeetCode, Math]
---
## {{ title }} ##

---

如果一个正整数的质因数中存在2，3，5以外的数就不是ugly数了。问题是判断一个数是否为ugly数。1认为是ugly数

我的方法是当数小于等于0的时候，返回false。接着消除2 3 5的质因数。先不断整除2得到没有质因数2的数，然后消除3和5的。最终的结果为1的话，那么这个数就是ugly数，反之不是ugly数。