title: Design Twitter
date: 2016-07-01 22:33:19
categories: 【LeetCode】
tags: [LeetCode, Hash Table, Heap, Design]
---
## {{ title }} ##

---

题目是设计twitter的数据结构，我的做法是用一个struct来存一条推特的发起者userId和这条推特的id，twitterId。在整个过程中维护一个推特的vector和一个键值对是[userId,关注者Id的Set]的map，这样发推、关注、取消关注都很容易处理，那么返回userId的前10条推特需要从后遍历整个推特vector.