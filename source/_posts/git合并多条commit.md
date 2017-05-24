title: git合并多条commit
date: 2017-05-24 19:50:39
categories: 【Git】
tags: [Git]
---
## {{ title }} ##

---

先利用git log --oneline来查看所有commit的id。

接着git rebase -i [commit_id] 这个commit_id就是你想从头合并到的某次提交。

接着根据展示的提交日志改squash即可。这里需要提到的是两两commit的合并是不行的，需要指明一条上游的commit。

改好squash后打回车后，会看到rebasing的指令，然后改合并后的message就可以了。

需要注意的是rebase的操作其实是新建一个commit，也就是在实践上的顺序就不对了。