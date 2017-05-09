title: Wildcard Matching
date: 2015-07-16 22:42:17
categories: 【LeetCode】
tags: [LeetCode, Dynamic Programming, Backtracking, Greedy, String]
---
## {{ title }} ##

---

问题是判断两个字符串是否匹配，但其中一个字符串中包括`?`和`*`字符，`?`表示可以匹配任何一个单个字符，`*`表示可以匹配任何连续字符，包括空字符。

比如:

`isMatch("aa","a")` -> false

`isMatch("aa","aa")` -> true

`isMatch("aaa","aa")` -> false

`isMatch("aa","*")` -> true

`isMatch("aa","a*")` -> true

`isMatch("ab","?*")` -> true

`isMatch("aab","c*a*b")` -> false

这道题目我利用动态规划，设二维数组isStrMatch[i][j]表示p[0...i-1]与s[0...j-1]是否匹配。

那么状态转移取决于这样的情况：当p[i-1]是否等于*，如果相等，那么isStrMatch[i][j]取决于isStrMatch[i-1][j] || isStrMatch[i][j-1]

如果不等，那么isStrMatch[i][j]取决于isStrMatch[i-1][j-1] && （p[i-1] == s[j-1] || p[i-1] == '?'）

这里需要注意的是，j=0的这一列，因为如果p的开头是*，那么之后的情况，只要*连续都是可以得，也就是说isStrMatch[i][0] = isStrMatch[i-1][0] && (p[i-1] == '*')