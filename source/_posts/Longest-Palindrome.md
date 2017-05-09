title: Longest Palindrome
date: 2016-10-02 12:14:11
categories: 【LeetCode】
tags: [LeetCode, Contest]
---
## {{ title }} ##

---

统计字符和它出现的次数，统计完后遍历map，如果出现次数是偶数，那么就加入长度和中；如果是奇数那么就加上该数-1。再遍历完后加上一个奇数（如果奇数存在）。