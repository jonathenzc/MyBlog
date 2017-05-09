title: Insert Delete GetRandom O(1) Duplicates Allowed
date: 2016-08-14 18:33:00
categories: 【LeetCode】
tags: [LeetCode, Array, Hash Table, Design]
---
## {{ title }} ##

---

我仍然用map和v来储存元素，但是在map是记录数和它所有在v中的下标集合，即map<int,vector<int>>。

获取随机数的方法仍然和之前一样

插入的方法也很简单，就是对两个map和v进行插入，然后判断一下待插入的元素之前是否存在过即可。

删除的方法需要获取该元素在v中的一个下标，然后更新v和map中相应的索引。