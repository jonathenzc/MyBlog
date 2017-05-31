title: highcharts右下角链接
date: 2017-05-27 13:53:41
categories: 【highcharts】
tags: [highcharts]
---
## {{ title }} ##

---

在使用highcharts的样例图时，经常会在右下角出现"highcharts.com"的超链接。虽然这样不太好，但是有时候为了显示更多的数据，我们只能把这个超链接去掉，可以有两种做法：

1. 在highcharts.js中搜索“credits”的内容，把enabled改为disabled，当然你也可以直接删掉
2. 在使用的地方为credits选项配置false

```javascript
credits:{
    enabled:false
}
```