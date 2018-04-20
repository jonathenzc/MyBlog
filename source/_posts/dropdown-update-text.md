title: dropdown update text
date: 2018-04-20 17:23:53
categories: 【jQuery】
tags: [jQuery]
---
## {{ title }} ##

---

bootstrap下拉框更新按钮的内容

```javascript
 $(function(){
    $(".dropdown-menu li a").click(function(){
      $(".btn:first-child").text($(this).text());
      $(".btn:first-child").val($(this).text());
   });
});
```

或者

```javascript
$(".dropdown-menu li a").click(function(){
  $(this).parents(".dropdown").find('.btn').html($(this).text() + ' <span class="caret"></span>');
  $(this).parents(".dropdown").find('.btn').val($(this).data('value'));
});
```

参考资料：

1. [How to Display Selected Item in Bootstrap Button Dropdown Title](https://stackoverflow.com/questions/13437446/how-to-display-selected-item-in-bootstrap-button-dropdown-title)