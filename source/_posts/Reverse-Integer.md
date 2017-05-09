title: Reverse Integer
date: 2015-05-15 09:34:11
categories: 【LeetCode】
tags: [LeetCode, Math]
---
## {{ title }} ##

---

这个问题就是将输入的整数反过来输出，比如123返回321，-123返回-321。

做法的话可以用整除和取余逐步得到这个整数的各项数位。接着再将它们逆向拼接起来。

我的做法是用stringstream直接将int转成string，接着再将string逆反即可。

这里需要注意的是逆反后的数可能越界，所以要对越界进行处理。