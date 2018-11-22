title: gradle _main | _test
date: 2018-11-22 15:37:09
categories: 【Gradle】
tags: [Gradle]
---
## {{ title }} ##

---

用Intellij引入项目后，gradle clean build可以通过，但项目在找各个模块的依赖会有问题，提示诸如“need to import XXX_main”。

这个问题是因为在引入项目的时候有问题，可以这样调整“File -> New -> Project from existing sources... -> select file -> Gradle -> uncheck create separate modules per source set”即可解决，关键的异步就是“create separate modules per source set”取消勾选。

参考资料：

[windows protobuf](https://stackoverflow.com/questions/37018567/why-my-gradle-projects-creates-separated-modules-for-main-and-test-in-intellij-i)