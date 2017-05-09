title: Search a 2D Matrix II
date: 2016-06-05 11:46:42
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Divide and Conquer]
---
## {{ title }} ##

---

我一开始的做法是对每行进行二分，这样的复杂度是m*log(n)，实际做下来这个算法的效果不是很好。

之后我从左下角的点开始搜索，如果比target元素要小，那么就向上搜索；如果比target元素要大，那么就向右搜索，直到横纵坐标超过了矩阵范围。