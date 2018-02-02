---
title: 如何积 1/ln(x)？
tags: []
date: 2018-02-02 07:00:19
---

欧拉他比题主你高到不知道哪里去了, 他想了半天, 直接钦点 ![\int_2^x \frac{1}{\log (t)} \, \mathrm{d}t=\text{Li}(x)](//www.zhihu.com/equation?tex=%5Cint_2%5Ex+%5Cfrac%7B1%7D%7B%5Clog+%28t%29%7D+%5C%2C+%5Cmathrm%7Bd%7Dt%3D%5Ctext%7BLi%7D%28x%29)

你问我支持不支持, 我当然是支持的, 因为这个没法按照积分的基本方法积出来...

* * *

杀鸡焉用牛刀, 这也用不到完全体的刘伟尔定理, 用一个特化情形就行了.

好好体会这种思想

考虑积分 ![\int f(x)e^{g(x)}\mathrm{d}x](//www.zhihu.com/equation?tex=%5Cint+f%28x%29e%5E%7Bg%28x%29%7D%5Cmathrm%7Bd%7Dx) , 其中 ![g(x) ](//www.zhihu.com/equation?tex=g%28x%29+) 为多项式.

那它的积分是不是应该是 ![R(x)e^{g(x)}](//www.zhihu.com/equation?tex=R%28x%29e%5E%7Bg%28x%29%7D) 的形式?

![\int f(x)e^{g(x)}\mathrm{d}x = R(x)e^{g(x)}](//www.zhihu.com/equation?tex=%5Cint+f%28x%29e%5E%7Bg%28x%29%7D%5Cmathrm%7Bd%7Dx+%3D+R%28x%29e%5E%7Bg%28x%29%7D)

很容易验证的呀, 两边求导:

![(R(x)e^{g(x)})](//www.zhihu.com/equation?tex=%28R%28x%29e%5E%7Bg%28x%29%7D%29%27%3D+e%5E%7Bg%28x%29%7D+%5Cleft%28R%28x%29+g%27%28x%29%2BR%27%28x%29%5Cright%29+%3D+f%28x%29e%5E%7Bg%28x%29%7D)

![e^{g(x)}](//www.zhihu.com/equation?tex=e%5E%7Bg%28x%29%7D) 怎么着也非零吧, 消掉

![R(x) g](//www.zhihu.com/equation?tex=R%28x%29+g%27%28x%29%2BR%27%28x%29%3D+f%28x%29)

如果 ![ f(x) ](//www.zhihu.com/equation?tex=+f%28x%29+) 是个有理函数, 那么我们也期望 ![ R(x) ](//www.zhihu.com/equation?tex=+R%28x%29+) 也是个有理函数

设 ![R(x):=\frac{P(x)}{Q(x)}](//www.zhihu.com/equation?tex=R%28x%29%3A%3D%5Cfrac%7BP%28x%29%7D%7BQ%28x%29%7D) , 其中 ![P(x),Q(x)](//www.zhihu.com/equation?tex=P%28x%29%2CQ%28x%29) 为互质多项式函数, 代入得

![f(x)=\left(\frac{P(x)}{Q(x)}\right)](//www.zhihu.com/equation?tex=f%28x%29%3D%5Cleft%28%5Cfrac%7BP%28x%29%7D%7BQ%28x%29%7D%5Cright%29%27%2B%5Cfrac%7BP%28x%29%7D%7BQ%28x%29%7Dg%27%28x%29)

整理下也就是

![Q(x)[Q(x)f(x)-P](//www.zhihu.com/equation?tex=Q%28x%29%5BQ%28x%29f%28x%29-P%27%28x%29-P%28x%29g%27%28x%29%5D%3D-P%28x%29Q%27%28x%29)

* * *
> 综上所述: 
> 若 ![f(x)](//www.zhihu.com/equation?tex=f%28x%29) 是有理函数, ![ g(x)](//www.zhihu.com/equation?tex=+g%28x%29) 是多项式函数, 那么 ![\int f(x)e^{g(x)}\mathrm{d}x ](//www.zhihu.com/equation?tex=%5Cint+f%28x%29e%5E%7Bg%28x%29%7D%5Cmathrm%7Bd%7Dx+) 初等的充要条件就是:
> 存在互质多项式 ![ P(x),Q(x) ](//www.zhihu.com/equation?tex=+P%28x%29%2CQ%28x%29+) 使得 ![ Q(x)[Q(x)f(x)-P](//www.zhihu.com/equation?tex=+Q%28x%29%5BQ%28x%29f%28x%29-P%27%28x%29-P%28x%29g%27%28x%29%5D%3D-P%28x%29Q%27%28x%29+) 成立.

于是我们就证明了刘伟尔定理的指数多项式情形, 其实也可以从刘伟尔定理特化得到, 就这样已经很强大了...

我们来考虑积分 ![ \int\frac{e^x}{x}\mathrm{d}x](//www.zhihu.com/equation?tex=+%5Cint%5Cfrac%7Be%5Ex%7D%7Bx%7D%5Cmathrm%7Bd%7Dx) ...

什么, 你问为什么不直接做题要考虑这个?

笨啊,变量替换啊

![\int e^{e^x}\mathrm{d}x\Leftrightarrow\int\frac{e^x}{x}\mathrm{d}x\Leftrightarrow\int\frac{\mathrm{d}x}{\ln x}](//www.zhihu.com/equation?tex=%5Cint+e%5E%7Be%5Ex%7D%5Cmathrm%7Bd%7Dx%5CLeftrightarrow%5Cint%5Cfrac%7Be%5Ex%7D%7Bx%7D%5Cmathrm%7Bd%7Dx%5CLeftrightarrow%5Cint%5Cfrac%7B%5Cmathrm%7Bd%7Dx%7D%7B%5Cln+x%7D)

选取 ![ f(x)=\frac1x,g(x)=x](//www.zhihu.com/equation?tex=+f%28x%29%3D%5Cfrac1x%2Cg%28x%29%3Dx) , 代入化简得

![Q(x)[Q(x)-x P](//www.zhihu.com/equation?tex=Q%28x%29%5BQ%28x%29-x+P%27%28x%29-xP%28x%29%5D%3D-xP%28x%29Q%27%28x%29)

![\small{\color{red}{注意接下来的这一波操作!}}](//www.zhihu.com/equation?tex=%5Csmall%7B%5Ccolor%7Bred%7D%7B%E6%B3%A8%E6%84%8F%E6%8E%A5%E4%B8%8B%E6%9D%A5%E7%9A%84%E8%BF%99%E4%B8%80%E6%B3%A2%E6%93%8D%E4%BD%9C%21%7D%7D)

![(x-a)^k=0](//www.zhihu.com/equation?tex=%28x-a%29%5Ek%3D0) 中 ![ a](//www.zhihu.com/equation?tex=+a) 叫重根或者重点, ![k](//www.zhihu.com/equation?tex=k) 叫重数或者重根数这个懂吧

因为 ![Q(x)](//www.zhihu.com/equation?tex=Q%28x%29) 为多项式, 所以在复数域中必有零点, 设零点 ![x=a](//www.zhihu.com/equation?tex=x%3Da) , 其重数为  ![r&gt;0](//www.zhihu.com/equation?tex=r%3E0)

由于 ![P(x), Q(x)](//www.zhihu.com/equation?tex=P%28x%29%2C+Q%28x%29) 为互质多项式, 所以 ![P(a)\neq 0, Q](//www.zhihu.com/equation?tex=P%28a%29%5Cneq+0%2C+Q%27%28x%29) 的重数为 ![r-1](//www.zhihu.com/equation?tex=r-1)

若 ![x=a\neq0](//www.zhihu.com/equation?tex=x%3Da%5Cneq0)

则 ![x=a](//www.zhihu.com/equation?tex=x%3Da) 既是 ![Q(x)[Q(x)-x P](//www.zhihu.com/equation?tex=Q%28x%29%5BQ%28x%29-x+P%27%28x%29-xP%28x%29%5D) 的重根,重数显然 ![&gt;=r](//www.zhihu.com/equation?tex=%3E%3Dr)

且右边 ![-xP(x)Q](//www.zhihu.com/equation?tex=-xP%28x%29Q%27%28x%29) 的重根重数为 ![r-1](//www.zhihu.com/equation?tex=r-1)

**矛盾!**

若 ![x=a=0](//www.zhihu.com/equation?tex=x%3Da%3D0) ,令 ![Q(x)=x^r h(x)](//www.zhihu.com/equation?tex=Q%28x%29%3Dx%5Er+h%28x%29) 好了,代入原式有

![h(x)x^{r+1}\left[h(x)x^{r-1}-P](//www.zhihu.com/equation?tex=h%28x%29x%5E%7Br%2B1%7D%5Cleft%5Bh%28x%29x%5E%7Br-1%7D-P%27%28x%29-P%28x%29%5Cright%5D%3D-x%5ErP%28x%29%5Brh%28x%29%2Bxh%27%28x%29%5D)

![x=0](//www.zhihu.com/equation?tex=x%3D0) 仍然同时是左右两边的重根, 左边重数 ![&gt;=r+1](//www.zhihu.com/equation?tex=%3E%3Dr%2B1) ,右边为 ![r](//www.zhihu.com/equation?tex=r) ..GG

**还是矛盾!**

好吧那么假设 ![Q(x)](//www.zhihu.com/equation?tex=Q%28x%29) 不是多项式而是常数 ![k](//www.zhihu.com/equation?tex=k)

于是有 ![ k[k-x P](//www.zhihu.com/equation?tex=+k%5Bk-x+P%27%28x%29-xP%28x%29%5D%3D0), 由上可知同样不行

**重数还是矛盾!**

* * *

于是综上所述 ![ \int\frac{e^x}{x}\mathrm{d}x ](//www.zhihu.com/equation?tex=+%5Cint%5Cfrac%7Be%5Ex%7D%7Bx%7D%5Cmathrm%7Bd%7Dx+) 非初等, 不能按照积分的基本法来....

那么就只能钦定 ![\int \frac{1}{\log (x)} \, dx=\text{li}(x)](//www.zhihu.com/equation?tex=%5Cint+%5Cfrac%7B1%7D%7B%5Clog+%28x%29%7D+%5C%2C+dx%3D%5Ctext%7Bli%7D%28x%29) 了啊...

題主儂識得唔識得噶?

来源：知乎 www.zhihu.com

作者：[酱紫君](http://www.zhihu.com/people/GalAster?utm_campaign=rss&utm_medium=rss&utm_source=rss&utm_content=author)

【知乎日报】千万用户的选择，做朋友圈里的新鲜事分享大牛。
        [点击下载](http://daily.zhihu.com?utm_source=rssyanwenzi&utm_campaign=tuijian&utm_medium=rssnormal)

此问题还有 [3 个回答，查看全部。](http://www.zhihu.com/question/266317634/answer/306550276?utm_campaign=rss&utm_medium=rss&utm_source=rss&utm_content=title)