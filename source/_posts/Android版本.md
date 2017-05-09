title: Android版本
date: 2016-05-08 10:40:42
categories: 【Android】
tags: [Android, version]
---
## {{ title }} ##

---

在android发布时，总会给他配置一个版本号。我们可以在AndroidManifest.xml文件中为其配置版本号


<manifest xmlns:android=""
    android:versionCode="1"
	android:versionName="1.0">

还需要在build.gradle中配置一下，将versionCode和versionName做一致地修改。

其中versionCode是对用户不可见的，可以表示这是第几次的提交；

versionName是对用户可见的，表示的是版本号。

