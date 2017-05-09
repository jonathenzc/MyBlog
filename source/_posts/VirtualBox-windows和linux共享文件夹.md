title: VirtualBox windows和linux共享文件夹
date: 2015-06-07 16:18:40
categories: 【Linux】
tags: [Linux]
---
## {{ title }} ##

---

1. 首先先要安装Virtualbox的高级功能，如果显示什么强制退出之类的对话框，可以先将linux快捷栏弹出类Virtualbox的光盘的图标。这样就可以安装高级功能了。
2. 在windows中选择一个文件夹，在virtualbox工具栏中选择需要共享的文件夹；
3. 在linux中需要打`mount -t vboxsf UBuntuFile /mnt/windowsFile`，其中UbuntuFile是在windows中设置的共享文件夹，而/mnt/windowsFile是在ubuntu下的路径。