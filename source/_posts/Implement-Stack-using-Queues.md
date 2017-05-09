title: Implement Stack using Queues
date: 2015-07-07 11:46:53
categories: 【LeetCode】
tags: [LeetCode, Stack, Data Structure]
---
## {{ title }} ##

---

问题是使用stl的queue来实现栈，并提供push，pop，top，empty等功能。

首先empty是最好判断的，可以使用队列的empty来判断。

为了简化pop和top的代码，我就只在push做多点，也就是说pop和top就使用queue的pop和front函数即可。

在push中，我用另一个队列来存储之前队列的内容，将新的元素压入到之前元素的第一个，再将另一个队列的内容重新压入，做到后进来的元素在队列的第一个，来实现栈的功能。 