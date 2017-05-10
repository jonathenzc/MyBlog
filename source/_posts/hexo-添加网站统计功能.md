title: hexo-添加网站统计功能
date: 2017-05-10 16:33:21
categories: 【Hexo】
tags: [Hexo]
---
## {{ title }} ##

---

我们经常可以看到别人的博客中下面有该网站的统计信息，我使用的是不如的不蒜子来统计网站信息，非常方便。

在themes/你的主题/layout/_partial/footer.ejs下添加以下内容即可

```html
<script async src="//dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js"></script>
```

然后我是在版权的地方放入统计的

```html
<p class="copyright">
	People: <span id="busuanzi_value_site_uv"></span> |
	Views: <span id="busuanzi_value_site_pv"></span> |
	Page: <span id="busuanzi_value_page_pv"></span>
</p>
```


参考网站：

[不如](http://ibruce.info/2015/04/04/busuanzi/)

[不蒜子](http://busuanzi.ibruce.info/)