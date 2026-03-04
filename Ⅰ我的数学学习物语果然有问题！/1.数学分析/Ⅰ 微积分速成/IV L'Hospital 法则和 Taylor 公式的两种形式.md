---
tags:
  - 微积分
---

> 我们再学习函数极限之后会遇到一些待定型的极限，如 $\frac{0}{0}$ , $\frac{\infty}{\infty}$ , $0^0$ , $\infty-\infty$ , $0\cdot \infty$ $\cdots$ 形式，使用"L'Hospital 法则" 和 "Taylar 公式" 是两个很有效的方法 。还记得我们在数列极限学过的 Stolz 定理吗 ？我们得到了同样有效的工具 。在后续的积分学习中，我们可能还会多次运用到泰勒展开的工具。那么，吾等开启今日学习旅程吧。

# L'Hospital 法则-求待定型极限的方法

Thm. 1.  有 $f(x)$ , $g(x)$ 在 $(a,a+d)$ 可导. $g'(x) \not= 0$ ,此时有 $$
\lim_{ x \to a^+ }f(x)=\lim_{ x \to a^+ }g(x)=0 $$或
$$ \lim_{ x \to a^+ }g(x)=\infty \quad
 且 \lim_{ x \to a^+ } \frac{f'(x)}{g'(x)}=A(或\infty) $$则 $$
\lim_{ x \to a^+ } \frac{f(x)}{g(x)}=\lim_{ x \to a^+ } \frac{f'(x)}{g'(x)}
$$

> [!NOTE] 说明
> 1. 目的：求待定型极限，利用导数
> 2. 对于极限下标，有自由性
> 3. 若求出导数的极限为 $A$ 其为原极限，对于其余情况（$\infty,-\infty,+\infty$）也适用
> 4. 针对于 $\frac{O}{O}$ 型，$\frac{*}{\infty}$ 型

proof. 
1. $\lim_{ x \to 0 }f(x)=\lim_{ x \to 0 }g(x)=0$
   令 $f(a)=g(a)=0$ , 则 $f,g$ 在 $[a,a+d]$ 连续，$x\in [a,a+d]$ 使用柯西中值定理就有
$$\frac{f(x)}{g(x)}=\frac{{f(x)-f(a)}}{g(x)-g(a)}=\frac{f'(\xi)}{g'(\xi)} \quad ,\xi\in(a,x)$$
   由 $\lim_{ x \to a+ } \frac{f'(x)}{g'(x)}=A \Rightarrow\ \lim_{ x \to a+ } \frac{f(x)}{g(x)}=A$ 
2. $\lim_{ x \to a+ } g(x)=\infty$
   $\frac{f(x)}{g(x)}=\frac{f(x)-f(x_{0})}{g(x)}+\frac{f(x_{0})}{g(x)}=\frac{{g(x)-g(x_{0})}}{g(x)}\cdot \frac{{f(x)-f(x_{0})}}{g(x)-g{(x_{0})}}+\frac{f( x_{0} )}{g(x)}=\left( 1- \frac{g(x_{0})}{g(x)} \right)\cdot \frac{{f(x)-f(x_{0})}}{g(x)-g(x_{0})}+\frac{f(x_{0})}{g(x)}$
   我们在得到柯西的部分减去 $A$ ,得到
$$\frac{f(x)}{g(x)}-A==\left( 1- \frac{g(x_{0})}{g(x)} \right)\cdot \left(\frac{{f(x)-f(x_{0})}}{g(x)-g(x_{0})}-A\right)+\frac{f(x_{0})-g(x)A}{g(x)}$$
   由 $\lim_{ x \to a+ } \frac{f'(x)}{g'(x)}=A$ ,   $\forall \varepsilon >0\ ,\exists\ \xi>0$  当 $0< x-a < \rho$ 时 ，
   $$| \frac{f'(x)}{g'(x)} -A|< \varepsilon$$
   取 $x_{0}=a+ \rho$ 
   $$|\frac{{f(x)-f(x_{0})}}{g(x)-g(x_{0})}-A|=| \frac{f'(x)}{g'(x)}-A |< \varepsilon$$
   由 $\lim_{ x \to a+ }g(x)=\infty$ , $\exists\ \delta>0\ (\delta<\rho)$ . 当 $0< x-a < \delta$ 时 
   $$|1-\frac{g(x_{0})}{g(x)}|<2.\ |\frac{f(x_{0})-g(x)A}{g(x)}|<\varepsilon\ . \implies | \frac{f(x)}{g(x)} -A|< 3\varepsilon $$

> [!NOTE] 一些待定型的变形
> 1. $0 \cdot \infty$ 可以化成 $\frac{1}{\infty}\cdot \infty$ 型或者 $0\cdot \frac{1}{0}$ , 即化为 $\frac{\infty}{\infty}$ 或者 $\frac{0}{0}$ 型
> 2. $\infty-\infty$ 可以化成 $\frac{1}{0}-\frac{1}{0}$ 后通分变为 $\frac{{0-0}}{0}$ 即 $\frac{0}{0}$ 
> 3. $\infty^0$ 型、$1^\infty$ 型、$0^0$ 型极限 $\lim f(x)^{g(x)}$ 可以通过对数恒等式统一化成  
$$\lim e^{\ln f(x)g(x)} = \lim e^{g(x)\ln f(x)} = e^{\lim g(x)\ln f(x)}$$
这里的 $\lim g(x)\ln f(x)$ 已成为 $0 \cdot \infty$ 型，再用上面的方法来进行计算


> 上述的洛必达法则其实我们在高中就已经有在进行机械的使用的，不过是尚且不知道其原理只微妙：我们数列中的 $Stolz$ 定理其实也有着相似的证明方式。在完成对点的逼近后，为什么不尝试对整个函数曲线进行逼近？这样一个非常自然的想法应运而生，那么，也是我们早就久仰大名的 $Taylor$ 公式承担了这个伟大而又光荣的任务。那么，我们将要学习如何逼近一个函数曲线，这不仅仅可以拿来辅助我们求取极限，我们也可以用其简化积分式子，辅助求值。哇！多么好的机会啊！

# 带 $Peano$ 余项的 $Taylor$ 多项式

Thm.2  设 $f(x)$ 在 $x_{0}$ 有 $n$ 阶导数 , 则在 $x_{0}$ 的邻域中，成立 
$$f(x)=f(x_{0})+f'(x_{0})(x-x_{0})+\frac{1}{2!} f''(x_{0})(x-x_{0})^2+\cdots+ \frac{1}{n!}f^{(n)}(x-x_{0})^n+r_{n}(x)$$
其中 , $r_{n}(x)=o((x-x_{0})^m)\ (x\to x_{0})$ ， 多项式部分记为 $P_{n}(x)$ 称为 $f$ 在 $x=x_{0}$ 处的 $n$ 次 $Taylor$ 多项式 ; $r_{n}x$ 就记为 $f$ 在 $x=x_{0}$ 处的 $Peano$ 余项。

现在到了惊心动魄的证明环节. 

proof. $r_{n}(x)=f(x)-p_{n}(x)=f(x)-\sum_{k=0}^n \frac{1}{k!}f^{(k)}(x_{0})(x-x_{0})^k$  可以得到
$$r_{n}(x)=0\quad,r_{n}'(x)=f'(x)-\sum_{k=1}^n \frac{1}{(k-1)!}f^{(k)}(x_{0})(x-x_{0})^{k-1}$$
$r_{n}'(x_{0})=f'(x_{0})-f'(x_{0})=0$ . 那么再推
$$r''(x_{0})=f''(x)-\sum_{k=2}^n \frac{1}{(k-2)!}f^{(k)}(x_{0})(x-x_{0})^{k-2}$$
$r_{n}''(x_{0})=0$
$\vdots$
$$r_{n}^{n-1}(x)=f^{(n-1)}(x)-\sum_{k=n-1}^{n} \frac{1}{(k-n+1)!}f^{(k)}(x_{0})(x-x_{0})^{k-n+1}$$ 后续的累加只有两项，于是我们展开就有
$$f^{(n-1)}(x)-f^{(n-1)}(x_{0})-f^{(n)}(x_{0})(x-x_{0})$$
$r_{n}^{(n-1)}(x_{0})=0$

我们要求的是 : $r_{n}(x)=o((x-x_{0})^m)\ (x\to x_{0})$ , 即求极限 : 
$$\lim_{ x \to x_{0} } \frac{r_{n}(x)}{(x-x_{0})} $$
我们可以连续使用洛必达法则来进行求解便得到了 
$$\lim_{ x \to x_{0} } \frac{1}{n!} \cdot\left[ \frac{{f^{(n-1)}(x)-f^{(n-1)}(x_{0})}}{x-x_{0}}-f^{(n)}(x) \right] =0$$
因此 $r_{n}(x)=o((x-x_{0})^m)\ (x\to x_{0})$ 得证 . 

# 带 $Lagrange$ 余项的 $Taylor$ 多项式

Thm.3.  $f(x)$ 在 $[a,b]$ 上有 $n$ 阶连续导数，在 $(a,b)$ 上有 $n+1$ 阶导数 .
设 $x_{0}\in[a,b]$ 是一定点，则 $\forall x \in[a,b]$ 
$$f(x)=f(x_{0})+f'(x_{0})(x-x_{0})+\frac{1}{2!} f''(x_{0})(x-x_{0})^2+\cdots+ \frac{1}{n!}f^{(n)}(x-x_{0})^n+r_{n}(x)$$
其中 $r_n(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1} \quad (\xi \text{ 在 } x \text{ 和 } x_0 \text{ 之间})$  ，称为 $Lagrange$ 余项
proof. 考虑辅助函数

$$ G(t) = f(x) - \sum_{k=0}^n \frac{1}{k!} f^{(k)}(t)(x-t)^k \quad \text{和} \quad H(t) = (x-t)^{n+1}. $$
我们可以知道 $G(x)=f(x)-\sum_{k=0}^n \frac{1}{k!} f^{(k)}(x)(x-x)^k=0$  , $H(x)=0$ 
$$G(x_{0})=f(x)-\sum_{k=0}^n \frac{1}{k!} f^{(k)}(x_{0})(x-x_{0})^k=r_{n}(x) .\quad H(x_{0})=(x-x_{0})^{(n+1)}$$
即 , 需要证明的是
$$ G(x_0) = \frac{f^{(n+1)}(\xi)}{(n+1)!}H(x_0). $$
不妨设 $x_0 < x ( x_0 <x$ 时证明类似 $)$ 。则 $G(t)$ 和 $H(t)$ 在 $[x_0,x]$ 上连续，在 $(x_0,x)$ 上可导，且
$$ G'(t) = \frac{f^{(n+1)}(t)}{n!}(x-t)^n, \quad H'(t) = -(n+1)(x-t)^n. $$

(此处 $G'(t)$ 可读者尝试自证)
显然 $H'(t)$ 在 $(x_0,x)$ 上不等于零。因为 $G(x) = H(x) = 0$，由 Cauchy 中值定理可得
$$ \frac{G(x_0)}{H(x_0)} = \frac{G(x)-G(x_0)}{H(x)-H(x_0)} = \frac{G'(\xi)}{H'(\xi)} = \frac{f^{(n+1)}(\xi)}{(n+1)!}, \quad \xi \in (x_0,x), $$

因此
$$ G(x_0) = \frac{f^{(n+1)}(\xi)}{(n+1)!}H(x_0). $$<p align="right">证毕</p>
注意到：当 $n=0$ 时，定理式子即为 $lagrange$ 中值定理

在实际使用时,我们经常将 Taylor 公式写成(带 Lagrange 余项)

$$ f(x + \Delta x) = f(x) + f'(x) \frac{\Delta x + \frac{f''(x)}{2!} \Delta x^2 + \cdots + \frac{f^{(n)}(x)}{n!} \Delta x^n + \frac{f^{(n+1)}(\xi)}{(n+1)!} \Delta x^{n+1}}{(n+1)!}, \quad (\theta \in (0, 1)), $$

或是(带 Peano 余项)

$$ f(x + \Delta x) = f(x) + f'(x) \frac{\Delta x + \frac{f''(x)}{2!} \Delta x^2 + \cdots + \frac{f^{(n)}(x)}{n!} \Delta x^n + o(\Delta x^n)}{(n+1)!} $$

的形式。


# 在 $0$ 处的 $Taylor$ 展开

我们把在 $0$ 处的 $Taylor$ 展开公式称为 $Maclaurin$ 公式，为 
$$ f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \cdots + \frac{f^{(n)}(0)}{n!}x^n + r_n(x), $$
其中 $r_n(x)$ 有 Peano 余项与 Lagrange 余项两种表示形式，即有 $r_n(x) = o(x^n)$，或 $r_n(x) = \frac{f^{(n+1)}(\theta x)}{(n+1)!}x^{n+1}, \theta \in (0, 1)$ 

以下是几个经典的 $Maclaurin$  公式
1. 指数函数 $e^x$

**带 Lagrange 余项：**
$$ e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots + \frac{x^n}{n!} + \frac{e^{\theta x}}{(n+1)!} x^{n+1}, \quad \theta \in (0, 1) $$

**带 Peano 余项：**
$$ e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots + \frac{x^n}{n!} + o(x^n) $$
2. 正弦函数 $\sin x$

**带 Lagrange 余项：**
$$ \sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots + (-1)^{m-1} \frac{x^{2m-1}}{(2m-1)!} + \frac{(-1)^m \cos(\theta x)}{(2m+1)!} x^{2m+1}, \quad \theta \in (0, 1) $$

**带 Peano 余项：**
$$ \sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots + (-1)^{m-1} \frac{x^{2m-1}}{(2m-1)!} + o(x^{2m}) $$
3. 余弦函数 $\cos x$ （我们注意到 $\cos x$ 是由 $\sin x$ 求导得出的）

**带 Lagrange 余项：**
$$ \cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots + (-1)^m \frac{x^{2m}}{(2m)!} + \frac{(-1)^{m+1} \cos(\theta x)}{(2m+2)!} x^{2m+2}, \quad \theta \in (0, 1) $$

**带 Peano 余项：**
$$ \cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots + (-1)^m \frac{x^{2m}}{(2m)!} + o(x^{2m+1}) $$
4. 对数函数 $\ln(1+x)$

**带 Lagrange 余项：**
$$ \ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots + (-1)^{n-1} \frac{x^n}{n} + (-1)^n \frac{x^{n+1}}{(n+1)(1+\theta x)^{n+1}}, \quad \theta \in (0, 1) $$

**带 Peano 余项：**
$$ \ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots + (-1)^{n-1} \frac{x^n}{n} + o(x^n) $$
5. 幂函数 $(1+x)^\alpha$（$\alpha \in \mathbb{R}$）-二项式展开

**带 Lagrange 余项：**
$$ (1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)}{2!} x^2 + \cdots + \frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!} x^n + \frac{\alpha(\alpha-1)\cdots(\alpha-n)}{(n+1)!} (1+\theta x)^{\alpha-n-1} x^{n+1}, \quad \theta \in (0, 1) $$

**带 Peano 余项：**
$$ (1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)}{2!} x^2 + \cdots + \frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!} x^n + o(x^n) $$


>我们所学的 $Taylor$ 展开可以有以下用处：
>1. 近似计算
>2. 求函数极限
>3. 证明不等式
>4. 求曲线渐近线方程
>5. 外推


我们把陈纪修留给我们的“饶有趣味”的问题来结束本节内容:

proof. $e$ 是无理数