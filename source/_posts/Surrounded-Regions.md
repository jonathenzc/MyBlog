title: Surrounded Regions
date: 2016-08-02 22:21:36
categories: 【LeetCode】
tags: [LeetCode, Breadth-first Search, Union Find]
---
## {{ title }} ##

---

先沿着4边，广度优先搜索找到所有的O，将O设成1。

接着遍历整个board，如果仍然是O那么可以进行翻转，将O变成X。

最后将1变回O。