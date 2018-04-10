title: gitbook 搭建
date: 2018-04-10 11:33:45
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

遇到no such file or directory fontsettings.js的问题，重新gitbook build一下。
 
```
gitbook init  # 初始化，即自动新建README.md和SUMMARY.md文件
gitbook install  # 解析book.json并自动下载插件包
gitbook build  # 生成_book目录（网站格式）
gitbook serve  # 启动web服务器，默认4000端口，可通过http://localhost:4000访问文档
gitbook serve --port 4567  # 启动4567端口
```

参考资料：

[gitbook安装与使用之windows下搭建gitbook平台](https://blog.csdn.net/jnloverll/article/details/78285681 "https://blog.csdn.net/jnloverll/article/details/78285681")