title: Self Crossing
date: 2016-06-08 12:53:28
categories: 【LeetCode】
tags: [LeetCode, Math]
---
## {{ title }} ##

---

我们针对每个4条边组成的正方形来看，第一种情况是x[i-1] <= x[i-3] && x[i] >= x[i-2]当前的边才有可能穿过之前的边

第二种是当前边与第i-4条边相连的情况；第三种情况是组成小矩形的情况，即[1,1,2,2,1,1]