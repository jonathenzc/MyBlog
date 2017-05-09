title: Best Time To Buy And Sell Stock
date: 2015-08-22 12:02:00
categories: 【LeetCode】
tags: [LeetCode, Array, Dynamic Programming]
---
## {{ title }} ##

---

给定一个整数数组，第i个元素表示第i天的股票价格。我们现在只被允许做一次操作（买入股票，卖出这个股票），求出可以得到的最大利益。

我的方法是记录最低的股价和当前最大的收益，如果当前价格减去这一天之前的最低价格所得到的收益比当前最大收益大，那么就更新这个收益。