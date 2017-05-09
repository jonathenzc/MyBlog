title: "Pascal's Triangle II"
date: 2015-05-20 22:03:16
categories: 【LeetCode】
tags: [LeetCode, Array]
---
## {{ title }} ##

---

这个问题和之前的Pascal三角形类似，之前的问题是要求出前numRows行的三角形，而这道题目需要求出第k行的内容。不过这里只能用额外O(k)的空间。

我的做法就是用另一个vector来记录上一行的内容。还是比较简单的。唯一需要注意的就是题目的第k行，和上一道不同。这道题目认为第0行是1，第1行是1 1，那么我们只要将这个k考虑成k+1即可。