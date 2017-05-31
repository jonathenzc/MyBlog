title: git合并多条commit
date: 2017-05-24 19:50:39
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

先利用git log --oneline来查看所有commit的id。

接着git rebase -i [commit_id] 这个commit_id就是你想从头合并到的某次提交。 (iterative)

接着根据展示的提交日志改squash即可。这里需要提到的是两两commit的合并是不行的，需要指明一条上游的commit。

改好squash后打回车后，会看到rebasing的指令，然后改合并后的message就可以了。

需要注意的是rebase的操作其实是新建一个commit，也就是在实践上的顺序就不对了。

**UPDATE:2017/5/31**

rebase后在本地分支的commit被压缩为1个，而远端的分支还未改变，这时需要把远端的分支与本地的commit个数一致，不然是通过merge来实现的。可以打git push -f这样远端和本地的分支都同步了。