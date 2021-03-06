title: Maximum Product of Word Lengths
date: 2016-02-14 13:08:11
categories: 【LeetCode】
tags: [LeetCode, Bit Manipulation]
---
## {{ title }} ##

---

给定一组字符串数组，找出这组数组中两字符串的最大乘积，这两个字符串不能包含共同的子串。这些字符串都只用小写字母。

比如["abcw","baz","foo","bar","xtfn","abcdef"]的返回值就是16

这道题目因为字符串只会包含小写字母，也就是说只有26种字符，那么这里可以用到一个技巧，就是我们可以用一个整数来表示该字符串，因为一个整数有32位，而字符串最多也就是26位的数。

将这个数组中的每个词转成整数：将'a'代表把1左移1位，'b'代表左移2位......对每个字符进行上述规则的转化，对每个字符转化的数进行按位或，这样可以消除相同的数。由此，字符串数组就转化成整数数组。

最后对这个整数数组中的每个数进行两两按位与的判断，如果结果为0表示字符串没有共享相同的子串，那么就可以计算他们的字符串长度乘积。