title: Repeated DNA Sequences
date: 2016-07-03 17:38:26
categories: 【LeetCode】
tags: [LeetCode,Hash Table, Bit Manipulation]
---
## {{ title }} ##

---

我的做法就是从0到s.size()-10去获取所有长度为10的子串，根据这些子串来生成一个map，记录它们出现的次数。最后遍历这个map，如果次数大于1，那么就压入容器中。