title: Combinations
date: 2016-08-02 16:22:33
categories: 【LeetCode】
tags: [LeetCode, Backtracking]
---
## {{ title }} ##

---

这道题目我一开始是用正常的递归回溯来得到所有的combination，但是效率不高。

看到一个解答是这样的

C(n,k) = C(n-1,k-1)+C(n-1,k)

第一个表示选定n后，在n-1中选择k-1个数；第二个表示不选n，在n-1个中选择k个数。

那么递归的终止条件就是k==0 || k==n，那么就赋一个初始值。

其他情况下，先获取C(n-1,k-1)返回的vector<vector<int>>，然后往这个vector中添加多个n这个元素；

再获取C(n-1,k)，合并两个vector即可。