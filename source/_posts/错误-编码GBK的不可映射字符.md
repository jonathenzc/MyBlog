title: '错误: 编码GBK的不可映射字符'
date: 2019-03-24 17:14:13
categories: 【gradle】
tags: [gradle]
---
## {{ title }} ##

---

在对项目进行gradle clean build的时候报“错误: 编码GBK的不可映射字符”，在Intellij的file encoding都加了utf-8仍然报错，猜测是gradle编译的时候应该有参数指定编码形式。

在build.gradle中添加如下代码即可

```
tasks.withType(JavaCompile) {  
    options.encoding = "UTF-8"  
}
```