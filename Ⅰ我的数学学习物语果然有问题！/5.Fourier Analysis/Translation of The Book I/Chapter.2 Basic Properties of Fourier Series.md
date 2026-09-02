---
tags:
  - Fourier_Analysis
---

# 第2章 傅里叶级数的基本性质

Nearly fifty years had passed without any progress on the question of analytic representation of an arbitrary function, when an assertion of Fourier threw new light on the subject. Thus a new era began for the development of this part of Mathematics and this was heralded in a stunning way by major developments in mathematical Physics.

B. Riemann, 1854

近五十年来，关于任意函数的解析表示问题毫无进展，直到傅里叶的一个断言给这个主题带来了新的曙光。因此，数学这一分支的发展开启了一个新时代，而数学物理的重大发展以惊人的方式预示了这一时代的到来。

—— B. 黎曼，1854年

In this chapter, we begin our rigorous study of Fourier series. We set the stage by introducing the main objects in the subject, and then formulate some basic problems which we have already touched upon earlier.

在本章中，我们开始对傅里叶级数进行严谨的研究。我们首先介绍该主题的主要对象，然后阐述一些我们之前已经初步接触过的基本问题。

Our first result disposes of the question of uniqueness: Are two functions with the same Fourier coefficients necessarily equal? Indeed, a simple argument shows that if both functions are continuous, then in fact they must agree.

我们的第一个结果解决了唯一性问题：具有相同傅里叶系数的两个函数是否必然相等？实际上，一个简单的论证表明，如果两个函数都是连续的，那么它们必然相等。

Next, we take a closer look at the partial sums of a Fourier series. Using the formula for the Fourier coefficients (which involves an integration), we make the key observation that these sums can be written conveniently as integrals:

接下来，我们更仔细地研究傅里叶级数的部分和。利用傅里叶系数的公式（涉及积分），我们得到一个关键观察：这些和可以方便地写成积分形式：

$$\frac{1}{2\pi}\int D_N(x - y)f(y)dy,$$

where $\{D_N\}$ is a family of functions called the Dirichlet kernels. The above expression is the convolution of $f$ with the function $D_N$ . Convolutions will play a critical role in our analysis. In general, given a family of functions $\{K_n\}$ , we are led to investigate the limiting properties as $n$ tends to infinity of the convolutions

其中 $\{D_N\}$ 是一族被称为狄利克雷核的函数。上述表达式是 $f$ 与函数 $D_N$ 的卷积。卷积将在我们的分析中起关键作用。一般来说，给定一族函数 $\{K_n\}$，我们研究当 $n$ 趋于无穷时卷积

$$\frac{1}{2\pi}\int K_n(x - y)f(y)dy.$$

We find that if the family $\{K_n\}$ satisfies the three important properties of "good kernels," then the convolutions above tend to $f(x)$ as $n \to \infty$ (at least when $f$ is continuous). In this sense, the family $\{K_n\}$ is an "approximation to the identity." Unfortunately, the Dirichlet kernels $D_{N}$ do not belong to the category of good kernels, which indicates that the question of convergence of Fourier series is subtle.

的极限性质。我们发现，如果族 $\{K_n\}$ 满足“好核”的三个重要性质，那么当 $n \to \infty$ 时，上述卷积趋于 $f(x)$（至少在 $f$ 连续时成立）。在这个意义上，族 $\{K_n\}$ 是“恒等逼近”。不幸的是，狄利克雷核 $D_{N}$ 不属于好核的范畴，这表明傅里叶级数的收敛问题是微妙的。

Instead of pursuing at this stage the problem of convergence, we consider various other methods of summing the Fourier series of a function. The first method, which involves averages of partial sums, leads to convolutions with good kernels, and yields an important theorem of Fejer. From this, we deduce the fact that a continuous function on the circle can be approximated uniformly by trigonometric polynomials. Second, we may also sum the Fourier series in the sense of Abel and again encounter a family of good kernels. In this case, the results about convolutions and good kernels lead to a solution of the Dirichlet problem for the steady- state heat equation in the disc, considered at the end of the previous chapter.

我们暂不在此阶段深入探讨收敛问题，而是考虑对函数的傅里叶级数进行求和的几种其他方法。第一种方法涉及部分和的平均，它导向了与好核的卷积，并得到了重要的费耶定理。由此，我们推导出圆周上的连续函数可以用三角多项式一致逼近这一事实。其次，我们也可以在阿贝尔意义下对傅里叶级数求和，并再次遇到一族好核。在这种情况下，关于卷积和好核的结果引出了上一章末尾考虑的圆盘内稳态热传导方程的狄利克雷问题的解。

---

## 1 例子与问题的阐述

We commence with a brief description of the types of functions with which we shall be concerned. Since the Fourier coefficients of $f$ are defined by

我们首先简要描述我们将要关注的函数类型。由于 $f$ 的傅里叶系数定义为

$$a_{n} = \frac{1}{L}\int_{0}^{L}f(x)e^{-2\pi inx / L}dx,\quad \mathrm{for} n\in \mathbb{Z},$$

where $f$ is complex- valued on $[0,L]$ , it will be necessary to place some integrability conditions on $f$ . We shall therefore assume for the remainder of this book that all functions are at least Riemann integrable. Sometimes it will be illuminating to focus our attention on functions that are more "regular," that is, functions that possess certain continuity or differentiability properties. Below, we list several classes of functions in increasing order of generality. We emphasize that we will not generally restrict our attention to real- valued functions, contrary to what the following pictures may suggest; we will almost always allow functions that take values in the complex numbers $\mathbb{C}$ . Furthermore, we sometimes think of our functions as being defined on the circle rather than an interval. We elaborate upon this below.

其中 $f$ 是在 $[0,L]$ 上取复值的函数，因此有必要对 $f$ 施加一些可积性条件。在本书的其余部分，我们将假设所有函数至少是黎曼可积的。有时，将注意力集中在更“正则”的函数上，即具有某些连续性或可微性性质的函数，会更有启发性。下面，我们按普遍性递增的顺序列出几类函数。我们强调，与下图可能暗示的相反，我们通常不会将注意力限制在实值函数上；我们几乎总是允许取复数值 $\mathbb{C}$ 的函数。此外，有时我们将函数视为定义在圆周上而不是一个区间上。我们将在下面详细说明这一点。

---

**Everywhere continuous functions**

**处处连续的函数**

These are the complex- valued functions $f$ which are continuous at every point of the segment $[0, L]$ . A typical continuous function is sketched in Figure 1 (a). We shall note later that continuous functions on the circle satisfy the additional condition $f(0) = f(L)$ .

这是指在区间 $[0, L]$ 上每一点都连续的复值函数 $f$。图1(a)描绘了一个典型的连续函数。我们稍后将指出，圆周上的连续函数满足附加条件 $f(0) = f(L)$。

**Piecewise continuous functions**

**分段连续的函数**

These are bounded functions on $[0, L]$ which have only finitely many discontinuities. An example of such a function with simple discontinuities is pictured in Figure 1 (b).

这是指在 $[0, L]$ 上仅有有限个间断点的有界函数。图1(b)描绘了一个具有简单间断点的此类函数的例子。

<center>Figure 1. Functions on $[0, L]$ : continuous and piecewise continuous </center>

<center>图1. $[0, L]$ 上的函数：连续函数与分段连续函数</center>

This class of functions is wide enough to illustrate many of the theorems in the next few chapters. However, for logical completeness we consider also the more general class of Riemann integrable functions. This more extended setting is natural since the formula for the Fourier coefficients involves integration.

这类函数足够广泛，足以说明接下来几章中的许多定理。然而，为了逻辑上的完备性，我们还考虑了更一般的黎曼可积函数类。这个更广泛的设定是自然的，因为傅里叶系数的公式涉及积分。

**Riemann integrable functions**

**黎曼可积函数**

This is the most general class of functions we will be concerned with. Such functions are bounded, but may have infinitely many discontinuities. We recall the definition of integrability. A real- valued function $f$ defined on $[0, L]$ is Riemann integrable (which we abbreviate as integrable $^2$ ) if it is bounded, and if for every $\epsilon > 0$ , there is a subdivision $0 = x_0 < x_1 < \dots < x_{N - 1} < x_N = L$ of the interval $[0, L]$ , so that if $\mathcal{U}$

这是我们关注的最一般的函数类。此类函数是有界的，但可能有无限多个间断点。我们回顾一下可积性的定义。定义在 $[0, L]$ 上的实值函数 $f$ 是黎曼可积的（我们简称为可积 $^2$），如果它是有界的，并且对于每个 $\epsilon > 0$，存在区间 $[0, L]$ 的一个分割 $0 = x_0 < x_1 < \dots < x_{N - 1} < x_N = L$，使得如果 $\mathcal{U}$

and $\mathcal{L}$ are, respectively, the upper and lower sums of $f$ for this subdivision, namely

和 $\mathcal{L}$ 分别是 $f$ 关于此分割的上和与下和，即

$$\mathcal{U} = \sum_{j = 1}^{N}\left[\sup_{x_{j - 1}\leq x\leq x_{j}}f(x)\right](x_{j} - x_{j - 1})$$

and

以及

$$\mathcal{L} = \sum_{j = 1}^{N}\left[\inf_{x_{j - 1}\leq x\leq x_{j}}f(x)\right](x_{j} - x_{j - 1}),$$

then we have $\mathcal{U} - \mathcal{L}< \epsilon$ . Finally, we say that a complex- valued function is integrable if its real and imaginary parts are integrable. It is worthwhile to remember at this point that the sum and product of two integrable functions are integrable.

那么我们有 $\mathcal{U} - \mathcal{L}< \epsilon$。最后，我们说一个复值函数是可积的，如果它的实部和虚部是可积的。此时值得记住的是，两个可积函数的和与积是可积的。

A simple example of an integrable function on $[0,1]$ with infinitely many discontinuities is given by

一个在 $[0,1]$ 上具有无限多个间断点的可积函数的简单例子由下式给出

$$f(x) = \begin{cases} 1 & \text{if } x = 1/n, n\in\mathbb{N},\\ 0 & \text{otherwise}. \end{cases}$$

This example is illustrated in Figure 2. Note that $f$ is discontinuous when $x = 1 / n$ and at $x = 0$ .

这个例子如图2所示。注意 $f$ 在 $x = 1 / n$ 和 $x = 0$ 处不连续。

<center>Figure 2. A Riemann integrable function </center>

<center>图2. 一个黎曼可积函数</center>

More elaborate examples of integrable functions whose discontinuities are dense in the interval $[0,1]$ are described in Problem 1. In general, while integrable functions may have infinitely many discontinuities, these

更复杂的、其间断点在区间 $[0,1]$ 中稠密分布的可积函数的例子在问题1中描述。一般来说，尽管可积函数可能有无限多个间断点，但

functions are actually characterized by the fact that, in a precise sense, their discontinuities are not too numerous: they are "negligible," that is, the set of points where an integrable function is discontinuous has "measure 0." The reader will find further details about Riemann integration in the appendix.

实际上，这些函数的特点在于，在一个精确的意义上，它们的间断点并不多：它们是“可忽略的”，即可积函数不连续的点集具有“测度0”。读者可以在附录中找到关于黎曼积分的更多细节。

From now on, we shall always assume that our functions are integrable, even if we do not state this requirement explicitly.

从现在开始，即使我们没有明确说明，我们也将始终假设我们的函数是可积的。

**Functions on the circle**

**圆周上的函数**

There is a natural connection between $2\pi$ - periodic functions on $\mathbb{R}$ like the exponentials $e^{in\theta}$ , functions on an interval of length $2\pi$ , and functions on the unit circle. This connection arises as follows.

在 $\mathbb{R}$ 上的 $2\pi$ 周期函数（如指数函数 $e^{in\theta}$）、长度为 $2\pi$ 的区间上的函数以及单位圆周上的函数之间存在着自然的联系。这种联系的产生方式如下。

A point on the unit circle takes the form $e^{i\theta}$ , where $\theta$ is a real number that is unique up to integer multiples of $2\pi$ . If $F$ is a function on the circle, then we may define for each real number $\theta$

单位圆周上的点形如 $e^{i\theta}$，其中 $\theta$ 是一个实数，且在相差 $2\pi$ 的整数倍的意义下是唯一的。如果 $F$ 是圆周上的一个函数，那么我们可以为每个实数 $\theta$ 定义

$$f(\theta) = F(e^{i\theta}),$$

and observe that with this definition, the function $f$ is periodic on $\mathbb{R}$ of period $2\pi$ , that is, $f(\theta +2\pi) = f(\theta)$ for all $\theta$ . The integrability, continuity and other smoothness properties of $F$ are determined by those of $f$ . For instance, we say that $F$ is integrable on the circle if $f$ is integrable on every interval of length $2\pi$ . Also, $F$ is continuous on the circle if $f$ is continuous on $\mathbb{R}$ , which is the same as saying that $f$ is continuous on any interval of length $2\pi$ . Moreover, $F$ is continuously differentiable if $f$ has a continuous derivative, and so forth.

并且观察到，根据这个定义，函数 $f$ 在 $\mathbb{R}$ 上是以 $2\pi$ 为周期的，即对于所有 $\theta$ 有 $f(\theta +2\pi) = f(\theta)$。$F$ 的可积性、连续性以及其他光滑性质由 $f$ 的这些性质决定。例如，我们说 $F$ 在圆周上可积，如果 $f$ 在每个长度为 $2\pi$ 的区间上可积。同样，$F$ 在圆周上连续，如果 $f$ 在 $\mathbb{R}$ 上连续，这等价于说 $f$ 在任何长度为 $2\pi$ 的区间上连续。此外，如果 $f$ 具有连续导数，则 $F$ 是连续可微的，等等。

Since $f$ has period $2\pi$ , we may restrict it to any interval of length $2\pi$ , say $[0,2\pi ]$ or $[- \pi ,\pi ]$ , and still capture the initial function $F$ on the circle. We note that $f$ must take the same value at the end- points of the interval since they correspond to the same point on the circle. Conversely, any function on $[0,2\pi ]$ for which $f(0) = f(2\pi)$ can be extended to a periodic function on $\mathbb{R}$ which can then be identified as a function on the circle. In particular, a continuous function $f$ on the interval $[0,2\pi ]$ gives rise to a continuous function on the circle if and only if $f(0) = f(2\pi)$ .

由于 $f$ 有周期 $2\pi$，我们可以将其限制在任何长度为 $2\pi$ 的区间上，例如 $[0,2\pi ]$ 或 $[- \pi ,\pi ]$，并且仍然能捕获到原始的圆周函数 $F$。我们注意到，$f$ 在区间端点处必须取相同的值，因为它们对应于圆周上的同一点。反之，任何在 $[0,2\pi ]$ 上满足 $f(0) = f(2\pi)$ 的函数可以延拓成 $\mathbb{R}$ 上的周期函数，然后可以等同于圆周上的一个函数。特别地，区间 $[0,2\pi ]$ 上的连续函数 $f$ 能产生圆周上的连续函数当且仅当 $f(0) = f(2\pi)$。

In conclusion, functions on $\mathbb{R}$ that $2\pi$ - periodic, and functions on an interval of length $2\pi$ that take on the same value at its end- points, are two equivalent descriptions of the same mathematical objects, namely, functions on the circle.

总之，$\mathbb{R}$ 上以 $2\pi$ 为周期的函数，以及长度为 $2\pi$ 的区间上在端点处取相同值的函数，是同一数学对象（即圆周上的函数）的两种等价描述。

In this connection, we mention an item of notational usage. When our functions are defined on an interval on the line, we often use $x$ as the independent variable; however, when we consider these as functions

在此，我们提一下符号使用习惯。当我们的函数定义在直线上的一个区间时，我们通常使用 $x$ 作为自变量；然而，当我们把它们看作是

on the circle, we usually replace the variable $x$ by $\theta$ . As the reader will note, we are not strictly bound by this rule since this practice is mostly a matter of convenience.

圆周上的函数时，我们通常将变量 $x$ 替换为 $\theta$。读者会注意到，我们并非严格遵循此规则，因为这主要是一个方便与否的问题。

### 1.1 Main definitions and some examples

### 1.1 主要定义与一些例子

We now begin our study of Fourier analysis with the precise definition of the Fourier series of a function. Here, it is important to pin down where our function is originally defined. If $f$ is an integrable function given on an interval $[a,b]$ of length $L$ (that is, $b - a = L$ ), then the $n^{\mathrm{th}}$ Fourier coefficient of $f$ is defined by

现在我们开始研究傅里叶分析，首先给出函数傅里叶级数的精确定义。这里，明确函数最初的定义域很重要。如果 $f$ 是定义在长度为 $L$ 的区间 $[a,b]$ 上的可积函数（即 $b - a = L$），那么 $f$ 的第 $n$ 个傅里叶系数定义为

$$\hat{f} (n) = \frac{1}{L}\int_{a}^{b}f(x)e^{-2\pi inx / L}dx,\quad n\in \mathbb{Z}.$$

The Fourier series of $f$ is given formally $^3$ by

$f$ 的傅里叶级数形式地 $^3$ 由下式给出

$$\sum_{n = -\infty}^{\infty}\hat{f} (n)e^{2\pi inx / L}.$$

We shall sometimes write $a_{n}$ for the Fourier coefficients of $f$ , and use the notation

我们有时会将 $f$ 的傅里叶系数记作 $a_{n}$，并使用记号

$$f(x)\sim \sum_{n = -\infty}^{\infty}a_{n}e^{2\pi inx / L}$$

to indicate that the series on the right- hand side is the Fourier series of $f$ .

来表示右边的级数是 $f$ 的傅里叶级数。

For instance, if $f$ is an integrable function on the interval $[-\pi ,\pi ]$ , then the $n^{\mathrm{th}}$ Fourier coefficient of $f$ is

例如，如果 $f$ 是区间 $[-\pi ,\pi ]$ 上的可积函数，那么 $f$ 的第 $n$ 个傅里叶系数是

$$\hat{f} (n) = a_{n} = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(\theta)e^{-in\theta}d\theta ,\quad n\in \mathbb{Z},$$

and the Fourier series of $f$ is

而 $f$ 的傅里叶级数是

$$f(\theta)\sim \sum_{n = -\infty}^{\infty}a_{n}e^{in\theta}.$$

Here we use $\theta$ as a variable since we think of it as an angle ranging from $-\pi$ to $\pi$ .

这里我们使用 $\theta$ 作为变量，因为我们将其视为从 $-\pi$ 到 $\pi$ 的角度。

Also, if $f$ is defined on $[0,2\pi ]$ , then the formulas are the same as above, except that we integrate from 0 to $2\pi$ in the definition of the Fourier coefficients.

同样，如果 $f$ 定义在 $[0,2\pi ]$ 上，那么公式与上面相同，只是在定义傅里叶系数时，我们从 0 积分到 $2\pi$。

We may also consider the Fourier coefficients and Fourier series for a function defined on the circle. By our previous discussion, we may think of a function on the circle as a function $f$ on $\mathbb{R}$ which is $2\pi$ - periodic. We may restrict the function $f$ to any interval of length $2\pi$ , for instance $[0,2\pi ]$ or $[-\pi ,\pi ]$ , and compute its Fourier coefficients. Fortunately, $f$ is periodic and Exercise 1 shows that the resulting integrals are independent of the chosen interval. Thus the Fourier coefficients of a function on the circle are well defined.

我们也可以考虑定义在圆周上的函数的傅里叶系数和傅里叶级数。根据我们之前的讨论，我们可以将圆周上的函数视为 $\mathbb{R}$ 上以 $2\pi$ 为周期的函数 $f$。我们可以将函数 $f$ 限制在任何长度为 $2\pi$ 的区间上，例如 $[0,2\pi ]$ 或 $[-\pi ,\pi ]$，并计算其傅里叶系数。幸运的是，$f$ 是周期的，并且练习1表明，所得的积分与所选的区间无关。因此，圆周上函数的傅里叶系数是良定义的。

Finally, we shall sometimes consider a function $g$ given on $[0,1]$ . Then

最后，我们有时会考虑定义在 $[0,1]$ 上的函数 $g$。那么

$$\hat{g} (n) = a_n = \int_0^1 g(x)e^{-2\pi inx}dx\quad \mathrm{and}\quad g(x)\sim \sum_{n = -\infty}^{\infty}a_ne^{2\pi inx}.$$

Here we use $x$ for a variable ranging from 0 to 1.

这里我们使用 $x$ 表示从 0 到 1 的变量。

Of course, if $f$ is initially given on $[0,2\pi ]$ , then $g(x) = f(2\pi x)$ is defined on $[0,1]$ and a change of variables shows that the $n^{\mathrm{th}}$ Fourier coefficient of $f$ equals the $n^{\mathrm{th}}$ Fourier coefficient of $g$ .

当然，如果 $f$ 最初定义在 $[0,2\pi ]$ 上，那么 $g(x) = f(2\pi x)$ 定义在 $[0,1]$ 上，并且通过变量替换可以证明 $f$ 的第 $n$ 个傅里叶系数等于 $g$ 的第 $n$ 个傅里叶系数。

Fourier series are part of a larger family called the trigonometric series which, by definition, are expressions of the form $\sum_{n = -\infty}^{\infty}c_n e^{2\pi inx / L}$ where $c_n\in \mathbb{C}$ . If a trigonometric series involves only finitely many nonzero terms, that is, $c_n = 0$ for all large $|n|$ , it is called a trigonometric polynomial; its degree is the largest value of $|n|$ for which $c_n\neq 0$ .

傅里叶级数是称为三角级数的更大族的一部分，根据定义，三角级数是形如 $\sum_{n = -\infty}^{\infty}c_n e^{2\pi inx / L}$ 的表达式，其中 $c_n\in \mathbb{C}$。如果一个三角级数只包含有限多个非零项，即对于所有足够大的 $|n|$ 有 $c_n = 0$，则称之为三角多项式；其次数是使 $c_n\neq 0$ 的 $|n|$ 的最大值。

The $N^{\mathrm{th}}$ partial sum of the Fourier series of $f$ , for $N$ a positive integer, is a particular example of a trigonometric polynomial. It is given by

对于正整数 $N$，$f$ 的傅里叶级数的第 $N$ 部分和是三角多项式的一个特例。它由下式给出

$$S_{N}(f)(x) = \sum_{n = -N}^{N}\hat{f} (n)e^{2\pi inx / L}.$$

Note that by definition, the above sum is symmetric since $n$ ranges from $- N$ to $N$ , a choice that is natural because of the resulting decomposition of the Fourier series as sine and cosine series. As a consequence, the convergence of Fourier series will be understood (in this book) as the "limit" as $N$ tends to infinity of these symmetric sums.

注意，根据定义，上述和是对称的，因为 $n$ 的取值范围是从 $- N$ 到 $N$，这种选择是自然的，因为它导致了傅里叶级数分解为正弦级数和余弦级数。因此，（在本书中）傅里叶级数的收敛将被理解为当 $N$ 趋于无穷时这些对称和的“极限”。

In fact, using the partial sums of the Fourier series, we can reformulate the basic question raised in Chapter 1 as follows:

实际上，利用傅里叶级数的部分和，我们可以将第一章提出的基本问题重新表述如下：

Problem: In what sense does $S_N(f)$ converge to $f$ as $N \to \infty$ ?

问题：当 $N \to \infty$ 时，$S_N(f)$ 在何种意义下收敛到 $f$？

Before proceeding further with this question, we turn to some simple examples of Fourier series.

在进一步探讨这个问题之前，我们先来看几个傅里叶级数的简单例子。

EXAMPLE 1. Let $f(\theta) = \theta$ for $- \pi \leq \theta \leq \pi$ . The calculation of the Fourier coefficients requires a simple integration by parts. First, if $n \neq 0$ , then

例1. 设 $f(\theta) = \theta$ 对于 $- \pi \leq \theta \leq \pi$。计算傅里叶系数需要简单的分部积分。首先，如果 $n \neq 0$，那么

$$\hat{f} (n) = \frac{1}{2\pi}\int_{-\pi}^{\pi}\theta e^{-in\theta}d\theta$$ $$= \frac{1}{2\pi}\left[-\frac{\theta}{in}e^{-in\theta}\right]_{-\pi}^{\pi} + \frac{1}{2\pi in}\int_{-\pi}^{\pi}e^{-in\theta}d\theta$$ $$= \frac{(-1)^{n + 1}}{in},$$

and if $n = 0$ we clearly have

而如果 $n = 0$，我们显然有

$$\hat{f} (0) = \frac{1}{2\pi}\int_{-\pi}^{\pi}\theta d\theta = 0.$$

Hence, the Fourier series of $f$ is given by

因此，$f$ 的傅里叶级数由下式给出

$$f(\theta)\sim \sum_{n\neq 0}\frac{(-1)^{n + 1}}{in} e^{in\theta} = 2\sum_{n = 1}^{\infty}(-1)^{n + 1}\frac{\sin n\theta}{n}.$$

The first sum is over all non- zero integers, and the second is obtained by an application of Euler's identities. It is possible to prove by elementary means that the above series converges for every $\theta$ , but it is not obvious that it converges to $f(\theta)$ . This will be proved later (Exercises 8 and 9 deal with a similar situation).

第一个和是对所有非零整数求和，第二个和是通过应用欧拉恒等式得到的。可以用初等方法证明上述级数对每个 $\theta$ 收敛，但显然它是否收敛到 $f(\theta)$ 并不明显。这将在后面证明（练习8和9处理了类似的情况）。

EXAMPLE 2. Define $f(\theta) = (\pi - \theta)^2 /4$ for $0 \leq \theta \leq 2\pi$ . Then successive integration by parts similar to that performed in the previous example yield

例2. 定义 $f(\theta) = (\pi - \theta)^2 /4$ 对于 $0 \leq \theta \leq 2\pi$。然后类似于上一个例子进行连续的分部积分得到

$$f(\theta)\sim \frac{\pi^2}{12} +\sum_{n = 1}^{\infty}\frac{\cos n\theta}{n^2}.$$

EXAMPLE 3. The Fourier series of the function

例3. 函数

$$f(\theta) = \frac{\pi}{\sin\pi\alpha} e^{i(\pi -\theta)\alpha}$$

on $[0,2\pi ]$ is

在 $[0,2\pi ]$ 上的傅里叶级数是

$$f(\theta)\sim \sum_{n = -\infty}^{\infty}\frac{e^{in\theta}}{n + \alpha},$$

whenever $\alpha$ is not an integer.

只要 $\alpha$ 不是整数。

EXAMPLE 4. The trigonometric polynomial defined for $x \in [-\pi , \pi ]$ by

例4. 定义在 $x \in [-\pi , \pi ]$ 上的三角多项式

$$D_{N}(x) = \sum_{n = -N}^{N}e^{inx}$$

is called the $N^{\mathrm{th}}$ Dirichlet kernel and is of fundamental importance in the theory (as we shall see later). Notice that its Fourier coefficients $a_{n}$ have the property that $a_{n} = 1$ if $|n| \leq N$ and $a_{n} = 0$ otherwise. A closed form formula for the Dirichlet kernel is

被称为第 $N$ 个狄利克雷核，并且在理论中具有根本重要性（我们将在后面看到）。注意，其傅里叶系数 $a_{n}$ 具有性质：如果 $|n| \leq N$ 则 $a_{n} = 1$，否则 $a_{n} = 0$。狄利克雷核的一个闭式公式是

$$D_{N}(x) = \frac{\sin((N + \frac{1}{2})x)}{\sin(x / 2)}.$$

This can be seen by summing the geometric progressions

这可以通过求和几何级数得到

$$\sum_{n = 0}^{N}\omega^{n}\quad \mathrm{and}\quad \sum_{n = -N}^{-1}\omega^{n}$$

with $\omega = e^{ix}$ . These sums are, respectively, equal to

其中 $\omega = e^{ix}$。这些和分别等于

$$\frac{1 - \omega^{N + 1}}{1 - \omega}\quad \mathrm{and}\quad \frac{\omega^{-N} - 1}{1 - \omega}.$$

Their sum is then

它们的和则为

$$\frac{\omega^{-N} - \omega^{N + 1}}{1 - \omega} = \frac{\omega^{-N - 1 / 2} - \omega^{N + 1 / 2}}{\omega^{-1 / 2} - \omega^{1 / 2}} = \frac{\sin((N + \frac{1}{2})x)}{\sin(x / 2)},$$

giving the desired result.

得到所需结果。

EXAMPLE 5. The function $P_{r}(\theta)$ , called the Poisson kernel, is defined for $\theta \in [-\pi , \pi ]$ and $0 \leq r < 1$ by the absolutely and uniformly convergent series

例5. 函数 $P_{r}(\theta)$，称为泊松核，对于 $\theta \in [-\pi , \pi ]$ 和 $0 \leq r < 1$ 由绝对且一致收敛的级数定义

$$P_{r}(\theta) = \sum_{n = -\infty}^{\infty}r^{|n|}e^{in\theta}.$$

This function arose implicitly in the solution of the steady- state heat equation on the unit disc discussed in Chapter 1. Note that in calculating the Fourier coefficients of $P_{r}(\theta)$ we can interchange the order of integration and summation since the sum converges uniformly in $\theta$ for

这个函数在第一章讨论的单位圆盘上稳态热传导方程的解中隐式地出现了。注意，在计算 $P_{r}(\theta)$ 的傅里叶系数时，我们可以交换积分和求和的顺序，因为对于每个固定的 $r$，该和在 $\theta$ 上一致收敛，

each fixed $r$ , and obtain that the $n^{\mathrm{th}}$ Fourier coefficient equals $r^{|n|}$ . One can also sum the series for $P_{r}(\theta)$ and see that

并得到第 $n$ 个傅里叶系数等于 $r^{|n|}$。我们也可以对 $P_{r}(\theta)$ 的级数求和，并看到

$$P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r\cos\theta + r^{2}}.$$

In fact,

实际上，

$$P_{r}(\theta) = \sum_{n = 0}^{\infty}\omega^{n} + \sum_{n = 1}^{\infty}\overline{\omega}^{n}\quad \mathrm{with}\omega = re^{i\theta},$$

where both series converge absolutely. The first sum (an infinite geometric progression) equals $1 / (1 - \omega)$ , and likewise, the second is $\overline{\omega} /(1 - \overline{\omega})$ . Together, they combine to give

其中两个级数都绝对收敛。第一个和（无穷几何级数）等于 $1 / (1 - \omega)$，类似地，第二个和等于 $\overline{\omega} /(1 - \overline{\omega})$。它们结合在一起得到

$$\frac{1 - \overline{\omega} + (1 - \omega)\overline{\omega}}{(1 - \omega)(1 - \overline{\omega})} = \frac{1 - |\omega|^2}{|1 - \omega|^2} = \frac{1 - r^2}{1 - 2r\cos\theta + r^2},$$

as claimed. The Poisson kernel will reappear later in the context of Abel summability of the Fourier series of a function.

正如所声称的。泊松核稍后将在函数傅里叶级数的阿贝尔可和性的背景下再次出现。

Let us return to the problem formulated earlier. The definition of the Fourier series of $f$ is purely formal, and it is not obvious whether it converges to $f$ . In fact, the solution of this problem can be very hard, or relatively easy, depending on the sense in which we expect the series to converge, or on what additional restrictions we place on $f$ .

让我们回到前面阐述的问题。$f$ 的傅里叶级数的定义纯粹是形式上的，它是否收敛到 $f$ 并不明显。事实上，这个问题的解决可能非常困难，也可能相对容易，这取决于我们期望级数以何种意义收敛，或者我们对 $f$ 施加了哪些额外的限制。

Let us be more precise. Suppose, for the sake of this discussion, that the function $f$ (which is always assumed to be Riemann integrable) is defined on $[-\pi ,\pi ]$ . The first question one might ask is whether the partial sums of the Fourier series of $f$ converge to $f$ pointwise. That is, do we have

让我们更精确地说。假设为了讨论方便，函数 $f$（我们总是假设它是黎曼可积的）定义在 $[-\pi ,\pi ]$ 上。人们可能首先问的是，$f$ 的傅里叶级数的部分和是否逐点收敛到 $f$。也就是说，我们是否有

$$\lim_{N\to \infty}S_N(f)(\theta) = f(\theta)\quad \mathrm{for~every~}\theta ? \quad (1)$$

We see quite easily that in general we cannot expect this result to be true at every $\theta$ , since we can always change an integrable function at one point without changing its Fourier coefficients. As a result, we might ask the same question assuming that $f$ is continuous and periodic. For a long time it was believed that under these additional assumptions the answer would be "yes." It was a surprise when Du Bois- Reymond showed that there exists a continuous function whose Fourier series diverges at a point. We will give such an example in the next chapter. Despite this negative result, we might ask what happens if we add more smoothness conditions on $f$ : for example, we might assume that $f$ is continuously

我们很容易看出，一般来说我们不能期望这个结果在每个 $\theta$ 上都成立，因为我们总可以改变一个可积函数在某一点的值而不改变其傅里叶系数。因此，我们可能会在假设 $f$ 连续且周期的前提下问同样的问题。很长一段时间里，人们相信在这些附加假设下答案会是“是”。所以当杜布瓦-雷蒙证明存在一个连续函数其傅里叶级数在某点发散时，这是一个意外。我们将在下一章给出这样一个例子。尽管有这个负面结果，我们可能会问，如果我们对 $f$ 添加更多的光滑性条件会发生什么：例如，我们可以假设 $f$ 是连续

differentiable, or twice continuously differentiable. We will see that then the Fourier series of $f$ converges to $f$ uniformly.

可微的，或者两次连续可微的。我们将看到，此时 $f$ 的傅里叶级数一致收敛到 $f$。

We will also interpret the limit (1) by showing that the Fourier series sums, in the sense of Cesaro or Abel, to the function $f$ at all of its points of continuity. This approach involves appropriate averages of the partial sums of the Fourier series of $f$ .

我们还将通过证明傅里叶级数在切萨罗或阿贝尔意义下，在 $f$ 的所有连续点处和到函数 $f$，来解释极限 (1)。这种方法涉及对 $f$ 的傅里叶级数部分和的适当平均。

Finally, we can also define the limit (1) in the mean square sense. In the next chapter, we will show that if $f$ is merely integrable, then

最后，我们也可以在均方意义下定义极限 (1)。在下一章中，我们将证明，如果 $f$ 仅仅是可积的，那么

$$\frac{1}{2\pi}\int_{-\pi}^{\pi}|S_N(f)(\theta) - f(\theta)|^2 d\theta \to 0\quad \mathrm{as} N\to \infty .$$

It is of interest to know that the problem of pointwise convergence of Fourier series was settled in 1966 by L. Carleson, who showed, among other things, that if $f$ is integrable in our sense, the Fourier series of $f$ converges to $f$ except possibly on a set of "measure 0." The proof of this theorem is difficult and beyond the scope of this book.

有趣的是，傅里叶级数的逐点收敛问题于1966年被L. Carleson解决，他证明了，除其他事项外，如果 $f$ 在我们意义下是可积的，那么 $f$ 的傅里叶级数除了可能在某个“测度0”的集合上之外，都收敛到 $f$。这个定理的证明很困难，超出了本书的范围。

---

## 2 Uniqueness of Fourier series

## 2 傅里叶级数的唯一性

If we were to assume that the Fourier series of functions $f$ converge to $f$ in an appropriate sense, then we could infer that a function is uniquely determined by its Fourier coefficients. This would lead to the following statement: if $f$ and $g$ have the same Fourier coefficients, then $f$ and $g$ are necessarily equal. By taking the difference $f - g$ , this proposition can be reformulated as: if $\hat{f} (n) = 0$ for all $n\in \mathbb{Z}$ , then $f = 0$ . As stated, this assertion cannot be correct without reservation, since calculating Fourier coefficients requires integration, and we see that, for example, any two functions which differ at finitely many points have the same Fourier series. However, we do have the following positive result.

如果我们假设函数 $f$ 的傅里叶级数以适当的意义收敛到 $f$，那么我们可以推断一个函数由其傅里叶系数唯一确定。这将导致以下陈述：如果 $f$ 和 $g$ 有相同的傅里叶系数，那么 $f$ 和 $g$ 必然相等。通过考虑差 $f - g$，这个命题可以重新表述为：如果对所有 $n\in \mathbb{Z}$ 有 $\hat{f} (n) = 0$，那么 $f = 0$。如所述，这个断言并非无条件正确，因为计算傅里叶系数需要积分，我们看到，例如，任何两个在有限个点处不同的函数有相同的傅里叶级数。然而，我们确实有以下的正面结果。

Theorem 2.1 Suppose that $f$ is an integrable function on the circle with $\hat{f} (n) = 0$ for all $n\in \mathbb{Z}$ . Then $f(\theta_0) = 0$ whenever $f$ is continuous at the point $\theta_0$ .

定理2.1 假设 $f$ 是圆周上的一个可积函数，且对所有 $n\in \mathbb{Z}$ 有 $\hat{f} (n) = 0$。那么，只要 $f$ 在点 $\theta_0$ 处连续，就有 $f(\theta_0) = 0$。

Thus, in terms of what we know about the set of discontinuities of integrable functions, we can conclude that $f$ vanishes for "most" values of $\theta$ .

因此，根据我们对可积函数间断点集的了解，我们可以得出结论：$f$ 对于“大多数” $\theta$ 值取值为零。

Proof. We suppose first that $f$ is real- valued, and argue by contradiction. Assume, without loss of generality, that $f$ is defined on

证明。我们首先假设 $f$ 是实值的，并用反证法论证。不失一般性，假设 $f$ 定义在

$[- \pi ,\pi ]$ ,that $\theta_0 = 0$ ,and $f(0) > 0$ .The idea now is to construct a family of trigonometric polynomials $\{p_k\}$ that "peak" at 0, and so that $\int p_k(\theta)f(\theta)d\theta \rightarrow \infty$ as $k\rightarrow \infty$ .This will be our desired contradiction since these integrals are equal to zero by assumption.

$[- \pi ,\pi ]$ 上，$\theta_0 = 0$，且 $f(0) > 0$。现在的想法是构造一族三角多项式 $\{p_k\}$，它们在 0 处“峰值”，并且使得当 $k\rightarrow \infty$ 时 $\int p_k(\theta)f(\theta)d\theta \rightarrow \infty$。这将是我们期望的矛盾，因为根据假设这些积分等于零。

Since $f$ is continuous at 0, we can choose $0< \delta \leq \pi /2$ , so that $f(\theta) > f(0) / 2$ whenever $|\theta |< \delta$ . Let

由于 $f$ 在 0 处连续，我们可以选择 $0< \delta \leq \pi /2$，使得只要 $|\theta |< \delta$ 就有 $f(\theta) > f(0) / 2$。令

$$p(\theta) = \epsilon +\cos \theta ,$$

where $\epsilon >0$ is chosen so small that $|p(\theta)|< 1 - \epsilon /2$ , whenever $\delta \leq |\theta |\leq$ $\pi$ .Then, choose a positive $\eta$ with $\eta < \delta$ , so that $p(\theta)\geq 1 + \epsilon /2$ ,for $|\theta |< \eta$ .Finally, let

其中选择 $\epsilon >0$ 足够小，使得只要 $\delta \leq |\theta |\leq \pi$ 就有 $|p(\theta)|< 1 - \epsilon /2$。然后，选择一个正数 $\eta$ 满足 $\eta < \delta$，使得对于 $|\theta |< \eta$ 有 $p(\theta)\geq 1 + \epsilon /2$。最后，令

$$p_k(\theta) = [p(\theta)]^k,$$

and select $B$ so that $|f(\theta)|\leq B$ for all $\theta$ .This is possible since $f$ is integrable, hence bounded. Figure 3 illustrates the family $\{p_k\}$ .By

并选择 $B$ 使得对所有 $\theta$ 有 $|f(\theta)|\leq B$。这是可能的，因为 $f$ 可积，从而有界。图3说明了族 $\{p_k\}$。

<center>Figure 3. The functions $p$ , $p_6$ , and $p_{15}$ when $\epsilon = 0.1$ </center>

<center>图3. 当 $\epsilon = 0.1$ 时的函数 $p$、$p_6$ 和 $p_{15}$</center>

construction, each $p_k$ is a trigonometric polynomial, and since $\hat{f} (n) = 0$ for all $n$ , we must have

根据构造，每个 $p_k$ 是一个三角多项式，并且由于对所有 $n$ 有 $\hat{f} (n) = 0$，我们必须有

$$\int_{-\pi}^{\pi}f(\theta)p_k(\theta)d\theta = 0\quad \mathrm{for~all~}k.$$

However, we have the estimate

然而，我们有估计

$$\left|\int_{\delta \leq |\theta |}f(\theta)p_k(\theta)d\theta \right|\leq 2\pi B(1 - \epsilon /2)^k.$$

Also, our choice of $\delta$ guarantees that $p(\theta)$ and $f(\theta)$ are non- negative whenever $|\theta |< \delta$ , thus

此外，我们对 $\delta$ 的选择保证了只要 $|\theta |< \delta$，$p(\theta)$ 和 $f(\theta)$ 是非负的，因此

$$\int_{\eta \leq |\theta |< \delta}f(\theta)p_k(\theta)d\theta \geq 0.$$

Finally,

最后，

$$\int_{|\theta |< \eta}f(\theta)p_k(\theta)d\theta \geq 2\eta \frac{f(0)}{2} (1 + \epsilon /2)^k.$$

Therefore, $\int p_k(\theta)f(\theta)d\theta \rightarrow \infty$ as $k\rightarrow \infty$ , and this concludes the proof when $f$ is real- valued. In general, write $f(\theta) = u(\theta) + iv(\theta)$ , where $u$ and $v$ are real- valued. If we define $\overline{f} (\theta) = \overline{f} (\theta)$ , then

因此，当 $k\rightarrow \infty$ 时 $\int p_k(\theta)f(\theta)d\theta \rightarrow \infty$，这就完成了 $f$ 为实值时的证明。一般情况下，记 $f(\theta) = u(\theta) + iv(\theta)$，其中 $u$ 和 $v$ 是实值的。如果我们定义 $\overline{f} (\theta) = \overline{f} (\theta)$，那么

$$u(\theta) = \frac{f(\theta) + \overline{f}(\theta)}{2}\quad \mathrm{and}\quad v(\theta) = \frac{f(\theta) - \overline{f}(\theta)}{2i},$$

and since $\hat{\overline{f}} (n) = \overline{\hat{f} (- n)}$ , we conclude that the Fourier coefficients of $u$ and $v$ all vanish, hence $f = 0$ at its points of continuity. The idea

并且由于 $\hat{\overline{f}} (n) = \overline{\hat{f} (- n)}$，我们得出结论：$u$ 和 $v$ 的所有傅里叶系数都为零，因此在其连续点处 $f = 0$。

of constructing a family of functions (trigonometric polynomials in this case) which peak at the origin, together with other nice properties, will play an important role in this book. Such families of functions will be taken up later in Section 4 in connection with the notion of convolution. For now, note that the above theorem implies the following.

构造一族在原点处达到峰值且具有其他良好性质的函数（此处为三角多项式）的想法将在本书中发挥重要作用。我们将在后面第4节结合卷积的概念来讨论这类函数族。现在，注意上述定理蕴含了以下结论。

Corollary 2.2 If $f$ is continuous on the circle and $\hat{f} (n) = 0$ for all $n\in \mathbb{Z}$ , then $f = 0$ .

推论2.2 如果 $f$ 在圆周上连续且对所有 $n\in \mathbb{Z}$ 有 $\hat{f} (n) = 0$，那么 $f = 0$。

The next corollary shows that the problem (1) formulated earlier has a simple positive answer under the assumption that the series of Fourier coefficients converges absolutely.

下一个推论表明，在傅里叶系数级数绝对收敛的假设下，之前阐述的问题 (1) 有一个简单的肯定答案。

Corollary 2.3 Suppose that $f$ is a continuous function on the circle and that the Fourier series of $f$ is absolutely convergent, $\sum_{n = -\infty}^{\infty}|\hat{f} (n)|< \infty$ . Then, the Fourier series converges uniformly to $f$ , that is,

推论2.3 假设 $f$ 是圆周上的一个连续函数，并且 $f$ 的傅里叶级数绝对收敛，$\sum_{n = -\infty}^{\infty}|\hat{f} (n)|< \infty$。那么，傅里叶级数一致收敛到 $f$，即

$$\lim_{N\to \infty}S_N(f)(\theta) = f(\theta)\quad \text{uniformly in} \theta .$$

Proof. Recall that if a sequence of continuous functions converges uniformly, then the limit is also continuous. Now observe that the assumption $\sum |\hat{f} (n)|< \infty$ implies that the partial sums of the Fourier

证明。回忆一下，如果一列连续函数一致收敛，那么极限也是连续的。现在观察到假设 $\sum |\hat{f} (n)|< \infty$ 意味着傅里叶级数的部分和

series of $f$ converge absolutely and uniformly, and therefore the function $g$ defined by

绝对且一致收敛，因此由下式定义的函数 $g$

$$g(\theta) = \sum_{n = -\infty}^{\infty}\hat{f} (n)e^{in\theta} = \lim_{N\to \infty}\sum_{n = -N}^{N}\hat{f} (n)e^{in\theta}$$

is continuous on the circle. Moreover, the Fourier coefficients of $g$ are precisely $\hat{f} (n)$ since we can interchange the infinite sum with the integral (a consequence of the uniform convergence of the series). Therefore, the previous corollary applied to the function $f - g$ yields $f = g$ , as desired.

在圆周上连续。此外，$g$ 的傅里叶系数正好是 $\hat{f} (n)$，因为我们可以交换无穷和与积分（这是级数一致收敛的结果）。因此，将前一个推论应用于函数 $f - g$ 得到 $f = g$，如所愿。

What conditions on $f$ would guarantee the absolute convergence of its Fourier series? As it turns out, the smoothness of $f$ is directly related to the decay of the Fourier coefficients, and in general, the smoother the function, the faster this decay. As a result, we can expect that relatively smooth functions equal their Fourier series. This is in fact the case, as we now show.

$f$ 上什么样的条件能保证其傅里叶级数的绝对收敛？事实证明，$f$ 的光滑性与傅里叶系数的衰减直接相关，并且一般来说，函数越光滑，衰减越快。因此，我们可以预期相对光滑的函数等于其傅里叶级数。事实确实如此，我们现在就来证明。

In order to state the result concisely we introduce the standard "O" notation, which we will use freely in the rest of this book. For example, the statement $\hat{f} (n) = O(1 / |n|^2)$ as $|n|\to \infty$ , means that the lefthand side is bounded by a constant multiple of the right- hand side; that is, there exists $C > 0$ with $|\hat{f} (n)|\leq C / |n|^2$ for all large $|n|$ . More generally, $f(x) = O(g(x))$ as $x\to a$ means that for some constant $C$ , $|f(x)|\leq C|g(x)|$ as $x$ approaches $a$ . In particular, $f(x) = O(1)$ means that $f$ is bounded.

为了简洁地陈述结果，我们引入标准的“O”记号，本书余下部分将自由使用它。例如，陈述 $\hat{f} (n) = O(1 / |n|^2)$ 当 $|n|\to \infty$ 时，意味着左边被右边的常数倍控制；即存在 $C > 0$ 使得对所有足够大的 $|n|$ 有 $|\hat{f} (n)|\leq C / |n|^2$。更一般地，当 $x\to a$ 时 $f(x) = O(g(x))$ 意味着存在某个常数 $C$，使得当 $x$ 趋近 $a$ 时 $|f(x)|\leq C|g(x)|$。特别地，$f(x) = O(1)$ 意味着 $f$ 有界。

Corollary 2.4 Suppose that $f$ is a twice continuously differentiable function on the circle. Then

推论2.4 假设 $f$ 是圆周上的一个两次连续可微函数。那么

$$\hat{f} (n) = O(1 / |n|^2)\quad as|n|\to \infty ,$$

so that the Fourier series of $f$ converges absolutely and uniformly to $f$ .

因此 $f$ 的傅里叶级数绝对且一致收敛到 $f$。

Proof. The estimate on the Fourier coefficients is proved by integrating by parts twice for $n \neq 0$ . We obtain

证明。傅里叶系数的估计是通过对 $n \neq 0$ 进行两次分部积分证明的。我们得到

$$2\pi \hat{f} (n) = \int_{0}^{2\pi}f(\theta)e^{-in\theta}d\theta$$ $$= \left[f(\theta)\cdot \frac{-e^{-in\theta}}{in}\right]_{0}^{2\pi} + \frac{1}{in}\int_{0}^{2\pi}f'(\theta)e^{-in\theta}d\theta$$ $$= \frac{1}{in}\int_{0}^{2\pi}f'(\theta)e^{-i n\theta}d\theta$$ $$= \frac{1}{in}\left[f'(\theta)\cdot \frac{-e^{-in\theta}}{in}\right]_{0}^{2\pi} + \frac{1}{(in)^{2}}\int_{0}^{2\pi}f''(\theta)e^{-in\theta}d\theta$$ $$= \frac{-1}{n^{2}}\int_{0}^{2\pi}f''(\theta)e^{-in\theta}d\theta.$$

The quantities in brackets vanish since $f$ and $f^{\prime}$ are periodic. Therefore

括号中的量消失，因为 $f$ 和 $f^{\prime}$ 是周期的。因此

$$2\pi |n|^2 |\hat{f} (n)| \leq \left| \int_0^{2\pi} f''(\theta) e^{-in\theta} d\theta \right| \leq \int_0^{2\pi} |f''(\theta)| d\theta \leq C,$$

where the constant $C$ is independent of $n$ . (We can take $C = 2\pi B$ where $B$ is a bound for $f''$ .) Since $\sum 1 / n^2$ converges, the proof of the corollary is complete.

其中常数 $C$ 与 $n$ 无关。（我们可以取 $C = 2\pi B$，其中 $B$ 是 $f''$ 的一个界。）由于 $\sum 1 / n^2$ 收敛，推论的证明完成。

Incidentally, we have also established the following important identity:

顺便提一下，我们也建立了以下重要的恒等式：

$$\hat{f} '(n) = in\hat{f} (n),\quad \mathrm{for~all~}n\in \mathbb{Z}.$$

If $n \neq 0$ the proof is given above, and if $n = 0$ it is left as an exercise to the reader. So if $f$ is differentiable and $f \sim \sum a_n e^{in\theta}$ , then $f' \sim \sum a_n in e^{in\theta}$ . Also, if $f$ is twice continuously differentiable, then $f'' \sim \sum a_n (in)^2 e^{in\theta}$ , and so on. Further smoothness conditions on $f$ imply even better decay of the Fourier coefficients (Exercise 10).

如果 $n \neq 0$，上面给出了证明，如果 $n = 0$，则作为练习留给读者。所以如果 $f$ 可微且 $f \sim \sum a_n e^{in\theta}$，那么 $f' \sim \sum a_n in e^{in\theta}$。同样，如果 $f$ 两次连续可微，那么 $f'' \sim \sum a_n (in)^2 e^{in\theta}$，依此类推。对 $f$ 的进一步光滑性条件意味着傅里叶系数的衰减更快（练习10）。

There are also stronger versions of Corollary 2.4. It can be shown, for example, that the Fourier series of $f$ converges absolutely, assuming only that $f$ has one continuous derivative. Even more generally, the Fourier series of $f$ converges absolutely (and hence uniformly to $f$ ) if $f$ satisfies a Hölder condition of order $\alpha$ , with $\alpha > 1 / 2$ , that is,

推论2.4也有更强的版本。例如，可以证明，仅假设 $f$ 有一个连续导数，$f$ 的傅里叶级数绝对收敛。更一般地，如果 $f$ 满足阶数为 $\alpha$ 的赫尔德条件，且 $\alpha > 1 / 2$，即

$$\sup_{\theta}|f(\theta +t) - f(\theta)|\leq A|t|^{\alpha}\quad \mathrm{for~all~}t.$$

For more on these matters, see the exercises at the end of Chapter 3.

关于这些问题的更多信息，请参见第三章末尾的练习。

At this point it is worthwhile to introduce a common notation: we say that $f$ belongs to the class $C^k$ if $f$ is $k$ times continuously differentiable. Belonging to the class $C^k$ or satisfying a Hölder condition are two possible ways to describe the smoothness of a function.

在这一点上，引入一个常见的记号是值得的：我们说 $f$ 属于 $C^k$ 类，如果 $f$ 是 $k$ 次连续可微的。属于 $C^k$ 类或满足赫尔德条件是描述函数光滑性的两种可能方式。

---

## 3 Convolutions

## 3 卷积

The notion of convolution of two functions plays a fundamental role in Fourier analysis; it appears naturally in the context of Fourier series but also serves more generally in the analysis of functions in other settings.

两个函数的卷积概念在傅里叶分析中起着基础性作用；它自然地出现在傅里叶级数的上下文中，但在其他设定下的函数分析中也更广泛地适用。

Given two $2\pi$ - periodic integrable functions $f$ and $g$ on $\mathbb{R}$ , we define their convolution $f*g$ on $[-\pi ,\pi ]$ by

给定 $\mathbb{R}$ 上的两个 $2\pi$ 周期可积函数 $f$ 和 $g$，我们在 $[-\pi ,\pi ]$ 上定义它们的卷积 $f*g$ 为

$$(f*g)(x) = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)g(x - y)dy. \quad (2)$$

The above integral makes sense for each $x$ , since the product of two integrable functions is again integrable. Also, since the functions are periodic, we can change variables to see that

上述积分对每个 $x$ 有意义，因为两个可积函数的乘积仍是可积的。同样，由于函数是周期的，我们可以通过变量替换看到

$$(f*g)(x) = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(x - y)g(y)dy.$$

Loosely speaking, convolutions correspond to "weighted averages." For instance, if $g = 1$ in (2), then $f*g$ is constant and equal to $\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)dy$ which we may interpret as the average value of $f$ on the circle. Also, the convolution $(f*g)(x)$ plays a role similar to, and in some sense replaces, the pointwise product $f(x)g(x)$ of the two functions $f$ and $g$ .

粗略地说，卷积对应于“加权平均”。例如，如果在(2)中取 $g = 1$，那么 $f*g$ 是常数，等于 $\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)dy$，我们可以将其解释为 $f$ 在圆周上的平均值。此外，卷积 $(f*g)(x)$ 的作用类似于，并且在某种意义上取代了，两个函数 $f$ 和 $g$ 的点态乘积 $f(x)g(x)$。

In the context of this chapter, our interest in convolutions originates from the fact that the partial sums of the Fourier series of $f$ can be expressed as follows:

在本章的上下文中，我们对卷积的兴趣源于以下事实：$f$ 的傅里叶级数的部分和可以表示如下：

$$S_N(f)(x) = \sum_{n = -N}^{N}\hat{f} (n)e^{inx}$$ $$\qquad = \sum_{n = -N}^{N}\left(\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)e^{-iny}dy\right)e^{inx}$$ $$\qquad = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)\left(\sum_{n = -N}^{N}e^{in(x - y)}\right)dy$$ $$\qquad = (f*D_N)(x),$$

where $D_{N}$ is the $N^{\mathrm{th}}$ Dirichlet kernel (see Example 4) given by

其中 $D_{N}$ 是第 $N$ 个狄利克雷核（见例4），由下式给出

$$D_{N}(x) = \sum_{n = -N}^{N}e^{inx}.$$

So we observe that the problem of understanding $S_{N}(f)$ reduces to the understanding of the convolution $f * D_{N}$ .

因此我们观察到，理解 $S_{N}(f)$ 的问题归结为理解卷积 $f * D_{N}$。

We begin by gathering some of the main properties of convolutions.

我们首先收集卷积的一些主要性质。

Proposition 3.1 Suppose that $f$ , $g$ , and $h$ are $2\pi$ - periodic integrable functions. Then:

命题3.1 假设 $f$、$g$ 和 $h$ 是 $2\pi$ 周期可积函数。那么：

$$(i)f*g(h)=(f*g)+(f*h).$$ $$(ii)(cf)*g=c(f*g)=f*(cg)foranyc\in\mathbb{C}.$$ $$(iii)f*g=g*f.$$ $$(iv)(f*g)*h=f*(g*h).$$ $$(v)f*giscontinuous.$$ $$(vi)\widehat{f*g}(n)=\hat{f}(n)\hat{g}(n).$$

The first four points describe the algebraic properties of convolutions: linearity, commutativity, and associativity. Property (v) exhibits an important principle: the convolution of $f*g$ is "more regular" than $f$ or $g$ . Here, $f*g$ is continuous while $f$ and $g$ are merely (Riemann) integrable. Finally, (vi) is key in the study of Fourier series. In general, the Fourier coefficients of the product $fg$ are not the product of the Fourier coefficients of $f$ and $g$ . However, (vi) says that this relation holds if we replace the product of the two functions $f$ and $g$ by their convolution $f*g$ .

前四点描述了卷积的代数性质：线性性、交换性和结合性。性质(v)展示了一个重要原则：$f*g$ 的卷积比 $f$ 或 $g$ “更正则”。这里，$f*g$ 是连续的，而 $f$ 和 $g$ 仅仅是（黎曼）可积的。最后，(vi) 是傅里叶级数研究中的关键。一般来说，乘积 $fg$ 的傅里叶系数不是 $f$ 和 $g$ 的傅里叶系数的乘积。然而，(vi) 表明，如果我们用两个函数 $f$ 和 $g$ 的卷积 $f*g$ 代替它们的乘积，那么这个关系成立。

Proof. Properties (i) and (ii) follow at once from the linearity of the integral.

证明。性质(i)和(ii)直接从积分的线性性得出。

The other properties are easily deduced if we assume also that $f$ and $g$ are continuous. In this case, we may freely interchange the order of

如果我们还假设 $f$ 和 $g$ 是连续的，那么其他性质很容易推导出来。在这种情况下，我们可以自由地交换积分的顺序

integration. For instance, to establish (vi) we write

。例如，为了建立(vi)，我们写

$$\widehat{f*g}(n) = \frac{1}{2\pi}\int_{-\pi}^{\pi}(f*g)(x)e^{-inx}dx$$ $$= \frac{1}{2\pi}\int_{-\pi}^{\pi}\frac{1}{2\pi}\left(\int_{-\pi}^{\pi}f(y)g(x - y)dy\right)e^{-inx}dx$$ $$= \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)e^{-inx}\left(\frac{1}{2\pi}\int_{-\pi}^{\pi}g(x - y)e^{-inx(-y)}dx\right)dy$$ $$= \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)e^{-inx}\left(\frac{1}{2\pi}\int_{-\pi}^{\pi}g(x)e^{-inx}dx\right)dy$$ $$= \hat{f}(n)\hat{g}(n).$$

To prove (iii), one first notes that if $F$ is continuous and $2\pi$ - periodic, then

为了证明(iii)，首先注意到如果 $F$ 连续且 $2\pi$ 周期，那么

$$\int_{-\pi}^{\pi}F(y)dy = \int_{-\pi}^{\pi}F(x - y)dy\quad \mathrm{for~any~}x\in \mathbb{R}.$$

The verification of this identity consists of a change of variables $y\mapsto - y$ followed by a translation $y\mapsto y - x$ . Then, one takes $F(y) = f(y)g(x - y)$

这个恒等式的验证包括变量替换 $y\mapsto - y$，然后平移 $y\mapsto y - x$。然后，取 $F(y) = f(y)g(x - y)$。

Also, (iv) follows by interchanging two integral signs, and an appropriate change of variables.

同样，(iv) 通过交换两个积分符号和适当的变量替换得出。

Finally, we show that if $f$ and $g$ are continuous, then $f*g$ is continuous. First, we may write

最后，我们证明如果 $f$ 和 $g$ 连续，那么 $f*g$ 连续。首先，我们可以写

$$(f*g)(x_1) - (f*g)(x_2) = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)[g(x_1 - y) - g(x_2 - y)]dy.$$

Since $g$ is continuous it must be uniformly continuous on any closed and bounded interval. But $g$ is also periodic, so it must be uniformly continuous on all of $\mathbb{R}$ ; given $\epsilon >0$ there exists $\delta >0$ so that $|g(s) - g(t)|< \epsilon$ whenever $|s - t|< \delta$ . Then, $|x_1 - x_2|< \delta$ implies $|(x_1 - y) - (x_2 - y)|< \delta$ for any $y$ , hence

由于 $g$ 是连续的，它在任何有界闭区间上必然一致连续。但 $g$ 也是周期的，所以它在整个 $\mathbb{R}$ 上必然一致连续；给定 $\epsilon >0$，存在 $\delta >0$ 使得只要 $|s - t|< \delta$ 就有 $|g(s) - g(t)|< \epsilon$。那么，$|x_1 - x_2|< \delta$ 意味着对任意 $y$ 有 $|(x_1 - y) - (x_2 - y)|< \delta$，因此

$$\begin{array}{r l} & {|(f*g)(x_{1}) - (f*g)(x_{2})|\leq \frac{1}{2\pi}\left|\int_{-\pi}^{\pi}f(y)[g(x_{1} - y) - g(x_{2} - y)]\right|dy}\\ & {\qquad \leq \frac{1}{2\pi}\int_{-\pi}^{\pi}|f(y)||g(x_{1} - y) - g(x_{2} - y)|dy}\\ & {\qquad \leq \frac{\epsilon}{2\pi}\int_{-\pi}^{\pi}|f(y)|dy}\\ & {\qquad \leq \frac{\epsilon}{2\pi} 2\pi B,} \end{array} \quad (1)$$

where $B$ is chosen so that $|f(x)|\leq B$ for all $x$ . As a result, we conclude that $f*g$ is continuous, and the proposition is proved, at least when $f$ and $g$ are continuous.

其中选择 $B$ 使得对所有 $x$ 有 $|f(x)|\leq B$。结果，我们得出结论 $f*g$ 是连续的，命题得证，至少在 $f$ 和 $g$ 连续的情况下。

In general, when $f$ and $g$ are merely integrable, we may use the results established so far (when $f$ and $g$ are continuous), together with the following approximation lemma, whose proof may be found in the appendix.

一般情况下，当 $f$ 和 $g$ 仅仅是可积时，我们可以使用到目前为止建立的结果（当 $f$ 和 $g$ 连续时），结合下面的逼近引理，其证明可在附录中找到。

Lemma 3.2 Suppose $f$ is integrable on the circle and bounded by $B$ . Then there exists a sequence $\{f_k\}_{k = 1}^{\infty}$ of continuous functions on the circle so that

引理3.2 假设 $f$ 在圆周上可积且以 $B$ 为界。那么存在一列圆周上的连续函数 $\{f_k\}_{k = 1}^{\infty}$，使得

$$\sup_{x\in [-\pi ,\pi ]}|f_k(x)|\leq B\quad \text{for all} k = 1,2,\ldots ,$$

and

并且

$$\int_{-\pi}^{\pi}|f(x) - f_k(x)|dx\to 0\quad as k\to \infty .$$

Using this result, we may complete the proof of the proposition as follows. Apply Lemma 3.2 to $f$ and $g$ to obtain sequences $\{f_k\}$ and $\{g_k\}$ of approximating continuous functions. Then

利用这个结果，我们可以如下完成命题的证明。将引理3.2应用于 $f$ 和 $g$，得到逼近连续函数序列 $\{f_k\}$ 和 $\{g_k\}$。那么

$$f*g - f_k*g_k = (f - f_k)*g + f_k*(g - g_k).$$

By the properties of the sequence $\{f_k\}$

根据序列 $\{f_k\}$ 的性质

$$|(f - f_k)*g(x)|\leq \frac{1}{2\pi}\int_{-\pi}^{\pi}|f(x - y) - f_k(x - y)||g(y)|dy$$ $$\leq \frac{1}{2\pi}\sup_y|g(y)|\int_{-\pi}^{\pi}|f(y) - f_k(y)|dy$$ $$\to 0\quad \mathrm{as} k\to \infty .$$

Hence $(f - f_k)*g\to 0$ uniformly in $x$ . Similarly, $f_k*(g - g_k)\to 0$ uniformly, and therefore $f_k*g_k$ tends uniformly to $f*g$ . Since each $f_k*g_k$ is continuous, it follows that $f*g$ is also continuous, and we have (v).

因此 $(f - f_k)*g\to 0$ 关于 $x$ 一致成立。类似地，$f_k*(g - g_k)\to 0$ 一致成立，因此 $f_k*g_k$ 一致趋于 $f*g$。由于每个 $f_k*g_k$ 是连续的，可得 $f*g$ 也是连续的，这就得到了 (v)。

Next, we establish (vi). For each fixed integer $n$ we must have $\widehat{f_k*g_k}(n)\to \widehat{f*g}(n)$ as $k$ tends to infinity since $f_k*g_k$ converges uniformly to $f*g$ . However, we found earlier that $\widehat{f_k}(n)\widehat{g_k}(n) = \widehat{f_k*g_k}(n)$ because both $f_k$ and $g_k$ are continuous. Hence

接下来，我们建立 (vi)。对每个固定的整数 $n$，由于 $f_k*g_k$ 一致收敛到 $f*g$，当 $k$ 趋于无穷时必须有 $\widehat{f_k*g_k}(n)\to \widehat{f*g}(n)$。然而，我们之前发现 $\widehat{f_k}(n)\widehat{g_k}(n) = \widehat{f_k*g_k}(n)$，因为 $f_k$ 和 $g_k$ 都是连续的。因此

$$\vert \hat{f} (n) - \hat{f}_k(n)\vert = \frac{1}{2\pi}\left|\int_{-\pi}^{\pi}(f(x) - f_k(x))e^{-inx}dx\right|$$ $$\qquad \leq \frac{1}{2\pi}\int_{-\pi}^{\pi}|f(x) - f_k(x)|dx,$$

and as a result we find that $\widehat{f_k} (n) \to \hat{f} (n)$ as $k$ goes to infinity. Similarly $\widehat{g_k} (n) \to \hat{g} (n)$ , and the desired property is established once we let $k$ tend to infinity. Finally, properties (iii) and (iv) follow from the same kind of arguments.

结果我们发现当 $k$ 趋于无穷时 $\widehat{f_k} (n) \to \hat{f} (n)$。类似地 $\widehat{g_k} (n) \to \hat{g} (n)$，当我们让 $k$ 趋于无穷时，所需性质即得证。最后，性质 (iii) 和 (iv) 由同样的论证得出。

---

## 4 Good kernels

## 4 好核

In the proof of Theorem 2.1 we constructed a sequence of trigonometric polynomials $\{p_k\}$ with the property that the functions $p_k$ peaked at the origin. As a result, we could isolate the behavior of $f$ at the origin. In this section, we return to such families of functions, but this time in a more general setting. First, we define the notion of good kernel, and discuss the characteristic properties of such functions. Then, by the use of convolutions, we show how these kernels can be used to recover a given function.

在定理2.1的证明中，我们构造了一列三角多项式 $\{p_k\}$，其性质是函数 $p_k$ 在原点处达到峰值。因此，我们可以分离出 $f$ 在原点的行为。在本节中，我们将回到这类函数族，但这次是在更一般的设定下。首先，我们定义好核的概念，并讨论此类函数的特征性质。然后，通过使用卷积，我们展示如何利用这些核来恢复一个给定的函数。

A family of kernels $\{K_n(x)\}_{n = 1}^{\infty}$ on the circle is said to be a family of good kernels if it satisfies the following properties:

圆周上的一族核 $\{K_n(x)\}_{n = 1}^{\infty}$ 被称为一族好核，如果它满足以下性质：

(a) For all $n \geq 1$

(a) 对所有 $n \geq 1$

$$\frac{1}{2\pi}\int_{-\pi}^{\pi}K_n(x)dx = 1.$$

(b) There exists $M > 0$ such that for all $n \geq 1$

(b) 存在 $M > 0$ 使得对所有 $n \geq 1$

$$\int_{-\pi}^{\pi}|K_n(x)|dx\leq M.$$

(c) For every $\delta > 0$

(c) 对每个 $\delta > 0$

$$\int_{\delta \leq |x|\leq \pi}|K_n(x)|dx\to 0,\quad \mathrm{as} n\to \infty .$$

In practice we shall encounter families where $K_n(x) \geq 0$ , in which case (b) is a consequence of (a). We may interpret the kernels $K_n(x)$ as weight distributions on the circle: property (a) says that $K_n$ assigns unit mass to the whole circle $[-\pi , \pi ]$ , and (c) that this mass concentrates near the origin as $n$ becomes large.6 Figure 4 (a) illustrates the typical character of a family of good kernels.

在实践中，我们将遇到 $K_n(x) \geq 0$ 的族，在这种情况下，(b) 是 (a) 的推论。我们可以将核 $K_n(x)$ 解释为圆周上的权重分布：性质 (a) 表明 $K_n$ 给整个圆周 $[-\pi , \pi ]$ 分配了单位质量，而 (c) 表明随着 $n$ 变大，这个质量集中在原点附近。⁶ 图4 (a) 说明了一族好核的典型特征。

<center>Figure 4. Good kernels </center>

<center>图4. 好核</center>

The importance of good kernels is highlighted by their use in connection with convolutions.

好核的重要性通过它们在卷积中的应用得以凸显。

Theorem 4.1 Let $\{K_{n}\}_{n = 1}^{\infty}$ be a family of good kernels, and $f$ an integrable function on the circle. Then

定理4.1 设 $\{K_{n}\}_{n = 1}^{\infty}$ 是一族好核，$f$ 是圆周上的一个可积函数。那么

$$\lim_{n\to \infty}(f*K_n)(x) = f(x)$$

whenever $f$ is continuous at $x$ . If $f$ is continuous everywhere, then the above limit is uniform.

只要 $f$ 在 $x$ 处连续。如果 $f$ 处处连续，那么上述极限是一致的。

Because of this result, the family $\{K_{n}\}$ is sometimes referred to as an approximation to the identity.

由于这个结果，族 $\{K_{n}\}$ 有时被称为恒等逼近。

We have previously interpreted convolutions as weighted averages. In this context, the convolution

我们之前将卷积解释为加权平均。在此上下文中，卷积

$$(f*K_n)(x) = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(x - y)K_n(y)dy$$

is the average of $f(x - y)$ , where the weights are given by $K_{n}(y)$ . However, the weight distribution $K_{n}$ concentrates its mass at $y = 0$ as $n$ becomes large. Hence in the integral, the value $f(x)$ is assigned the full mass as $n\to \infty$ . Figure 4 (b) illustrates this point.

是 $f(x - y)$ 的平均，其中权重由 $K_{n}(y)$ 给出。然而，随着 $n$ 变大，权重分布 $K_{n}$ 将其质量集中在 $y = 0$ 处。因此，在积分中，当 $n\to \infty$ 时，值 $f(x)$ 被赋予了全部质量。图4 (b) 说明了这一点。

Proof of Theorem 4.1. If $\epsilon >0$ and $f$ is continuous at $x$ , choose $\delta$ so that $|y|< \delta$ implies $|f(x - y) - f(x)|< \epsilon$ . Then, by the first property of good kernels, we can write

定理4.1的证明。如果 $\epsilon >0$ 且 $f$ 在 $x$ 处连续，选择 $\delta$ 使得 $|y|< \delta$ 蕴含 $|f(x - y) - f(x)|< \epsilon$。然后，根据好核的第一个性质，我们可以写

$$(f*K_n)(x) - f(x) = \frac{1}{2\pi}\int_{-\pi}^{\pi}K_n(y)f(x - y)dy - f(x)$$ $$= \frac{1}{2\pi}\int_{-\pi}^{\pi}K_n(y)[f(x - y) - f(x)]dy.$$

Hence,

因此，

$$\begin{array}{r l} & {|(f*K_{n})(x) - f(x)| = \left|\frac{1}{2\pi}\int_{-\pi}^{\pi}K_{n}(y)[f(x - y) - f(x)]dy\right|}\\ & {\qquad \leq \frac{1}{2\pi}\int_{|y|< \delta}|K_{n}(y)||f(x - y) - f(x)|dy}\\ & {\qquad \qquad +\frac{1}{2\pi}\int_{\delta \leq |y|\leq \pi}|K_{n}(y)||f(x - y) - f(x)|dy}\\ & {\qquad \leq \frac{\epsilon}{2\pi}\int_{-\pi}^{\pi}|K_{n}(y)|dy + \frac{2B}{2\pi}\int_{\delta \leq |y|\leq \pi}|K_{n}(y)|dy,} \end{array} \quad (1)$$

where $B$ is a bound for $f$ . The first term is bounded by $\epsilon M / 2\pi$ because of the second property of good kernels. By the third property we see that for all large $n$ , the second term will be less than $\epsilon$ . Therefore, for some constant $C > 0$ and all large $n$ we have

其中 $B$ 是 $f$ 的一个界。根据好核的第二个性质，第一项被 $\epsilon M / 2\pi$ 界定。由第三个性质，我们看到对所有足够大的 $n$，第二项将小于 $\epsilon$。因此，对某个常数 $C > 0$ 和所有足够大的 $n$，我们有

$$|(f*K_n)(x) - f(x)| \leq C\epsilon,$$

thereby proving the first assertion in the theorem. If $f$ is continuous everywhere, then it is uniformly continuous, and $\delta$ can be chosen independent of $x$ . This provides the desired conclusion that $f*K_n \to f$ uniformly.

从而证明了定理的第一个断言。如果 $f$ 处处连续，那么它是一致连续的，并且 $\delta$ 可以选择与 $x$ 无关。这给出了所需的结论：$f*K_n \to f$ 一致收敛。

Recall from the beginning of Section 3 that

回顾第3节开头的内容

$$S_{N}(f)(x) = (f*D_{N})(x),$$

where $D_{N}(x) = \sum_{n = - N}^{N}e^{inx}$ is the Dirichlet kernel. It is natural now for us to ask whether $D_{N}$ is a good kernel, since if this were true, Theorem 4.1 would imply that the Fourier series of $f$ converges to $f(x)$ whenever $f$ is continuous at $x$ . Unfortunately, this is not the case. Indeed, an estimate shows that $D_{N}$ violates the second property; more precisely, one has (see Problem 2)

其中 $D_{N}(x) = \sum_{n = - N}^{N}e^{inx}$ 是狄利克雷核。现在我们自然会问 $D_{N}$ 是否是一个好核，因为如果这是真的，定理4.1将蕴含：只要 $f$ 在 $x$ 处连续，$f$ 的傅里叶级数就收敛到 $f(x)$。不幸的是，情况并非如此。事实上，一个估计表明 $D_{N}$ 违反了第二个性质；更精确地说，有（见问题2）

$$\int_{-\pi}^{\pi}|D_{N}(x)|dx\geq c\log N,\quad \mathrm{as}N\to \infty .$$

However, we should note that the formula for $D_{N}$ as a sum of exponentials immediately gives

然而，我们应该注意到，$D_{N}$ 作为指数和的公式立即给出

$$\frac{1}{2\pi}\int_{-\pi}^{\pi}D_{N}(x)dx = 1,$$

so the first property of good kernels is actually verified. The fact that the mean value of $D_{N}$ is 1, while the integral of its absolute value is large,

所以好核的第一个性质实际上被验证了。$D_{N}$ 的平均值为 1，而其绝对值的积分很大这一事实，

is a result of cancellations. Indeed, Figure 5 shows that the function $D_{N}(x)$ takes on positive and negative values and oscillates very rapidly as $N$ gets large.

是相消的结果。事实上，图5表明函数 $D_{N}(x)$ 取正值和负值，并且随着 $N$ 变大而非常快速地振荡。

<center>Figure 5. The Dirichlet kernel for large $N$ </center>

<center>图5. 大 $N$ 时的狄利克雷核</center>

This observation suggests that the pointwise convergence of Fourier series is intricate, and may even fail at points of continuity. This is indeed the case, as we will see in the next chapter.

这个观察表明傅里叶级数的逐点收敛是复杂的，甚至在连续点处也可能失败。事实确实如此，我们将在下一章看到。

---

## 5 Cesaro and Abel summability: applications to Fourier series

## 5 切萨罗与阿贝尔可和性：傅里叶级数的应用

Since a Fourier series may fail to converge at individual points, we are led to try to overcome this failure by interpreting the limit

由于傅里叶级数可能在个别点处不收敛，我们试图通过以下方式来解释极限来克服这个失败

$$\lim_{N\to \infty}S_N(f) = f$$

in a different sense.

在不同的意义下。

### 5.1 Cesaro means and summation

### 5.1 切萨罗平均与求和

We begin by taking ordinary averages of the partial sums, a technique which we now describe in more detail.

我们首先取部分和的普通平均，我们现在更详细地描述这种技术。

Suppose we are given a series of complex numbers

假设我们给定一个复数项级数

$$c_0 + c_1 + c_2 + \dots = \sum_{k = 0}^{\infty}c_k.$$

We define the $n^{\mathrm{th}}$ partial sum $s_n$ by

我们定义第 $n$ 个部分和 $s_n$ 为
\begin{frame}  
\textbf{Definition} For a series $\sum_{k=0}^{\infty} c_k$, let $s_n = \sum_{k=0}^n c_k$ be the $n^{\mathrm{th}}$ partial sum. The $N^{\mathrm{th}}$ Cesàro mean $\sigma_N$ is the average of the first $N$ partial sums.

\textbf{Formula}  
\begin{equation}  
\sigma_N = \frac{1}{N} \sum_{k=0}^{N-1} s_k.  
\end{equation}  
If $\displaystyle \lim_{N\to\infty} \sigma_N = \sigma$, the series is said to be Cesàro summable to $\sigma$.

\textbf{Significance} Cesàro summation extends the notion of convergence: every convergent series is Cesàro summable to the same limit, and some divergent series (e.g., $1-1+1-1+\cdots$) become summable, yielding a natural value like $1/2$.  
\end{frame}
$$s_n = \sum_{k = 0}^{n}c_k,$$

and say that the series converges to $s$ if $\lim_{n\to \infty}s_n = s$ . This is the most natural and most commonly used type of "summability." Consider, however, the example of the series

并且说级数收敛到 $s$ 如果 $\lim_{n\to \infty}s_n = s$。这是最自然和最常用的“可和性”类型。然而，考虑级数的例子

$$1 - 1 + 1 - 1 + \dots = \sum_{k = 0}^{\infty}(-1)^k. \quad (3)$$

Its partial sums form the sequence $\{1,0,1,0,\ldots \}$ which has no limit. Because these partial sums alternate evenly between 1 and 0, one might therefore suggest that $1 / 2$ is the "limit" of the sequence, and hence $1 / 2$ equals the "sum" of that particular series. We give a precise meaning to this by defining the average of the first $N$ partial sums by

它的部分和形成序列 $\{1,0,1,0,\ldots \}$，该序列没有极限。因为这些部分和在 1 和 0 之间均匀交替，人们可能因此建议 $1 / 2$ 是该序列的“极限”，因此 $1 / 2$ 等于该特定级数的“和”。我们通过定义前 $N$ 个部分和的平均来给这个一个精确的意义

$$\sigma_{N} = \frac{s_{0} + s_{1} + \dots + s_{N - 1}}{N}.$$

The quantity $\sigma_{N}$ is called the $N^{\mathrm{th}}$ Cesaro mean $^7$ of the sequence $\{s_k\}$ or the $N^{\mathrm{th}}$ Cesaro sum of the series $\sum_{k = 0}^{\infty}c_k$

量 $\sigma_{N}$ 被称为序列 $\{s_k\}$ 的第 $N$ 个切萨罗平均 $^7$ 或级数 $\sum_{k = 0}^{\infty}c_k$ 的第 $N$ 个切萨罗和。

If $\sigma_{N}$ converges to a limit $\sigma$ as $N$ tends to infinity, we say that the series $\sum c_n$ is Cesaro summable to $\sigma$ . In the case of series of functions, we shall understand the limit in the sense of either pointwise or uniform convergence, depending on the situation.

如果当 $N$ 趋于无穷时 $\sigma_{N}$ 收敛到极限 $\sigma$，我们说级数 $\sum c_n$ 是切萨罗可和到 $\sigma$。在函数项级数的情况下，我们将根据情况在逐点或一致收敛的意义上理解极限。

The reader will have no difficulty checking that in the above example (3), the series is Cesaro summable to $1 / 2$ . Moreover, one can show that Cesaro summation is a more inclusive process than convergence. In fact, if a series is convergent to $s$ , then it is also Cesaro summable to the same limit $s$ (Exercise 12).

读者不难验证，在上述例子 (3) 中，级数是切萨罗可和到 $1 / 2$ 的。此外，可以证明切萨罗求和是一个比收敛更具包容性的过程。事实上，如果一个级数收敛到 $s$，那么它也是切萨罗可和到同一个极限 $s$ (练习12)。

### 5.2 Fejér's theorem

### 5.2 费耶定理

An interesting application of Cesaro summability appears in the context of Fourier series.

切萨罗可和性的一个有趣应用出现在傅里叶级数的上下文中。

We mentioned earlier that the Dirichlet kernels fail to belong to the family of good kernels. Quite surprisingly, their averages are very well behaved functions, in the sense that they do form a family of good kernels.

我们之前提到狄利克雷核不属于好核族。相当令人惊讶的是，它们的平均是行为非常好的函数，因为它们确实构成了一族好核。

To see this, we form the $N^{\mathrm{th}}$ Cesaro mean of the Fourier series, which by definition is

为了看到这一点，我们构造傅里叶级数的第 $N$ 个切萨罗平均，根据定义它是

$$\sigma_{N}(f)(x) = \frac{S_{0}(f)(x) + \dots + S_{N - 1}(f)(x)}{N}.$$

Since $S_{n}(f) = f * D_{n}$ , we find that

由于 $S_{n}(f) = f * D_{n}$，我们发现

$$\sigma_{N}(f)(x) = (f * F_{N})(x),$$

where $F_{N}(x)$ is the $N$ - th Fejer kernel given by

其中 $F_{N}(x)$ 是第 $N$ 个费耶核，由下式给出

$$F_{N}(x) = \frac{D_{0}(x) + \dots + D_{N - 1}(x)}{N}.$$

Lemma 5.1 We have

引理5.1 我们有

$$F_{N}(x) = \frac{1}{N}\frac{\sin^{2}(Nx / 2)}{\sin^{2}(x / 2)},$$

and the Fejer kernel is a good kernel.

并且费耶核是一个好核。

The proof of the formula for $F_{N}$ (a simple application of trigonometric identities) is outlined in Exercise 15. To prove the rest of the lemma, note that $F_{N}$ is positive and $\begin{array}{r}\frac{1}{2\pi}\int_{-\pi}^{\pi}F_{N}(x)dx = 1 \end{array}$ , in view of the fact that a similar identity holds for the Dirichlet kernels $D_{n}$ . However, $\sin^{2}(x / 2)\geq$ $c_{\delta} > 0$ , if $\delta \leq |x|\leq \pi$ , hence $F_{N}(x)\leq 1 / (Nc_{\delta})$ , from which it follows that

$F_{N}$ 公式的证明（三角恒等式的简单应用）在练习15中概述。为了证明引理的其余部分，注意 $F_{N}$ 是正的，并且 $\begin{array}{r}\frac{1}{2\pi}\int_{-\pi}^{\pi}F_{N}(x)dx = 1 \end{array}$，鉴于狄利克雷核 $D_{n}$ 有类似恒等式成立。然而，如果 $\delta \leq |x|\leq \pi$，则 $\sin^{2}(x / 2)\geq c_{\delta} > 0$，因此 $F_{N}(x)\leq 1 / (Nc_{\delta})$，由此可得

$$\int_{\delta \leq |x|\leq \pi}|F_{N}(x)|dx\to 0\quad \mathrm{as}N\to \infty .$$

Applying Theorem 4.1 to this new family of good kernels yields the following important result.

将定理4.1应用于这个新的好核族，得到以下重要结果。

Theorem 5.2 If $f$ is integrable on the circle, then the Fourier series of $f$ is Cesaro summable to $f$ at every point of continuity of $f$ .

定理5.2 如果 $f$ 在圆周上可积，那么 $f$ 的傅里叶级数在 $f$ 的每个连续点处切萨罗可和到 $f$。

Moreover, if $f$ is continuous on the circle, then the Fourier series of $f$ is uniformly Cesaro summable to $f$ .

此外，如果 $f$ 在圆周上连续，那么 $f$ 的傅里叶级数一致切萨罗可和到 $f$。

We may now state two corollaries. The first is a result that we have already established. The second is new, and of fundamental importance.

我们现在可以陈述两个推论。第一个是我们已经建立的结果。第二个是新的，并且具有根本重要性。

Corollary 5.3 If $f$ is integrable on the circle and $\hat{f} (n) = 0$ for all $n$ , then $f = 0$ at all points of continuity of $f$ .

推论5.3 如果 $f$ 在圆周上可积且对所有 $n$ 有 $\hat{f} (n) = 0$，那么 $f$ 在其所有连续点处等于 0。

The proof is immediate since all the partial sums are 0, hence all the Cesaro means are 0.

证明是直接的，因为所有部分和都是 0，因此所有切萨罗平均都是 0。

Corollary 5.4 Continuous functions on the circle can be uniformly approximated by trigonometric polynomials.

推论5.4 圆周上的连续函数可以被三角多项式一致逼近。

This means that if $f$ is continuous on $[- \pi ,\pi ]$ with $f(- \pi) = f(\pi)$ and $\epsilon >0$ , then there exists a trigonometric polynomial $P$ such that

这意味着如果 $f$ 在 $[- \pi ,\pi ]$ 上连续，且 $f(- \pi) = f(\pi)$，并且 $\epsilon >0$，那么存在一个三角多项式 $P$ 使得

$$|f(x) - P(x)|< \epsilon \quad \mathrm{for~all} - \pi \leq x\leq \pi .$$

This follows immediately from the theorem since the partial sums, hence the Cesaro means, are trigonometric polynomials. Corollary 5.4 is the periodic analogue of the Weierstrass approximation theorem for polynomials which can be found in Exercise 16.

这直接从定理得出，因为部分和，以及切萨罗平均，都是三角多项式。推论5.4是多项式魏尔斯特拉斯逼近定理的周期版本，可以在练习16中找到。

### 5.3 Abel means and summation

### 5.3 阿贝尔平均与求和

Another method of summation was first considered by Abel and actually predates the Cesaro method.

另一种求和方法是阿贝尔首先考虑的，实际上早于切萨罗方法。

A series of complex numbers $\sum_{k = 0}^{\infty}c_{k}$ is said to be Abel summable to $s$ if for every $0\leq r< 1$ , the series

一个复数项级数 $\sum_{k = 0}^{\infty}c_{k}$ 被称为阿贝尔可和到 $s$，如果对每个 $0\leq r< 1$，级数

$$A(r) = \sum_{k = 0}^{\infty}c_{k}r^{k}$$

converges, and

收敛，并且

$$\lim_{r\to 1}A(r) = s.$$

The quantities $A(r)$ are called the Abel means of the series. One can prove that if the series converges to $s$ , then it is Abel summable to $s$ . Moreover, the method of Abel summability is even more powerful than the Cesaro method: when the series is Cesaro summable, it is always Abel summable to the same sum. However, if we consider the series

量 $A(r)$ 被称为该级数的阿贝尔平均。可以证明，如果级数收敛到 $s$，那么它是阿贝尔可和到 $s$ 的。此外，阿贝尔可和性方法甚至比切萨罗方法更强大：当级数切萨罗可和时，它总是阿贝尔可和到同一个和。然而，如果我们考虑级数

$$1 - 2 + 3 - 4 + 5 - \dots = \sum_{k = 0}^{\infty}(-1)^{k}(k + 1),$$

then one can show that it is Abel summable to $1 / 4$ since

那么可以证明它是阿贝尔可和到 $1 / 4$ 的，因为

$$A(r) = \sum_{k = 0}^{\infty}(-1)^{k}(k + 1)r^{k} = \frac{1}{(1 + r)^{2}},$$

but this series is not Cesaro summable; see Exercise 13.

但是这个级数不是切萨罗可和的；见练习13。

### 5.4 The Poisson kernel and Dirichlet's problem in the unit disc

### 5.4 泊松核与单位圆盘中的狄利克雷问题

To adapt Abel summability to the context of Fourier series, we define the Abel means of the function $f(\theta) \sim \sum_{n = -\infty}^{\infty} a_n e^{in\theta}$ by

为了将阿贝尔可和性应用于傅里叶级数，我们定义函数 $f(\theta) \sim \sum_{n = -\infty}^{\infty} a_n e^{in\theta}$ 的阿贝尔平均为

$$A_r(f)(\theta) = \sum_{n = -\infty}^{\infty} r^{|n|} a_n e^{in\theta}.$$

Since the index $n$ takes positive and negative values, it is natural to write $c_0 = a_0$ , and $c_n = a_n e^{in\theta} + a_{- n} e^{- in\theta}$ for $n > 0$ , so that the Abel means of the Fourier series correspond to the definition given in the previous section for numerical series.

由于指标 $n$ 取正值和负值，很自然地写 $c_0 = a_0$，并且对于 $n > 0$ 写 $c_n = a_n e^{in\theta} + a_{- n} e^{- in\theta}$，这样傅里叶级数的阿贝尔平均对应于前一节中给数值级数的定义。

We note that since $f$ is integrable, $|a_n|$ is uniformly bounded in $n$ , so that $A_r(f)$ converges absolutely and uniformly for each $0 \leq r < 1$ . Just as in the case of Cesàro means, the key fact is that these Abel means can be written as convolutions

我们注意到，由于 $f$ 是可积的，$|a_n|$ 在 $n$ 中一致有界，因此对于每个 $0 \leq r < 1$，$A_r(f)$ 绝对且一致收敛。就像切萨罗平均的情况一样，关键事实是这些阿贝尔平均可以写成卷积

$$A_r(f)(\theta) = (f * P_r)(\theta),$$

where $P_r(\theta)$ is the Poisson kernel given by

其中 $P_r(\theta)$ 是泊松核，由下式给出

$$P_r(\theta) = \sum_{n = -\infty}^{\infty} r^{|n|} e^{in\theta}. \quad (4)$$

In fact,

实际上，

$$A_r(f)(\theta) = \sum_{n = -\infty}^{\infty} r^{|n|} a_n e^{in\theta}$$ $$\qquad = \sum_{n = -\infty}^{\infty} r^{|n|} \left(\frac{1}{2\pi} \int_{-\pi}^{\pi} f(\phi) e^{-in\phi} d\phi\right) e^{in\theta}$$ $$\qquad = \frac{1}{2\pi} \int_{-\pi}^{\pi} f(\phi) \left(\sum_{n = -\infty}^{\infty} r^{|n|} e^{-in(\phi -\theta)}\right) d\phi ,$$

where the interchange of the integral and infinite sum is justified by the uniform convergence of the series.

其中积分与无穷和交换是由级数的一致收敛性证明的。

Lemma 5.5 If $0 \leq r < 1$ , then

引理5.5 如果 $0 \leq r < 1$，那么

$$P_r(\theta) = \frac{1 - r^2}{1 - 2r \cos \theta + r^2}.$$

The Poisson kernel is a good kernel, as $r$ tends to 1 from below.

当 $r$ 从下方趋于 1 时，泊松核是一个好核。

Proof. The identity $P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r\cos\theta + r^{2}}$ has already been derived in Section 1.1. Note that

证明。恒等式 $P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r\cos\theta + r^{2}}$ 已经在1.1节中推导过。注意

$$1 - 2r\cos \theta +r^{2} = (1 - r)^{2} + 2r(1 - \cos \theta).$$

Hence if $1 / 2\leq r\leq 1$ and $\delta \leq |\theta |\leq \pi$ ,then

因此，如果 $1 / 2\leq r\leq 1$ 且 $\delta \leq |\theta |\leq \pi$，那么

$$1 - 2r\cos \theta +r^{2}\geq c_{\delta} > 0.$$

Thus $P_{r}(\theta)\leq (1 - r^{2}) / c_{\delta}$ when $\delta \leq |\theta |\leq \pi$ ,and the third property of good kernels is verified. Clearly $P_{r}(\theta)\geq 0$ ,and integrating the expression (4) term by term (which is justified by the absolute convergence of the series) yields

因此当 $\delta \leq |\theta |\leq \pi$ 时 $P_{r}(\theta)\leq (1 - r^{2}) / c_{\delta}$，并且好核的第三个性质被验证。显然 $P_{r}(\theta)\geq 0$，并且逐项积分表达式(4)（由级数的绝对收敛性证明）得到

$$\frac{1}{2\pi}\int_{-\pi}^{\pi}P_{r}(\theta)d\theta = 1,$$

thereby concluding the proof that $P_{r}$ is a good kernel.

从而完成了 $P_{r}$ 是好核的证明。

Combining this lemma with Theorem 4.1, we obtain our next result.

将此引理与定理4.1结合，我们得到下一个结果。

Theorem 5.6 The Fourier series of an integrable function on the circle is Abel summable to $f$ at every point of continuity. Moreover, if $f$ is continuous on the circle, then the Fourier series of $f$ is uniformly Abel summable to $f$ .

定理5.6 圆周上可积函数的傅里叶级数在其每个连续点处阿贝尔可和到 $f$。此外，如果 $f$ 在圆周上连续，那么 $f$ 的傅里叶级数一致阿贝尔可和到 $f$。

We now return to a problem discussed in Chapter 1, where we sketched the solution of the steady- state heat equation $\Delta u = 0$ in the unit disc with boundary condition $u = f$ on the circle. We expressed the Laplacian in terms of polar coordinates, separated variables, and expected that a solution was given by

现在我们回到第一章讨论过的一个问题，在那里我们概述了单位圆盘中稳态热传导方程 $\Delta u = 0$ 的解，边界条件为圆上 $u = f$。我们用极坐标表示了拉普拉斯算子，分离了变量，并期望解由下式给出

$$u(r,\theta) = \sum_{m = -\infty}^{\infty}a_{m}r^{|m|}e^{im\theta}, \quad (5)$$

where $a_{m}$ was the $m^{\mathrm{th}}$ Fourier coefficient of $f$ . In other words, we were led to take

其中 $a_{m}$ 是 $f$ 的第 $m$ 个傅里叶系数。换句话说，我们被引导取

$$u(r,\theta) = A_{r}(f)(\theta) = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(\phi)P_{r}(\theta -\phi)d\phi .$$

We are now in a position to show that this is indeed the case.

我们现在能够证明情况确实如此。

Theorem 5.7 Let $f$ be an integrable function defined on the unit circle. Then the function $u$ defined in the unit disc by the Poisson integral

定理5.7 设 $f$ 是定义在单位圆周上的一个可积函数。那么由泊松积分在单位圆盘中定义的函数 $u$

$$u(r,\theta) = (f*P_r)(\theta) \quad (6)$$

has the following properties:

具有以下性质：

(i) $u$ has two continuous derivatives in the unit disc and satisfies $\Delta u = 0$ .

(i) $u$ 在单位圆盘内具有两个连续导数，并满足 $\Delta u = 0$。

(ii) If $\theta$ is any point of continuity of $f$ , then

(ii) 如果 $\theta$ 是 $f$ 的任意一个连续点，那么

$$\lim_{r\to 1}u(r,\theta) = f(\theta).$$

If $f$ is continuous everywhere, then this limit is uniform.

如果 $f$ 处处连续，那么这个极限是一致的。

(iii) If $f$ is continuous, then $u(r,\theta)$ is the unique solution to the steady- state heat equation in the disc which satisfies conditions (i) and (ii).

(iii) 如果 $f$ 连续，那么 $u(r,\theta)$ 是圆盘中满足条件 (i) 和 (ii) 的稳态热传导方程的唯一解。

Proof. For (i), we recall that the function $u$ is given by the series (5). Fix $\rho < 1$ ; inside each disc of radius $r < \rho < 1$ centered at the origin, the series for $u$ can be differentiated term by term, and the differentiated series is uniformly and absolutely convergent. Thus $u$ can be differentiated twice (in fact infinitely many times), and since this holds for all $\rho < 1$ , we conclude that $u$ is twice differentiable inside the unit disc. Moreover, in polar coordinates,

证明。对于 (i)，我们回顾函数 $u$ 由级数 (5) 给出。固定 $\rho < 1$；在每个以原点为中心、半径 $r < \rho < 1$ 的圆盘内，$u$ 的级数可以逐项微分，并且微分后的级数是一致且绝对收敛的。因此 $u$ 可以微分两次（实际上是无限多次），并且由于这对所有 $\rho < 1$ 成立，我们得出结论 $u$ 在单位圆盘内是两次可微的。此外，在极坐标中，

$$\Delta u = \frac{\partial^2u}{\partial r^2} +\frac{1}{r}\frac{\partial u}{\partial r} +\frac{1}{r^2}\frac{\partial^2u}{\partial\theta^2},$$

so term by term differentiation shows that $\Delta u = 0$ .

因此逐项微分表明 $\Delta u = 0$。

The proof of (ii) is a simple application of the previous theorem.

(ii) 的证明是前一个定理的简单应用。

To prove (iii) we argue as follows. Suppose $v$ solves the steady- state heat equation in the disc and converges to $f$ uniformly as $r$ tends to 1 from below. For each fixed $r$ with $0 < r < 1$ , the function $v(r,\theta)$ has a Fourier series

为了证明 (iii)，我们如下论证。假设 $v$ 在圆盘中解稳态热传导方程，并且当 $r$ 从下方趋于 1 时一致收敛到 $f$。对每个固定的 $0 < r < 1$，函数 $v(r,\theta)$ 有一个傅里叶级数

$$\sum_{n = -\infty}^{\infty}a_{n}(r)e^{in\theta}\quad \mathrm{where}\quad a_{n}(r) = \frac{1}{2\pi}\int_{-\pi}^{\pi}v(r,\theta)e^{-in\theta}d\theta .$$

Taking into account that $v(r,\theta)$ solves the equation

考虑到 $v(r,\theta)$ 解方程

$$\frac{\partial^2v}{\partial r^2} +\frac{1}{r}\frac{\partial v}{\partial r} +\frac{1}{r^2}\frac{\partial^2v}{\partial\theta^2} = 0, \quad (7)$$

we find that

我们发现

$$a_n''(r) + \frac{1}{r} a_n'(r) - \frac{n^2}{r^2} a_n(r) = 0.$$

Indeed, we may first multiply (7) by $e^{- in\theta}$ and integrate in $\theta$ . Then, since $v$ is periodic, two integrations by parts give

事实上，我们可以先将 (7) 乘以 $e^{- in\theta}$ 并在 $\theta$ 上积分。然后，由于 $v$ 是周期的，两次分部积分给出

$$\frac{1}{2\pi}\int_{-\pi}^{\pi}\frac{\partial^2v}{\partial\theta^2} (r,\theta)e^{-in\theta}d\theta = -n^2a_n(r).$$

Finally, we may interchange the order of differentiation and integration, which is permissible since $v$ has two continuous derivatives; this yields (8).

最后，我们可以交换微分和积分的顺序，这是允许的，因为 $v$ 有两个连续导数；这得到 (8)。

Therefore, we must have $a_{n}(r) = A_{n}r^{n} + B_{n}r^{- n}$ for some constants $A_{n}$ and $B_{n}$ , when $n\neq 0$ (see Exercise 11 in Chapter 1). To evaluate the constants, we first observe that each term $a_{n}(r)$ is bounded because $v$ is bounded, therefore $B_{n} = 0$ . To find $A_{n}$ we let $r\rightarrow 1$ . Since $v$ converges uniformly to $f$ as $r\rightarrow 1$ we find that

因此，当 $n\neq 0$ 时，我们必须有 $a_{n}(r) = A_{n}r^{n} + B_{n}r^{- n}$，其中 $A_{n}$ 和 $B_{n}$ 是某个常数（见第一章练习11）。为了计算这些常数，我们首先观察到每个项 $a_{n}(r)$ 是有界的，因为 $v$ 是有界的，因此 $B_{n} = 0$。为了找到 $A_{n}$，我们令 $r\rightarrow 1$。由于当 $r\rightarrow 1$ 时 $v$ 一致收敛到 $f$，我们发现

$$A_{n} = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(\theta)e^{-in\theta}d\theta .$$

By a similar argument, this formula also holds when $n = 0$ . Our conclusion is that for each $0< r< 1$ , the Fourier series of $v$ is given by the series of $u(r,\theta)$ , so by the uniqueness of Fourier series for continuous functions, we must have $u = v$ .

通过类似的论证，当 $n = 0$ 时这个公式也成立。我们的结论是，对每个 $0< r< 1$，$v$ 的傅里叶级数由 $u(r,\theta)$ 的级数给出，因此根据连续函数傅里叶级数的唯一性，我们必须有 $u = v$。

Remark. By part (iii) of the theorem, we may conclude that if $u$ solves $\triangle u = 0$ in the disc, and converges to 0 uniformly as $r\rightarrow 1$ , then $u$ must be identically 0. However, if uniform convergence is replaced by pointwise convergence, this conclusion may fail; see Exercise 18.

注记。根据定理的第 (iii) 部分，我们可以得出结论：如果 $u$ 在圆盘中解 $\triangle u = 0$，并且当 $r\rightarrow 1$ 时一致收敛到 0，那么 $u$ 必须恒为 0。然而，如果一致收敛被逐点收敛所取代，这个结论可能不成立；见练习18。

---

## 6 Exercises

## 6 练习

1. Suppose $f$ is $2\pi$ -periodic and integrable on any finite interval. Prove that if $a,b\in \mathbb{R}$ , then

2. 假设 $f$ 是 $2\pi$ 周期的，并且在任何有限区间上可积。证明如果 $a,b\in \mathbb{R}$，那么

$$\int_{a}^{b}f(x)dx = \int_{a + 2\pi}^{b + 2\pi}f(x)dx = \int_{a - 2\pi}^{b - 2\pi}f(x)dx.$$

Also prove that

并证明

$$\int_{-\pi}^{\pi}f(x + a)dx = \int_{-\pi}^{\pi}f(x)dx = \int_{-\pi +\alpha}^{\pi +\alpha}f(x)dx.$$

2. In this exercise we show how the symmetries of a function imply certain properties of its Fourier coefficients. Let $f$ be a $2\pi$ - periodic Riemann integrable function defined on $\mathbb{R}$ .

3. 在本练习中，我们展示函数的对称性如何暗示其傅里叶系数的某些性质。设 $f$ 是定义在 $\mathbb{R}$ 上的一个 $2\pi$ 周期黎曼可积函数。

(a) Show that the Fourier series of the function $f$ can be written as

(a) 证明函数 $f$ 的傅里叶级数可以写成

$$f(\theta)\sim \hat{f} (0) + \sum_{n\geq 1}[\hat{f} (n) + \hat{f} (-n)]\cos n\theta +i[\hat{f} (n) - \hat{f} (-n)]\sin n\theta .$$

(b) Prove that if $f$ is even, then $\hat{f} (n) = \hat{f} (-n)$ , and we get a cosine series.

(b) 证明如果 $f$ 是偶函数，那么 $\hat{f} (n) = \hat{f} (-n)$，并且我们得到一个余弦级数。

(c) Prove that if $f$ is odd, then $\hat{f} (n) = -\hat{f} (-n)$ , and we get a sine series.

(c) 证明如果 $f$ 是奇函数，那么 $\hat{f} (n) = -\hat{f} (-n)$，并且我们得到一个正弦级数。

(d) Suppose that $f(\theta +\pi) = f(\theta)$ for all $\theta \in \mathbb{R}$ . Show that $\hat{f} (n) = 0$ for all odd $n$ .

(d) 假设对所有 $\theta \in \mathbb{R}$ 有 $f(\theta +\pi) = f(\theta)$。证明对所有奇数 $n$ 有 $\hat{f} (n) = 0$。

(e) Show that $f$ is real-valued if and only if $\overline{f(n)} = \hat{f} (-n)$ for all $n$ .

(e) 证明 $f$ 是实值的当且仅当对所有 $n$ 有 $\overline{f(n)} = \hat{f} (-n)$。

3. We return to the problem of the plucked string discussed in Chapter 1. Show that the initial condition $f$ is equal to its Fourier sine series

4. 我们回到第一章讨论的拨弦问题。证明初始条件 $f$ 等于其傅里叶正弦级数

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx\quad \mathrm{with}\quad A_{m} = \frac{2h}{m^{2}}\frac{\sin mp}{p(\pi -p)}.$$

Hint: Note that $|A_{m}|\leq C / m^{2}$ .

提示：注意 $|A_{m}|\leq C / m^{2}$。

4. Consider the $2\pi$ - periodic odd function defined on $[0,\pi ]$ by $f(\theta) = \theta (\pi - \theta)$ .

5. 考虑定义在 $[0,\pi ]$ 上的 $2\pi$ 周期奇函数 $f(\theta) = \theta (\pi - \theta)$。

(a) Draw the graph of $f$ .

(a) 画出 $f$ 的图形。

(b) Compute the Fourier coefficients of $f$ , and show that

(b) 计算 $f$ 的傅里叶系数，并证明

$$f(\theta) = \frac{8}{\pi}\sum_{k\mathrm{~odd~}\geq 1}\frac{\sin k\theta}{k^{3}}.$$

5. On the interval $[-\pi ,\pi ]$ consider the function

6. 在区间 $[-\pi ,\pi ]$ 上考虑函数

$$f(\theta) = \begin{cases} 1 - \frac{|\theta|}{\delta} & \text{if } |\theta| \le \delta \\ 0 & \text{if } \delta \le |\theta| \le \pi \end{cases}$$

Thus the graph of $f$ has the shape of a triangular tent. Show that

因此 $f$ 的图形具有三角形帐篷的形状。证明

$$f(\theta) = \frac{\delta}{2\pi} +2\sum_{n = 1}^{\infty}\frac{1 - \cos n\delta}{n^{2}\pi\delta}\cos n\theta .$$

6. Let $f$ be the function defined on $[-\pi ,\pi ]$ by $f(\theta) = |\theta |$ .设 $f$ 是定义在 $[-\pi ,\pi ]$ 上的函数，$f(\theta) = |\theta |$。

(a) Draw the graph of $f$ .

(a) 画出 $f$ 的图形。

(b) Calculate the Fourier coefficients of $f$ , and show that

(b) 计算 $f$ 的傅里叶系数，并证明

$$\hat{f}(n) = \begin{cases} \frac{\pi}{2} & n=0 \\ \frac{(-1)^n -1}{\pi n^2} & n\neq 0 \end{cases}$$

(c) What is the Fourier series of $f$ in terms of sines and cosines?

(c) $f$ 的正弦和余弦形式的傅里叶级数是什么？

(d) Taking $\theta = 0$ , prove that

(d) 取 $\theta = 0$，证明

$$\sum_{n\mathrm{~odd~}\geq 1}\frac{1}{n^2} = \frac{\pi^2}{8}\quad \mathrm{and}\quad \sum_{n = 1}^{\infty}\frac{1}{n^2} = \frac{\pi^2}{6}.$$

See also Example 2 in Section 1.1.

另见1.1节中的例2。

7. Suppose $\{a_{n}\}_{n = 1}^{N}$ and $\{b_{n}\}_{n = 1}^{N}$ are two finite sequences of complex numbers. Let $B_{k} = \sum_{n = 1}^{k}b_{n}$ denote the partial sums of the series $\sum b_{n}$ with the convention $B_{0} = 0$ .

8. 假设 $\{a_{n}\}_{n = 1}^{N}$ 和 $\{b_{n}\}_{n = 1}^{N}$ 是两个有限的复数序列。令 $B_{k} = \sum_{n = 1}^{k}b_{n}$ 表示级数 $\sum b_{n}$ 的部分和，约定 $B_{0} = 0$。

(a) Prove the summation by parts formula

(a) 证明分部求和公式

$$\sum_{n = M}^{N}a_{n}b_{n} = a_{N}B_{N} - a_{M}B_{M - 1} - \sum_{n = M}^{N - 1}(a_{n + 1} - a_{n})B_{n}.$$

(b) Deduce from this formula Dirichlet's test for convergence of a series: if the partial sums of the series $\sum b_{n}$ are bounded, and $\{a_{n}\}$ is a sequence of real numbers that decreases monotonically to 0, then $\sum a_{n}b_{n}$ converges.

(b) 从这个公式推导出级数收敛的狄利克雷判别法：如果级数 $\sum b_{n}$ 的部分和有界，且 $\{a_{n}\}$ 是单调递减趋于 0 的实数序列，那么 $\sum a_{n}b_{n}$ 收敛。

8. Verify that $\frac{1}{2i}\sum_{n\neq 0}\frac{e^{inx}}{n}$ is the Fourier series of the $2\pi$ -periodic sawtooth function illustrated in Figure 6, defined by $f(0) = 0$ , and

 验证 $\frac{1}{2i}\sum_{n\neq 0}\frac{e^{inx}}{n}$ 是图6所示的 $2\pi$ 周期锯齿函数的傅里叶级数，该函数定义为 $f(0) = 0$，且

$$f(x) = \begin{cases} \frac{i(\pi+x)}{2} & -\pi \le x < 0 \\ 0 & x=0 \\ \frac{i(\pi-x)}{2} & 0 < x \le \pi \end{cases}$$

Note that this function is not continuous. Show that nevertheless, the series converges for every $x$ (by which we mean, as usual, that the symmetric partial sums of the series converge). In particular, the value of the series at the origin, namely 0, is the average of the values of $f(x)$ as $x$ approaches the origin from the left and the right.

注意这个函数不连续。证明尽管如此，该级数对每个 $x$ 收敛（按照惯例，我们指的是级数的对称部分和收敛）。特别地，该级数在原点的值，即 0，是 $f(x)$ 当 $x$ 从左边和右边趋近原点时的值的平均。

<center>Figure 6. The sawtooth function </center>

<center>图6. 锯齿函数</center>

Hint: Use Dirichlet's test for convergence of a series $\sum a_{n}b_{n}$ .

提示：使用级数收敛的狄利克雷判别法 $\sum a_{n}b_{n}$。

9. Let $f(x) = \chi_{[a,b]}(x)$ be the characteristic function of the interval $[a,b]\subset [- \pi ,\pi ]$ , that is,

10. 设 $f(x) = \chi_{[a,b]}(x)$ 是区间 $[a,b]\subset [- \pi ,\pi ]$ 的特征函数，即

$$\chi_{[a,b]}(x) = \begin{cases} 1 & \text{if } x\in[a,b] \\ 0 & \text{otherwise} \end{cases}$$

(a) Show that the Fourier series of $f$ is given by

(a) 证明 $f$ 的傅里叶级数由下式给出

$$f(x)\sim \frac{b - a}{2\pi} +\sum_{n\neq 0}\frac{e^{-in a} - e^{-in b}}{2\pi in} e^{inx}.$$

The sum extends over all positive and negative integers excluding 0.

该和遍及所有非零的正负整数。

(b) Show that if $a\neq - \pi$ or $b\neq \pi$ and $a\neq b$ , then the Fourier series does not converge absolutely for any $x$ . Hint: It suffices to prove that for many values of $n$ one has $|\sin n\theta_0|\geq c > 0$ where $\theta_0 = (b - a) / 2$ .

(b) 证明如果 $a\neq - \pi$ 或 $b\neq \pi$ 且 $a\neq b$，那么该傅里叶级数对任何 $x$ 都不绝对收敛。提示：只需证明对许多 $n$ 的值，有 $|\sin n\theta_0|\geq c > 0$，其中 $\theta_0 = (b - a) / 2$。

(c) However, prove that the Fourier series converges at every point $x$ . What happens if $a = - \pi$ and $b = \pi$ ?

(c) 然而，证明该傅里叶级数在每个点 $x$ 收敛。如果 $a = - \pi$ 且 $b = \pi$ 会发生什么？

10. Suppose $f$ is a periodic function of period $2\pi$ which belongs to the class $C^k$ . Show that

11. 假设 $f$ 是一个周期为 $2\pi$ 且属于 $C^k$ 类的周期函数。证明

$$\hat{f} (n) = O(1 / |n|^k)\quad \mathrm{as}|n|\to \infty .$$

This notation means that there exists a constant $C$ such $|\hat{f} (n)|\leq C / |n|^k$ . We could also write this as $|n|^k\hat{f} (n) = O(1)$ , where $O(1)$ means bounded. Hint: Integrate by parts.

这个记号意味着存在常数 $C$ 使得 $|\hat{f} (n)|\leq C / |n|^k$。我们也可以将其写作 $|n|^k\hat{f} (n) = O(1)$，其中 $O(1)$ 表示有界。提示：分部积分。

11. Suppose that $\{f_k\}_{k = 1}^{\infty}$ is a sequence of Riemann integrable functions on the interval $[0,1]$ such that

12. 假设 $\{f_k\}_{k = 1}^{\infty}$ 是区间 $[0,1]$ 上的一列黎曼可积函数，使得

$$\int_0^1 |f_k(x) - f(x)|dx\to 0\quad \mathrm{as}k\to \infty .$$

12. Prove that if a series of complex numbers $\sum c_{n}$ converges to $s$ , then $\sum c_{n}$ is Cesaro summable to $s$ . 
13. Hint: Assume  as  .

13. 证明如果一个复数项级数 $\sum c_{n}$ 收敛到 $s$，那么 $\sum c_{n}$ 是切萨罗可和到 $s$ 的。
14. 提示：假设 $s_{n} \to 0$ 当 $n \to \infty$。

14. The purpose of this exercise is to prove that Abel summability is stronger than the standard or Cesaro methods of summation.

15. 本练习的目的是证明阿贝尔可和性比标准或切萨罗求和法更强。

(a) Show that if the series $\sum_{n = 1}^{\infty}c_{n}$ of complex numbers converges to a finite limit $s$ , then the series is Abel summable to $s$ .  Hint: Why is it enough to prove the theorem when $s = 0$ ? Assuming $s = 0$ , show that if $s_{N} = c_{1} + \dots +c_{N}$ , then $\sum_{n = 1}^{N}c_{n}r^{n} = (1 - r)\sum_{n = 1}^{N}s_{n}r^{n} + s_{N}r^{N + 1}$ . Let $N\to \infty$ to show that

(a) 证明如果复数项级数 $\sum_{n = 1}^{\infty}c_{n}$ 收敛到有限极限 $s$，那么该级数是阿贝尔可和到 $s$ 的
提示：为什么在 $s = 0$ 时证明定理就够了？假设 $s = 0$，证明如果 $s_{N} = c_{1} + \dots +c_{N}$，那么 $\sum_{n = 1}^{N}c_{n}r^{n} = (1 - r)\sum_{n = 1}^{N}s_{n}r^{n} + s_{N}r^{N + 1}$。令 $N\to \infty$ 证明

$$\sum c_{n}r^{n} = (1 - r)\sum s_{n}r^{n}.$$

Finally, prove that the right- hand side converges to 0 as $r \to 1$ .]

最后，证明右边当 $r \to 1$ 时收敛到 0。]

(b) However, show that there exist series which are Abel summable, but that do not converge. 
Hint: Try  . What is the Abel limit of $\sum c_{n}?$ (c) Argue similarly to prove that if a series  is Cesaro summable to $\sigma$ , then it is Abel summable to $\sigma$ . 
Hint: Note that

(b) 然而，证明存在一些级数是阿贝尔可和的，但不收敛。
提示：尝试 $c_{n} = (-1)^{n}$。 的阿贝尔极限是什么？(c) 类似地论证，证明如果一个级数 $\sum_{n = 1}^{\infty}c_{n}$ 是切萨罗可和到  的，那么它是阿贝尔可和到  的。
提示：注意

$$\sum_{n = 1}^{\infty}c_{n}r^{n} = (1 - r)^{2}\sum_{n = 1}^{\infty}n\sigma_{n}r^{n},$$

and assume $\sigma = 0$ .]

并假设 $\sigma = 0$。]

(d) Give an example of a series that is Abel summable but not Cesaro summable. 
Hint: Try  . Note that if  is Cesaro summable, then  tends to 0. 

(d) 给出一个级数，它是阿贝尔可和的但不是切萨罗可和的。
提示：尝试 $c_{n} = (-1)^{n - 1}n$。注意如果  是切萨罗可和的，那么 $c_{n} / n$ 趋于 0。

The results above can be summarized by the following implications about series:

上述结果可以用关于级数的以下蕴含关系来总结：

$$\mathrm{convergent}\Longrightarrow \mathrm{Cesaro~summable}\Longrightarrow \mathrm{Abel~summable},$$

and the fact that none of the arrows can be reversed.

以及没有一个箭头可以反向的事实。

14. This exercise deals with a theorem of Tauber which says that under an additional condition on the coefficients $c_{n}$ , the above arrows can be reversed.

15. 本练习涉及陶伯的一个定理，该定理说，在对系数 $c_{n}$ 施加附加条件的情况下，上述箭头可以反向。

(a) If $\sum c_{n}$ is Cesaro summable to $\sigma$ and $c_{n} = o(1 / n)$ (that is, $n c_{n} \to 0$ ), then $\sum c_{n}$ converges to $\sigma$ . 
Hint:  .

(a) 如果 $\sum c_{n}$ 是切萨罗可和到 $\sigma$ 的，且 $c_{n} = o(1 / n)$（即 $n c_{n} \to 0$），那么 $\sum c_{n}$ 收敛到 $\sigma$。
提示：$s_{n} - \sigma_{n} = [(n - 1)c_{n} + \dots +c_{2}] / n$。
(b) The above statement holds if we replace Cesaro summable by Abel summable. 
Hint: Estimate the difference between  and  where  .

(b) 如果我们用阿贝尔可和替换切萨罗可和，上述陈述仍然成立。 
提示：估计 $\sum_{n = 1}^{N}c_{n}$ 和 $\sum_{n = 1}^{N}c_{n}r^{n}$ 之间的差，其中 $r = 1 - 1 / N$。

15. Prove that the Fejer kernel is given by

16. 证明费耶核由下式给出

$$F_{N}(x) = \frac{1}{N}\frac{\sin^{2}(Nx / 2)}{\sin^{2}(x / 2)}.$$

Hint: Remember that $NF_{N}(x) = D_{0}(x) + \dots +D_{N - 1}(x)$ where $D_{n}(x)$ is the Dirichlet kernel. Therefore, if $\omega = e^{ix}$ we have

提示：记住 $NF_{N}(x) = D_{0}(x) + \dots +D_{N - 1}(x)$，其中 $D_{n}(x)$ 是狄利克雷核。因此，如果 $\omega = e^{ix}$，我们有

$$NF_{N}(x) = \sum_{n = 0}^{N - 1}\frac{\omega^{-n} - \omega^{n + 1}}{1 - \omega}.$$

16. The Weierstrass approximation theorem states: Let $f$ be a continuous function on the closed and bounded interval $[a,b]\subset \mathbb{R}$ .Then, for any $\epsilon >0$ there exists a polynomial $P$ such that

17. 魏尔斯特拉斯逼近定理指出：设 $f$ 是闭有界区间 $[a,b]\subset \mathbb{R}$ 上的一个连续函数。那么，对任意 $\epsilon >0$，存在一个多项式 $P$ 使得

$$\sup_{x\in [a,b]}|f(x) - P(x)|< \epsilon .$$

Prove this by applying Corollary 5.4 of Fejer's theorem and using the fact that the exponential function $e^{ix}$ can be approximated by polynomials uniformly on any interval.

通过应用费耶定理的推论5.4，并利用指数函数 $e^{ix}$ 可以在任何区间上被多项式一致逼近这一事实来证明这一点。

17. In Section 5.4 we proved that the Abel means of $f$ converge to $f$ at all points of continuity, that is,

18. 在5.4节中，我们证明了 $f$ 的阿贝尔平均在其所有连续点处收敛到 $f$，即

$$\lim_{r\to 1}A_{r}(f)(\theta) = \lim_{r\to 1}(P_{r}*f)(\theta) = f(\theta),\quad \mathrm{with~}0< r< 1,$$

whenever $f$ is continuous at $\theta$ .In this exercise, we will study the behavior of $A_{r}(f)(\theta)$ at certain points of discontinuity.

只要 $f$ 在 $\theta$ 处连续。在本练习中，我们将研究 $A_{r}(f)(\theta)$ 在某些间断点处的行为。

An integrable function is said to have a jump discontinuity at $\theta$ if the two limits

一个可积函数被称为在 $\theta$ 处有一个跳跃间断点，如果两个极限

$$\lim_{h\to 0\atop h > 0}f(\theta +h) = f(\theta^{+})\quad \mathrm{and}\quad \lim_{h\to 0\atop h > 0}f(\theta -h) = f(\theta^{-})$$

exist.

存在。

(a) Prove that if $f$ has a jump discontinuity at $\theta$ , then

(a) 证明如果 $f$ 在 $\theta$ 处有一个跳跃间断点，那么

$$\lim_{r\to 1}A_{r}(f)(\theta) = \frac{f(\theta^{+}) + f(\theta^{-})}{2},\quad \mathrm{with~}0\leq r< 1.$$

【Hint: Explain why  then modify the proof given in the text.】

【提示：解释为什么 $\begin{array}{r}{\frac{1}{2\pi}\int_{-\pi}^{0}P_{r}(\theta)d\theta = \frac{1}{2\pi}\int_{0}^{\pi}P_{r}(\theta)d\theta = \frac{1}{2}} \end{array}$，然后修改文中给出的证明。】

(b) Using a similar argument, show that if $f$ has a jump discontinuity at $\theta$ the Fourier series of $f$ at $\theta$ is Cesaro summable to $\frac{f(\theta^{+}) + f(\theta^{-})}{2}$ .

(b) 使用类似的论证，证明如果 $f$ 在 $\theta$ 处有一个跳跃间断点，那么 $f$ 的傅里叶级数在 $\theta$ 处是切萨罗可和到 $\frac{f(\theta^{+}) + f(\theta^{-})}{2}$ 的。

18. If $P_{r}(\theta)$ denotes the Poisson kernel, show that the function

19. 如果 $P_{r}(\theta)$ 表示泊松核，证明函数

$$u(r,\theta) = \frac{\partial P_r}{\partial\theta},$$

defined for $0\leq r< 1$ and $\theta \in \mathbb{R}$ satisfies:

对于 $0\leq r< 1$ 和 $\theta \in \mathbb{R}$ 定义，满足：

(i) $\Delta u = 0$ in the disc. (ii) $\lim_{r\to 1}u(r,\theta) = 0$ for each $\theta$

(i) 在圆盘中 $\Delta u = 0$。(ii) 对每个 $\theta$ 有 $\lim_{r\to 1}u(r,\theta) = 0$

However, $u$ is not identically zero.

然而，$u$ 不恒为零。

19. Solve Laplace's equation $\Delta u = 0$ in the semi infinite strip

20. 在半无限长条带中求解拉普拉斯方程 $\Delta u = 0$

$$S = \{(x,y):0< x< 1,0< y\} ,$$

subject to the following boundary conditions

满足以下边界条件

$$u(x,0) = f(x), \quad u(0,y) = 0, \quad u(1,y) = 0,$$

where $f$ is a given function, with of course $f(0) = f(1) = 0$ . Write

其中 $f$ 是一个给定的函数，当然有 $f(0) = f(1) = 0$。写

$$f(x) = \sum_{n = 1}^{\infty}a_{n}\sin (n\pi x)$$

and expand the general solution in terms of the special solutions given by

并将通解展开为由下式给出的特解的线性组合

$$u_{n}(x,y) = e^{-n\pi y}\sin (n\pi x).$$

Express $u$ as an integral involving $f$ , analogous to the Poisson integral formula (6).

将 $u$ 表示为涉及 $f$ 的积分，类似于泊松积分公式 (6)。

20. Consider the Dirichlet problem in the annulus defined by $\{(r,\theta):\rho < r< 1\}$ where $0< \rho < 1$ is the inner radius. The problem is to solve

21. 考虑由 $\{(r,\theta):\rho < r< 1\}$ 定义的环域中的狄利克雷问题，其中 $0< \rho < 1$ 是内半径。问题是求解

$$\frac{\partial^2u}{\partial r^2} +\frac{1}{r}\frac{\partial u}{\partial r} +\frac{1}{r^2}\frac{\partial^2u}{\partial\theta^2} = 0$$

subject to the boundary conditions

满足边界条件

$$u(1,\theta) = f(\theta), \quad u(\rho,\theta) = g(\theta),$$

where $f$ and $g$ are given continuous functions.

其中 $f$ 和 $g$ 是给定的连续函数。

Arguing as we have previously for the Dirichlet problem in the disc, we can hope to write

像我们之前对圆盘中的狄利克雷问题那样论证，我们可以希望写

$$u(r,\theta) = \sum c_n(r)e^{in\theta}$$

with $c_{n}(r) = A_{n}r^{n} + B_{n}r^{- n}$ $n\neq 0$ .Set

其中 $c_{n}(r) = A_{n}r^{n} + B_{n}r^{- n}$，$n\neq 0$。设

$$f(\theta)\sim \sum a_{n}e^{in\theta}\qquad \mathrm{and}\qquad g(\theta)\sim \sum b_{n}e^{in\theta}.$$

We want $c_{n}(1) = a_{n}$ and $c_{n}(\rho) = b_{n}$ . This leads to the solution

我们希望 $c_{n}(1) = a_{n}$ 且 $c_{n}(\rho) = b_{n}$。这导致解

$$u(r,\theta) = \sum_{n\neq 0}\left(\frac{1}{\rho^n - \rho^{-n}}\right)\left[((\rho / r)^n - (r / \rho)^n)a_n + (r^n - r^{-n})b_n\right]e^{in\theta}$$ $$+a_0 + (b_0 - a_0)\frac{\log r}{\log\rho}.$$

Show that as a result we have

证明结果我们有

$$u(r,\theta) - (P_{r}*f)(\theta)\to 0\quad \mathrm{as} r\to 1\mathrm{~uniformly~in~}\theta ,$$

and

以及

$$u(r,\theta) - (P_{\rho /r}*g)(\theta)\to 0\quad \mathrm{as} r\to \rho \mathrm{~uniformly~in~}\theta .$$

---

## 7 Problems

## 7 问题

1. One can construct Riemann integrable functions on $[0,1]$ that have a dense set of discontinuities as follows.

2. 可以如下构造在 $[0,1]$ 上具有稠密间断点集的黎曼可积函数。

(a) Let $f(x) = 0$ when $x< 0$ , and $f(x) = 1$ if $x\geq 0$ . Choose a countable dense sequence $\{r_n\}$ in $[0,1]$ . Then, show that the function

(a) 设当 $x< 0$ 时 $f(x) = 0$，如果 $x\geq 0$ 则 $f(x) = 1$。在 $[0,1]$ 中选择一个可数的稠密序列 $\{r_n\}$。然后证明函数

$$F(x) = \sum_{n = 1}^{\infty}\frac{1}{n^2} f(x - r_n)$$

is integrable and has discontinuities at all points of the sequence $\{r_n\}$ . 【Hint:  is monotonic and bounded.】

是可积的，并且在序列 $\{r_n\}$ 的所有点处有间断点。【提示： 是单调且有界的。】

(b) Consider next

(b) 接下来考虑

$$F(x) = \sum_{n = 1}^{\infty}3^{-n}g(x - r_n),$$

where $g(x) = \sin 1 / x$ when $x\neq 0$ , and $g(0) = 0$ . Then $F$ is integrable, discontinuous at each $x = r_n$ , and fails to be monotonic in any subinterval of $[0,1]$ . 【Hint: Use the fact that  .】

其中当 $x\neq 0$ 时 $g(x) = \sin 1 / x$，且 $g(0) = 0$。那么 $F$ 是可积的，在每个 $x = r_n$ 处不连续，并且在 $[0,1]$ 的任何子区间上都不是单调的。【提示：利用 $3^{- k} > \sum_{n > k}3^{- n}$ 这一事实。】

(c) The original example of Riemann is the function

(c) 黎曼最初的例子是函数

$$F(x) = \sum_{n = 1}^{\infty}\frac{(nx)}{n^2},$$

where $(x) = x$ for $x\in (- 1 / 2,1 / 2]$ and $(x)$ is continued to $\mathbb{R}$ by periodicity, that is, $(x + 1) = (x)$ . It can be shown that $F$ is discontinuous whenever $x = m / 2n$ , where $m,n\in \mathbb{Z}$ with $m$ odd and $n\neq 0$ .

其中对于 $x\in (- 1 / 2,1 / 2]$ 有 $(x) = x$，并且 $(x)$ 通过周期性延拓到 $\mathbb{R}$，即 $(x + 1) = (x)$。可以证明，只要 $x = m / 2n$，其中 $m,n\in \mathbb{Z}$，$m$ 为奇数且 $n\neq 0$，$F$ 就不连续。

2. Let $D_{N}$ denote the Dirichlet kernel

3. 设 $D_{N}$ 表示狄利克雷核

$$D_{N}(\theta) = \sum_{k = -N}^{N}e^{ik\theta} = \frac{\sin((N + 1 / 2)\theta)}{\sin(\theta / 2)},$$

and define
$$L_{N} = \frac{1}{2\pi}\int_{-\pi}^{\pi}|D_{N}(\theta)|d\theta .$$
(a) Prove that
$$L_{N}\geq c\log N$$
for some constant $c > 0$ . 【Hint: Show that  , change variables, and prove that】


$$L_{N}\geq c\int_{\pi}^{N\pi}\frac{|\sin\theta|}{|\theta|} d\theta +O(1).$$

Write the integral as a sum $\sum_{k = 1}^{N - 1}\int_{k\pi}^{(k + 1)\pi}$ . To conclude, use the fact that $\sum_{k = 1}^{n}1 / k\geq c\log n$ . A more careful estimate gives

$$L_{N} = \frac{4}{\pi^{2}}\log N + O(1).$$

(b) Prove the following as a consequence: for each $n\geq 1$ , there exists a continuous function $f_{n}$ such that $|f_{n}|\leq 1$ and $|S_{n}(f_{n})(0)|\geq c^{\prime}\log n$ . {Hint: The function $g_{n}$ which is equal to 1 when $D_{n}$ is positive and $-1$ when $D_{n}$ is negative has the desired property but is not continuous. Approximate $g_{n}$ in the integral norm (in the sense of Lemma 3.2) by continuous functions $h_{k}$ satisfying $|h_{k}|\leq 1$ .}


3. \* Littlewood provided a refinement of Tauber's theorem:

4. \* 李特尔伍德给出了陶伯定理的一个精化：

(a) If $\sum c_{n}$ is Abel summable to $s$ and $c_{n} = O(1 / n)$ , then $\sum c_{n}$ converges to $s$ .
(b) As a consequence, if $\sum c_{n}$ is Cesaro summable to $s$ and $c_{n} = O(1 / n)$ , then $\sum c_{n}$ converges to $s$ .

(a) 如果 $\sum c_{n}$ 是阿贝尔可和到 $s$ 的且 $c_{n} = O(1 / n)$，那么 $\sum c_{n}$ 收敛到 $s$。
(b) 因此，如果 $\sum c_{n}$ 是切萨罗可和到 $s$ 的且 $c_{n} = O(1 / n)$，那么 $\sum c_{n}$ 收敛到 $s$。

These results may be applied to Fourier series. By Exercise 17, they imply that if $f$ is an integrable function that satisfies $\hat{f} (\nu) = O(1 / |\nu |)$ , then:

这些结果可以应用于傅里叶级数。由练习17，它们意味着如果 $f$ 是一个可积函数，且满足 $\hat{f} (\nu) = O(1 / |\nu |)$，那么：

(i) If $f$ is continuous at $\theta$ , then

(i) 如果 $f$ 在 $\theta$ 处连续，那么

$$S_{N}(f)(\theta)\rightarrow f(\theta)\qquad \mathrm{as} N\rightarrow \infty .$$

(ii) If $f$ has a jump discontinuity at $\theta$ , then

(ii) 如果 $f$ 在 $\theta$ 处有一个跳跃间断点，那么

$$S_{N}(f)(\theta)\rightarrow \frac{f(\theta^{+}) + f(\theta^{-})}{2}\qquad \mathrm{as} N\rightarrow \infty .$$

(iii) If $f$ is continuous on $[-\pi ,\pi ]$ , then $S_{N}(f)\rightarrow f$ uniformly.

(iii) 如果 $f$ 在 $[-\pi ,\pi ]$ 上连续，那么 $S_{N}(f)\rightarrow f$ 一致收敛。

For the simpler assertion (b), hence a proof of (i), (ii), and (iii), see Problem 5 in Chapter 4.

对于较简单的断言 (b)，因此也是 (i)、(ii) 和 (iii) 的证明，见第四章问题5。