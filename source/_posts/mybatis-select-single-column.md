title: mybatis select single column
date: 2016-05-20 12:42:57
categories: 【Mybatis】
tags: [Mybatis]
---
## {{ title }} ##

---

使用mybatis generator可以自动生成与数据库连接的mapper和相应的xml文件。在mapper文件中会生成一些select的函数，默认的select函数会返回该表类型的所有链表，比如List<Model> selectByExample(RawModelExample example)这样的函数。

有时候我们只想得到一列内容，不需要获取所有的column，这时候需要人工在mapper的xml配置文件中修改，比如

```
  <select id="selectModelNameList" resultType="String">  <!-- java.lang.String这样也行 -->
    select ModelName
    from jf_raw_model
  </select>
```

就是返回List<String> selectModelNameList()是这样的函数。