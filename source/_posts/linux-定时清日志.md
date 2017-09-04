title: linux 定时清日志
date: 2017-09-04 15:02:08
categories: 【linux】
tags: [linux]
---
## {{ title }} ##

---

```bash
#!/bin/bash

log_path="/usr/local/tomcat/logs"         #此处定义你的日志文件夹路径
expried_time=15      #此处定义你的日志过期时间，如7天

function deleteLogs(){
    # 获取系统时间，所有时间格式都是秒
    local currentDate=`date +%s`
    echo "current date: " $currentDate

    for file in `find $1 -name "catalina-*.out"` #此处定义文件名格式，避免误删
    do  
        local name=$file
        local modifyDate=$(stat -c %Y $file)

        #对比时间，算出日志存在时间，距离最近一次修改
        local logExistTime=$(($currentDate - $modifyDate))
        logExistTime=$(($logExistTime/86400))
    
        if [ $logExistTime -gt $expried_time ]; then
            echo "File: " $name "Modify Date: " $modifyDate + "Exist Time: " $logExistTime + "Delete: yes"
            rm -f $file
        else
            echo "File: " $name "Modify Date: " $modifyDate + "Exist Time: " $logExistTime + "Delete: no"
        fi  
    done
}

deleteLogs $log_path
```


参考资料：

[Crontab定时删除日志](http://www.cnblogs.com/KevinSong/p/3816981.html)
[Crontab定时删除日志2](http://blog.csdn.net/taiyang1987912/article/details/43018505)

