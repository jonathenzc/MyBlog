title: word Break
date: 2015-07-10 23:09:09
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

问题是给定一个字符串s和一个由单词组成的“字典”（数据类型是unordered_set），现在要求出这个字典中是否存在可以组成s的单词组合。

比如s="leetcode"，dict=["leet","code"]。

我用的方法是动态规划，声明canBeSegmented[s.size()+1]，canBeSegmented[i]表示字符串[1...i]能否在字典中找到组成的单词。那么当前状态的值取决于canBeSegmented[i-dict[j].size()]是否可取，且s[i-dict[j].size()...dict[j].size()]是否与dict[j]相同，j为0到dict.size()-1。