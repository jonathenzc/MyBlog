title: Remove Element
date: 2015-05-29 09:30:00
categories: 【LeetCode】
tags: [LeetCode, Two Pointers, Array]
---
## {{ title }} ##

---
给定一个数组和一个值，需要将这个数组中的所有和这个值相同的元素移除，返回移除后的数组大小。移除后的元素顺序可以变，长度之后的元素不用去在意。

我的方法是用一个vector来记录和val相同的元素，接着从后开始，与val不同的数就将他填入坑中。