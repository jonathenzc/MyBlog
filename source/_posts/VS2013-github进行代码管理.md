title: VS2013+github进行代码管理
date: 2015-03-03 12:36:29
categories: 【工欲善其事必先利其器】
tags: [VS2013,github]
---
## {{ title }} ##

---
“工欲善其事，必先利其器”，平时我既会在台式机上写代码，也会在自己的笔记本电脑上写代码，所以经常会有一致性的问题，使用github可以帮我很好的管理项目和代码。

### 环境搭建 ###

---
我们需要有VS2013和github插件。

#### VS2013 ####

---
我用的vs版本是2013的express，是免费的。相比于正式的VS版本要少了不少功能，但是已经足够我们开发了。可以在[这里](http://www.visualstudio.com/zh-cn/downloads#d-express-windows-8 "VS下载")下载。

需要注意的是网页有**两**个版本，分别是Express 2013 with Update 4 for **Windows** 和 **Windows Desktop**。前者是用来开发Windows应用商店和Windows Phone应用的，后者是用来开发C#、VB、C++桌面应用的。

#### github插件 ####

---
有了VS之后，我们需要下载github的插件。这里因为我之前已经弄好了，记得速度挺慢的，可以使用官方提供的git插件来下载：[Visual Studio Tools for Git](https://visualstudiogallery.msdn.microsoft.com/abafc7d6-dcaa-40f4-8a5e-d6724bdb980c "Visual Studio Tools for Git")

### 创建repo仓库 ###

---
我们需要在github上创建一个repo。

<img src="/img/CreateGithubRepo.png"/ class="img-shadow" />

这里需要提一下：我当初选择了`Initialize this repository with a README`选项，结果在使用vs进行上传的时候出了点小状况，所以那个选项不用去选。创建好之后记得复制这个仓库的URL：`https://github.com/jonathenzc/Helloworld.git`

### 将项目添加到项目管理器 ###

---
这段是我最近添加的，如果没有这部的话，分支是无分支而不是master。先在文件选项卡中找到“添加到源码控制”。

<img src="/img/SourceCodeManager.png"/ class="img-shadow" />

点击后，会看到这样的选项，选择git即可，这时分支会变成master。

<img src="/img/ChooseSourceControl.png"/ class="img-shadow" />

### 进入未提交同步选项卡 ###

---
如果你环境配置顺利的话，会看到在vs平时的方案资源管理器的选项卡旁边会出现一个团队资源管理器。

<img src="/img/teamManager.png"/ class="img-shadow" />

进入这个团队资源管理器选项卡，找到未同步提交，将刚刚得到的仓库URL复制进去。

### 更改和同步 ###

---
<img src="/img/teamManager1.png"/ class="img-shadow" />

进入更改选项卡，编辑这次提交的内容，比如:我第一次提交，修改了***

<img src="/img/changeTab.png"/ class="img-shadow" />

接着点击`同步`按钮，这样你的项目就同步到github上啦！

以后如果在其他地点对项目进行了编辑，需要更新最新的内容的话，可以进入`未同步提交`选项卡，点击`拉取`按钮，这样你的项目就同步到最新版本了！