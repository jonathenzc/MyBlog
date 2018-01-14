title: datatables 单列的数据由多个json字段组成
date: 2018-01-14 16:46:49
categories: 【jQuery】
tags: [jQuery]
---
## {{ title }} ##

---

第一种方法，用一个其他函数来操作：

```javascript
aoColumns = [ 
    { "mData": getNameAndEmail },
    { "mData": "address" }
]; 

function getNameAndEmail(data, type, dataToSet) {
    return data.name + "<br>" + data.email;
}
```

第二个方法，直接写函数，本质上不指明特定的json key就可以直接操作json的根key：
```javascript
"aoColumns": [
    { "mData": "i_id" },
    { "mData": "i_name" },
    { "mData": function (data, type, dataToSet) {
        return data.i_id + "<br/>" + data.i_name;
    }}
],
```

参考资料：

[how-to-put-multiple-data-in-a-datatable-column](https://stackoverflow.com/questions/15174560/how-to-put-multiple-data-in-a-datatable-column)