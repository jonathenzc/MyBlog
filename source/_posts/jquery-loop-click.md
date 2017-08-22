title: jquery loop click
date: 2017-07-30 17:36:50
categories: 【jQuery】
tags: [jQuery]
---
## {{ title }} ##

---

在处理javascript时，我们常常会利用循环对命名相近的一些控件进行处理，比如按钮，我们给它赋id为button0,button1... 这时，我们需要给它们绑定click事件，

```javascript
$someBtn.click(function(){
    window.open(someArray.url);
});
```

如果这样写的话，就会有闭包的问题，导致获取不到url，根据参考资料里的讲解可以这样写：

```javascript
function createCallback( i ){
  return function(){
    alert('you clicked' + i);
  }
}

$(document).ready(function(){
  for(var i = 0; i < 20; i++) {
    $('#question' + i).click( createCallback( i ) );
  }
});
```

参考资料：

1. [Assign Click Handlers in for loop](https://stackoverflow.com/questions/4091765/assign-click-handlers-in-for-loop)