title: Bulls and Cows
date: 2016-07-03 17:04:29
categories: 【LeetCode】
tags: [LeetCode,Hash Table]
---
## {{ title }} ##

---

我的做法是先为secret的字符串构建一个数字与出现次数的映射map。

遍历guess字符串，如果guess[i]与secret[i]相同，那么bull的计数器+1，map[guess[i]-'0']--; 如果不想等且map[guess[i]-'0']>0，那么cow的计数器+1，map[guess[i]-'0']--

最后遍历map，如果map[i]<0，那么补全cow的个数（处理1222,1122的情况）