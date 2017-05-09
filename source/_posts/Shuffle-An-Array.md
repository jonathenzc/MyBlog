title: Shuffle An Array
date: 2016-08-15 11:10:04
categories: 【LeetCode】
tags: [LeetCode]
---
## {{ title }} ##

---

这道题目我一开始是用map来记录随机过的下标，后来看到讨论里面可以这样来做，就是将随机出的位置和待交换的位置进行交换，这样下次只需要在剩下的集合中进行随机就可以了。