title: gitbook 搭建
date: 2018-04-10 11:33:45
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

遇到no such file or directory fontsettings.js的问题，重新gitbook build一下。
 
在文档目录下执行 gitbook build 会生成一个_book的目录，维护gitbook里文章时不需要去维护_book生成的内容，在git ignore中把_book添加进去即可。

```
gitbook init  # 初始化，即自动新建README.md和SUMMARY.md文件
gitbook install  # 解析book.json并自动下载插件包
gitbook build  # 生成_book目录（网站格式）
gitbook serve  # 启动web服务器，默认4000端口，可通过http://localhost:4000访问文档
gitbook serve --port 4567  # 启动4567端口
```

添加新插件需要通过gitbook install 来安装

fontsettings.js缺失问题：

1. Edit file: C:\Users[user].gitbook\versions\3.2.3\lib\output\website\copyPluginAssets.js
2. Modify in two places copyAssets(output, plugin) and copyResources(output, plugin), the line:
3. confirm:true -> confirm:false

参考资料：

1. [gitbook安装与使用之windows下搭建gitbook平台](https://blog.csdn.net/jnloverll/article/details/78285681 "https://blog.csdn.net/jnloverll/article/details/78285681")
2. [gitbook命令](http://gitbook.zhangjikai.com/commands.html "http://gitbook.zhangjikai.com/commands.html")
3. [fontsettings缺失](https://github.com/GitbookIO/gitbook/issues/1309 "https://github.com/GitbookIO/gitbook/issues/1309")