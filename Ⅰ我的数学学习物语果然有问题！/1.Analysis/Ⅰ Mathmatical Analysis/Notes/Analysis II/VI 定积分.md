---
tags:
  - 微积分
  - Mathematical_Analysis
---
> 大家好各位，好久没有写笔记了。本期内容是美赛结束后第一次速成回归（速成在哪里？），不知道刷到这篇文章的人美赛打得怎么样呢？都祝愿我们有一个好结果吧！总之，比赛之类的，就让它崇高一点，让它精神一些。

> 我们已经学习了不定积分，现在我们要开启定积分的旅程了。上一篇文章有观众提出题目量太少的问题，其实这是一个很棘手的问题。一是我找题目首先要自己先做过一遍，二是像微积分这种需要大量练习来提高熟练度的学科需要大量练习 (练习一定要有练习！) 我单打打题目就很累了orz 。如果你们真的要我干的话，请你充值吧 (doge) ，你可以提一个为期一期的内容要求 —— 前提是我能办到 . 不过不建议大家为我充值哦，太浪费了！！！好的，我们在在不定积分的基础上可以聚焦于解决一些更加实用的问题。实际上来说，我们之前一直准备的几何直观就是为定积分准备的，只不过当时我操之过急，提前秀出了.诸位可以去看看此前的文章 ：[[V 不定积分#圆为何如此？（这是一个朴素的思维）]] 

# 求求面积、算算功

好比我们之前提到的计算圆的面积，我们截取函数的一段 —— 那么这一段函数就不一定是一个一次曲线了。回忆我们之前所模拟的叠胶带的方法，这里稍微做一下逆向，也就是说，我们也可以把这个曲线像撕胶带一样撕开，单独计算一块的面积再相加形如 
$$S=\sum_{i=1}^nf(\xi_{i})\Delta x\ , \quad (\Delta x=x_{i}-x_{i-1})$$
没错，这就是我们要求的面积！我们做到了，非常好理解。
好的，现在我给出一个相对熟悉的例子 —— 做功。我们小学二年级就学过 
$$W=Fs$$
恒力做功高中就写烂了，我们要研究变力做功 . 联系我们之前微分和导数学习的知识，我们可以近似地认为我们再极短路程中所用地变力是一个恒力 (对，变力一定是恒力) 于是我们又得到一个公式 
$$W=\sum_{i=1}^n F(\xi_{i})\Delta s \, ,\quad (\Delta s=s_{i}-s_{i-1})$$
总结来说，我们的定积分思想就是 “**分割，近似求和，取极限**” 

# 初识定积分

Def.1 ( $\mathbf{分割}$ ) 设闭区间 $[a,b]$ 上有 $n-1$ 个点，依次为 
$$a=x_{0}<x_{1}<\cdots<x_{n-1}<x_{n}=b$$
我们把 $[a.b]$ 分割为 $n$ 个小区间 $\Delta_{i}=[x_{i-1},x_{i}]$ , $i=1,2,\cdots,n$ 这些分点或这些闭子区间构成对 $[a,b]$ 的一个**分割** .记为 
$$T=\{x_{0},x_{1},\cdots,x_n\}\ 或\ \{\Delta_{1}.\Delta_{2},\cdots,\Delta n\}\ .$$
小区间 $\Delta_{i}$ 的长度称为分割 $T$ 的模，记为 
$$||T||=\max_{1\leq i\leq n}\{\Delta x_{i}\} \ ,\ \Delta_{i}=x_{i}-x_{i-1}$$
我们要注意的是分割 $T$ 一旦给出，$||T||$ 就随之确定，具有同一细度 $||T||$ 的分割 $T$ 却有无数多个

Def.2 ( $近似求和$ ) 在一个分割中取任意点 $\xi_{i}$ 分别求和就有 
$$\sum_{i=1}^nf(\xi_{i})\Delta x$$
我们称此和式为 $f$ 在 $[a,b]$ 中的积分和，也称 $Riemann$ **和** 
从这个式子，我们可以知道：积分和既和分割 $T$ 有关，又与选取的 $\{\xi_{i}\}$ 有关

$Def.3\ (取极限)$  设 $f$ 定义在 $[a.b]$ 上， $J$ 是一个确定的实数. 若对任给的正数 $\varepsilon$ , 总是存在某一正数 $\delta$ , 使得对 $[a,b]$ 内的任何分割 $T$ , 以及在其上选择的任意点集 $\{\xi_{i}\}$ , 只要 $||T||<\delta$ , 就有 
$$|\sum_{i=1}^n f(\xi_{i})\Delta x-J|<\varepsilon\ ,$$
则称 $f$ 在区间 $[a,b]$ 上 **可积** 或 $Riemann$ **可积** ; 就称该确定的实数 $J$ 为 $f$ 在 $[a,b]$ 上的定积分或者 $Riemann$ 积分。记为 
$$J=\int_{a}^bf(x)dx$$
其中 $f$ 为**被积函数**，$x$ 为**积分变量**，$[a,b]$ 为**积分区间**，分别为**下限**和**上限** 

我们在先前就已经讨论了用积分求面积的问题。在二维函数中，我们的函数会时不时穿过 $x$ 轴 . 我们就 定义 处于 $y$ 轴负半轴的虚线的积分面积为 ''-"   $-J=\int_{a}^b[-f(x)]dx$ . 

这里我们来理解一个概念：当 $a\geq b$ 时积分式有，
$$\int_{a}^bf(x)dx=-\int_{b}^a f(x)dx$$
关于这个我有一个可能不太成熟的证明:
![[微信图片_20260208012111_287_7.jpg]]

# 可积 "可不" 积？

是可不哎，好！

我们研究过的 $Dirichlet$ 函数，其在选取无理数和有理数时的值不同，所以在我们给定的一个区间内若都选取有理数和若都选取无理数所得到的值数不一样。那么我们所言，积分也一脉相承的是一个求极限的问题，怎么可能存在两个极限？！那么这就是一个不可积的情况。

那么我们可以知道，并不是所有的有界函数都是可积的，那我们要怎么确定一个函数是否可积呢？

这里我们引入一个概念，$Darboux$ **和**

$Thm.1$ （$可积的第一充要条件$）有界函数  $f(x)$  在 $[a, b]$可积的充分必要条件是，$f$ 在 $[a,b]$ 上的上下积分相等，即：  
$$\overline{\int_{a}^b} f(x)dx=  \underline{\int_{a}^b}f(x)dx$$
$Darboux$ 和，即使将每一个分割与上确界和下确界积做和 
$$M_{i}=\sup_{x\in \Delta _{i}}f(x),\ S(T)=\sum_{i=1}^nM_{i}\Delta x_{i}$$
$$m_{i}=\inf_{x\in \Delta _{i}}f(x),\ s(T)=\sum_{i=1}^nm_{i}\Delta x_{i}$$
分别就称为 $f$ 关于分割 $T$ 的$Darboux$ **上和**与 $Darboux$ **下和** (陈纪修书中翻译为**大和**和**小和**)

proof. 充要证明
可积 "$\Rightarrow$" 设 $f$ 在 $[a,b]$ 可积，则 $\forall \varepsilon >0$ , $\exists \delta >0$ , $||T||<\delta$ , 有 
$$|\sum_{i=1}^nf(\xi_{i})\Delta x_{i}-J|<\varepsilon$$
由于 $\sup_{x\in \Delta _{i}}f(x),\inf_{x\in \Delta _{i}}f(x)$ 是点集 $\{\xi_{i}\}$的上下确界于是就有
$$|S(T)-J|\leq\varepsilon\ , \quad |s(T)-J|\leq\varepsilon$$
于是得证
可积 "$\Leftarrow$" 设 $S(T)=s(T)=J$. 由不等式： 
$$J-\varepsilon\leq s(T)\leq\sum_{i=1}^nf(\xi_{i})\Delta x_{i}\leq S(T)\leq J+\varepsilon$$
于是得证.

$Thm.2$ （$可积的第二充要条件$）$f$ 在 $[a,b]$ 上可积的充要的充要条件是 : 任给 $\varepsilon>0$ , 总是存在一个分割 $T$ ,使得 
$$S(T)-s(T)<\varepsilon, \ 即 \sum_{i=1}^n \omega_{i}\Delta x{i<\varepsilon}$$
其中 $\omega_{i}=M_{i}-m_{i}$ 我们称 $\omega_{i}$ 为 $f$ 在 $\Delta_{i}$ 上的振幅 , $i=1,2,\cdots,n$ 

proof.  可积 "$\Rightarrow$"  $f$ 在 $[a,b]$ 可积，由可积第一充要条件可得 
$$\lim_{ ||T|| \to 0 }[S(T)-s(T)]=0 $$
因此，$\forall \varepsilon$ , 只要 $||T||$ 足够小 , 就总是存在 
$$S(T)-s(T)<\varepsilon$$
可积 "$\Leftarrow$"  由不等式 
$$s(T)<\underline{\int_{a}^b} f(x)dx<\overline{\int_{a}^b} f(x)dx<S(T)$$
可推得： 
$$0\leq \overline{\int_{a}^b} f(x)dx -  \underline{\int_{a}^b} f(x)dx  \leq S(T)-s(T)<\varepsilon$$
由 $\varepsilon$ 的任意性，有 $\overline{\int_{a}^b} f(x)dx=  \underline{\int_{a}^b}f(x)dx$ ，根据第一可积充要条件，得证 .

$Thm.3$ （$可积的第三充要条件$） $\forall \varepsilon,\eta$ ,总是存在某一个分割 $T$ ,使得属于 $T$ 的所有小区间中，对应于振幅 $\omega_{k'}\geq \varepsilon$ 的那些小区间 $\Delta_{k'}$ 的总长 $\sum_{k'}\Delta_{k'}<\eta$ 

proof.  可积 "$\Rightarrow$"  对于 $\sigma=\varepsilon \eta>0$  ，存在某个分割 $T$ , 使 $\sum_{k}\omega_{k\Delta x_{k}}<\sigma$ . 于是有 
$$\varepsilon \sum_{k'}\Delta x_{k'}\leq \sum_{k'}\omega_{k'}\Delta_{k'}\leq \sum_{k}w_{k \Delta_{k'}}<\varepsilon \eta$$
于是可得 
$$\sum_{k'}\Delta x_{k'}<\eta\ .$$
可积 "$\Leftarrow$"   $\forall \varepsilon'>0$ , 取 $\varepsilon=\frac{{\varepsilon'}}{2(b-a)>0}$ , $\eta=\frac{{\varepsilon'}}{2(M-m)}>0$ . 根据题设，有
$$\begin{align}
\sum_{k}\omega_{k}\Delta x_{k}=\sum_{k'}\omega_{k'}\Delta x_{k'}+\sum_{k''}\omega_{k''}\Delta x_{k''} \\
<(M-m)\sum_{k'}\Delta x_{k'}+\varepsilon \sum_{k''}\Delta x_{k''} \\
\leq (M-m)\eta+\varepsilon(b-a)\\
=\frac{\varepsilon'}{2}+\frac{{\varepsilon'}}{2}=\varepsilon'
\end{align}$$
于是可积

根据可积的充要条件，我们可以证明可积的充分条件，来帮助我们判断一些函数是可积的 . 

$Thm.\ 4.1$ ( $连续函数可积$ ) $f$ 在 $[a,b]$ 上连续 , 则 $f$ 在 $[a,b]$ 上可积 .

> 快速理解连续可以借助手指描一下，我们又有分几类间断点，第一类中又分可去间断点和跳跃间断点：分别代表了一个函数在某点无定义或者极限于函数值不相等与左右极限不等（<font color="#c00000">极限指有限极限</font>）；第二类则指至少有一侧极限不存在的点，如：$y=\frac{1}{x}$ 、 $y=\sin \frac{1}{x}$ 在 $0$ 处的情况

proof. 由于 $f$ 在闭区间 $[a,b]$ 上连续 , 因此在 $[a.b]$ 上一致连续 . 于是给定区间 $[a,b]$ 两点 $x',x''$ ，只要 $|x'-x''|<\delta$ 我们就有 
$$|f(x')-f(x'')|< \frac{\varepsilon}{b-a}$$
可以发现，只要满足 $||T||<\delta$ 就能使 $f$ 的振幅满足 
$$\omega_{i}=M_{i}-m_{i}=\sup_{x'.x''\in\Delta_{i}}|f(x')-f(x'')|\leq \frac{\varepsilon}{b-a}$$
从而有 
$$\sum_{T}\omega_{i}\Delta x_{i}\leq \frac{\varepsilon}{b-a}\sum_{T}\Delta x_{i}=\varepsilon$$
得证

$Thm.\ 4.2$ ( $有限个间断点可积$ ) 若 $f$ 在区间 $[a,b]$ 上只有有限个间断点的有界函数，则 $f$ 在 $[a,b]$ 上可积

> 这个定理我们可以脱离数理证明进行一个朴素的理解：当我们的分割足够小时，即使除去了某一个 $f(x_{i})\Delta x_{i}$ 也不影响积分的结果。有限个具有一般性，但如我们的 $Dirichlet$ 函数，其每一个点都间断，那就不是有限个了。对其具体的理解可以尝试了解实分析中的勒贝格测度。

proof. 我们只要证明仅有一个间断点的情况即可推广，不妨设该点为 $b$ 
$\forall \varepsilon$ , 取 $\delta'$ 满足 $0<\delta'< \frac{\varepsilon}{2(M-m)}$ , 且 $\delta'<b-a$ ，其中 $M \& m$ 分别为 $f$ 在 $[a,b]$ 上的上确界与下确界 . 记 $f$ 在小区间 $\Delta'=[b-\delta',b]$ 上的振幅为 $\omega'$ , 则 
$$\omega'\delta'<(M-m)\ \cdot{}\ \frac{\varepsilon}{2(M-m)}=\frac{\varepsilon}{2}$$
在区间 $[a,b-\delta']$ 中必存在一个分割 $T'=\{\Delta_{1},\Delta_{2},\cdots,\Delta_{n-1}\}$ 使得 
$$\sum_{T}\omega_{i}\Delta x_{i}< \frac{\varepsilon}{2}$$
我们只要令 $\Delta_{n}=\Delta'$ 就能完成证明

$Thm.\ 4.3$ ( $单调函数可积$ ) 若 $f$ 在 $[a.b]$ 上单调，那么 $f$ 在 $[a,b]$ 上可积

proof. 只要令 $||T||< \frac{\varepsilon}{f(b)-f(a)}$ 即可，证明省略

# 牛顿 - 莱布尼茨公式

如果我们采用求极限的方法来求积分，我们的运算和脑力会大大消耗。那么有没有什么好的方法可以求积分呢？有的，兄弟有的，我们有一个公式叫做牛顿 - 莱布尼茨公式。我们先不看公式，我们先来想一想这个公式是怎么来的。

在我们学习不定积分的时候，就能从原函数反导出积分函数。某种意义上，我们得到的函数是原函数的一个面积函数，但是他会随着你取的值而变化。我们可以随意画一个函数图像，取其中一个自变量，画出此时的阴影。然后我们取另一个自变量，进行同样的操作。我们能看到函数的阴影有重叠部分，也有独立部分。这个独立部分正好是我们要求的那个两个自变量之间的 "类梯形"。于是，我们能类似写出这样的公式 
$$\int_{a}^b f(x)dx=F(b)-F(a)$$
$Thm.\ 5$ 若函数 $f$ 在 $[a,b]$ 上连续，且存在原函数 $F$ , $F'(x)=f(x)$ , $x\in [a,b]$ , 则 $f$ 在 $[a,b]$ 上可积，且 
$$\int_{a}^b f(x)dx=F(b)-F(a)$$
我们称此公式为 $Newton-Laibinz$ 公式，或可写为 
$$\int _{a}^b f(x)dx=F(x)\big|^b_{a}$$
proof. 只要证，$\forall\varepsilon>0$ , $\exists \delta>0$ , 当 $||T||< \delta$ 时 ，有 
$$|\sum_{i=1}^nf(x_{i}\Delta x_{i})-[F(b)-F(a)]|<\varepsilon$$
我们对 $F(x)$ 使用拉格朗日中值定理，就有 
$$F(b)-F(a)=\sum_{i=1}^n[F(x_{i})-F(x_{i-1})]=\sum_{i=1}^nF'(\eta_{i})\Delta x_{i}$$
由积分连续的充要条件证明可知：当 $\Delta x_{i}\leq ||T||< \delta$ 时，任取 $\xi_{i}\in[x_{i-1},x_{i}]$ , 有 $|\xi_{i}-\eta_{i}|<\delta$ ,我们就有 
$$|\sum_{i=1}^nf(x_{i}\Delta x_{i})-[F(b)-F(a)]|\leq\sum_{i=1}^n |f(\xi_{i})-f(\eta_{i})|\Delta x_{i}< \frac{\varepsilon}{b-a}\cdot \sum_{i=1}^n\Delta x_{i} =\varepsilon$$
于是得证 . 

> **削弱定理条件**
>
> 1. 闭区间连续，开区间可导
> 2. 在 $[a,b]$ 可积

> 今天的内容是微积分的最后一部分内容。至此，该系列完结（单元完结），不知道大家有没有做到速成捏。话说其实是带着点“科普性质”在这里讲概念的，真正的成才还是要大家多多练习，达到一定的熟练度。在做题过程中多 "注意注意" ，不过 這種機會不必刻意去求！

# 定积分性质

#### 定积分基本性质

$Prop. 1$ 
若 $f$ 在 $[a,b]$ 上可积 , $k$ 为常数 , 则 $kf$ 在 $[a,b]$ 上也可积 , 且 
$$\int_{a}^b kf(x)dx=k \int_{a}^b f(x)dx$$
proof. 略

$Prop. 2$ 
若 $f\ ,\ g$ 在 ${a,b}$ 上都可积，则 $f\pm g$ 在 $[a,b]$ 上也可积，且 
$$\int_{a}^b [f(x)\pm g(x)]dx=\int_{a}^b f(x)dx\pm \int_{a}^b g(x)dx$$
proof. 略

> 我们知道了 , 积分对数乘和加减法封闭 . $Prop. 1$ 、$Prop. 2$  或可称为积分的线性性质 
>$$\int_{a}^b [\alpha f(x)\pm\beta g(x)]dx=\alpha\int_{a}^b f(x)dx\pm \beta\int_{a}^b g(x)dx$$

$Prop. 3$  
若 $f\ ,\ g$ 在 $[a,b]$ 上都可积，则 $f\cdot g$ 在 $[a,b]$ 上也可积 

proof. 
 $f\ ,\ g$ 在 $[a,b]$ 上都可积 , 所以它们在 $[a,b]$ 上有界。
 因此存在常数 $M$，使得  
$$|f(x)| \leq M ,\quad|g(x)| \leq M, \quad x \in [a,b]$$
对 $[a,b]$ 的任意划分
$$a = x_0 < x_1 < x_2 < \cdots < x_n = b$$
设 $\hat{x}$ 和 $\bar{x}$ 是 $[x_{i-1}, x_i]$ 中的任意两点，则有
$$\begin{aligned}
|f(\hat{x})g(\bar{x}) - f(\bar{x})g(\hat{x})| 
&\leq |f(\hat{x}) - f(\bar{x})| \cdot |g(\hat{x})| + |f(\bar{x})| \cdot |g(\bar{x}) - g(\hat{x})| \\
&\leq M\bigl(|f(\hat{x}) - f(\bar{x})| + |g(\hat{x}) - g(\bar{x})|\bigr).
\end{aligned}$$
记 $f(x) \cdot g(x)$ 在小区间 $[x_{i-1}, x_i]$ 上的振幅为 $\omega_i$，$f(x)$ 和 $g(x)$ 在小区间 $[x_{i-1}, x_i]$ 上的振幅分别为 $\omega'_i$ 和 $\omega''_i$，则上式意味着
$$\omega_i \leq M(\omega'_i + \omega''_i),$$
因此
$$0 \leq \sum_{i=1}^n \omega_i \Delta x_i \leq M\left(\sum_{i=1}^n \omega'_i \Delta x_i + \sum_{i=1}^n \omega''_i \Delta x_i\right).$$
由于 $f(x)$ 和 $g(x)$ 都在 $[a,b]$ 可积，因而当 $\lambda = \max\{ \Delta x_i \} \to 0$ 时，上面的不等式的右端趋于零。由极限的夹逼性，得到  
$$\lim_{\lambda \to 0} \sum_{i=1}^n \omega_i \Delta x_i = 0,$$
根据 $Riemann$ 可积的充分必要条件，即知 $f(x) \cdot g(x)$ 在 $[a,b]$ 可积。
不过我们通常不会出现  
$$\int_{a}^b f(x)dx \cdot \int_{a}^b g(x)dx=\int_{a}^b [f(x)\cdot g(x)]dx$$
的情况

$Prop. 4$ 
若 $f$ 在 $[a,b]$ 上可积 , $\forall c \in(a,b)$ , $f$ 在 $[a,c]$ 与 $[c,b]$ 均可积，且 
$$\int_{a}^b f(x)dx=\int_{a}^c f(x)dx+\int_{c}^b f(x)dx$$
proof. 略 (这个性质是充要的)
这个式子称为 **关于积分区间的可加性**  

> 为了让这个式子对任意 $a,b,c$ 都成立我们有如下可证的规定 ：
> 1. $\int_{a}^bf(x)dx=-\int_{b}^a f(x)dx$
> 2. $\int_{a}^af(x)dx=0$

$Prop. 5$ 
设 $f$ 为 $[a,b]$ 上可积函数 . 若 $f(x)\geq 0$ 那么 
$$\int_{a}^b f(x)dx\geq 0$$
我们可以结合线性运算进行推广，于是得到积分的**保序性** 
若 $f$ 和 $g$ 都在 $[a,b]$ 上可积，且 $f(x)\geq g(x)$ , 有
$$\int^b_{a}f(x)dx\geq\int^b_{a}g(x)dx$$
$Prop. 6$  若 $f$ 在 $[a,b]$ s上可积，那么 $|f|$ 在 $[a,b]$ 上也可积，且 
$$|\int^b_{a}f(x)dx|\leq\int^b_{a}|f(x)|dx$$
这个结论也比较符合我们的直觉，也很直接得用了 $Prop.\ 5$ 的推论结论。故证明过程略
但是我们要注意：这个性质是不可逆的，有些不可积函数在取绝对值后便可积。

#### 积分中值定理

$Thm. 7.1$ ($积分第一中值定理$) 若 $f$ 在 $[a,b]$ 上连续，则至少存在一点 $\xi\in [a,b]$ 使得  
$$\int_{a}^b f(x)dx=f(\xi )(b-a)$$
```tikz
\usepackage{amsmath}
\usepackage{tikz}
\usetikzlibrary{patterns}

\begin{document}
\begin{tikzpicture}[scale=1.3]
    % axes
    \draw[->] (0,0) -- (5.5,0) node[right] {$x$};
    \draw[->] (0,0) -- (0,4.5) node[above] {$y$};

    % endpoints
    \def\a{1}
    \def\b{4}
    \def\xiVal{2.3}          % numeric x-coordinate of ξ
    \def\avgheight{1.85}    % average height f(ξ)

    % function f(x)
    \draw[blue, thick, smooth, samples=50] plot[variable=\x, domain=0.8:4.2]
        ({\x}, {0.3*sin(deg(2*\x)) + 2 - 0.05*(\x-2.5)^2});
    \node[blue, right] at (4.2,1.8) {$f(x)$};

    % mark a and b
    \draw[dashed] (\a,0) node[below] {$a$} -- (\a,{0.3*sin(deg(2*\a)) + 2 - 0.05*(\a-2.5)^2});
    \draw[dashed] (\b,0) node[below] {$b$} -- (\b,{0.3*sin(deg(2*\b)) + 2 - 0.05*(\b-2.5)^2});

    % rectangle f(ξ)(b-a)
    \fill[blue!20, opacity=0.6] (\a,0) rectangle (\b,\avgheight);

    % mark ξ and f(ξ) 
    \draw[red, dashed, thick] (0,\avgheight) node[left] {$f(\xi)$} -- (4,\avgheight);

    % area under the curve
    \begin{scope}
        \clip (\a,0) rectangle (\b,3);
        \fill[green!20, opacity=0.3]
            plot[variable=\x, domain=\a:\b, smooth, samples=50]
            ({\x}, {0.3*sin(deg(2*\x)) + 2 - 0.05*(\x-2.5)^2}) -- (\b,0) -- (\a,0) -- cycle;
    \end{scope}

    % label for the integral
    \node[orange] at (2.5,1.2) {$\displaystyle\int_a^b f(x)\,dx$};

    % theorem statement
    \node[above, align=center] at (2.9,4.2)
        {\textbf{First Mean Value Theorem for Integrals}};

\end{tikzpicture}
\end{document}
```

结合我们的示意图，我们的证明也渐渐浮现出来。我们可以这样理解，所得到的 $f(\xi)$ 实际上是在区间$[a,b]$ 的所有函数值的平均值 . 我们在证明中的核心思想是连续函数的 **介值性** 以及积分不等式性性质 .
倘若我们将得到 $f(\xi)$ 的值视为一个常函数即 $y=f(\xi)$ 我们对 $Thm. 7.1$ 进行推广
$Thm.\ 7.1.1$ 若有 $g(x)$ 在 $[a,b]$ 不变号 ，则
$$\int_{a}^b f(x)g(x)dx=f(\xi)\int_{a}^b g(x)d(x)$$
不过我们也可以不在第一中值定理下进行推广，其证明是不变其宗的

$Thm.\ 7.2$ ($积分第二中值定理$) 设 $f(x)$ 在$[a,b]$ 上可积 .
1. 若函数 $g(x)$ 在 $[a,b]$ 上减，且 $g(x)\geq_{0}$ ,则存在 $\xi\in[a,b]$ ,使得 
   $$\int_{a}^b f(x)g(x)dx=g(a)\int_{a}^\xi f(x)dx$$
2. 若函数 $g(x)$ 在 $[a,b]$ 上增，且 $g(x)\geq_{0}$ ,则存在 $\eta\in[a,b]$ ,使得 
   $$\int_{a}^b f(x)g(x)dx=g(b)\int_{\eta}^b f(x)dx$$
这里证明较为复杂，我们手写证明过程如下：
![[微信图片_20260212112903_292_7.jpg]]
![[微信图片_20260212112904_293_7.jpg]]

$Thm.\ 7.2.1$ 于是我们又能进行一个推论：
若 $g$ 在 $[a,b]$ 上单调，则存在 $\xi \in [a,b]$  使得 
$$\int_{a}^b f(x)g(x)dx=g(a)\int_{a}^{\xi}f(x)dx+g(b)\int_{\xi}^b f(x)dx$$
> 骗你的，还有反常积分（）

证明不难，积分第二定理是今后建立反常积分收敛判别法的工具 - 虽然我不知道是什么（），以后可以link过来

对于积分第二中值定理的证明我们需要用到变限积分，好问题，变限积分是啥？
 $Def.\ 4$  设 $f$ 在 $[a,b]$ 上可积，若 $x$ 在区间 $[a,b]$ 内，那么 $f$ 在 $[a,x]$ 区间内可可积，于是 
$$\Phi(x)=\int_{a}^x f(t)dt\ ,\quad x\in[a,b]$$
这样一个以积分上限为 $x$ 自变量的函数称为 **变上限定积分** ；同理，下限为 $x$ 的为 **变下限定积分** . 我们取积分变量为非 $x$ 的未知量，以免混淆 . 

$Thm. \ 7.3$ 若 $f$ 在 $[a,b]$ 可积，由 $Def.\ 4$ 定义的函数 $\Phi$ 在 $[a,b]$ 上连续 .
Proof. 对 $[a,b]$ 上任意确定的点 $x$ , 只要 $x+\Delta x\in[a,b]$  就有 
$$\Delta \Phi=\int_{a}^{x+\Delta x} f(t)dt-\int_{a}^x f(t)dt=\int_{x}^{x+\Delta x} f(t)dt$$
此时我们只要证明 $\int_{x}^{x+\Delta x} f(t)dt$ 的极限为 $0$ 即可，我们设 $\max{f(t)}=M,\quad t\in[a,b]$ , $\Delta x>0$ 就有 
$$|\Delta\Phi|=|\int_{x}^{x+\Delta x} f(t)dt|\leq\int_{x}^{x+\Delta x} |f(t)|dt\leq M\Delta x\ ;$$
$\Delta x<0$ 则不等式方向相反，由于夹逼，就有 
$$\lim_{ \Delta x \to 0 }\Delta \Phi=0 $$
得证

$Thm.\ 7.4$ 若 $f$ 在 $[a,b]$ 上连续 , 则我们定义的函数 $\Phi$ 在 $[a,b]$ 上处处可导，且 
$$\Delta \Phi'(x)=f(x),\quad x\in[a,b]$$
proof. 利用积分第一中值定理，来进行导数的表达，结果易得

这个概念称为 **原函数存在定理** 由于其沟通了导数和定积分，又被誉为 **微积分学基本定理** . 我们同时可以利用这个定理完成 $Newton-Leibniz$ 的证明。真好啊（）

#### 换元积分法和分步积分法

啊哈，我们之前是不是学过了不定积分的积分换元法和分布积分法，现在我们终于可以搬到定积分这边来了。

$Thm.\ 7.5$  ($定积分积分换元法$) 若 $f$ 在 $[a,b]$ 上连续 ， $\varphi'$ 在 $[\alpha,\beta]$ 上可积，且满足
$$\varphi(\alpha)=a\quad \varphi(\beta)=b\ ,\quad \varphi([\alpha,\beta]) \subseteq [a,b]$$
则有积分换元公式 
$$\int_{a}^b f(x)dx=\int_{\alpha}^\beta f(\varphi(t))\varphi'(t)dt$$
Proof. 对此我们先复习一下我们的复合函数求导 
$$F(\varphi(t))'=\varphi'(t)F'(\varphi(t))=\varphi'(t)f(\varphi(t))$$
可以知道 $F(\varphi(t))$ 便是 $\varphi'(t)f(\varphi(t))$ 的原函数 . 可直接由 $Newton-Leibniz$ 公式得到 
$$\int_{a}^b f(x)dx=\int_{\alpha}^\beta f(\varphi(t))\varphi'(t)dt=F(\varphi(\beta))-F(\varphi(\alpha))$$
于是得证

$Thm.\ 7.6$  ($定积分分步积分法$) 若 $u(x)$  $v(x)$ 为 $[a,b]$ 上的可微函数，且 $u'(x)$ 和 $v'(x)$ 都在 $[a,b]$ 上可积，则定积分分部积分公式： 
$$\int_{a}^b  u(x)v'(x)dx=u(x)v(x)|_{a}^b -\int_{a}^b u'(x)v(x)dx$$
Proof. 由于 $nv$ 是 $u'v+uv'$ 的原函数，所以有 
$$\int_{a}^b u(x)v'(x)dx+\int_{a}^b u'(x)v(x)dx=\int_{a}^b [u(x)v'(x)+u'(x)v(x)]dx=u(x)v(x)|^b_{a}$$
移项后得证，该公式亦可写成 
$$\int_{a}^b u(x)dv(x)=u(x)v(x)|^b_{a}-\int_{a}^b v(x)du(x)\ . $$

#### 泰勒公式的积分型余项

$Def.\ 5$ 若 $[a,b]$ 上 $u(x)$ , $v(x)$ 有 $n+1$ 阶连续导数，则有 
$$\int_{a}^b u(x)v^{(n+1)}(x)dx=\sum_{i=1}^{n+1} (-1)^{i+1}u^{i}(x)v^{n+1-i}(x)+(-1)^{n+1} \int_{a}^b u^{(n+1)}(x)v(x)dx$$
这是推广的分布积分公式，令 $x\in U(x_{0})$ , $u(t)=(x-t)^n$ , $v(t)=f(t)$ , $t\in[a_{0},x]$ 由上式得 
$$\begin{flalign}
& \int_{x_{0}}^x (x-t)^nf^{(n+1)}(t)dt\\
&=[(x-t)^nf^{(n)}(t)+n(x-t)^{n-1}f^{(n-1)}(t)+\cdots+n!f(t)]^x_{x_{0}}+\int_{x_{0}}^x 0 \cdot f(t)dt \\
&=n!R_{n}(x)
\end{flalign}$$

此处的 $R_{n}(x)$ 就是泰勒公式的 $n$ 阶余项 . 由此求得 
$$R_{n}(x)=\frac{1}{n!}\int_{x_{0}}^x f^{(n+1)}(t)(x-t)^n dx$$
这就是泰勒展开的 **积分型余项** ，我们对其使用推广的第一积分中值定理，就得到 **拉格朗日型余项** . 若直接使用，就得到 **柯西型余项** 。

至此，定积分部分就完结了。对于反常积分，我也将出手。