title: First Bad Version
date: 2016-08-24 11:51:01
categories: 【LeetCode】
tags: [LeetCode, Binary Search]
---
## {{ title }} ##

---

这道题目就是正常的二分，start为1，end为n，mid为两者的一半。

如果mid指向的数是bad version，那么说明最后一个非bad version在前面，那么就往前找(end=mid);

如果mid指向的数不是bad version，那么说明最后一个非bad version在后面，那么就往后找(start=mid),一旦发现start和end-1相等，那么就返回end。

这里需要注意的是mid的计算方式，直接(start+end)/2会导致溢出，所以我们应该这样来计算mid=start+(end-start)/2