title: git commit -am
date: 2017-05-24 19:34:53
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

git commit -a中的参数是all。它的含义相当于是先add所有的东西，然后在commit上去，这样不需要额外打git add了。

**UPDATE:2017/5/26**

如果文件没有被添加到缓冲区，即文件没有被git跟踪的话，直接git commit是不行的；而如果文件已经被跟踪，那可以直接git commit -am