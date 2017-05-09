title: Number of 1 bits
date: 2015-05-04 14:06:09
categories: 【LeetCode】
tags: [LeetCode, Bit Manipulation]
---
## {{ title }} ##

---

### 问题描述 ###

---

问题是求一个无符号整形转化成二进制数中数位为1的个数（*Hamming Weight*）。比如在32位中11的二进制是00000000000000000000000000001011，那么我们的结果是3。

### 解法 ###

---

这个问题的解法挺简单的，将一个数转成二进制，接着遍历一遍就可以得到结果了。

这里需要注意的是变量类型是uint32_t，这个类型平时倒不常用，一般都是unsigned int。它的头文件是stdint.h。