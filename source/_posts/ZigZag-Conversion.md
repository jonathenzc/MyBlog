title: ZigZag Conversion
date: 2015-05-13 12:48:13
categories: 【LeetCode】
tags: [LeetCode, String]
---
## {{ title }} ##

---

问题是将一个字符串按z字形风格来转化。z的横杠长度由一个参数来决定，比如“PAYPALISHIRING”，按横杠为3来进行转化。

P   A   H   N

A P L S I I G

Y   I   R

转化得到的字符串是将变化后的Z字型横过来读取，也就是"PAHNAPLSIIGYIR"。

解法:

横杠的长度参数是nRows，先判断字符串长度是否会超过nRows，如果没超过，那么原字符串也只能是一个横杠，转化后的字符串还是原字符串。接着我们发现这样一个规律：

<img src="/img/Zigzag.png"  class="img-shadow img-center"/>

这些数字认为是字符串的索引，可以看到第一行和最后一行的数字相差是2\*(nRows-1)个，我们设为interval个，比如这里nRows是7，那么就相差12。接下来的每行相差interval-2\*i和2\*i，其中i是行数，总共有nRows行。

需要注意的是，每行的数字不一定正好增长到，需要进行是否超过字符串长度的判断。
