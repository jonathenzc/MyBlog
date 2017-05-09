title: Is log(n!) = Θ(n·log(n))？
date: 2015-03-04 14:31:41
categories: 【算法】
tags: [算法, brain teaser]
---
## {{ title }} ##

---
在上算法课的时候，老师给我们做了个quiz，题目是`f(n)=ln(n!)`和`g(n)=nlog(n)`的关系。

当然根据解题经验来说，`ln(n!) = Θ(n·log(n))`，那么怎么证明它是对的呢？

首先利用**换底公式**可以将ln换成log，也就是说在算法分析中以e为底和以2为底是等价的。

接着，证明`log(n!)`的上界是`nlog(n)`。

`log(n!) = log(n) + log(n-1) + ... + log(2)` 

`<= log(n) + log(n) + ... + log(n) = nlog(n)`

所以`log(n!)`的上界是`nlog(n)`还是比较好证的。

那么最后需要证明`log(n!)`的下界是`nlog(n)`。

`log(n!) = log(n) + log(n-1) + ... + log(2)`

`>= log(n) + log(n-1) + ... + log(n/2)`

`>= log(n/2) + log(n/2) + ... + log(n/2)`

`= (n/2)log(n/2) = (n/2)(logn - log2)`

因为nlogn的阶数比nlog2的高，所以可以忽略。

那么`log(n!)`的上下界都是`nlog(n)`，log(n!) = Θ(n·log(n))得证。

 