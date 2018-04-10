title: dig命令
date: 2018-04-10 11:57:19
categories: 【Cmd】
tags: [Cmd]
---
## {{ title }} ##

---

dig -x {待查ip} @{dns的ip} +short (+tcp #dig)

其中@server表示不使用/etc/resolv.conf默认的DNS服务器，指定一个特定的DNS发起请求，括号内的参数可以不打

参考资料：

[linux中与域名解析和反解相关的命令host|nslookup|dig](https://blog.csdn.net/wangjianno2/article/details/44521445)  