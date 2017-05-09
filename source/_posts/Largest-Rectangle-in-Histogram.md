title: Largest Rectangle in Histogram
date: 2016-07-09 00:17:19
categories: 【LeetCode】
tags: [LeetCode, Array, Stack]
---
## {{ title }} ##

---

这道题目的解答可以这样来看，我们每次都只求一个波峰图的最大面积，比如3 4 5 6 7 2，那么波峰图就是3 4 5 6 7。我们可以用一个栈来维护这个波峰图。

栈记录的是波峰图的下标，这样我们就不需要额外的空间来储存宽度了。栈中的内容就是一个记录递增的柱状图的下标。

从头遍历柱状图，

如果当前元素比栈顶元素要小的话，那么就开始弹栈直到栈顶元素比当前元素的高度要小，计算波峰图可以通过左边的面积和右边的面积来计算整个波峰图。

如果栈为空了，那么左边的面积就为当前高度*从当前元素直到开头的宽度；不为空，左边的面积就为当前高度乘以（当前下标-栈顶元素）

右边面积就是计算当前高度*（比高度小的下标-当前元素的下标）

参考资料：

[http://www.cnblogs.com/felixfang/p/3676193.html](http://www.cnblogs.com/felixfang/p/3676193.html "http://www.cnblogs.com/felixfang/p/3676193.html")