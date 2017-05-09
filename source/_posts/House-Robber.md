title: House Robber
date: 2015-05-04 11:21:47
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming]
---
## {{ title }} ##

---

### 问题描述 ###

---

问题是说有个贼偷沿街的房屋，每间房屋都有相应的钱存着。贼当然可以把所有房屋的钱都偷走，但是这里有个限制：房屋和它邻近的房屋有安全系统，如果两个相邻的房屋被偷了，那么就是触发报警系统。也就是说贼不能偷相邻房屋的钱。

### 解法 ###

---

这个问题第一想到的就是动态规划，设数组moneyStolen表示贼可以偷的钱，moneyStolen[i]表示从房屋0到房屋i最多可以偷到的钱。那么moneyStolen[i] = max{moneyStolen[i-2]+nums[i],moneyStolen[i-1]}，其中nums[i]表示房屋i存有的钱。

这里需要注意的就是当传入的vector<int>nums参数大小是0的话就直接返回0就是了。