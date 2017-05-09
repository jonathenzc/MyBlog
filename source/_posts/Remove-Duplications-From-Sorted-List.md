title: Remove Duplications From Sorted List
date: 2015-05-29 21:34:41
categories: 【LeetCode】
tags: [LeetCode, Linked List]
---
## {{ title }} ##

---

这道题目是对有序列表去除重复的元素。我用两个指针a和b分别表示相同元素序列的第一个指针和下一个不同元素序列的第一个指针，有了这两个指针，我们在去重时只需要将a的next指向b就可以将之前相同的元素去除了。

首先先判断传进来的节点是否为空，为空就直接返回。不为空时，先声明两个上面描述过的指针，分别指向头节点和头节点的next。进入循环，当指针a和b都不为空时就继续循环。如果发现指针b和
指针a的内容不同时，就将a的next指向b。

在最后跳出循环时，如果指针a不为空，就将a的next指向指针b。