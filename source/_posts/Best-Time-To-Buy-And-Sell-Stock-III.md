title: Best Time To Buy And Sell Stock III
date: 2016-09-01 22:23:51
categories: 【LeetCode】
tags: [LeetCode, Array, Dynamic Programming]
---
## {{ title }} ##

---

维护两个动态规划数组，分别是local和global，其中global[i][j]表示第i天的股票在第j次交易的最大盈利，而local[i][j]表示第i天的股票买入的第j次交易的最大盈利。那么

local[i][j] = max(global[i-1][j-1]+max(prices[i]-prices[i-1],0) , local[i-1][j]+prices[i]-prices[i-1] )

global[i][j] = max(global[i-1][j], local[i][j]);

参考资料：

[http://blog.csdn.net/linhuanmars/article/details/23236995](http://blog.csdn.net/linhuanmars/article/details/23236995 "http://blog.csdn.net/linhuanmars/article/details/23236995")