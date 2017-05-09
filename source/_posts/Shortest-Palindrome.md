title: Shortest Palindrome
date: 2016-06-22 11:59:39
categories: 【LeetCode】
tags: [LeetCode, String]
---
## {{ title }} ##

---

我的做法是先将字符串s翻转，得到翻转后的字符串reversedStr，比如：

s:aacecaaa
r:aaacecaa

然后根据长度len来获取子串，从最大的长度开始，s从0到len的子串是否等于r从(size-len)到底的子串，如果相等直接break。

最后拼接子串，r.substr(0,size-len)+s即可。