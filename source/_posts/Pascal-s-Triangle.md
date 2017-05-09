title: "Pascal's Triangle"
date: 2015-05-20 21:43:20
categories: 【LeetCode】
tags: [LeetCode, Array]
---
## {{ title }} ##

---

问题是给定一个正数`numRows`，求出前`numRows`行的Pascal三角形。那么说明是Pascal三角形呢？这里给出例子，比如`numRows`为5，那么我们将会返回

<img src="/img/PascalTriangle.png"  class="img-shadow img-center"/>

我用两个循环，第一个循环用来对每行内容进行处理，第二个循环用来求出第i行的内容。我们可以发现第i行第j个的数字等于第i-1行第j-1个数字与第i-1行第j个数字的和。

需要注意的是当`numRows`的值为0时，只返回一个空的vector<vector<int>>的二维容器，不需要再push一个空的vector<int>。