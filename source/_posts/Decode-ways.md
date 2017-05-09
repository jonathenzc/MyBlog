title: Decode ways
date: 2016-06-19 11:16:30
categories: 【LeetCode】
tags: [LeetCode, String, Dynamic Programming]
---
## {{ title }} ##

---

我的做法是用动态规划，waysCnt[i]表示字符串的子串s[0...i]能够被解码的个数，那么waysCnt[i]由waysCnt[i-1]和waysCnt[i-2]决定。

waysCnt[i-1]的值由s[i]决定，如果s[i]是非0数，那么waysCnt[i-1]可以被加入到waysCnt[i]中；

waysCnt[i-2]的值由s[i-1...i]决定，如果s[i-1...i]是小于27,那么waysCnt[i-2]可以被加入到waysCnt[i]中。

初始值，waysCnt[0]为1和waysCnt[1]为1如果s[0]是非0数；为0如果s[0]是0
