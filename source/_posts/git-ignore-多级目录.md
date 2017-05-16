title: git ignore 多级目录
date: 2017-05-16 14:34:11
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

有时候我们想要忽略多个深目录下的同类名文件，比如/a/b/c/config.xml和/a/b/d/config.xml

我们在ignore中这样写**/config.xml，这样就可以把两个文件忽略了。

注：

有时候加了ignore还会继续跟踪，那是因为你把之前想忽略的文件提交到git中了，只能先把这个文件删掉，然后提交一次，再添加ignore才行。