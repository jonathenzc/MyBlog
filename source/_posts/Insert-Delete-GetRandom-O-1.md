title: Insert Delete GetRandom O(1)
date: 2016-08-14 14:32:42
categories: 【LeetCode】
tags: [LeetCode, Array, Hash Table, Design]
---
## {{ title }} ##

---

使用map和容器，map记录了元素和它在容器中下标的映射。

插入的时候先检验该元素是否在映射中，如果不在就记录该新元素和容器下标，同时在容器中压入该元素，返回true；如果在就返回false

删除的时候先检验该元素是否在映射中，如果不在就返回false；如果在就先获取该元素在容器中的下标i，将容器顶部的元素在map中的下标调整成i，在map中删除该元素。

最后调整v[i]为容器顶部的元素，同时弹出容器最后的元素。