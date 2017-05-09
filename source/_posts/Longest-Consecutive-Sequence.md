title: Longest Consecutive Sequence
date: 2016-08-02 18:50:54
categories: 【LeetCode】
tags: [LeetCode, Array, Union Find]
---
## {{ title }} ##

---

利用map来储存数，遍历整个map中的元素，如果后一个元素是前一个元素+1，那么当前序列的长度加1（这个map是有序的，当然也可以用一个数组来维护）