title: 使用hexo搭建博客
date: 2015-02-21 22:05:21
categories: 【Hexo】
tags: [Hexo]
---
## 使用Hexo编写博客 ##

---

我使用Hexo在github构建博客，主要的步骤分为：
> * 安装Git
> * 安装Node.js
> * 安装Hexo
> * 配置和部署Hexo

### 安装Git ###
我使用的是[msysgit](http://msysgit.github.io/ "msysgit")来进行安装。

### 安装Node.js ###
去Node.js的官网（[http://nodejs.org/](http://nodejs.org/)）下载最新版的Node.js

### 安装Hexo ###
在任意位置右击打开Git bash，输入下面的命令

    npm install -g hexo
执行完上面的命令后，创建以后编写博客的目录(如D:\MyBlog), 右击打开Git Bash，输入下面的命令进行Hexo初始化

    npm init
	npm install
接着执行下面的命令来测试一下我们Hexo部署是否成功：

	hexo generate
	hexo server
在浏览器中输入localhost：4000就可以看到我们部署的博客了。

### 配置和部署Hexo ###
安装完Hexo后，我们需要将Hexo部署到github上。在你的github上创建一个新的repository，名字为jonathenzc.github.io（当然如果你之前使用过github来创建博客的话，应该已经有这个repo了）

复制这个repo的地址。

#### 部署 ####
在D:\MyBlog中编辑_config.yml，找到deploy这一块。

	deploy:
		type: github	
		repository: https://github.com/jonathenzc/jonathenzc.github.io.git
		branch: master

接着，执行下列命令就可以完成部署啦
	
	hexo generate
	hexo deploy

当然以后频繁使用hexo的话，我们可以使用一些简单的命令，比如

hexo g == hexo generate
hexo d == hexo deploy
hexo s == hexo server
hexo n == hexo new