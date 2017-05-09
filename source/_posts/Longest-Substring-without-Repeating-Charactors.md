title: Longest Substring without Repeating Charactors
date: 2016-06-10 19:28:48
categories: 【LeetCode】
tags: [LeetCode, Two Pointers, Hash Table, String]
---
## {{ title }} ##

---

我的方法是用map来记录访问过的字符，如果该字符没有出现过，那么连续字符串的长度+1，并将该字符更新到map中；如果出现过，获取该字符的上一个下标，如果该下标比字符串开头的下标高，那么开头的下标更新。

我一开始用的是std的map，但效率不高，因为std的map是用红黑树实现的，如果用128大小的数组来记录，会很大的提高效率