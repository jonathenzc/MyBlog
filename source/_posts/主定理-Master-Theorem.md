title: 主定理(Master Theorem)
date: 2015-03-04 11:22:35
categories: 【算法】
tags: [算法, brain teaser]
---
## {{ title }} ##

---
主定理在分析算法复杂度的时候作用还是挺大的，比如给你来个T(n) = aT(n/b) + O(n^d)，递推公式都得到了，但是求不出来那还是挺遗憾的。

我们可以这样来看这个问题，将需要T(n)时间完成的事情分成a份需要花T(n/b)时间来完成的事情再加上需要花费O(n^d)时间来完成的事情。

那么可以得到一颗a叉树，树的高度是logbn。

<img src="/img/masterTheorem.png"  class="img-shadow img-center"/>

那么在任意K层，对每个分割后的事情需要花费多少时间来执行呢？

<img src="/img/kLayer.png"  class="img-center"/>

其中`a^k`表示有a^k个分叉，`O((n/b^k)^d)`为在第k层每个事情的时间花费为n/b^k，带入到O(n^d)中,得到花费。

这是个等比数列，对它求和，数列共有logbn个，所以指数上是logbn，得到

<img src="/img/kLayerSum.png"  class="img-center"/>

那么三种情况讨论：

1. a/b^d = 1时，即d = logba, 那么原数列之和为`logbn`个`O(n^d)`，T(n) = O(n^d*logbn) = O(n^d logn)
2. a/b^d > 1时，即d < logba, 那么数列之和表达式中，分子右边的多项式的阶数大于左边多项式阶数，化简，n^d可以和分母的b^d*(logbn)约掉，得到a^logbn，最后整理为T(n) = O(n^logba)
3. a/b^d < 1时，即d > lobba, 那么数列之和表达式中，分子右边的多项式的阶数小于左边多项式阶数，那么T(n) = O(n^d)

**结论**

<img src="/img/masterTheoremFormula.png"  class="img-center"/>