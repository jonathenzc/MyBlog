title: Mini Parser
date: 2016-11-24 18:12:04
categories: 【LeetCode】
tags: [LeetCode, Stack, String]
---
## {{ title }} ##

---

针对这样的NestedInteger "[[123],[456],[789]]"，实际上是一个大的NestedInteger，里面有3个小的NestedInteger，比如

NestedInteger ni;

NestedInteger ni1;

NestedInteger ni2;

NestedInteger ni3;

ni1.add(123);

ni2.add(456);

ni3.add(789);

ni.add(ni1);

ni.add(ni2);

ni.add(ni3);

和"[123,456,789]"有所区别：

NestedInteger ni;

NestedInteger ni1(123);

NestedInteger ni2(456);

NestedInteger ni3(789);

ni.add(ni1);

ni.add(ni2);

ni.add(ni3);