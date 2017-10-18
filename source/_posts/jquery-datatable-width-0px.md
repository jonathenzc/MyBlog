title: 'jquery datatable width: 0px'
date: 2017-10-18 15:51:34
categories: 【jQuery】
tags: [jQuery]
---
## {{ title }} ##

---

在将tab和datatable结合的时候，由于没有设置bAutoWidth参数，使得除了第一个tab外，其他的tab下的table都有个width:0px的style。查了之后，发现只需要设置datatable的参数bAuthoWidth false就可以了。

参考资料：

[DataTables width problem](https://stackoverflow.com/questions/7023224/datatables-width-problem)