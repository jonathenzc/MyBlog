title: Valid Anagram
date: 2015-08-02 15:09:52
categories: 【LeetCode】
tags: [LeetCode, Hash Table, Sort]
---
## {{ title }} ##

---

给定两个字符串s和t，判断t是不是s的anagram。Anagram表示一个字符串中的字符是由前一个字符串中的字符组成，但顺序可以不同。

这道题目可以这样做，建立一个字母表的hash，键是26个字母（因为题目中说只能是小写字母），值是单词出现的次数。我们先对s构建映射，接着检查t中的字符，如果字母表中的出现次数是0，说明t中用到了之前s没有的字母，返回false；如果不为0，则将出现次数减1。