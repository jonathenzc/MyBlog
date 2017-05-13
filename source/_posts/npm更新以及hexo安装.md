title: npm更新以及hexo安装
date: 2017-05-13 16:07:48
categories: 【Hexo】
tags: [Hexo]
---
## {{ title }} ##

---

Windows下，直接去node.js的官网下载个新版本覆盖一下即可。

npm下载的东西都会放到这个路径下

```shell
npm root -g
```

安装hexo的话，打下面的命令就会在上面的路径中添加一个hexo的文件夹

```shell
npm install hexo-cli -g
```

为了验证hexo是否安装好，可以打

```shell
hexo -v
```

就会显示hexo的版本
