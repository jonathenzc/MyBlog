title: Implement Queue using Stacks
date: 2015-07-07 12:48:21
categories: 【LeetCode】
tags: [LeetCode, Stack, Data Structure]
---
## {{ title }} ##

---

问题是使用stl的stack来实现栈，并提供push，pop，peek，empty等功能。

首先empty是最好判断的，可以使用队列的empty来判断。

为了简化pop和peek的代码，我就只在push做多点，也就是说pop和top就使用stack的pop和top函数即可。

在push中，我用另一个栈来存储之前栈的内容，将新的元素压入到之前元素的第一个，再将另一个栈的内容重新压入，做到后进来的元素在栈的第一个，来实现队列的功能。