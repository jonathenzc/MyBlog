title: radio点不中
date: 2016-07-05 00:02:53
categories: 【html】
tags: [html]
---
## {{ title }} ##

---

radio按钮点不中，需要往旁边移一点才能点到，这是因为html写的是

```
<input type="radio" id="type2_radio" name="evatype" value="random">radio1
```

我们只需要在外面套一个<label>标签即可

```
<label> <input type="radio" id="type2_radio" name="evatype"	value="random">radio1 </label>
```