title: Word Break II
date: 2015-07-11 21:24:41
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Backtracking]
---
## {{ title }} ##

---

问题和之前的一道word break类似，不过这次需要将所有可以组成字符串的子串按空格相连。

比如s = "catsanddog"，dict=["cat","cats","and","sand","dog"]

返回["cats and dog","cat sand dog"]

我的方法是递归深搜来找到可能的组合。这里麻烦的是有个测试用例特别长，但是只有最后一位不同，这导致花了很多时间但实际并没有用。所以我们这里可以进行这样的优化，判断字符串是否可以由字典组成。这样看只需要跑一下之前的word break就可以了。

不过这样的时间开销还是很大，所以我们可以粗略来判断，末尾元素为s末尾的所有子串是否出现在字典中，如果没有出现，那么就不用进行下面的深搜了。