title: "#1102 Individual Income Tax"
date: 2016-08-25 17:36:58
categories: 【HihoCoder】
tags: [HihoCoder, 数学]
---
## {{ title }} ##

---

| Grade Monthly Taxable Income  |     Tax Rate(%)     |
|----------|:-------------:|
| Income of 1,500 yuan or less |  3% |
| That part of income in excess of 1,500 to 4,500 yuan |    10%   |
| That part of income in excess of 4,500 to 9,000 yuan |    20%   |
| That part of income in excess of 9,000 to 35,000 yuan |    25%   |
| That part of income in excess of 35,000 to 55,000 yuan |    30%   |
| That part of income in excess of 55,000 to 80,000 yuan |    35%   |
| That part of income in excess of 80,000 yuan |    45%   |

这道题目需要注意的是税率的结算，比如我的salary超过15000，那么实际征税是15000-3500。这部分的钱在9000~35000之间，那么税率就是25%。

剩下在4500~9000之间的呢？就是（9000-4500）来征税；在1500~4500之间的呢？用（4500-1500）来征税。这些税的额度是不会变的。

所以我们构建一个大小为7的数组来储存应该缴纳的税，tax[0]为0

tax[i] = tax[i-1]+(bound[i]-bound[i-1])*rate[i-1];bound就是{0,1500,4500,9000,35000,55000,80000}

这样我们只要知道税率征收的区间就可以得到收入是多少了。
