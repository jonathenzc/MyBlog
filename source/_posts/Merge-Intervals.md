title: Merge Intervals
date: 2016-08-13 23:38:40
categories: 【LeetCode】
tags: [LeetCode, Array, Sort]
---
## {{ title }} ##

---

先对区间进行根据start进行排序，接着新建一个返回的容器，遍历intervals

如果返回容器为空或者当前区间的start > 容器顶部元素的end，那么就压入容器

反之就更新容器顶部元素的end = max(intervals[i].end, v.back().end)