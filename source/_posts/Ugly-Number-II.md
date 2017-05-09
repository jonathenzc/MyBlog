title: Ugly Number II
date: 2015-08-20 18:41:56
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Heap, Math]
---
## {{ title }} ##

---

如何判断一个数是否是ugly数在之前一篇博客里已经提到过了。这次问题是要求出第n个ugly数。这道题目可以用动态规划来做，uglyNumber[i]表示第i个ugly数。uglyNumber[i]等于min(2\*uglyNumber[a],3\*uglyNumber[b],5\*uglyNumber[c])。这里要解释一下a,b,c分别指uglyNumber中的某个位置。比如uglyNumber中的第一个数是1，a,b,c分别是0,0,0。因为2\*1,3\*1,5\*1中2最小，uglyNumber[1]为2,a进位到1。

这里需要注意一点，需要处理2*3和3*2这样的情况，也就是公约数，所以当相同的时候a,b,c也要进位。