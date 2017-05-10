title: hexo 博客源文件同步
date: 2017-05-10 14:25:49
categories: 【Hexo】
tags: [Hexo]
---
## {{ title }} ##

---

我新建一个git仓库只放scaffolds，source和themes这三个文件夹，剩下的文件会保留_config.yml, db.json和package.json。

这样在新环境下先安装npm，node.js和git，然后打npm install就可以开始hexo g, hexo s, hexo d的功能了。