title: Spiral Matrix II
date: 2016-07-28 00:04:37
categories: 【LeetCode】
tags: [LeetCode, Array]
---
## {{ title }} ##

---

这道题目我先声明一个n\*n的vector, vector<vector<int>> v(n,vector<int>(n))，这样的初始化会有效地提高速度。

接着用一个cnt从1到n\*n遍历，用一个direction来表示移动的方向，另一个diff来表示目前再转的是第几圈。

在循环中，先更新v[row][col] = cnt.

接着更新row和col，如果是从左往右那么只更新col++，从上往下更新row++，从右往左更新col--，从下往上更新row--。

最后更新direction，如果当前是从左往右且col到了n-diff，那么方向变成向下，以此类推。需要注意的是如果当前是从下往上，那么row到了diff，还要更新diff，因为一圈走完了。