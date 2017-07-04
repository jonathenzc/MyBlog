title: dataTable render
date: 2017-07-04 11:29:46
categories: 【jQuery】
tags: [jQuery]
---
## {{ title }} ##

---

操作jQuery的dataTable时，想对传入的数据进行一些处理，可以给该行添加一个render的属性，传入操作的函数名。

比如

```javascript
{ targets: 8, visible: true, data: 'accessNumber', render: thousandSeparator}
```

其实render后的thousandSeparator函数是对数字进行千位分隔符的操作，加了这个属性后，就会把data所对的数据传入thousandSeparator的函数中。

