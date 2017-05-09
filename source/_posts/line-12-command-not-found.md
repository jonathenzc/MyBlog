title: "line 12: command not found"
date: 2015-07-15 10:12:12
categories: 【Hexo】
tags: [Hexo]
---
## {{ title }} ##

---

之前使用hexo的时候都很正常，生成新博文、部署到github都没有出现什么问题。但是突然有一天部署的时候遇到了`Line 12: command not found`的问题。

在网上搜索的时候没有发现什么解决方案，于是打算重新用hexo搭建下博文，结果发现只要重装一下Node.js这些问题就解决了。我猜测很有可能是因为前几天用`Latex`的时候影响到了环境变量，重装一下`Node.js`就解决了。