title: git behind origin * commits
date: 2017-05-21 22:35:28
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

有时候你会发现虽然当前分支与你最新的代码同步了，但是git status的结果是显示你当前的本地分支领先远端的分支。出现这种情况，多半是你本地的git log没有更新，只需要git fetch一下就可以将本地的git信息与远端的git信息同步了。这时你再git status的结果就是同步的。