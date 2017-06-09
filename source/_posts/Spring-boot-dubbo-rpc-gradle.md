title: Spring boot + dubbo rpc + gradle
date: 2017-04-04 14:34:25
categories: 【Career】
tags: [Spring boot, dubbo, gradle]
---
## {{ title }} ##

---

最近刚刚入职，公司给了2周时间来完成新手任务。新手任务需要利用Spring Boot作为业务逻辑的框架，dubbo作为rpc调用的框架。由于之前没有接触过这些框架，所以在实现过程中是各种资料各种查，今天有时间整理一下之前收集的知识，同时把整个项目的git放出来，希望可以帮助到其他人。

下面会列一下我在做项目时查看的资料。

# git 与 SourceTree #
公司内部使用gitlab来维护代码库。

参考资料：

1. [SourceTree克隆等待](http://blog.csdn.net/u011439289/article/details/42968513 "SourceTree克隆等待")
2. [SSH Key 连接gitlab](http://www.tuicool.com/articles/BVJjiez "SSH Key 连接gitlab")
3. [生成SSH Key](http://www.jianshu.com/p/31cbbbc5f9fa/ "SourceTree克隆等待")

# Gradle与Maven #

gradle和maven都是用来管理项目的构建和编译。Java的构建基本经历了Ant->Maven->Gradle这样的时代。

可以把gradle类比成makefile一样的东西

参考资料：

1. [http://mvnrepository.com/](http://mvnrepository.com/ "http://mvnrepository.com/")
2. [http://www.cnblogs.com/guogangj/p/5465740.html](http://www.cnblogs.com/guogangj/p/5465740.html)
3. [https://rominirani.com/announcing-gradle-tutorial-series-5fd134223bf8](https://rominirani.com/announcing-gradle-tutorial-series-5fd134223bf8)
4. [http://blog.csdn.net/codezjx/article/details/49531887](http://blog.csdn.net/codezjx/article/details/49531887)
5. [http://stackoverflow.com/questions/20376965/no-gradle-tool-window-in-intellij-idea-13](http://stackoverflow.com/questions/20376965/no-gradle-tool-window-in-intellij-idea-13)
6. [http://benweizhu.github.io/blog/categories/gradleshen-ru-yu-shi-zhan/](http://benweizhu.github.io/blog/categories/gradleshen-ru-yu-shi-zhan/)

# Intellij IDEA #
Gradle Dependencies Formatter 将maven依赖的格式转成gradle依赖的格式;

alt+左方向或者右方向 打开文件，前进后退功能;

参考资料：
1. [注释](https://www.jetbrains.com/help/idea/2017.1/creating-documentation-comments.html)
2. [插件](http://www.cnblogs.com/huaxingtianxia/p/6030741.html)
3. [lombok 需要在IDEA中enable annotation processing](http://blog.csdn.net/u011781521/article/details/53055632)
4. [lombok奇技淫巧](http://www.cnblogs.com/holten/p/5729226.html)

# RESTful API#

参考资料：
1. [http://www.ruanyifeng.com/blog/2011/09/restful](http://www.ruanyifeng.com/blog/2011/09/restful)
2. [https://spring.io/understanding/REST](https://spring.io/understanding/REST)
3. [http://www.cnblogs.com/weidagang2046/archive/2011/06/04/2063696.html](http://www.cnblogs.com/weidagang2046/archive/2011/06/04/2063696.html)

# Spring Boot #

参考资料：
1. [http://blog.csdn.net/u013360850/article/details/53415005](http://blog.csdn.net/u013360850/article/details/53415005)
2. [http://www.bysocket.com/?page_id=1639](http://www.bysocket.com/?page_id=1639)
3. [http://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/htmlsingle/#boot-features-external-config-application-property-files](http://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/htmlsingle/#boot-features-external-config-application-property-files)
4. [http://www.cnblogs.com/ityouknow/p/5662753.html](http://www.cnblogs.com/ityouknow/p/5662753.html)
5. [http://blog.csdn.net/txw910/article/details/50430178](http://blog.csdn.net/txw910/article/details/50430178)
6. [application类启动失败问题](http://blog.csdn.net/itegel84/article/details/62422726)

# Dubbo rpc #

参考资料：
1. [dubbo demo](http://www.cnblogs.com/fri-yu/p/5981436.html)
2. [dubbo配置](http://www.cnblogs.com/chanshuyi/p/5144288.html)
3. [dubbo环境](http://www.jianshu.com/p/ea2b04752765)
4. [dubbo+spring+mybatis+gradle](https://segmentfault.com/a/1190000005170426)
5. [另一个demo](http://www.tuicool.com/articles/QrYvyqR)

# mybatis #

参考资料：
1. [http://www.jianshu.com/p/5c85becf5f73](http://www.jianshu.com/p/5c85becf5f73)
2. [http://chenkaihua.com/2015/12/19/running-mybatis-generator-with-gradle/](http://chenkaihua.com/2015/12/19/running-mybatis-generator-with-gradle/)

# postman #

参考资料：
1. [http://blog.csdn.net/ccc20134/article/details/45094679](http://blog.csdn.net/ccc20134/article/details/45094679)

# 微信服务号 #

使用ngrok来进行地址映射，命令是ngrok http 8081

参考资料：
1. [http://www.henkuai.com/thread-6377-1-1.html](http://www.henkuai.com/thread-6377-1-1.html)
2. [http://www.jianshu.com/p/c2e4ec6e0b23](http://www.jianshu.com/p/c2e4ec6e0b23	)
3. [http://phpervip.blog.51cto.com/11075781/1875807](http://phpervip.blog.51cto.com/11075781/1875807)
4. [http://blog.csdn.net/huweijun_2012/article/details/51859496](http://blog.csdn.net/huweijun_2012/article/details/51859496)
5. [http://wiki.jikexueyuan.com/project/java-wechat/6.html](http://wiki.jikexueyuan.com/project/java-wechat/6.html)

# git中添加gif #

参考资料：
1. [LICEcap 录制](http://www.cockos.com/licecap/)
2. [github gif](http://www.jianshu.com/p/92925e6152f0)

# markdown #

[meditor](https://www.zybuluo.com/mdeditor)

# 项目git url #

[项目git](https://github.com/jonathenzc/DubboPlayground.git "https://github.com/jonathenzc/DubboPlayground.git") 

项目中的Newbeeshop就是新手任务。