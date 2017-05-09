title: Word Ladder II
date: 2016-06-26 19:25:46
categories: 【LeetCode】
tags: [LeetCode, Array, Backtracking,Breadth-first Search, String]
---
## {{ title }} ##

---

我一开始是采用搜索枚举的方法，当然可想而知的是Time Limited Error。后来看了参考资料，用了作者的方法：先是构建一张两个节点之间只差一个字符的图，接着对这张图进行广搜，从start节点到end节点的搜索。结果还是爆Time Limited Error。

之后，我根据作者的思路继续改进实现，将构建图时比较两个字符串是否相差一个字符的方法进行改进，我之前的方法就是根据传入的字符串，一个个的比较两者是否只差一个字符。改进的方法是将遍历当前层的当前节点，对该节点的每个字符根据26个字母进行修改，将在wordlist中搜索修改后的字符串。这样做大大提高了每次比较的效率，但还是Time Limited Error。

最后我又改进图的储存形式，之前是由上至下的记录图中节点的相连情况，改进后我记录由下至上的相连情况，广搜的时候也是由最下层的点搜索到开始节点，这样可以避免一些不会访问到的节点。

最终在写完代码Submit后，告诉我的错误信息是Memory Limited Error。在多次调试后我才发现原来是在BFS时传入的那张图是传值的，导致它的memory超过了范围，最后改成了引用，就顺利的ac了。

参考资料：

[http://www.cnblogs.com/ShaneZhang/p/3748494.html](http://www.cnblogs.com/ShaneZhang/p/3748494.html "http://www.cnblogs.com/ShaneZhang/p/3748494.html")