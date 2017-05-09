title: "Pow(x,n)"
date: 2016-05-21 14:52:18
categories: 【LeetCode】
tags: [LeetCode, Binary Search, Math]
---
## {{ title }} ##

---

问题是求x^n的幂。直白的方法就是乘n次x，就可以求出它的幂，但是这个算法的复杂度是O(N)。有O(LogN)的算法，比如指数n=6，二进制下可以表示成110。

x^6 = x^(2^1+x^2)。每次获取指数的某位数，如果为1的话，就和总数相乘，为0的话就累积乘的结果。

参考资料：

[http://baike.baidu.com/link?url=q42Ybpf-x3OAmf09Zt0zUEinMhEN_LYucVQCPAfAHXtSjYGeAB3K8Wp2e8nc-SNu5qCKtQx4jNkWHHijuCwYr_](http://baike.baidu.com/link?url=q42Ybpf-x3OAmf09Zt0zUEinMhEN_LYucVQCPAfAHXtSjYGeAB3K8Wp2e8nc-SNu5qCKtQx4jNkWHHijuCwYr_ "http://baike.baidu.com/link?url=q42Ybpf-x3OAmf09Zt0zUEinMhEN_LYucVQCPAfAHXtSjYGeAB3K8Wp2e8nc-SNu5qCKtQx4jNkWHHijuCwYr_")