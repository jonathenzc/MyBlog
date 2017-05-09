title: Valid Word Abbreviation
date: 2016-10-02 12:14:03
categories: 【LeetCode】
tags: [LeetCode, Contest]
---
## {{ title }} ##

---

用两个下标来记录word和abbr的位置，记录abbr中出现的数字，word的下标加上数字如果不等于abbr下标指向的字符，那么返回false。需要注意"01","a"与"0a"这样的情况