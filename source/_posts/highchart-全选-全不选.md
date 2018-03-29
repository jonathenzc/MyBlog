title: highchart 全选 | 全不选
date: 2018-03-27 11:45:32
categories: 【highcharts】
tags: [highcharts]
---
## {{ title }} ##

---

当highcharts要展示的series变多后，想要全选和全不选变得非常迫切

```
$('#checkAll').click(function(){
    for(i=0; i < chart.series.length; i++) {
        if(chart.series[i].selected == false){
            chart.series[i].select();
            showSeries.call(chart.series[i], {checked: true});
        }
    }
});
```

用visible、show()和hide()也可以实现

```
$('#checkAll').click(function(){
    for(i=0; i < chart.series.length; i++) {
        if(chart.series[i].visible == false){
            chart.series[i].show();
        }
    }
});
```


参考资料：

1. [stack overflow 问题](https://stackoverflow.com/questions/16357921/how-to-check-and-uncheck-all-the-legend-elements-in-highcharts-linechart)
2. [解决示例](http://jsfiddle.net/simo/57SR9/94/)