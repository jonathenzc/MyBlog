title: Insert Interval
date: 2016-08-13 23:20:00
categories: 【LeetCode】
tags: [LeetCode, Array, Sort]
---
## {{ title }} ##

---

这道题目默认间隔都是排好序的，那么就可以分为3步，新建一个容器

第一步：把newInterval左边的区间都放入容器中，左边的判断就可以用intervals[i].end < newInterval.start

第二步：合并在newInterval右边的区间，右边的判断可以用intervals[i].start <= newInterval.end。更新newInterval的start和end

start = min（intervals[i].start, newInterval.start）

end = max（intervals[i].end, newInterval.end）

第三步：将剩余的区间压入容器中。