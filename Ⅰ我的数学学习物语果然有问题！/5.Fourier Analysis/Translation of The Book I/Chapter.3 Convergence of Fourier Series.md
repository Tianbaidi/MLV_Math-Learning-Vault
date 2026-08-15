---

---
---

===== Page 86 =====

3 Convergence of Fourier Series

The sine and cosine series, by which one can represent an arbitrary function in a given interval, enjoy among other remarkable properties that of being convergent. This property did not escape the great geometer (Fourier) who began, through the introduction of the representation of functions just mentioned, a new career for the applications of analysis; it was stated in the Memoir which contains his first research on heat. But no one so far, to my knowledge, gave a general proof of it ...

G.Dirichlet,1829

3 傅里叶级数的收敛性

正弦级数和余弦级数，可以用它们在一个给定区间内表示任意函数，除了其他显著性质外，还具有收敛性。这个性质没有逃过伟大的几何学家（傅里叶）的眼睛，他通过引入刚才提到的函数表示法，开启了分析学应用的新纪元；这一点在他包含关于热学的首次研究的回忆录中已有阐述。但据我所知，至今还没有人给出一个通用的证明……

G. 狄利克雷，1829年

In this chapter, we continue our study of the problem of convergence of Fourier series. We approach the problem from two different points of view.

在本章中，我们继续研究傅里叶级数的收敛性问题。我们将从两个不同的角度来探讨这个问题。

The first is "global" and concerns the overall behavior of a function $f$ over the entire interval $[0,2\pi]$ . The result we have in mind is "mean-square convergence": if $f$ is integrable on the circle, then

$$
\frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - S_N(f)(\theta)|^2 d\theta \to 0\quad \mathrm{as} N\to \infty .
$$

第一个是“全局”的，关注函数 $f$ 在整个区间 $[0,2\pi]$ 上的整体行为。我们想到的结果是“均方收敛”：如果 $f$ 在圆上是可积的，那么

$$
\frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - S_N(f)(\theta)|^2 d\theta \to 0\quad \mathrm{as} N\to \infty .
$$

At the heart of this result is the fundamental notion of "orthogonality"; this idea is expressed in terms of vector spaces with inner products, and their related infinite dimensional variants, the Hilbert spaces. A connected result is the Parseval identity which equates the mean-square "norm" of the function with a corresponding norm of its Fourier coefficients. Orthogonality is a fundamental mathematical notion which has many applications in analysis.

这个结果的核心是“正交性”的基本概念；这个概念通过带有内积的向量空间及其相关的无穷维变体——希尔伯特空间来表达。一个相关的结果是帕塞瓦尔恒等式，它将函数的均方“范数”与其傅里叶系数的相应范数等同起来。正交性是一个基本的数学概念，在分析学中有许多应用。

The second viewpoint is "local" and concerns the behavior of $f$ near a given point. The main question we consider is the problem of pointwise convergence: does the Fourier series of $f$ converge to the value $f(\theta)$ for a given $\theta$ ? We first show that this convergence does indeed hold whenever $f$ is differentiable at $\theta$ . As a corollary, we obtain the Riemann localization principle, which states that the question of whether or not $S_N(f)(\theta) \to f(\theta)$ is completely determined by the behavior of $f$ in an

第二个观点是“局部”的，关注 $f$ 在给定点附近的行为。我们考虑的主要问题是逐点收敛：对于给定的 $\theta$，$f$ 的傅里叶级数是否收敛到值 $f(\theta)$？我们首先证明，只要 $f$ 在 $\theta$ 处可微，这种收敛确实成立。作为推论，我们得到黎曼局部化原理，该原理指出 $S_N(f)(\theta) \to f(\theta)$ 是否成立完全由 $f$ 在

===== Page 87 =====

arbitrarily small interval about $\theta$ . This is a remarkable result since the Fourier coefficients, hence the Fourier series, of $f$ depend on the values of $f$ on the whole interval $[0, 2\pi]$ .Even though convergence of the Fourier series holds at points where $f$ is differentiable, it may fail if $f$ is merely continuous. The chapter concludes with the presentation of a continuous function whose Fourier series does not converge at a given point, as promised earlier.

$\theta$ 的任意小邻域内的行为完全决定。这是一个非凡的结果，因为 $f$ 的傅里叶系数，从而其傅里叶级数，依赖于 $f$ 在整个区间 $[0,2\pi]$ 上的值。尽管傅里叶级数在 $f$ 可微的点处收敛，但如果 $f$ 仅仅是连续的，则可能不收敛。本章最后，将按照之前的承诺，给出一个连续函数，其傅里叶级数在给定点不收敛的例子。

Even though convergence of the Fourier series holds at points where $f$ is differentiable, it may fail if $f$ is merely continuous. The chapter concludes with the presentation of a continuous function whose Fourier series does not converge at a given point, as promised earlier.

尽管傅里叶级数在 $f$ 可微的点处收敛，但如果 $f$ 仅仅是连续的，则可能不收敛。本章最后，将按照之前的承诺，给出一个连续函数，其傅里叶级数在给定点不收敛的例子。

## 1 Mean-square convergence of Fourier series

## 1 傅里叶级数的均方收敛

The aim of this section is the proof of the following theorem.

本节旨在证明以下定理。

Theorem 1.1 Suppose $f$ is integrable on the circle. Then

$$
\frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - S_N(f)(\theta)|^2 d\theta \to 0\quad as N\to \infty .
$$

定理 1.1 假设 $f$ 在圆上是可积的。那么

$$
\frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - S_N(f)(\theta)|^2 d\theta \to 0\quad as N\to \infty .
$$

As we remarked earlier, the key concept involved is that of orthogonality. The correct setting for orthogonality is in a vector space equipped with an inner product.

正如我们之前提到的，所涉及的关键概念是正交性。正交性的正确设定是在一个配备了内积的向量空间中。

### 1.1 Vector spaces and inner products

### 1.1 向量空间与内积

We now review the definitions of a vector space over $\mathbb{R}$ or $\mathbb{C}$ , an inner product, and its associated norm. In addition to the familiar finite- dimensional vector spaces $\mathbb{R}^d$ and $\mathbb{C}^d$ , we also examine two infinite- dimensional examples which play a central role in the proof of Theorem 1.1.

我们现在回顾一下在 $\mathbb{R}$ 或 $\mathbb{C}$ 上的向量空间、内积及其相关范数的定义。除了熟悉的有限维向量空间 $\mathbb{R}^d$ 和 $\mathbb{C}^d$ 之外，我们还将考察两个在定理 1.1 的证明中起核心作用的无穷维例子。

## Preliminaries on vector spaces

## 向量空间预备知识

A vector space $V$ over the real numbers $\mathbb{R}$ is a set whose elements may be "added" together, and "multiplied" by scalars. More precisely, we may associate to any pair $X,Y\in V$ an element in $V$ called their sum and denoted by $X + Y$ . We require that this addition respects the usual laws of arithmetic, such as commutativity $X + Y = Y + X$ , and associativity $X + (Y + Z) = (X + Y) + Z$ , etc. Also, given any $X\in V$ and real number $\lambda$ , we assign an element $\lambda X\in V$ called the product of $X$ by $\lambda$ . This scalar multiplication must satisfy the standard properties, for instance $\lambda_1(\lambda_2X) = (\lambda_1\lambda_2)X$ and $\lambda (X + Y) = \lambda X + \lambda Y$ . We may instead allow scalar multiplication by numbers in $\mathbb{C}$ ; we then say that $V$ is a vector space over the complex numbers.

实数集 $\mathbb{R}$ 上的向量空间 $V$ 是一个集合，其中的元素可以“相加”，并且可以“乘以”标量。更精确地说，对于任意一对元素 $X, Y \in V$，我们可以指定 $V$ 中的一个元素，称为它们的和，记为 $X + Y$。我们要求这种加法遵循通常的算术法则，例如交换律 $X + Y = Y + X$，结合律 $X + (Y + Z) = (X + Y) + Z$，等等。此外，给定任意 $X \in V$ 和实数 $\lambda$，我们指定一个元素 $\lambda X \in V$，称为 $X$ 与 $\lambda$ 的积。这种标量乘法必须满足标准性质，例如 $\lambda_1(\lambda_2X) = (\lambda_1\lambda_2)X$ 和 $\lambda (X + Y) = \lambda X + \lambda Y$。我们也可以允许用 $\mathbb{C}$ 中的数进行标量乘法；这时我们说 $V$ 是复数域上的向量空间。

===== Page 88 =====

For example, the set $\mathbb{R}^d$ of $d$ - tuples of real numbers $(x_{1},x_{2},\ldots ,x_{d})$ is a vector space over the reals. Addition is defined componentwise by

$$(x_{1},\ldots ,x_{d}) + (y_{1},\ldots ,y_{d}) = (x_{1} + y_{1},\ldots ,x_{d} + y_{d}),$$

and so is multiplication by a scalar $\lambda \in \mathbb{R}$

$$\lambda (x_{1},\ldots ,x_{d}) = (\lambda x_{1},\ldots ,\lambda x_{d}).$$

例如，由实数 $d$ 元组 $(x_{1},x_{2},\ldots ,x_{d})$ 组成的集合 $\mathbb{R}^d$ 是实数域上的向量空间。加法按分量定义为

$$(x_{1},\ldots ,x_{d}) + (y_{1},\ldots ,y_{d}) = (x_{1} + y_{1},\ldots ,x_{d} + y_{d}),$$

标量乘法也是按分量定义的，对于 $\lambda \in \mathbb{R}$

$$\lambda (x_{1},\ldots ,x_{d}) = (\lambda x_{1},\ldots ,\lambda x_{d}).$$

Similarly, the space $\mathbb{C}^d$ (the complex version of the previous example) is the set of $d$ - tuples of complex numbers $(z_{1},z_{2},\ldots ,z_{d})$ . It is a vector space over $\mathbb{C}$ with addition defined componentwise by

$$(z_{1},\ldots ,z_{d}) + (w_{1},\ldots ,w_{d}) = (z_{1} + w_{1},\ldots ,z_{d} + w_{d}).$$

Multiplication by scalars $\lambda \in \mathbb{C}$ is given by

$$\lambda (z_{1},\ldots ,z_{d}) = (\lambda z_{1},\ldots ,\lambda z_{d}).$$

类似地，空间 $\mathbb{C}^d$（前一个例子的复数版本）是由复数 $d$ 元组 $(z_{1},z_{2},\ldots ,z_{d})$ 组成的集合。它是复数域 $\mathbb{C}$ 上的向量空间，加法按分量定义为

$$(z_{1},\ldots ,z_{d}) + (w_{1},\ldots ,w_{d}) = (z_{1} + w_{1},\ldots ,z_{d} + w_{d}),$$

标量乘法对于 $\lambda \in \mathbb{C}$ 定义为

$$\lambda (z_{1},\ldots ,z_{d}) = (\lambda z_{1},\ldots ,\lambda z_{d}).$$

An inner product on a vector space $V$ over $\mathbb{R}$ associates to any pair $X,Y$ of elements in $V$ a real number which we denote by $(X,Y)$ . In particular, the inner product must be symmetric $(X,Y) = (Y,X)$ and linear in both variables; that is,

$$(\alpha X + \beta Y,Z) = \alpha (X,Z) + \beta (Y,Z)$$

whenever $\alpha ,\beta \in \mathbb{R}$ and $X,Y,Z\in V$ . Also, we require that the inner product be positive- definite, that is, $(X,X)\geq 0$ for all $X$ in $V$ . In particular, given an inner product $(\cdot ,\cdot)$ we may define the norm of $X$ by

$$\| X\| = (X,X)^{1 / 2}.$$

If in addition $\| X\| = 0$ implies $X = 0$ , we say that the inner product is strictly positive- definite.

实数域 $\mathbb{R}$ 上的向量空间 $V$ 上的内积为任意一对元素 $X,Y \in V$ 关联一个实数，记为 $(X,Y)$。特别地，内积必须是对称的 $(X,Y) = (Y,X)$ 并且在两个变量上都是线性的；即

$$(\alpha X + \beta Y,Z) = \alpha (X,Z) + \beta (Y,Z)$$

对所有 $\alpha ,\beta \in \mathbb{R}$ 和 $X,Y,Z\in V$ 成立。此外，我们要求内积是正定的，即对所有 $X \in V$ 有 $(X,X)\geq 0$。特别地，给定内积 $(\cdot ,\cdot)$，我们可以定义 $X$ 的范数为

$$\| X\| = (X,X)^{1 / 2}.$$

如果另外 $\| X\| = 0$ 蕴含 $X = 0$，我们就称这个内积是严格正定的。

For example, the space $\mathbb{R}^d$ is equipped with a (strictly positive- definite) inner product defined by

$$(X,Y) = x_{1}y_{1} + \dots +x_{d}y_{d}$$

when $X = (x_{1},\ldots ,x_{d})$ and $Y = (y_{1},\ldots ,y_{d})$ . Then

$$\| X\| = (X,X)^{1 / 2} = \sqrt{x_{1}^{2} + \dots +x_{d}^{2}},$$

例如，空间 $\mathbb{R}^d$ 配备了（严格正定的）内积，定义为

$$(X,Y) = x_{1}y_{1} + \dots +x_{d}y_{d}$$

其中 $X = (x_{1},\ldots ,x_{d})$ 和 $Y = (y_{1},\ldots ,y_{d})$。那么

$$\| X\| = (X,X)^{1 / 2} = \sqrt{x_{1}^{2} + \dots +x_{d}^{2}},$$

===== Page 89 =====

which is the usual Euclidean distance. One also uses the notation $|X|$ instead of $\| X\|$ .

这就是通常的欧几里得距离。有时也使用符号 $|X|$ 代替 $\| X\|$。

For vector spaces over the complex numbers, the inner product of two elements is a complex number. Moreover, these inner products are called Hermitian (instead of symmetric) since they must satisfy $(X,Y) = \overline{(Y,X)}$ . Hence the inner product is linear in the first variable, but conjugate- linear in the second:

$$(\alpha X + \beta Y,Z) = \alpha (X,Z) + \beta (Y,Z)\quad \mathrm{and}$$

$$(X,\alpha Y + \beta Z) = \overline{\alpha} (X,Y) + \overline{\beta} (X,Z).$$

Also, we must have $(X,X)\geq 0$ , and the norm of $X$ is defined by $\| X\| = (X,X)^{1 / 2}$ as before. Again, the inner product is strictly positive- definite if $\| X\| = 0$ implies $X = 0$ .

对于复数域上的向量空间，两个元素的内积是一个复数。此外，这些内积被称为埃尔米特内积（而不是对称的），因为它们必须满足 $(X,Y) = \overline{(Y,X)}$。因此内积对第一个变量是线性的，但对第二个变量是共轭线性的：

$$(\alpha X + \beta Y,Z) = \alpha (X,Z) + \beta (Y,Z)\quad \mathrm{and}$$

$$(X,\alpha Y + \beta Z) = \overline{\alpha} (X,Y) + \overline{\beta} (X,Z).$$

同时，我们必须有 $(X,X)\geq 0$，并且 $X$ 的范数仍然定义为 $\| X\| = (X,X)^{1 / 2}$。同样，如果 $\| X\| = 0$ 蕴含 $X = 0$，则内积是严格正定的。

For example, the inner product of two vectors $Z = (z_{1},\ldots ,z_{d})$ and $W = (w_{1},\ldots ,w_{d})$ in $\mathbb{C}^{d}$ is defined by

$$(Z,W) = z_{1}\overline{w_{1}} +\dots +z_{d}\overline{w_{d}}.$$

The norm of the vector $Z$ is then given by

$$\| Z\| = (Z,Z)^{1 / 2} = \sqrt{|z_1|^2 + \dots + |z_d|^2}.$$

例如，$\mathbb{C}^{d}$ 中两个向量 $Z = (z_{1},\ldots ,z_{d})$ 和 $W = (w_{1},\ldots ,w_{d})$ 的内积定义为

$$(Z,W) = z_{1}\overline{w_{1}} +\dots +z_{d}\overline{w_{d}}.$$

向量 $Z$ 的范数则为

$$\| Z\| = (Z,Z)^{1 / 2} = \sqrt{|z_1|^2 + \dots + |z_d|^2}.$$

The presence of an inner product on a vector space allows one to define the geometric notion of "orthogonality." Let $V$ be a vector space (over $\mathbb{R}$ or $\mathbb{C}$ ) with inner product $(\cdot ,\cdot)$ and associated norm $\| \cdot \|$ . Two elements $X$ and $Y$ are orthogonal if $(X,Y) = 0$ , and we write $X\perp Y$ . Three important results can be derived from this notion of orthogonality:

(i) The Pythagorean theorem: if $X$ and $Y$ are orthogonal, then

$$\| X + Y\| ^2 = \| X\| ^2 +\| Y\| ^2.$$

(ii) The Cauchy- Schwarz inequality: for any $X,Y\in V$ we have

$$\| (X,Y)\| \leq \| X\| \| Y\| .$$

(iii) The triangle inequality: for any $X,Y\in V$ we have

$$\| X + Y\| \leq \| X\| +\| Y\| .$$

向量空间上内积的存在允许我们定义“正交性”的几何概念。设 $V$ 是一个带有内积 $(\cdot ,\cdot)$ 和相关范数 $\| \cdot \|$ 的（实数或复数域上的）向量空间。如果 $(X,Y) = 0$，则两个元素 $X$ 和 $Y$ 是正交的，记作 $X\perp Y$。从这个正交性概念可以推导出三个重要结果：

(i) 勾股定理：如果 $X$ 和 $Y$ 正交，那么

$$\| X + Y\| ^2 = \| X\| ^2 +\| Y\| ^2.$$

(ii) 柯西-施瓦茨不等式：对于任意 $X,Y\in V$，有

$$\| (X,Y)\| \leq \| X\| \| Y\| .$$

(iii) 三角不等式：对于任意 $X,Y\in V$，有

$$\| X + Y\| \leq \| X\| +\| Y\| .$$

===== Page 90 =====

The proofs of these facts are simple. For (i) it suffices to expand $(X + Y,X + Y)$ and use the assumption that $(X,Y) = 0$ .

这些事实的证明很简单。对于 (i)，只需展开 $(X + Y,X + Y)$ 并利用 $(X,Y) = 0$ 的假设即可。

For (ii), we first dispose of the case when $\| Y\| = 0$ by showing that this implies $(X,Y) = 0$ for all $X$ . Indeed, for all real $t$ we have

$$0\leq \| X + tY\| ^2 = \| X\| ^2 +2t\operatorname {Re}(X,Y)$$

and $\operatorname {Re}(X,Y)\neq 0$ contradicts the inequality if we take $t$ to be large and positive (or negative). Similarly, by considering $\| X + itY\| ^2$ , we find that $\operatorname {Im}(X,Y) = 0$ .

对于 (ii)，我们首先处理 $\| Y\| = 0$ 的情况，通过证明这蕴含对所有 $X$ 有 $(X,Y) = 0$。事实上，对所有实数 $t$，有

$$0\leq \| X + tY\| ^2 = \| X\| ^2 +2t\operatorname {Re}(X,Y)$$

如果 $\operatorname {Re}(X,Y)\neq 0$，取 $t$ 很大且为正（或负）就会与不等式矛盾。类似地，通过考虑 $\| X + itY\| ^2$，我们发现 $\operatorname {Im}(X,Y) = 0$。

If $\| Y\| \neq 0$ , we may set $c = (X,Y) / (Y,Y)$ ; then $X - cY$ is orthogonal to $Y$ , and therefore also to $cY$ . If we write $X = X - cY + cY$ and apply the Pythagorean theorem, we get

$$\| X\| ^2 = \| X - cY\| ^2 +\| cY\| ^2 \geq |c|^2\| Y\| ^2.$$

Taking square roots on both sides gives the result. Note that we have equality in the above precisely when $X = cY$ .

如果 $\| Y\| \neq 0$，我们可以设 $c = (X,Y) / (Y,Y)$；那么 $X - cY$ 与 $Y$ 正交，因此也与 $cY$ 正交。如果我们写 $X = X - cY + cY$ 并应用勾股定理，得到

$$\| X\| ^2 = \| X - cY\| ^2 +\| cY\| ^2 \geq |c|^2\| Y\| ^2.$$

两边取平方根即得结果。注意，当 $X = cY$ 时，上述等式成立。

Finally, for (iii) we first note that

$$\| X + Y\| ^2 = (X,X) + (X,Y) + (Y,X) + (Y,Y).$$

But $(X,X) = \| X\| ^2$ , $(Y,Y) = \| Y\| ^2$ , and by the Cauchy- Schwarz inequality

$$|(X,Y) + (Y,X)|\leq 2\| X\|\| Y\| ,$$

therefore

$$\| X + Y\| ^2 \leq \| X\| ^2 + 2\| X\| \| Y\| + \| Y\| ^2 = (\| X\| + \| Y\|)^2.$$

最后，对于 (iii)，我们首先注意到

$$\| X + Y\| ^2 = (X,X) + (X,Y) + (Y,X) + (Y,Y).$$

但是 $(X,X) = \| X\| ^2$，$(Y,Y) = \| Y\| ^2$，并且根据柯西-施瓦茨不等式

$$|(X,Y) + (Y,X)|\leq 2\| X\|\| Y\| ,$$

因此

$$\| X + Y\| ^2 \leq \| X\| ^2 + 2\| X\| \| Y\| + \| Y\| ^2 = (\| X\| + \| Y\|)^2.$$

## Two important examples

## 两个重要的例子

The vector spaces $\mathbb{R}^d$ and $\mathbb{C}^d$ are finite dimensional. In the context of Fourier series, we need to work with two infinite- dimensional vector spaces, which we now describe.

向量空间 $\mathbb{R}^d$ 和 $\mathbb{C}^d$ 是有限维的。在傅里叶级数的背景下，我们需要处理两个无穷维向量空间，现描述如下。

EXAMPLE 1. The vector space $\ell^2 (\mathbb{Z})$ over $\mathbb{C}$ is the set of all (two- sided) infinite sequences of complex numbers

$$(\ldots ,a_{-n},\ldots ,a_{-1},a_0,a_1,\ldots ,a_n,\ldots)$$

such that

$$\sum_{n\in \mathbb{Z}}|a_n|^2 < \infty ;$$

例 1. 复数域 $\mathbb{C}$ 上的向量空间 $\ell^2 (\mathbb{Z})$ 是所有（双向）无穷复数列

$$(\ldots ,a_{-n},\ldots ,a_{-1},a_0,a_1,\ldots ,a_n,\ldots)$$

满足

$$\sum_{n\in \mathbb{Z}}|a_n|^2 < \infty ;$$

===== Page 91 =====

that is, the series converges. Addition is defined componentwise, and so is scalar multiplication. The inner product between the two vectors $A = (\ldots ,a_{- 1},a_0,a_1,\ldots)$ and $B = (\ldots ,b_{- 1},b_0,b_1,\ldots)$ is defined by the absolutely convergent series

$$(A,B) = \sum_{n\in \mathbb{Z}}a_n\overline{b_n}.$$

The norm of $A$ is then given by

$$\| A\| = (A,A)^{1 / 2} = \left(\sum_{n\in \mathbb{Z}}|a_n|^2\right)^{1 / 2}.$$

即该级数收敛。加法按分量定义，标量乘法亦然。两个向量 $A = (\ldots ,a_{- 1},a_0,a_1,\ldots)$ 和 $B = (\ldots ,b_{- 1},b_0,b_1,\ldots)$ 之间的内积由绝对收敛的级数定义

$$(A,B) = \sum_{n\in \mathbb{Z}}a_n\overline{b_n}.$$

那么 $A$ 的范数为

$$\| A\| = (A,A)^{1 / 2} = \left(\sum_{n\in \mathbb{Z}}|a_n|^2\right)^{1 / 2}.$$

We must first check that $\ell^2 (\mathbb{Z})$ is a vector space. This requires that if $A$ and $B$ are two elements in $\ell^2 (\mathbb{Z})$ , then so is the vector $A + B$ . To see this, for each integer $N > 0$ we let $A_N$ denote the truncated element

$$A_{N} = (\ldots ,0,0,a_{-N},\ldots ,a_{-1},a_{0},a_{1},\ldots ,a_{N},0,0,\ldots),$$

where we have set $a_{n} = 0$ whenever $|n| > N$ . We define the truncated element $B_N$ similarly. Then, by the triangle inequality which holds in a finite dimensional Euclidean space, we have

$$\| A_N + B_N\| \leq \| A_N\| +\| B_N\| \leq \| A\| +\| B\| .$$

Thus

$$\sum_{|n|\leq N}|a_n + b_n|^2\leq (\| A\| +\| B\|)^2,$$

and letting $N$ tend to infinity gives $\textstyle \sum_{n\in \mathbb{Z}}|a_{n} + b_{n}|^{2}< \infty$ . It also follows that $\| A + B\| \leq \| A\| +\| B\|$ , which is the triangle inequality. The Cauchy- Schwarz inequality, which states that the sum $\textstyle \sum_{n\in \mathbb{Z}}a_{n}\overline{b_{n}}$ converges absolutely and that $|(A,B)|\leq \| A\| \| B\|$ , can be deduced in the same way from its finite analogue.

我们首先必须验证 $\ell^2 (\mathbb{Z})$ 是一个向量空间。这需要证明如果 $A$ 和 $B$ 是 $\ell^2 (\mathbb{Z})$ 中的两个元素，那么向量 $A + B$ 也在 $\ell^2 (\mathbb{Z})$ 中。为了证明这一点，对于每个整数 $N > 0$，令 $A_N$ 表示截断后的元素

$$A_{N} = (\ldots ,0,0,a_{-N},\ldots ,a_{-1},a_{0},a_{1},\ldots ,a_{N},0,0,\ldots),$$

其中我们设定当 $|n| > N$ 时 $a_{n} = 0$。类似地定义截断后的元素 $B_N$。然后，根据有限维欧几里得空间中成立的三角不等式，我们有

$$\| A_N + B_N\| \leq \| A_N\| +\| B_N\| \leq \| A\| +\| B\| .$$

因此

$$\sum_{|n|\leq N}|a_n + b_n|^2\leq (\| A\| +\| B\|)^2,$$

令 $N \to \infty$ 得到 $\textstyle \sum_{n\in \mathbb{Z}}|a_{n} + b_{n}|^{2}< \infty$。由此也得到 $\| A + B\| \leq \| A\| +\| B\|$，即三角不等式。柯西-施瓦茨不等式，它指出 $\textstyle \sum_{n\in \mathbb{Z}}a_{n}\overline{b_{n}}$ 绝对收敛且 $|(A,B)|\leq \| A\| \| B\|$，同样可以通过其有限维版本推导出来。

In the three examples $\mathbb{R}^d$ $\mathbb{C}^d$ , and $\ell^2 (\mathbb{Z})$ , the vector spaces with their inner products and norms satisfy two important properties:

(i) The inner product is strictly positive-definite, that is, $\| X\| = 0$ implies $X = 0$ . (ii) The vector space is complete, which by definition means that every Cauchy sequence in the norm converges to a limit in the vector space.

在三个例子 $\mathbb{R}^d$、$\mathbb{C}^d$ 和 $\ell^2 (\mathbb{Z})$ 中，带有内积和范数的向量空间满足两个重要性质：

(i) 内积是严格正定的，即 $\| X\| = 0$ 蕴含 $X = 0$。(ii) 向量空间是完备的，根据定义，这意味着每个在范数意义下的柯西序列都收敛到向量空间中的一个极限。

===== Page 92 =====

An inner product space with these two properties is called a Hilbert space. We see that $\mathbb{R}^d$ and $\mathbb{C}^d$ are examples of finite- dimensional Hilbert spaces, while $\ell^2 (\mathbb{Z})$ is an example of an infinite- dimensional Hilbert space (see Exercises 1 and 2). If either of the conditions above fail, the space is called a pre- Hilbert space.

具有这两个性质的内积空间称为希尔伯特空间。我们看到 $\mathbb{R}^d$ 和 $\mathbb{C}^d$ 是有限维希尔伯特空间的例子，而 $\ell^2 (\mathbb{Z})$ 是无穷维希尔伯特空间的例子（见练习 1 和 2）。如果上述条件中任何一个不满足，该空间称为预希尔伯特空间。

We now give an important example of a pre- Hilbert space where both conditions (i) and (ii) fail.

现在我们给出一个预希尔伯特空间的重要例子，其中条件 (i) 和 (ii) 都不满足。

EXAMPLE 2. Let $\mathcal{R}$ denote the set of complex- valued Riemann integrable functions on $[0,2\pi ]$ (or equivalently, integrable functions on the circle). This is a vector space over $\mathbb{C}$ . Addition is defined pointwise by

$$(f + g)(\theta) = f(\theta) + g(\theta).$$

Naturally, multiplication by a scalar $\lambda \in \mathbb{C}$ is given by

$$(\lambda f)(\theta) = \lambda \cdot f(\theta).$$

An inner product is defined on this vector space by

$$(f,g) = \frac{1}{2\pi}\int_{0}^{2\pi}f(\theta)\overline{g(\theta)} d\theta . \quad (1)$$

The norm of $f$ is then

$$\| f\| = \left(\frac{1}{2\pi}\int_{0}^{2\pi}|f(\theta)|^{2}d\theta\right)^{1 / 2}.$$

例 2. 令 $\mathcal{R}$ 表示 $[0,2\pi]$ 上复值黎曼可积函数（或等价地，圆上的可积函数）的集合。这是复数域 $\mathbb{C}$ 上的一个向量空间。加法按点定义

$$(f + g)(\theta) = f(\theta) + g(\theta).$$

自然地，乘以标量 $\lambda \in \mathbb{C}$ 定义为

$$(\lambda f)(\theta) = \lambda \cdot f(\theta).$$

在这个向量空间上定义内积为

$$(f,g) = \frac{1}{2\pi}\int_{0}^{2\pi}f(\theta)\overline{g(\theta)} d\theta . \quad (1)$$

那么 $f$ 的范数为

$$\| f\| = \left(\frac{1}{2\pi}\int_{0}^{2\pi}|f(\theta)|^{2}d\theta\right)^{1 / 2}.$$

One needs to check that the analogue of the Cauchy- Schwarz and triangle inequalities hold in this example; that is, $|(f,g)|\leq \| f\| \| g\|$ and $\| f + g\| \leq \| f\| +\| g\|$ . While these facts can be obtained as consequences of the corresponding inequalities in the previous examples, the argument is a little elaborate and we prefer to proceed differently.

需要验证在这个例子中柯西-施瓦茨不等式和三角不等式的类似物是否成立；即 $|(f,g)|\leq \| f\| \| g\|$ 和 $\| f + g\| \leq \| f\| +\| g\|$。虽然这些事实可以作为前面例子中相应不等式的推论得到，但论证有点繁琐，我们更倾向于采用不同的方法。

We first observe that $2AB\leq (A^2 +B^2)$ for any two real numbers $A$ and $B$ . If we set $A = \lambda^{1 / 2}|f(\theta)|$ and $B = \lambda^{- 1 / 2}|g(\theta)|$ with $\lambda >0$ , we get

$$|f(\theta)\overline{g(\theta)} |\leq \frac{1}{2} (\lambda |f(\theta)|^2 +\lambda^{-1}|g(\theta)|^2).$$

We then integrate this in $\theta$ to obtain

$$|(f,g)|\leq \frac{1}{2\pi}\int_{0}^{2\pi}|f(\theta)|\overline{|g(\theta)|} d\theta \leq \frac{1}{2} (\lambda \| f\|^{2} + \lambda^{-1}\| g\|^{2}).$$

Then, put $\lambda = \| g\| /\| f\|$ to get the Cauchy- Schwarz inequality. The triangle inequality is then a simple consequence, as we have seen above.

我们首先注意到对于任意两个实数 $A$ 和 $B$，有 $2AB\leq (A^2 +B^2)$。设 $A = \lambda^{1 / 2}|f(\theta)|$ 和 $B = \lambda^{- 1 / 2}|g(\theta)|$，其中 $\lambda >0$，得到

$$|f(\theta)\overline{g(\theta)} |\leq \frac{1}{2} (\lambda |f(\theta)|^2 +\lambda^{-1}|g(\theta)|^2).$$

然后对 $\theta$ 积分得到

$$|(f,g)|\leq \frac{1}{2\pi}\int_{0}^{2\pi}|f(\theta)|\overline{|g(\theta)|} d\theta \leq \frac{1}{2} (\lambda \| f\|^{2} + \lambda^{-1}\| g\|^{2}).$$

然后，令 $\lambda = \| g\| /\| f\|$ 即得柯西-施瓦茨不等式。如上所见，三角不等式是其简单推论。

===== Page 93 =====

Of course, in our choice of $\lambda$ we must assume that $\| f\| \neq 0$ and $\| g\| \neq 0$ which leads us to the following observation.

当然，在我们选择 $\lambda$ 时，必须假设 $\| f\| \neq 0$ 和 $\| g\| \neq 0$，这引出了以下观察。

In $\mathcal{R}$ , condition (i) for a Hilbert space fails, since $\| f\| = 0$ implies only that $f$ vanishes at its points of continuity. This is not a very serious problem since in the appendix we show that an integrable function is continuous except for a "negligible" set, so that $\| f\| = 0$ implies that $f$ vanishes except on a set of "measure zero." One can get around the difficulty that $f$ is not identically zero by adopting the convention that such functions are actually the zero function, since for the purpose of integration, $f$ behaves precisely like the zero function.

在 $\mathcal{R}$ 中，希尔伯特空间的条件 (i) 不成立，因为 $\| f\| = 0$ 只意味着 $f$ 在其连续点处为零。这不是一个非常严重的问题，因为在附录中我们证明了一个可积函数除了一个“可忽略”的集合外是连续的，因此 $\| f\| = 0$ 意味着 $f$ 除了在一个“测度为零”的集合上外处处为零。我们可以通过约定这样的函数实际上就是零函数来规避 $f$ 不恒为零的困难，因为就积分而言，$f$ 的行为完全等同于零函数。

A more essential difficulty is that the space $\mathcal{R}$ is not complete. One way to see this is to start with the function

$$f(x) = \begin{cases} \log (1/x) & \text{for } 0 < x \leq 1/2, \\ \text{extended appropriately to } [0,2\pi] \text{ so that it is continuous and } f(0)=0, \end{cases}$$

一个更本质的困难是空间 $\mathcal{R}$ 不是完备的。一种方法是考虑函数

$$f(x) = \begin{cases} \log (1/x) & \text{对于 } 0 < x \leq 1/2, \\ \text{适当延拓到 } [0,2\pi] \text{ 使其连续且 } f(0)=0, \end{cases}$$

Since $f$ is not bounded, it does not belong to the space $\mathcal{R}$ . Moreover, the sequence of truncations $f_{n}$ defined by

$$f_n(x) = \begin{cases} \min(f(x), n) & \text{for } x \in [0,2\pi], \end{cases}$$

由于 $f$ 无界，它不属于空间 $\mathcal{R}$。此外，截断序列 $f_{n}$ 定义为

$$f_n(x) = \begin{cases} \min(f(x), n) & \text{对于 } x \in [0,2\pi], \end{cases}$$

can easily be seen to form a Cauchy sequence in $\mathcal{R}$ (see Exercise 5). However, this sequence cannot converge to an element in $\mathcal{R}$ , since that limit, if it existed, would have to be $f$ ; for another example, see Exercise 7.

可以很容易地看出它在 $\mathcal{R}$ 中形成一个柯西序列（见练习 5）。然而，这个序列不能收敛到 $\mathcal{R}$ 中的元素，因为如果极限存在，它必须是 $f$；另一个例子见练习 7。

This and more complicated examples motivate the search for the completion of $\mathcal{R}$ , the class of Riemann integrable functions on $[0,2\pi ]$ . The construction and identification of this completion, the Lebesgue class $L^{2}([0,2\pi ])$ , represents an important turning point in the development of analysis (somewhat akin to the much earlier completion of the rationals, that is, the passage from $\mathbb{Q}$ to $\mathbb{R}$ ). A further discussion of these fundamental ideas will be postponed until Book III, where we take up the Lebesgue theory of integration.

这个和更复杂的例子促使我们寻找 $\mathcal{R}$（即 $[0,2\pi]$ 上黎曼可积函数的类）的完备化。这个完备化的构造和识别，即勒贝格类 $L^{2}([0,2\pi])$，代表了分析发展中的一个重要转折点（有点类似于更早的有理数完备化，即从 $\mathbb{Q}$ 到 $\mathbb{R}$ 的跨越）。对这些基本思想的进一步讨论将推迟到第三卷，届时我们将讨论勒贝格积分理论。

We now turn to the proof of Theorem 1.1.

我们现在转向定理 1.1 的证明。

### 1.2 Proof of mean-square convergence

### 1.2 均方收敛的证明

Consider the space $\mathcal{R}$ of integrable functions on the circle with inner product

$$(f,g) = \frac{1}{2\pi}\int_{0}^{2\pi}f(\theta)\overline{g(\theta)} d\theta$$

考虑圆上的可积函数空间 $\mathcal{R}$，其内积为

$$(f,g) = \frac{1}{2\pi}\int_{0}^{2\pi}f(\theta)\overline{g(\theta)} d\theta$$

===== Page 94 =====

and norm $\| f\|$ defined by

$$\| f\| ^2 = (f,f) = \frac{1}{2\pi}\int_0^{2\pi}|f(\theta)|^2 d\theta .$$

With this notation, we must prove that $\| f - S_N(f)\| \to 0$ as $N$ tends to infinity.

以及范数 $\| f\|$ 定义为

$$\| f\| ^2 = (f,f) = \frac{1}{2\pi}\int_0^{2\pi}|f(\theta)|^2 d\theta .$$

使用这个记号，我们必须证明当 $N \to \infty$ 时 $\| f - S_N(f)\| \to 0$。

For each integer $n$ , let $e_n(\theta) = e^{in\theta}$ , and observe that the family $\{e_n\}_{n \in \mathbb{Z}}$ is orthonormal; that is,

$$\frac{1}{2\pi} \int_0^{2\pi} e_n(\theta) \overline{e_m(\theta)} d\theta = \begin{cases} 1 & \text{if } n=m, \\ 0 & \text{if } n \neq m. \end{cases}$$

对于每个整数 $n$，令 $e_n(\theta) = e^{in\theta}$，并观察到族 $\{e_n\}_{n \in \mathbb{Z}}$ 是正交归一的；即

$$\frac{1}{2\pi} \int_0^{2\pi} e_n(\theta) \overline{e_m(\theta)} d\theta = \begin{cases} 1 & \text{若 } n=m, \\ 0 & \text{若 } n \neq m. \end{cases}$$

Let $f$ be an integrable function on the circle, and let $a_n$ denote its Fourier coefficients. An important observation is that these Fourier coefficients are represented by inner products of $f$ with the elements in the orthonormal set $\{e_n\}_{n \in \mathbb{Z}}$ :

$$(f,e_n) = \frac{1}{2\pi}\int_0^{2\pi}f(\theta)e^{-in\theta}d\theta = a_n.$$

设 $f$ 是圆上的一个可积函数，并令 $a_n$ 表示其傅里叶系数。一个重要观察是，这些傅里叶系数可以通过 $f$ 与正交归一集 $\{e_n\}_{n \in \mathbb{Z}}$ 中元素的内积来表示：

$$(f,e_n) = \frac{1}{2\pi}\int_0^{2\pi}f(\theta)e^{-in\theta}d\theta = a_n.$$

In particular, $S_N(f) = \sum_{|n| \leq N} a_n e_n$ . Then the orthonormal property of the family $\{e_n\}$ and the fact that $a_n = (f, e_n)$ imply that the difference $f - \sum_{|n| \leq N} a_n e_n$ is orthogonal to $e_n$ for all $|n| \leq N$ . Therefore, we must have

$$(f - \sum_{|n| \leq N} a_n e_n) \perp \sum_{|n| \leq N} b_n e_n \quad (2)$$

for any complex numbers $b_n$ . We draw two conclusions from this fact. First, we can apply the Pythagorean theorem to the decomposition

$$f = f - \sum_{|n| \leq N} a_n e_n + \sum_{|n| \leq N} a_n e_n,$$

where we now choose $b_n = a_n$ , to obtain

$$\| f\| ^2 = \| f - \sum_{|n| \leq N} a_n e_n\| ^2 + \| \sum_{|n| \leq N} a_n e_n\| ^2.$$

特别地，$S_N(f) = \sum_{|n| \leq N} a_n e_n$。然后，族 $\{e_n\}$ 的正交归一性质以及 $a_n = (f, e_n)$ 的事实意味着差 $f - \sum_{|n| \leq N} a_n e_n$ 对于所有 $|n| \leq N$ 都与 $e_n$ 正交。因此，对于任意复数 $b_n$，我们有

$$(f - \sum_{|n| \leq N} a_n e_n) \perp \sum_{|n| \leq N} b_n e_n \quad (2)$$

我们从这一事实得出两个结论。首先，我们可以将勾股定理应用于分解

$$f = f - \sum_{|n| \leq N} a_n e_n + \sum_{|n| \leq N} a_n e_n,$$

现在选择 $b_n = a_n$，得到

$$\| f\| ^2 = \| f - \sum_{|n| \leq N} a_n e_n\| ^2 + \| \sum_{|n| \leq N} a_n e_n\| ^2.$$

Since the orthonormal property of the family $\{e_n\}_{n \in \mathbb{Z}}$ implies that

$$\| \sum_{|n| \leq N} a_n e_n\| ^2 = \sum_{|n| \leq N} |a_n|^2,$$

由于族 $\{e_n\}_{n \in \mathbb{Z}}$ 的正交归一性质意味着

$$\| \sum_{|n| \leq N} a_n e_n\| ^2 = \sum_{|n| \leq N} |a_n|^2,$$

===== Page 95 =====

we deduce that

$$\| f\| ^2 = \| f - S_N(f)\| ^2 +\sum_{|n|\leq N}|a_n|^2.$$

我们推导出

$$\| f\| ^2 = \| f - S_N(f)\| ^2 +\sum_{|n|\leq N}|a_n|^2.$$

The second conclusion we may draw from (2) is the following simple lemma.

我们从 (2) 可以得出的第二个结论是以下简单引理。

Lemma 1.2 (Best approximation) If $f$ is integrable on the circle with Fourier coefficients $a_n$ , then

$$\| f - S_N(f)\| \leq \| f - \sum_{|n|\leq N}c_ne_n\|$$

for any complex numbers $c_n$ . Moreover, equality holds precisely when $c_n = a_n$ for all $|n|\leq N$ .

引理 1.2 (最佳逼近) 如果 $f$ 在圆上可积，傅里叶系数为 $a_n$，那么对于任意复数 $c_n$，有

$$\| f - S_N(f)\| \leq \| f - \sum_{|n|\leq N}c_ne_n\|$$

此外，当且仅当对所有 $|n|\leq N$ 有 $c_n = a_n$ 时等号成立。

Proof. This follows immediately by applying the Pythagorean theorem to

$$f - \sum_{|n|\leq N}c_ne_n = f - S_N(f) + \sum_{|n|\leq N}b_ne_n,$$

where $b_n = a_n - c_n$ .

证明。这可以通过将勾股定理应用于

$$f - \sum_{|n|\leq N}c_ne_n = f - S_N(f) + \sum_{|n|\leq N}b_ne_n,$$

立即得到，其中 $b_n = a_n - c_n$。

This lemma has a clear geometric interpretation. It says that the trigonometric polynomial of degree at most $N$ which is closest to $f$ in the norm $\| \cdot \|$ is the partial sum $S_N(f)$ . This geometric property of the partial sums is depicted in Figure 1, where the orthogonal projection of $f$ in the plane spanned by $\{e_{- N},\ldots ,e_0,\ldots ,e_N\}$ is simply $S_N(f)$ .

这个引理有一个清晰的几何解释。它表明在范数 $\| \cdot \|$ 下，次数不超过 $N$ 且最接近 $f$ 的三角多项式是部分和 $S_N(f)$。部分和的这个几何性质如图 1 所示，其中 $f$ 在由 $\{e_{- N},\ldots ,e_0,\ldots ,e_N\}$ 张成的平面上的正交投影正是 $S_N(f)$。

<center>Figure 1. The best approximation lemma </center>

<center>图 1. 最佳逼近引理 </center>

We can now give the proof that $\| S_N(f) - f\| \to 0$ using the best approximation lemma, as well as the important fact that trigonometric polynomials are dense in the space of continuous functions on the circle.

我们现在可以给出 $\| S_N(f) - f\| \to 0$ 的证明，使用最佳逼近引理以及三角多项式在圆上连续函数空间中稠密的重要事实。

===== Page 96 =====

Suppose that $f$ is continuous on the circle. Then, given $\epsilon >0$ , there exists (by Corollary 5.4 in Chapter 2) a trigonometric polynomial $P$ , say of degree $M$ , such that

$$|f(\theta) - P(\theta)|< \epsilon \quad \mathrm{for~all~}\theta .$$

In particular, taking squares and integrating this inequality yields $\| f - P\| < \epsilon$ , and by the best approximation lemma we conclude that

$$\| f - S_N(f)\| < \epsilon \quad \mathrm{whenever~}N\geq M.$$

This proves Theorem 1.1 when $f$ is continuous.

假设 $f$ 在圆上连续。那么，给定 $\epsilon >0$，存在（根据第 2 章推论 5.4）一个三角多项式 $P$，设其次数为 $M$，使得

$$|f(\theta) - P(\theta)|< \epsilon \quad \mathrm{对所有~}\theta \mathrm{~成立}.$$

特别地，对该不等式取平方并积分得到 $\| f - P\| < \epsilon$，然后根据最佳逼近引理我们得出结论

$$\| f - S_N(f)\| < \epsilon \quad \mathrm{只要~}N\geq M.$$

当 $f$ 连续时，这证明了定理 1.1。

If $f$ is merely integrable, we can no longer approximate $f$ uniformly by trigonometric polynomials. Instead, we apply the approximation Lemma 3.2 in Chapter 2 and choose a continuous function $g$ on the circle which satisfies

$$\sup_{\theta \in [0,2\pi ]}|g(\theta)|\leq \sup_{\theta \in [0,2\pi ]}|f(\theta)| = B,$$

and

$$\int_0^{2\pi}|f(\theta) - g(\theta)|d\theta < \epsilon^2.$$

如果 $f$ 仅仅是可积的，我们不能再通过三角多项式一致逼近 $f$。相反，我们应用第 2 章的逼近引理 3.2，并选择一个圆上的连续函数 $g$，使其满足

$$\sup_{\theta \in [0,2\pi ]}|g(\theta)|\leq \sup_{\theta \in [0,2\pi ]}|f(\theta)| = B,$$

且

$$\int_0^{2\pi}|f(\theta) - g(\theta)|d\theta < \epsilon^2.$$

Then we get

$$
\begin{aligned} \| f - g\| ^2 & = \frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - g(\theta)|^2 d\theta \\ & = \frac{1}{2\pi}\int_0^{2\pi}|f(\bar{\theta}) - g(\theta)||f(\theta) - g(\theta)|d\theta \\ & \leq \frac{2B}{2\pi}\int_0^{2\pi}|f(\theta) - g(\theta)|d\theta \\ & \leq C\epsilon^2. \end{aligned}
$$

那么得到

$$
\begin{aligned} \| f - g\| ^2 & = \frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - g(\theta)|^2 d\theta \\ & = \frac{1}{2\pi}\int_0^{2\pi}|f(\bar{\theta}) - g(\theta)||f(\theta) - g(\theta)|d\theta \\ & \leq \frac{2B}{2\pi}\int_0^{2\pi}|f(\theta) - g(\theta)|d\theta \\ & \leq C\epsilon^2. \end{aligned}
$$

Now we may approximate $g$ by a trigonometric polynomial $P$ so that $\| g - P\| < \epsilon$ . Then $\| f - P\| < C' \epsilon$ , and we may again conclude by applying the best approximation lemma. This completes the proof that the partial sums of the Fourier series of $f$ converge to $f$ in the mean square norm $\| \cdot \|$ .

现在我们可以用三角多项式 $P$ 逼近 $g$，使得 $\| g - P\| < \epsilon$。那么 $\| f - P\| < C' \epsilon$，再次应用最佳逼近引理即可得出结论。这就完成了证明：$f$ 的傅里叶级数的部分和在均方范数 $\| \cdot \|$ 下收敛到 $f$。

Note that this result and the relation (3) imply that if $a_{n}$ is the $n^{\mathrm{th}}$ Fourier coefficient of an integrable function $f$ , then the series $\sum_{n = -\infty}^{\infty}|a_{n}|^{2}$ converges, and in fact we have Parseval's identity

$$\sum_{n = -\infty}^{\infty}|a_n|^2 = \| f\| ^2.$$

注意，这个结果和关系式 (3) 意味着如果 $a_{n}$ 是可积函数 $f$ 的第 $n$ 个傅里叶系数，那么级数 $\sum_{n = -\infty}^{\infty}|a_{n}|^{2}$ 收敛，实际上我们有帕塞瓦尔恒等式

$$\sum_{n = -\infty}^{\infty}|a_n|^2 = \| f\| ^2.$$

===== Page 97 =====

This identity provides an important connection between the norms in the two vector spaces $\ell^2 (\mathbb{Z})$ and $\mathcal{R}$ .

这个恒等式在两个向量空间 $\ell^2 (\mathbb{Z})$ 和 $\mathcal{R}$ 的范数之间提供了一个重要的联系。

We now summarize the results of this section.

我们现在总结本节的结果。

Theorem 1.3 Let $f$ be an integrable function on the circle with $f\sim \sum_{n = -\infty}^{\infty}a_{n}e^{in\theta}$ . Then we have:

(i) Mean-square convergence of the Fourier series

$$\frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - S_N(f)(\theta)|^2 d\theta \to 0\quad as N\to \infty .$$

(ii) Parseval's identity

$$\sum_{n = -\infty}^{\infty}|a_n|^2 = \frac{1}{2\pi}\int_0^{2\pi}|f(\theta)|^2 d\theta .$$

定理 1.3 设 $f$ 是圆上的可积函数，$f\sim \sum_{n = -\infty}^{\infty}a_{n}e^{in\theta}$。那么我们有：

(i) 傅里叶级数的均方收敛

$$\frac{1}{2\pi}\int_0^{2\pi}|f(\theta) - S_N(f)(\theta)|^2 d\theta \to 0\quad as N\to \infty .$$

(ii) 帕塞瓦尔恒等式

$$\sum_{n = -\infty}^{\infty}|a_n|^2 = \frac{1}{2\pi}\int_0^{2\pi}|f(\theta)|^2 d\theta .$$

Remark 1. If $\{e_n\}$ is any orthonormal family of functions on the circle, and $a_n = (f, e_n)$ , then we may deduce from the relation (3) that

$$\sum_{n = -\infty}^{\infty}|a_n|^2\leq \| f\| ^2.$$

This is known as Bessel's inequality. Equality holds (as in Parseval's identity) precisely when the family $\{e_n\}$ is also a "basis," in the sense that $\| \sum_{|n|\leq N}a_n e_n - f\| \to 0$ as $N\to \infty$ .

注记 1. 如果 $\{e_n\}$ 是圆上的任意正交归一函数族，且 $a_n = (f, e_n)$，那么我们可以从关系式 (3) 推导出

$$\sum_{n = -\infty}^{\infty}|a_n|^2\leq \| f\| ^2.$$

这被称为贝塞尔不等式。当且仅当族 $\{e_n\}$ 也是一个“基”，即当 $N\to \infty$ 时 $\| \sum_{|n|\leq N}a_n e_n - f\| \to 0$，等号成立（如同帕塞瓦尔恒等式）。

Remark 2. We may associate to every integrable function the sequence $\{a_n\}$ formed by its Fourier coefficients. Parseval's identity guarantees that $\{a_n\} \in \ell^2 (\mathbb{Z})$ . Since $\ell^2 (\mathbb{Z})$ is a Hilbert space, the failure of $\mathcal{R}$ to be complete, discussed earlier, may be understood as follows: there exist sequences $\{a_n\}_{n\in \mathbb{Z}}$ such that $\sum_{n\in \mathbb{Z}}|a_n|^2 < \infty$ , yet no Riemann integrable function $F$ has $n^{\mathrm{th}}$ Fourier coefficient equal to $a_n$ for all $n$ . An example is given in Exercise 6.

注记 2. 我们可以将每个可积函数与由其傅里叶系数组成的序列 $\{a_n\}$ 相关联。帕塞瓦尔恒等式保证 $\{a_n\} \in \ell^2 (\mathbb{Z})$。由于 $\ell^2 (\mathbb{Z})$ 是一个希尔伯特空间，前面讨论过的 $\mathcal{R}$ 的不完备性可以这样理解：存在序列 $\{a_n\}_{n\in \mathbb{Z}}$，使得 $\sum_{n\in \mathbb{Z}}|a_n|^2 < \infty$，但没有任何黎曼可积函数 $F$ 对所有 $n$ 的第 $n$ 个傅里叶系数等于 $a_n$。练习 6 中给出了一个例子。

Since the terms of a converging series tend to 0, we deduce from Parseval's identity or Bessel's inequality the following result.

由于收敛级数的项趋于 0，我们从帕塞瓦尔恒等式或贝塞尔不等式推导出以下结果。

Theorem 1.4 (Riemann- Lebesgue lemma) If $f$ is integrable on the circle, then $\hat{f} (n)\to 0$ as $|n|\to \infty$ .

定理 1.4 (黎曼-勒贝格引理) 如果 $f$ 在圆上可积，那么当 $|n|\to \infty$ 时 $\hat{f} (n)\to 0$。

An equivalent reformulation of this proposition is that if $f$ is integrable on $[0,2\pi ]$ , then

$$\int_0^{2\pi}f(\theta)\sin (N\theta)d\theta \to 0\quad \mathrm{as}N\to \infty$$

这个命题的一个等价表述是，如果 $f$ 在 $[0,2\pi]$ 上可积，那么

$$\int_0^{2\pi}f(\theta)\sin (N\theta)d\theta \to 0\quad \mathrm{as}N\to \infty$$

===== Page 98 =====

and

$$\int_{0}^{2\pi}f(\theta)\cos (N\theta)d\theta \rightarrow 0\quad \mathrm{as}N\rightarrow \infty .$$

以及

$$\int_{0}^{2\pi}f(\theta)\cos (N\theta)d\theta \rightarrow 0\quad \mathrm{as}N\rightarrow \infty .$$

To conclude this section, we give a more general version of the Parseval identity which we will use in the next chapter.

为了结束本节，我们给出一个将在下一章使用的更一般的帕塞瓦尔恒等式版本。

Lemma 1.5 Suppose $F$ and $G$ are integrable on the circle with

$$F\sim \sum a_{n}e^{in\theta}\quad and\quad G\sim \sum b_{n}e^{in\theta}.$$

Then

$$\frac{1}{2\pi}\int_{0}^{2\pi}F(\theta)\overline{G(\theta)} d\theta = \sum_{n = -\infty}^{\infty}a_{n}\overline{b_{n}}.$$

引理 1.5 假设 $F$ 和 $G$ 在圆上可积，且

$$F\sim \sum a_{n}e^{in\theta}\quad 和 \quad G\sim \sum b_{n}e^{in\theta}.$$

那么

$$\frac{1}{2\pi}\int_{0}^{2\pi}F(\theta)\overline{G(\theta)} d\theta = \sum_{n = -\infty}^{\infty}a_{n}\overline{b_{n}}.$$

Recall from the discussion in Example 1 that the series $\sum_{n = -\infty}^{\infty}a_{n}\overline{b_{n}}$ converges absolutely.

回忆例 1 中的讨论，级数 $\sum_{n = -\infty}^{\infty}a_{n}\overline{b_{n}}$ 绝对收敛。

Proof. The proof follows from Parseval's identity and the fact that

$$(F,G) = \frac{1}{4}\left[\| F + G\|^{2} - \| F - G\|^{2} + i\left(\| F + iG\|^{2} - \| F - iG\|^{2}\right)\right]$$

which holds in every Hermitian inner product space. The verification of this fact is left to the reader.

证明。证明遵循帕塞瓦尔恒等式以及以下事实

$$(F,G) = \frac{1}{4}\left[\| F + G\|^{2} - \| F - G\|^{2} + i\left(\| F + iG\|^{2} - \| F - iG\|^{2}\right)\right]$$

这在每个埃尔米特内积空间中都成立。这个事实的验证留给读者。

## 2 Return to pointwise convergence

## 2 回到逐点收敛

The mean- square convergence theorem does not provide further insight into the problem of pointwise convergence. Indeed, Theorem 1.1 by itself does not guarantee that the Fourier series converges for any $\theta$ . Exercise 3 helps to explain this statement. However, if a function is differentiable at a point $\theta_{0}$ , then its Fourier series converges at $\theta_{0}$ . After proving this result, we give an example of a continuous function with diverging Fourier series at one point. These phenomena are indicative of the intricate nature of the problem of pointwise convergence in the theory of Fourier series.

均方收敛定理并没有为逐点收敛问题提供进一步的见解。实际上，定理 1.1 本身并不能保证傅里叶级数对任何 $\theta$ 收敛。练习 3 有助于解释这一说法。然而，如果一个函数在点 $\theta_{0}$ 处可微，那么它的傅里叶级数在 $\theta_{0}$ 处收敛。在证明这个结果之后，我们将给出一个连续函数在其一点上傅里叶级数发散的例子。这些现象表明了傅里叶级数理论中逐点收敛问题的复杂性。

### 2.1 A local result

### 2.1 一个局部结果

Theorem 2.1 Let $f$ be an integrable function on the circle which is differentiable at a point $\theta_{0}$ . Then $S_{N}(f)(\theta_{0}) \to f(\theta_{0})$ as $N$ tends to infinity.

定理 2.1 设 $f$ 是圆上的可积函数，且在点 $\theta_{0}$ 处可微。那么当 $N \to \infty$ 时，$S_{N}(f)(\theta_{0}) \to f(\theta_{0})$。

===== Page 99 =====

Proof. Define

$$F(t) = \begin{cases} \frac{f(\theta_0 - t) - f(\theta_0)}{t} & \text{for } t \neq 0, \\ -f'(\theta_0) & \text{for } t = 0. \end{cases}$$

证明。定义

$$F(t) = \begin{cases} \frac{f(\theta_0 - t) - f(\theta_0)}{t} & \text{对于 } t \neq 0, \\ -f'(\theta_0) & \text{对于 } t = 0. \end{cases}$$

First, $F$ is bounded near $0$ since $f$ is differentiable there. Second, for all small $\delta$ the function $F$ is integrable on $[-\pi , - \delta ]\cup [\delta ,\pi ]$ because $f$ has this property and $|t| > \delta$ there. As a consequence of Proposition 1.4 in the appendix, the function $F$ is integrable on all of $[-\pi ,\pi ]$ .We know that $S_{N}(f)(\theta_{0}) = (f*D_{N})(\theta_{0})$ ,where $D_{N}$ is the Dirichlet kernel. Since $\frac{1}{2\pi}\int D_{N} = 1$ ,we find that

$$S_{N}(f)(\theta_{0}) - f(\theta_{0}) = \frac{1}{2\pi}\int_{-\pi}^{\pi}[f(\theta_{0} - t) - f(\theta_{0})]D_{N}(t)dt$$ $$\qquad = \frac{1}{2\pi}\int_{-\pi}^{\pi}F(t)tD_{N}(t)dt.$$

首先，由于 $f$ 在 $0$ 处可微，$F$ 在 $0$ 附近有界。其次，对于所有小的 $\delta$，函数 $F$ 在 $[-\pi , - \delta ]\cup [\delta ,\pi ]$ 上可积，因为 $f$ 具有此性质且在此处 $|t| > \delta$。根据附录中命题 1.4 的结果，函数 $F$ 在整个 $[-\pi ,\pi ]$ 上可积。我们知道 $S_{N}(f)(\theta_{0}) = (f*D_{N})(\theta_{0})$，其中 $D_{N}$ 是狄利克雷核。由于 $\frac{1}{2\pi}\int D_{N} = 1$，我们得到

$$S_{N}(f)(\theta_{0}) - f(\theta_{0}) = \frac{1}{2\pi}\int_{-\pi}^{\pi}[f(\theta_{0} - t) - f(\theta_{0})]D_{N}(t)dt$$ $$\qquad = \frac{1}{2\pi}\int_{-\pi}^{\pi}F(t)tD_{N}(t)dt.$$

We recall that

$$tD_{N}(t) = \frac{t}{\sin(t / 2)}\sin ((N + 1 / 2)t),$$

where the quotient $\frac{t}{\sin(t / 2)}$ is continuous in the interval $[-\pi ,\pi ]$ . Since we can write

$$\sin ((N + 1 / 2)t) = \sin (Nt)\cos (t / 2) + \cos (Nt)\sin (t / 2),$$

we can apply the Riemann- Lebesgue lemma to the Riemann integrable functions $F(t)\cos (t / 2) / \sin (t / 2)$ and $F(t)t$ to finish the proof of the theorem.

我们回忆

$$tD_{N}(t) = \frac{t}{\sin(t / 2)}\sin ((N + 1 / 2)t),$$

其中商 $\frac{t}{\sin(t / 2)}$ 在区间 $[-\pi ,\pi ]$ 上连续。因为我们可以写

$$\sin ((N + 1 / 2)t) = \sin (Nt)\cos (t / 2) + \cos (Nt)\sin (t / 2),$$

我们可以对黎曼可积函数 $F(t)\cos (t / 2) / \sin (t / 2)$ 和 $F(t)t$ 应用黎曼-勒贝格引理来完成定理的证明。

Observe that the conclusion of the theorem still holds if we only assume that $f$ satisfies a Lipschitz condition at $\theta_{0}$ ; that is,

$$|f(\theta) - f(\theta_0)|\leq M|\theta -\theta_0|$$

for some $M\geq 0$ and all $\theta$ . This is the same as saying that $f$ satisfies a Hölder condition of order $\alpha = 1$ .

注意，如果我们只假设 $f$ 在 $\theta_{0}$ 处满足利普希茨条件，定理的结论仍然成立；即

$$|f(\theta) - f(\theta_0)|\leq M|\theta -\theta_0|$$

对某个 $M\geq 0$ 和所有 $\theta$ 成立。这等价于说 $f$ 满足阶数为 $\alpha = 1$ 的赫尔德条件。

A striking consequence of this theorem is the localization principle of Riemann. This result states that the convergence of $S_{N}(f)(\theta_{0})$ depends only on the behavior of $f$ near $\theta_{0}$ . This is not clear at first, since forming the Fourier series requires integrating $f$ over the whole circle.

这个定理的一个惊人推论是黎曼局部化原理。这个结果指出 $S_{N}(f)(\theta_{0})$ 的收敛性只取决于 $f$ 在 $\theta_{0}$ 附近的行为。这初看起来并不明显，因为构造傅里叶级数需要对 $f$ 在整个圆上进行积分。

===== Page 100 =====

Theorem 2.2 Suppose $f$ and $g$ are two integrable functions defined on the circle, and for some $\theta_0$ there exists an open interval $I$ containing $\theta_0$ such that

$$f(\theta) = g(\theta)\quad \text{for all} \theta \in I.$$

Then $S_N(f)(\theta_0) - S_N(g)(\theta_0) \to 0$ as $N$ tends to infinity.

定理 2.2 假设 $f$ 和 $g$ 是定义在圆上的两个可积函数，并且对于某个 $\theta_0$，存在一个包含 $\theta_0$ 的开区间 $I$，使得

$$f(\theta) = g(\theta)\quad \text{对所有} \theta \in I \text{成立}.$$

那么当 $N \to \infty$ 时，$S_N(f)(\theta_0) - S_N(g)(\theta_0) \to 0$。

Proof. The function $f - g$ is 0 in $I$ , so it is differentiable at $\theta_0$ , and we may apply the previous theorem to conclude the proof.

证明。函数 $f - g$ 在 $I$ 中为 0，因此它在 $\theta_0$ 处可微，我们可以应用前面的定理得出结论。

### 2.2 A continuous function with diverging Fourier series

### 2.2 一个傅里叶级数发散的连续函数

We now turn our attention to an example of a continuous periodic function whose Fourier series diverges at a point. Thus, Theorem 2.1 fails if the differentiability assumption is replaced by the weaker assumption of continuity. Our counter- example shows that this hypothesis which had appeared plausible, is in fact false; moreover, its construction also illuminates an important principle of the theory.

现在我们将注意力转向一个连续周期函数的例子，其傅里叶级数在某点发散。因此，如果将可微性假设替换为更弱的连续性假设，定理 2.1 就不成立了。我们的反例表明，这个看似合理的假设实际上是错误的；此外，它的构造也阐明了该理论的一个重要原理。

The principle that is involved here will be referred to as "symmetrybreaking." The symmetry that we have in mind is the symmetry between the frequencies $e^{in\theta}$ and $e^{- in\theta}$ which appear in the Fourier expansion of a function. For example, the partial sum operator $S_N$ is defined in a way that reflects this symmetry. Also, the Dirichlet, Fejer, and Poisson kernels are symmetric in this sense. When we break the symmetry, that is, when we split the Fourier series $\sum_{n = -\infty}^{\infty} a_n e^{in\theta}$ into the two pieces $\sum_{n \geq 0} a_n e^{in\theta}$ and $\sum_{n < 0} a_n e^{in\theta}$ , we introduce new and far- reaching phenomena.

这里涉及的原则将被称为“对称破缺”。我们想到的对称性是函数傅里叶展开中出现的频率 $e^{in\theta}$ 和 $e^{- in\theta}$ 之间的对称性。例如，部分和算子 $S_N$ 的定义方式反映了这种对称性。同样，狄利克雷核、费耶核和泊松核在这个意义上也是对称的。当我们打破这种对称性，即当我们把傅里叶级数 $\sum_{n = -\infty}^{\infty} a_n e^{in\theta}$ 分成两部分 $\sum_{n \geq 0} a_n e^{in\theta}$ 和 $\sum_{n < 0} a_n e^{in\theta}$ 时，我们引入了新的、影响深远的现象。

We give a simple example. Start with the sawtooth function $f$ which is odd in $\theta$ and which equals $i(\pi - \theta)$ when $0 < \theta < \pi$ . Then, by Exercise 8 in Chapter 2, we know that

$$f(\theta) \sim \sum_{n \neq 0} \frac{e^{in\theta}}{n}. \quad (4)$$

我们给出一个简单的例子。从锯齿函数 $f$ 开始，它在 $\theta$ 上是奇函数，并且当 $0 < \theta < \pi$ 时等于 $i(\pi - \theta)$。然后，根据第 2 章练习 8，我们知道

$$f(\theta) \sim \sum_{n \neq 0} \frac{e^{in\theta}}{n}. \quad (4)$$

Consider now the result of breaking the symmetry and the resulting series

$$\sum_{n = -\infty}^{n = -1} \frac{e^{in\theta}}{n}.$$

Then, unlike (4), the above is no longer the Fourier series of a Riemann integrable function. Indeed, suppose it were the Fourier series of an

现在考虑打破对称性的结果以及由此得到的级数

$$\sum_{n = -\infty}^{n = -1} \frac{e^{in\theta}}{n}.$$

那么，与 (4) 不同，上式不再是黎曼可积函数的傅里叶级数。实际上，假设它是某个

===== Page 101 =====

integrable function, say $\tilde{f}$ , where in particular $\tilde{f}$ is bounded. Using the Abel means, we then have

$$|A_r(\tilde{f})(0)| = \sum_{n = 1}^{\infty}\frac{r^n}{n},$$

which tends to infinity as $r$ tends to 1, because $\sum 1 / n$ diverges. This gives the desired contradiction since

$$|A_r(\tilde{f})(0)|\leq \frac{1}{2\pi}\int_{-\pi}^{\pi}|\tilde{f}(\theta)|P_r(\theta)d\theta \leq \sup_{\theta}|\tilde{f}(\theta)|,$$

where $P_r(\theta)$ denotes the Poisson kernel discussed in the previous chapter.

可积函数 $\tilde{f}$ 的傅里叶级数，特别地 $\tilde{f}$ 有界。然后使用阿贝尔平均，我们有

$$|A_r(\tilde{f})(0)| = \sum_{n = 1}^{\infty}\frac{r^n}{n},$$

当 $r \to 1$ 时趋于无穷，因为 $\sum 1 / n$ 发散。这给出了所需的矛盾，因为

$$|A_r(\tilde{f})(0)|\leq \frac{1}{2\pi}\int_{-\pi}^{\pi}|\tilde{f}(\theta)|P_r(\theta)d\theta \leq \sup_{\theta}|\tilde{f}(\theta)|,$$

其中 $P_r(\theta)$ 表示前一章讨论的泊松核。

The sawtooth function is the object from which we will fashion our counter- example. We proceed as follows. For each $N\geq 1$ we define the following two functions on $[-\pi ,\pi ]$

$$f_{N}(\theta) = \sum_{1\leq |n|\leq N}\frac{e^{in\theta}}{n}\quad \mathrm{and}\quad \tilde{f}_{N}(\theta) = \sum_{-N\leq n\leq -1}\frac{e^{in\theta}}{n}.$$

锯齿函数是我们构建反例的出发点。我们按如下步骤进行。对于每个 $N\geq 1$，我们在 $[-\pi ,\pi]$ 上定义以下两个函数

$$f_{N}(\theta) = \sum_{1\leq |n|\leq N}\frac{e^{in\theta}}{n}\quad \mathrm{和}\quad \tilde{f}_{N}(\theta) = \sum_{-N\leq n\leq -1}\frac{e^{in\theta}}{n}.$$

We contend that:

(i) $|\tilde{f}_N(0)|\geq c\log N.$ (ii) $f_{N}(\theta)$ is uniformly bounded in $N$ and $\theta$

我们断言：

(i) $|\tilde{f}_N(0)|\geq c\log N.$ (ii) $f_{N}(\theta)$ 关于 $N$ 和 $\theta$ 一致有界。

The first statement is a consequence of the fact that $\sum_{n = 1}^{N}1 / n\geq$ $\log N$ , which is easily established (see also Figure 2):

$$\sum_{n = 1}^{N}\frac{1}{n}\geq \sum_{n = 1}^{N - 1}\int_{n}^{n + 1}\frac{dx}{x} = \int_{1}^{N}\frac{dx}{x} = \log N.$$

第一个论断是 $\sum_{n = 1}^{N}1 / n\geq \log N$ 这一事实的结果，这很容易证明（另见图 2）：

$$\sum_{n = 1}^{N}\frac{1}{n}\geq \sum_{n = 1}^{N - 1}\int_{n}^{n + 1}\frac{dx}{x} = \int_{1}^{N}\frac{dx}{x} = \log N.$$

To prove (ii), we argue in the same spirit as in the proof of Tauber's theorem, which says that if the series $\sum c_n$ is Abel summable to $s$ and $c_n = o(1 / n)$ , then $\sum c_n$ actually converges to $s$ (see Exercise 14 in Chapter 2). In fact, the proof of Tauber's theorem is quite similar to that of the lemma below.

为了证明 (ii)，我们采用与陶伯定理证明类似的方法，该定理指出如果级数 $\sum c_n$ 阿贝尔可和到 $s$ 且 $c_n = o(1 / n)$，那么 $\sum c_n$ 实际上收敛到 $s$（见第 2 章练习 14）。事实上，陶伯定理的证明与下面引理的证明非常相似。

Lemma 2.3 Suppose that the Abel means $A_{r} = \sum_{n = 1}^{\infty}r^{n}c_{n}$ of the series $\sum_{n = 1}^{\infty}c_{n}$ are bounded as $r$ tends to 1 (with $r< 1$ ). If $c_{n} = O(1 / n)$ , then the partial sums $S_{N} = \sum_{n = 1}^{N}c_{n}$ are bounded.

引理 2.3 假设级数 $\sum_{n = 1}^{\infty}c_{n}$ 的阿贝尔平均 $A_{r} = \sum_{n = 1}^{\infty}r^{n}c_{n}$ 当 $r \to 1$（且 $r< 1$）时有界。如果 $c_{n} = O(1 / n)$，那么部分和 $S_{N} = \sum_{n = 1}^{N}c_{n}$ 有界。

===== Page 102 =====

Proof. Let $r = 1 - 1 / N$ and choose $M$ so that $n|c_n| \leq M$ . We estimate the difference

$$S_N - A_r = \sum_{n = 1}^N (c_n - r^n c_n) - \sum_{n = N + 1}^\infty r^n c_n$$

as follows:

$$|S_N - A_r| \leq \sum_{n = 1}^N |c_n| (1 - r^n) + \sum_{n = N + 1}^\infty r^n |c_n|$$ $$\leq M \sum_{n = 1}^N (1 - r) + \frac{M}{N} \sum_{n = N + 1}^\infty r^n$$ $$\leq MN(1 - r) + \frac{M}{N} \frac{1}{1 - r}$$ $$= 2M,$$

where we have used the simple observation that

$$1 - r^n = (1 - r)(1 + r + \dots + r^{n - 1}) \leq n(1 - r).$$

证明。令 $r = 1 - 1 / N$ 并选择 $M$ 使得 $n|c_n| \leq M$。我们按如下方式估计差值

$$S_N - A_r = \sum_{n = 1}^N (c_n - r^n c_n) - \sum_{n = N + 1}^\infty r^n c_n$$

：

$$|S_N - A_r| \leq \sum_{n = 1}^N |c_n| (1 - r^n) + \sum_{n = N + 1}^\infty r^n |c_n|$$ $$\leq M \sum_{n = 1}^N (1 - r) + \frac{M}{N} \sum_{n = N + 1}^\infty r^n$$ $$\leq MN(1 - r) + \frac{M}{N} \frac{1}{1 - r}$$ $$= 2M,$$

其中我们使用了简单的观察

$$1 - r^n = (1 - r)(1 + r + \dots + r^{n - 1}) \leq n(1 - r).$$

So we see that if $M$ satisfies both $|A_r| \leq M$ and $n|c_n| \leq M$ , then $|S_N| \leq 3M$ .

因此我们看到，如果 $M$ 同时满足 $|A_r| \leq M$ 和 $n|c_n| \leq M$，那么 $|S_N| \leq 3M$。

We apply the lemma to the series

$$\sum_{n \neq 0} \frac{e^{in \theta}}{n},$$

我们将该引理应用于级数

$$\sum_{n \neq 0} \frac{e^{in \theta}}{n},$$

===== Page 103 =====

which is the Fourier series of the sawtooth function $f$ used above. Here $c_{n} = e^{in\theta} / n + e^{- in\theta} / (- n)$ for $n\neq 0$ so clearly $c_{n} = O(1 / |n|)$ .Finally, the Abel means of this series are $A_{r}(f)(\theta) = (f*P_{r})(\theta)$ .But $f$ is bounded and $P_{r}$ is a good kernel, so $S_{N}(f)(\theta)$ is uniformly bounded in $N$ and $\theta$ as was to be shown.

这就是上面使用的锯齿函数 $f$ 的傅里叶级数。这里对于 $n\neq 0$ 有 $c_{n} = e^{in\theta} / n + e^{- in\theta} / (- n)$，所以显然 $c_{n} = O(1 / |n|)$。最后，这个级数的阿贝尔平均是 $A_{r}(f)(\theta) = (f*P_{r})(\theta)$。但是 $f$ 有界且 $P_{r}$ 是一个好核，所以 $S_{N}(f)(\theta)$ 关于 $N$ 和 $\theta$ 一致有界，正如所要证明的。

We now come to the heart of the matter. Notice that $f_{N}$ and $\tilde{f}_{N}$ are trigonometric polynomials of degree $N$ (that is, they have non- zero Fourier coefficients only when $|n|\leq N$ ).From these, we form trigonometric polynomials $P_{N}$ and $\tilde{P}_{N}$ ,now of degrees $3N$ and $2N - 1$ ,by displacing the frequencies of $f_{N}$ and $\tilde{f}_{N}$ by $2N$ units. In other words, we define $P_{N}(\theta) = e^{i(2N)\theta}f_{N}(\theta)$ and $\tilde{P}_{N}(\theta) = e^{i(2N)\theta}\tilde{f}_{N}(\theta)$ . So while $f_{N}$ has non- vanishing Fourier coefficients when $0< |n|\leq N$ ,now the coefficients of $P_{N}$ are non- vanishing for $N\leq n\leq 3N$ $n\neq 2N$ .Moreover, while $n = 0$ is the center of symmetry of $f_{N}$ ,now $n = 2N$ is the center of symmetry of $P_{N}$ .We next consider the partial sums $S_{M}$

现在我们进入问题的核心。注意 $f_{N}$ 和 $\tilde{f}_{N}$ 是次数为 $N$ 的三角多项式（即只有当 $|n|\leq N$ 时它们的傅里叶系数才非零）。从这些出发，我们通过将 $f_{N}$ 和 $\tilde{f}_{N}$ 的频率移动 $2N$ 个单位，形成三角多项式 $P_{N}$ 和 $\tilde{P}_{N}$，现在次数分别为 $3N$ 和 $2N - 1$。换句话说，我们定义 $P_{N}(\theta) = e^{i(2N)\theta}f_{N}(\theta)$ 和 $\tilde{P}_{N}(\theta) = e^{i(2N)\theta}\tilde{f}_{N}(\theta)$。因此，虽然 $f_{N}$ 在 $0< |n|\leq N$ 时有非零傅里叶系数，但现在 $P_{N}$ 的系数在 $N\leq n\leq 3N$，$n\neq 2N$ 时非零。此外，虽然 $n = 0$ 是 $f_{N}$ 的对称中心，但现在 $n = 2N$ 是 $P_{N}$ 的对称中心。接下来我们考虑部分和 $S_{M}$

Lemma 2.4

$$S_{M}(P_{N})(\theta) = \begin{cases} P_{N}(\theta) & \text{if } M \geq 3N, \\ \tilde{P}_{N}(\theta) & \text{if } M = 2N, \\ 0 & \text{if } M < N. \end{cases}$$

引理 2.4

$$S_{M}(P_{N})(\theta) = \begin{cases} P_{N}(\theta) & \text{如果 } M \geq 3N, \\ \tilde{P}_{N}(\theta) & \text{如果 } M = 2N, \\ 0 & \text{如果 } M < N. \end{cases}$$

This is clear from what has been said above and from Figure 3.

从上述内容以及图 3 可以清楚地看出这一点。

<center>Figure 3. Breaking symmetry in Lemma 2.4 </center>

<center>图 3. 引理 2.4 中的对称破缺 </center>

The effect is that when $M = 2N$ , the operator $S_{M}$ breaks the symmetry of $P_{N}$ , but in the other cases covered in the lemma, the action of $S_{M}$

其效果是，当 $M = 2N$ 时，算子 $S_{M}$ 打破了 $P_{N}$ 的对称性，但在引理涵盖的其他情况下，$S_{M}$ 的作用

===== Page 104 =====

is relatively benign, since then the outcome is either $P_{N}$ or 0.

相对温和，因为结果要么是 $P_{N}$，要么是 0。

Finally, we need to find a convergent series of positive terms $\sum \alpha_{k}$ and a sequence of integers $\{N_{k}\}$ which increases rapidly enough so that:

$$(i)N_{k + 1} > 3N_{k},$$ $$(ii)\alpha_{k}\log N_{k}\to \infty \mathrm{as}k\to \infty .$$

最后，我们需要找到一个收敛的正项级数 $\sum \alpha_{k}$ 和一个增长足够快的整数序列 $\{N_{k}\}$，使得：

$$(i)N_{k + 1} > 3N_{k},$$ $$(ii)\alpha_{k}\log N_{k}\to \infty \mathrm{as}k\to \infty .$$

We choose (for example) $\alpha_{k} = 1 / k^{2}$ and $N_{k} = 3^{2^{k}}$ which are easily seen to satisfy the above criteria.

我们选择（例如）$\alpha_{k} = 1 / k^{2}$ 和 $N_{k} = 3^{2^{k}}$，它们很容易验证满足上述标准。

Finally, we can write down our desired function. It is

$$f(\theta) = \sum_{k = 1}^{\infty}\alpha_{k}P_{N_{k}}(\theta).$$

Due to the uniform boundedness of the $P_{N}$ (recall that $|P_{N}(\theta)| = |f_{N}(\theta)|)$ the series above converges uniformly to a continuous periodic function. However, by our lemma we get

$$|S_{2N_{m}}(f)(0)|\geq c\alpha_{m}\log N_{m} + O(1)\to \infty \quad \mathrm{as} m\to \infty .$$

最后，我们可以写出我们想要的函数。它是

$$f(\theta) = \sum_{k = 1}^{\infty}\alpha_{k}P_{N_{k}}(\theta).$$

由于 $P_{N}$ 的一致有界性（回忆 $|P_{N}(\theta)| = |f_{N}(\theta)|$），上面的级数一致收敛到一个连续周期函数。然而，根据我们的引理，我们得到

$$|S_{2N_{m}}(f)(0)|\geq c\alpha_{m}\log N_{m} + O(1)\to \infty \quad \mathrm{as} m\to \infty .$$

<center>Figure 4. Symmetry broken in the middle interval $(N_{k},3N_{k})$ </center>

<center>图 4. 在中间区间 $(N_{k},3N_{k})$ 内对称性被打破 </center>

Indeed, the terms that correspond to $N_{k}$ with $k< m$ or $k > m$ contribute $O(1)$ or 0, respectively (because the $P_{N}$ 's are uniformly bounded), while the term that corresponds to $N_{m}$ is in absolute value greater than $c\alpha_{m}\log N_{m}$ because $|\tilde{P}_{N}(\theta)| = |\tilde{f}_{N}(\theta)|\geq c\log N$ . So the partial sums of the Fourier series of $f$ at 0 are not bounded, and we are done since this proves the divergence of the Fourier series of $f$ at $\theta = 0$ . To produce a function whose series diverges at any other preassigned $\theta = \theta_{0}$ , it suffices to consider the function $f(\theta - \theta_{0})$ .

事实上，对应于 $N_{k}$ 且 $k< m$ 或 $k > m$ 的项分别贡献 $O(1)$ 或 0（因为 $P_{N}$ 一致有界），而对应于 $N_{m}$ 的项其绝对值大于 $c\alpha_{m}\log N_{m}$，因为 $|\tilde{P}_{N}(\theta)| = |\tilde{f}_{N}(\theta)|\geq c\log N$。因此 $f$ 的傅里叶级数在 0 处的部分和无界，这就完成了证明，因为这证明了 $f$ 的傅里叶级数在 $\theta = 0$ 处发散。要构造一个级数在任何其他预先指定的 $\theta = \theta_{0}$ 处发散的函数，只需考虑函数 $f(\theta - \theta_{0})$。

## 3 Exercises

## 3 练习

1. Show that the first two examples of inner product spaces, namely $\mathbb{R}^{d}$ and $\mathbb{C}^{d}$ , are complete.

2. 证明前两个内积空间的例子，即 $\mathbb{R}^{d}$ 和 $\mathbb{C}^{d}$，是完备的。

===== Page 105 =====

[Hint: Every Cauchy sequence in $\mathbb{R}$ has a limit.]

[提示：$\mathbb{R}$ 中的每个柯西序列都有一个极限。]

2. Prove that the vector space $\ell^2 (\mathbb{Z})$ is complete.

3. 证明向量空间 $\ell^2 (\mathbb{Z})$ 是完备的。

[Hint: Suppose $A_{k} = \{a_{k,n}\}_{n\in \mathbb{Z}}$ with $k = 1,2,\ldots$ is a Cauchy sequence. Show that for each $n$ , $\{a_{k,n}\}_{k = 1}^{\infty}$ is a Cauchy sequence of complex numbers, therefore it converges to a limit, say $b_{n}$ . By taking partial sums of $\| A_{k} - A_{k^{\prime}}\|$ and letting $k^{\prime}\to \infty$ , show that $\| A_{k} - B\| \to 0$ as $k\to \infty$ , where $B = (\ldots ,b_{- 1},b_{0},b_{1},\ldots)$ . Finally, prove that $B\in \ell^2 (\mathbb{Z})$ .]

[提示：假设 $A_{k} = \{a_{k,n}\}_{n\in \mathbb{Z}}$，$k = 1,2,\ldots$ 是一个柯西序列。证明对于每个 $n$，$\{a_{k,n}\}_{k = 1}^{\infty}$ 是一个复数柯西序列，因此它收敛到一个极限，比如 $b_{n}$。通过对 $\| A_{k} - A_{k^{\prime}}\|$ 取部分和并令 $k^{\prime}\to \infty$，证明当 $k\to \infty$ 时 $\| A_{k} - B\| \to 0$，其中 $B = (\ldots ,b_{- 1},b_{0},b_{1},\ldots)$。最后，证明 $B\in \ell^2 (\mathbb{Z})$。]

3. Construct a sequence of integrable functions $\{f_{k}\}$ on $[0,2\pi ]$ such that

$$\lim_{k\to \infty}\frac{1}{2\pi}\int_{0}^{2\pi}|f_{k}(\theta)|^{2}d\theta = 0$$

but $\lim_{k\to \infty}f_{k}(\theta)$ fails to exist for any $\theta$ .

3. 构造 $[0,2\pi]$ 上的一列可积函数 $\{f_{k}\}$，使得

$$\lim_{k\to \infty}\frac{1}{2\pi}\int_{0}^{2\pi}|f_{k}(\theta)|^{2}d\theta = 0$$

但对任何 $\theta$，$\lim_{k\to \infty}f_{k}(\theta)$ 都不存在。

[Hint: Choose a sequence of intervals $I_{k}\subset [0,2\pi ]$ whose lengths tend to 0, and so that each point belongs to infinitely many of them; then let $f_{k} = \chi_{I_{k}}$ .]

[提示：选择一列区间 $I_{k}\subset [0,2\pi]$，其长度趋于 0，并且每个点属于其中无穷多个；然后令 $f_{k} = \chi_{I_{k}}$。]

4. Recall the vector space $\mathcal{R}$ of integrable functions, with its inner product and norm

$$\| f\| = \left(\frac{1}{2\pi}\int_{0}^{2\pi}|f(x)|^{2}dx\right)^{1 / 2}.$$

4. 回忆可积函数的向量空间 $\mathcal{R}$，及其内积和范数

$$\| f\| = \left(\frac{1}{2\pi}\int_{0}^{2\pi}|f(x)|^{2}dx\right)^{1 / 2}.$$

(a) Show that there exist non-zero integrable functions $f$ for which $\| f\| = 0$ .

(a) 证明存在非零的可积函数 $f$，使得 $\| f\| = 0$。

(b) However, show that if $f\in \mathcal{R}$ with $\| f\| = 0$ , then $f(x) = 0$ whenever $f$ is continuous at $x$ .

(b) 然而，证明如果 $f\in \mathcal{R}$ 且 $\| f\| = 0$，那么只要 $f$ 在 $x$ 处连续，就有 $f(x) = 0$。

(c) Conversely, show that if $f\in \mathcal{R}$ vanishes at all of its points of continuity, then $\| f\| = 0$ .

(c) 反过来，证明如果 $f\in \mathcal{R}$ 在其所有连续点处为零，那么 $\| f\| = 0$。

5. Let

$$f(x) = \begin{cases} \log(1/x) & \text{for } 0 < x \leq 1/2, \\ \text{extended appropriately to } [0,2\pi] \text{ so that it is continuous and } f(0)=0, \end{cases}$$

5. 令

$$f(x) = \begin{cases} \log(1/x) & \text{对于 } 0 < x \leq 1/2, \\ \text{适当延拓到 } [0,2\pi] \text{ 使其连续且 } f(0)=0, \end{cases}$$

and define a sequence of functions in $\mathcal{R}$ by

$$f_n(x) = \begin{cases} \min(f(x), n) & \text{for } x \in [0,2\pi]. \end{cases}$$

并在 $\mathcal{R}$ 中定义一列函数为

$$f_n(x) = \begin{cases} \min(f(x), n) & \text{对于 } x \in [0,2\pi]. \end{cases}$$

===== Page 106 =====

Prove that $\{f_{n}\}_{n = 1}^{\infty}$ is a Cauchy sequence in $\mathcal{R}$ . However, $f$ does not belong to $\mathcal{R}$ .

证明 $\{f_{n}\}_{n = 1}^{\infty}$ 是 $\mathcal{R}$ 中的柯西序列。然而，$f$ 不属于 $\mathcal{R}$。

[Hint: Show that $\int_{a}^{b}(\log \theta)^{2}d\theta \to 0$ if $0< a< b$ and $b\to 0$ , by using the fact that the derivative of $\theta (\log \theta)^{2} - 2\theta \log \theta +2\theta$ is equal to $(\log \theta)^{2}$ .]

[提示：通过利用 $\theta (\log \theta)^{2} - 2\theta \log \theta +2\theta$ 的导数等于 $(\log \theta)^{2}$ 这一事实，证明如果 $0< a< b$ 且 $b\to 0$，则 $\int_{a}^{b}(\log \theta)^{2}d\theta \to 0$。]

6. Consider the sequence $\{a_{k}\}_{k = -\infty}^{\infty}$ defined by

$$a_{0} = 0,\qquad a_{k} = \frac{1}{\log |k|}\quad \text{for } |k| \geq 2.$$

6. 考虑序列 $\{a_{k}\}_{k = -\infty}^{\infty}$，定义为

$$a_{0} = 0,\qquad a_{k} = \frac{1}{\log |k|}\quad \text{对于 } |k| \geq 2.$$

Note that $\{a_{k}\} \in \ell^{2}(\mathbb{Z})$ , but that no Riemann integrable function has $k^{\mathrm{th}}$ Fourier coefficient equal to $a_{k}$ for all $k$ .

注意 $\{a_{k}\} \in \ell^{2}(\mathbb{Z})$，但没有黎曼可积函数对所有 $k$ 的第 $k$ 个傅里叶系数等于 $a_{k}$。

7. Show that the trigonometric series

$$\sum_{n\geq 2}\frac{1}{\log n}\sin nx$$

converges for every $x$ , yet it is not the Fourier series of a Riemann integrable function.

7. 证明三角级数

$$\sum_{n\geq 2}\frac{1}{\log n}\sin nx$$

对每个 $x$ 收敛，但它不是黎曼可积函数的傅里叶级数。

The same is true for $\sum \frac{\sin n x}{n^{\alpha}}$ for $0< \alpha < 1$ , but the case $1 / 2< \alpha < 1$ is more difficult. See Problem 1.

对于 $0< \alpha < 1$，$\sum \frac{\sin n x}{n^{\alpha}}$ 也是如此，但 $1 / 2< \alpha < 1$ 的情况更难。见问题 1。

8. Exercise 6 in Chapter 2 dealt with the sums

$$\sum_{n\mathrm{odd}\geq 1}\frac{1}{n^2}\quad \mathrm{and}\quad \sum_{n = 1}^{\infty}\frac{1}{n^2}.$$

Similar sums can be derived using the methods of this chapter.

8. 第 2 章练习 6 处理了和式

$$\sum_{n\mathrm{odd}\geq 1}\frac{1}{n^2}\quad \mathrm{和}\quad \sum_{n = 1}^{\infty}\frac{1}{n^2}.$$

类似的和式可以使用本章的方法推导出来。

(a) Let $f$ be the function defined on $[- \pi , \pi ]$ by $f(\theta) = |\theta |$ . Use Parseval's identity to find the sums of the following two series:

$$\sum_{n = 0}^{\infty}\frac{1}{(2n + 1)^4}\quad \mathrm{and}\quad \sum_{n = 1}^{\infty}\frac{1}{n^4}.$$

In fact, they are $\pi^{4} / 96$ and $\pi^{4} / 90$ , respectively.

(a) 设 $f$ 是定义在 $[- \pi , \pi]$ 上的函数，$f(\theta) = |\theta|$。使用帕塞瓦尔恒等式求下列两个级数的和：

$$\sum_{n = 0}^{\infty}\frac{1}{(2n + 1)^4}\quad \mathrm{和}\quad \sum_{n = 1}^{\infty}\frac{1}{n^4}.$$

实际上，它们分别是 $\pi^{4} / 96$ 和 $\pi^{4} / 90$。

(b) Consider the $2\pi$ -periodic odd function defined on $[0, \pi ]$ by $f(\theta) = \theta (\pi - \theta)$ . Show that

$$\sum_{n = 0}^{\infty}\frac{1}{(2n + 1)^6} = \frac{\pi^6}{960}\quad \mathrm{and}\quad \sum_{n = 1}^{\infty}\frac{1}{n^6} = \frac{\pi^6}{945}.$$

(b) 考虑定义在 $[0, \pi]$ 上的 $2\pi$ 周期奇函数 $f(\theta) = \theta (\pi - \theta)$。证明

$$\sum_{n = 0}^{\infty}\frac{1}{(2n + 1)^6} = \frac{\pi^6}{960}\quad \mathrm{和}\quad \sum_{n = 1}^{\infty}\frac{1}{n^6} = \frac{\pi^6}{945}.$$

Remark. The general expression when $k$ is even for $\sum_{n = 1}^{\infty}1 / n^{k}$ in terms of $\pi^{k}$ is given in Problem 4. However, finding a formula for the sum $\sum_{n = 1}^{\infty}1 / n^{3}$ , or more generally $\sum_{n = 1}^{\infty}1 / n^{k}$ with $k$ odd, is a famous unresolved question.

注记。当 $k$ 为偶数时，$\sum_{n = 1}^{\infty}1 / n^{k}$ 用 $\pi^{k}$ 表示的一般表达式在问题 4 中给出。然而，找到和 $\sum_{n = 1}^{\infty}1 / n^{3}$，或更一般地 $\sum_{n = 1}^{\infty}1 / n^{k}$（$k$ 为奇数）的公式是一个著名的未解决问题。

===== Page 107 =====

9. Show that for $\alpha$ not an integer, the Fourier series of

$$\frac{\pi}{\sin\pi\alpha} e^{i(\pi -x)\alpha}$$

on $[0,2\pi ]$ is given by

$$\sum_{n = -\infty}^{\infty}\frac{e^{inx}}{n + \alpha}.$$

9. 证明对于非整数 $\alpha$，函数

$$\frac{\pi}{\sin\pi\alpha} e^{i(\pi -x)\alpha}$$

在 $[0,2\pi]$ 上的傅里叶级数为

$$\sum_{n = -\infty}^{\infty}\frac{e^{inx}}{n + \alpha}.$$

Apply Parseval's formula to show that

$$\sum_{n = -\infty}^{\infty}\frac{1}{(n + \alpha)^2} = \frac{\pi^2}{(\sin\pi\alpha)^2}.$$

应用帕塞瓦尔公式证明

$$\sum_{n = -\infty}^{\infty}\frac{1}{(n + \alpha)^2} = \frac{\pi^2}{(\sin\pi\alpha)^2}.$$

10. Consider the example of a vibrating string which we analyzed in Chapter 1. The displacement $u(x,t)$ of the string at time $t$ satisfies the wave equation

$$\frac{1}{c^2}\frac{\partial^2u}{\partial t^2} = \frac{\partial^2u}{\partial x^2},\qquad c^2 = \tau /\rho .$$

10. 考虑我们在第 1 章中分析的振动弦的例子。弦在时间 $t$ 的位移 $u(x,t)$ 满足波动方程

$$\frac{1}{c^2}\frac{\partial^2u}{\partial t^2} = \frac{\partial^2u}{\partial x^2},\qquad c^2 = \tau /\rho .$$

The string is subject to the initial conditions

$$u(x,0) = f(x)\quad \mathrm{and}\quad \frac{\partial u}{\partial t} (x,0) = g(x),$$

where we assume that $f\in C^1$ and $g$ is continuous. We define the total energy of the string by

$$E(t) = \frac{1}{2}\rho \int_{0}^{L}\left(\frac{\partial u}{\partial t}\right)^{2}dx + \frac{1}{2}\tau \int_{0}^{L}\left(\frac{\partial u}{\partial x}\right)^{2}dx.$$

弦满足初始条件

$$u(x,0) = f(x)\quad \mathrm{和}\quad \frac{\partial u}{\partial t} (x,0) = g(x),$$

其中我们假设 $f\in C^1$ 且 $g$ 连续。我们定义弦的总能量为

$$E(t) = \frac{1}{2}\rho \int_{0}^{L}\left(\frac{\partial u}{\partial t}\right)^{2}dx + \frac{1}{2}\tau \int_{0}^{L}\left(\frac{\partial u}{\partial x}\right)^{2}dx.$$

The first term corresponds to the "kinetic energy" of the string (in analogy with $(1 / 2)m v^{2}$ , the kinetic energy of a particle of mass $m$ and velocity $v$ ), and the second term corresponds to its "potential energy."

第一项对应于弦的“动能”（类似于质量为 $m$、速度为 $v$ 的粒子的动能 $(1 / 2)m v^{2}$），第二项对应于其“势能”。

Show that the total energy of the string is conserved, in the sense that $E(t)$ is constant. Therefore,

$$E(t) = E(0) = \frac{1}{2}\rho \int_{0}^{L}g(x)^{2}dx + \frac{1}{2}\tau \int_{0}^{L}f^{\prime}(x)^{2}dx.$$

证明弦的总能量是守恒的，即 $E(t)$ 是常数。因此，

$$E(t) = E(0) = \frac{1}{2}\rho \int_{0}^{L}g(x)^{2}dx + \frac{1}{2}\tau \int_{0}^{L}f^{\prime}(x)^{2}dx.$$

11. The inequalities of Wirtinger and Poincaré establish a relationship between the norm of a function and that of its derivative.

12. 维尔廷格不等式和庞加莱不等式建立了函数范数与其导数范数之间的关系。

===== Page 108 =====

(a) If $f$ is $T$ -periodic, continuous, and piecewise $C^1$ with $\int_0^T f(t)dt = 0$ , show that

$$\int_0^T |f(t)|^2 dt \leq \frac{T^2}{4\pi^2} \int_0^T |f'(t)|^2 dt,$$

with equality if and only if $f(t) = A\sin (2\pi t / T) + B\cos (2\pi t / T)$ . [Hint: Apply Parseval's identity.]

(a) 如果 $f$ 是 $T$ 周期的、连续的、分段 $C^1$ 的，且 $\int_0^T f(t)dt = 0$，证明

$$\int_0^T |f(t)|^2 dt \leq \frac{T^2}{4\pi^2} \int_0^T |f'(t)|^2 dt,$$

当且仅当 $f(t) = A\sin (2\pi t / T) + B\cos (2\pi t / T)$ 时等号成立。[提示：应用帕塞瓦尔恒等式。]

(b) If $f$ is as above and $g$ is just $C^1$ and $T$ -periodic, prove that

$$\left|\int_0^T \overline{f(t)} g(t) dt\right|^2 \leq \frac{T^2}{4\pi^2} \int_0^T |f(t)|^2 dt \int_0^T |g'(t)|^2 dt.$$

(b) 如果 $f$ 如上所述，$g$ 是 $C^1$ 且 $T$ 周期的，证明

$$\left|\int_0^T \overline{f(t)} g(t) dt\right|^2 \leq \frac{T^2}{4\pi^2} \int_0^T |f(t)|^2 dt \int_0^T |g'(t)|^2 dt.$$

(c) For any compact interval $[a,b]$ and any continuously differentiable function $f$ with $f(a) = f(b) = 0$ , show that

$$\int_{a}^{b}|f(t)|^{2}dt\leq \frac{(b - a)^{2}}{\pi^{2}}\int_{a}^{b}|f^{\prime}(t)|^{2}dt.$$

(c) 对于任何紧区间 $[a,b]$ 和任何连续可微函数 $f$，且 $f(a) = f(b) = 0$，证明

$$\int_{a}^{b}|f(t)|^{2}dt\leq \frac{(b - a)^{2}}{\pi^{2}}\int_{a}^{b}|f^{\prime}(t)|^{2}dt.$$

Discuss the case of equality, and prove that the constant $(b - a)^2 /\pi^2$ cannot be improved. [Hint: Extend $f$ to be odd with respect to $a$ and periodic of period $T = 2(b - a)$ so that its integral over an interval of length $T$ is 0. Apply part a) to get the inequality, and conclude that equality holds if and only if $f(t) = A\sin (\pi \frac{t - a}{b - a})$ .

讨论等号成立的情况，并证明常数 $(b - a)^2 /\pi^2$ 不能再改进。[提示：将 $f$ 延拓为关于 $a$ 的奇函数，且周期为 $T = 2(b - a)$，使其在一个长度为 $T$ 的区间上的积分为 0。应用 a) 部分得到不等式，并得出当且仅当 $f(t) = A\sin (\pi \frac{t - a}{b - a})$ 时等号成立。]

12. Prove that $\int_0^\infty \frac{\sin x}{x} dx = \frac{\pi}{2}$ .

13. 证明 $\int_0^\infty \frac{\sin x}{x} dx = \frac{\pi}{2}$。

[Hint: Start with the fact that the integral of $D_N(\theta)$ equals $2\pi$ , and note that the difference $(1 / \sin (\theta /2)) - 2 / \theta$ is continuous on $[-\pi ,\pi ]$ . Apply the Riemann- Lebesgue lemma.]

[提示：从 $D_N(\theta)$ 的积分等于 $2\pi$ 这一事实开始，并注意差值 $(1 / \sin (\theta /2)) - 2 / \theta$ 在 $[-\pi ,\pi]$ 上连续。应用黎曼-勒贝格引理。]

13. Suppose that $f$ is periodic and of class $C^k$ . Show that

$$\hat{f} (n) = o(1 / |n|^k),$$

that is, $|n|^k f(n)$ goes to 0 as $|n| \to \infty$ . This is an improvement over Exercise 10 in Chapter 2.

13. 假设 $f$ 是周期的且属于 $C^k$ 类。证明

$$\hat{f} (n) = o(1 / |n|^k),$$

即当 $|n| \to \infty$ 时，$|n|^k f(n)$ 趋于 0。这是对第 2 章练习 10 的改进。

[Hint: Use the Riemann- Lebesgue lemma.]

[提示：使用黎曼-勒贝格引理。]

14. Prove that the Fourier series of a continuously differentiable function $f$ on the circle is absolutely convergent.

15. 证明圆上连续可微函数 $f$ 的傅里叶级数绝对收敛。

[Hint: Use the Cauchy- Schwarz inequality and Parseval's identity for $f'$ .]

[提示：对 $f'$ 使用柯西-施瓦茨不等式和帕塞瓦尔恒等式。]

15. Let $f$ be $2\pi$ -periodic and Riemann integrable on $[-\pi ,\pi ]$ .

16. 设 $f$ 是 $2\pi$ 周期的且在 $[-\pi ,\pi]$ 上黎曼可积。

===== Page 109 =====

(a) Show that

$$\hat{f} (n) = -\frac{1}{2\pi}\int_{-\pi}^{\pi}f(x + \pi /n)e^{-inx}dx$$

hence

$$\hat{f} (n) = \frac{1}{4\pi}\int_{-\pi}^{\pi}[f(x) - f(x + \pi /n)]e^{-inx}dx.$$

(a) 证明

$$\hat{f} (n) = -\frac{1}{2\pi}\int_{-\pi}^{\pi}f(x + \pi /n)e^{-inx}dx$$

因此

$$\hat{f} (n) = \frac{1}{4\pi}\int_{-\pi}^{\pi}[f(x) - f(x + \pi /n)]e^{-inx}dx.$$

(b) Now assume that $f$ satisfies a Hölder condition of order $\alpha$ , namely

$$|f(x + h) - f(x)| \leq C|h|^{\alpha}$$

for some $0< \alpha \leq 1$ , some $C > 0$ , and all $x,h$ . Use part a) to show that

$$\hat{f} (n) = O(1 / |n|^{\alpha}).$$

(b) 现在假设 $f$ 满足阶为 $\alpha$ 的赫尔德条件，即

$$|f(x + h) - f(x)| \leq C|h|^{\alpha}$$

对某个 $0< \alpha \leq 1$、某个 $C > 0$ 以及所有 $x,h$ 成立。使用 a) 部分证明

$$\hat{f} (n) = O(1 / |n|^{\alpha}).$$

(c) Prove that the above result cannot be improved by showing that the function

$$f(x) = \sum_{k = 0}^{\infty}2^{-k\alpha}e^{i2^k x},$$

where $0< \alpha < 1$ , satisfies

$$|f(x + h) - f(x)| \leq C|h|^{\alpha},$$

and $\hat{f} (N) = 1 / N^{\alpha}$ whenever $N = 2^{k}$

(c) 通过证明函数

$$f(x) = \sum_{k = 0}^{\infty}2^{-k\alpha}e^{i2^k x},$$

其中 $0< \alpha < 1$，满足

$$|f(x + h) - f(x)| \leq C|h|^{\alpha},$$

并且当 $N = 2^{k}$ 时 $\hat{f} (N) = 1 / N^{\alpha}$，从而证明上述结果不能再改进。

[Hint: For (c), break up the sum as follows $f(x + h) - f(x) = \sum_{2^{k} \leq 1 / |h|} + \sum_{2^{k} > 1 / |h|}$ . To estimate the first sum use the fact that $|1 - e^{i\theta}| \leq |\theta |$ whenever $\theta$ is small. To estimate the second sum, use the obvious inequality $|e^{ix} - e^{iy}| \leq 2$ .]

[提示：对于 (c)，将和式分解如下 $f(x + h) - f(x) = \sum_{2^{k} \leq 1 / |h|} + \sum_{2^{k} > 1 / |h|}$。为了估计第一个和，使用当 $\theta$ 很小时 $|1 - e^{i\theta}| \leq |\theta|$ 的事实。为了估计第二个和，使用显然的不等式 $|e^{ix} - e^{iy}| \leq 2$。]

16. Let $f$ be a $2\pi$ -periodic function which satisfies a Lipschitz condition with constant $K$ ; that is,

$$|f(x) - f(y)| \leq K|x - y| \quad \text{for all } x, y.$$

16. 设 $f$ 是一个 $2\pi$ 周期函数，满足常数为 $K$ 的利普希茨条件；即

$$|f(x) - f(y)| \leq K|x - y| \quad \text{对所有 } x, y \text{ 成立}.$$

This is simply the Hölder condition with $\alpha = 1$ , so by the previous exercise, we see that $\hat{f} (n) = O(1 / |n|)$ . Since the harmonic series $\sum 1 / n$ diverges, we cannot say anything (yet) about the absolute convergence of the Fourier series of $f$ . The outline below actually proves that the Fourier series of $f$ converges absolutely and uniformly.

这仅仅是 $\alpha = 1$ 时的赫尔德条件，所以由前一个练习，我们看到 $\hat{f} (n) = O(1 / |n|)$。由于调和级数 $\sum 1 / n$ 发散，我们（还）不能对 $f$ 的傅里叶级数的绝对收敛性说任何话。下面的提纲实际上证明了 $f$ 的傅里叶级数绝对且一致收敛。

===== Page 110 =====

(a) For every positive $h$ we define $g_{h}(x) = f(x + h) - f(x - h)$ . Prove that

$$\frac{1}{2\pi}\int_{0}^{2\pi}|g_{h}(x)|^{2}dx = \sum_{n = -\infty}^{\infty}4|\sin nh|^{2}|\hat{f} (n)|^{2},$$

and show that

$$\sum_{n = -\infty}^{\infty}|\sin nh|^{2}|\hat{f} (n)|^{2}\leq K^{2}h^{2}.$$

(a) 对每个正数 $h$，定义 $g_{h}(x) = f(x + h) - f(x - h)$。证明

$$\frac{1}{2\pi}\int_{0}^{2\pi}|g_{h}(x)|^{2}dx = \sum_{n = -\infty}^{\infty}4|\sin nh|^{2}|\hat{f} (n)|^{2},$$

并证明

$$\sum_{n = -\infty}^{\infty}|\sin nh|^{2}|\hat{f} (n)|^{2}\leq K^{2}h^{2}.$$

(b) Let $p$ be a positive integer. By choosing $h = \pi /2^{p + 1}$ , show that

$$\sum_{2^{p - 1}< |n|\leq 2^{p}}|\hat{f} (n)|^{2}\leq \frac{K^{2}\pi^{2}}{2^{2p + 1}}.$$

(b) 设 $p$ 为正整数。通过选择 $h = \pi /2^{p + 1}$，证明

$$\sum_{2^{p - 1}< |n|\leq 2^{p}}|\hat{f} (n)|^{2}\leq \frac{K^{2}\pi^{2}}{2^{2p + 1}}.$$

(c) Estimate $\sum_{2^{p - 1}< |n|\leq 2^{p}}|\hat{f} (n)|$ , and conclude that the Fourier series of $f$ converges absolutely, hence uniformly. [Hint: Use the Cauchy-Schwarz inequality to estimate the sum.]

(c) 估计 $\sum_{2^{p - 1}< |n|\leq 2^{p}}|\hat{f} (n)|$，并得出结论 $f$ 的傅里叶级数绝对收敛，因此一致收敛。[提示：使用柯西-施瓦茨不等式来估计和式。]

(d) In fact, modify the argument slightly to prove Bernstein's theorem: If $f$ satisfies a Hölder condition of order $\alpha >1 / 2$ , then the Fourier series of $f$ converges absolutely.

(d) 实际上，稍微修改论证来证明伯恩斯坦定理：如果 $f$ 满足阶数 $\alpha >1 / 2$ 的赫尔德条件，那么 $f$ 的傅里叶级数绝对收敛。

17. If $f$ is a bounded monotonic function on $[-\pi ,\pi ]$ , then

$$\hat{f} (n) = O(1 / |n|).$$

17. 如果 $f$ 是 $[-\pi ,\pi]$ 上的有界单调函数，那么

$$\hat{f} (n) = O(1 / |n|).$$

[Hint: One may assume that $f$ is increasing, and say $|f|\leq M$ . First check that the Fourier coefficients of the characteristic function of $[a,b]$ satisfy $O(1 / |n|)$ . Now show that a sum of the form

$$\sum_{k = 1}^{N}\alpha_{k}\chi_{[a_{k},a_{k + 1}]}(x)$$

with $-\pi = a_{1}< a_{2}< \dots < a_{N}< a_{N + 1} = \pi$ and $- M\leq \alpha_{1}\leq \dots \leq \alpha_{N}\leq M$ has Fourier coefficients that are $O(1 / |n|)$ uniformly in $N$ . Summing by parts one gets a telescopic sum $\sum (\alpha_{k + 1} - \alpha_{k})$ which can be bounded by $2M$ . Now approximate $f$ by functions of the above type.]

[提示：可以假设 $f$ 是递增的，并且设 $|f|\leq M$。首先验证 $[a,b]$ 的特征函数的傅里叶系数满足 $O(1 / |n|)$。现在证明形式为

$$\sum_{k = 1}^{N}\alpha_{k}\chi_{[a_{k},a_{k + 1}]}(x)$$

的和，其中 $-\pi = a_{1}< a_{2}< \dots < a_{N}< a_{N + 1} = \pi$ 且 $- M\leq \alpha_{1}\leq \dots \leq \alpha_{N}\leq M$，其傅里叶系数关于 $N$ 一致地为 $O(1 / |n|)$。通过分部求和得到一个可以受 $2M$ 控制的伸缩和 $\sum (\alpha_{k + 1} - \alpha_{k})$。然后用上述类型的函数逼近 $f$。]

18. Here are a few things we have learned about the decay of Fourier coefficients:

(a) if $f$ is of class $C^{k}$ , then $\hat{f} (n) = o(1 / |n|^{k})$ ;

(b) if $f$ is Lipschitz, then $\hat{f} (n) = O(1 / |n|)$ ;

18. 以下是我们学到的关于傅里叶系数衰减的一些知识：

(a) 如果 $f$ 属于 $C^{k}$ 类，则 $\hat{f} (n) = o(1 / |n|^{k})$；

(b) 如果 $f$ 是利普希茨的，则 $\hat{f} (n) = O(1 / |n|)$；

===== Page 111 =====

(c) if $f$ is monotonic, then $\hat{f} (n) = O(1 / |n|)$ ;

(d) if $f$ is satisfies a Hölder condition with exponent $\alpha$ where $0< \alpha < 1$ , then $\hat{f} (n) = O(1 / |n|^{\alpha})$ ;

(e) if $f$ is merely Riemann integrable, then $\sum |\hat{f} (n)|^2 < \infty$ and therefore $\hat{f} (n) = o(1)$ .

(c) 如果 $f$ 是单调的，则 $\hat{f} (n) = O(1 / |n|)$；

(d) 如果 $f$ 满足指数为 $\alpha$（$0< \alpha < 1$）的赫尔德条件，则 $\hat{f} (n) = O(1 / |n|^{\alpha})$；

(e) 如果 $f$ 仅仅是黎曼可积的，则 $\sum |\hat{f} (n)|^2 < \infty$，因此 $\hat{f} (n) = o(1)$。

Nevertheless, show that the Fourier coefficients of a continuous function can tend to 0 arbitrarily slowly by proving that for every sequence of nonnegative real numbers $\{\epsilon_{n}\}$ converging to 0, there exists a continuous function $f$ such that $|\hat{f} (n)|\geq \epsilon_{n}$ for infinitely many values of $n$ .

尽管如此，通过证明对于每个收敛到 0 的非负实数序列 $\{\epsilon_{n}\}$，存在一个连续函数 $f$，使得对无穷多个 $n$ 有 $|\hat{f} (n)|\geq \epsilon_{n}$，来证明连续函数的傅里叶系数可以任意慢地趋于 0。

[Hint: Choose a subsequence $\{\epsilon_{n_k}\}$ so that $\sum_{k}\epsilon_{n_k}< \infty$ .]

[提示：选择一个子序列 $\{\epsilon_{n_k}\}$，使得 $\sum_{k}\epsilon_{n_k}< \infty$。]

19. Give another proof that the sum $\sum_{0< |n|\leq N}e^{inx} / n$ is uniformly bounded in $N$ and $x\in [- \pi ,\pi ]$ by using the fact that

$$\frac{1}{2i}\sum_{0< |n|\leq N}\frac{e^{inx}}{n} = \sum_{n = 1}^{N}\frac{\sin nx}{n} = \frac{1}{2}\int_{0}^{x}(D_{N}(t) - 1)dt,$$

where $D_{N}$ is the Dirichlet kernel. Now use the fact that $\int_{0}^{\infty}\frac{\sin t}{t} dt< \infty$ which was proved in Exercise 12.

19. 利用以下事实给出和式 $\sum_{0< |n|\leq N}e^{inx} / n$ 关于 $N$ 和 $x\in [- \pi ,\pi]$ 一致有界的另一个证明：

$$\frac{1}{2i}\sum_{0< |n|\leq N}\frac{e^{inx}}{n} = \sum_{n = 1}^{N}\frac{\sin nx}{n} = \frac{1}{2}\int_{0}^{x}(D_{N}(t) - 1)dt,$$

其中 $D_{N}$ 是狄利克雷核。然后使用在练习 12 中证明的 $\int_{0}^{\infty}\frac{\sin t}{t} dt< \infty$ 这一事实。

20. Let $f(x)$ denote the sawtooth function defined by $f(x) = (\pi -x) / 2$ on the interval $(0,2\pi)$ with $f(0) = 0$ and extended by periodicity to all of $\mathbb{R}$ . The Fourier series of $f$ is

$$f(x)\sim \frac{1}{2i}\sum_{|n|\neq 0}\frac{e^{inx}}{n} = \sum_{n = 1}^{\infty}\frac{\sin nx}{n},$$

and $f$ has a jump discontinuity at the origin with

$$f(0^{+}) = \frac{\pi}{2},\qquad f(0^{-}) = -\frac{\pi}{2},\qquad \mathrm{and~hence}\qquad f(0^{+}) - f(0^{-}) = \pi .$$

20. 设 $f(x)$ 表示锯齿函数，在区间 $(0,2\pi)$ 上定义为 $f(x) = (\pi -x) / 2$，$f(0) = 0$，并通过周期性延拓到整个 $\mathbb{R}$。$f$ 的傅里叶级数为

$$f(x)\sim \frac{1}{2i}\sum_{|n|\neq 0}\frac{e^{inx}}{n} = \sum_{n = 1}^{\infty}\frac{\sin nx}{n},$$

且 $f$ 在原点处有一个跳跃间断，满足

$$f(0^{+}) = \frac{\pi}{2},\qquad f(0^{-}) = -\frac{\pi}{2},\qquad \mathrm{因此}\qquad f(0^{+}) - f(0^{-}) = \pi .$$

Show that

$$\max_{0< x\leq \pi /N}S_{N}(f)(x) - \frac{\pi}{2} = \int_{0}^{\pi}\frac{\sin t}{t} dt - \frac{\pi}{2},$$

which is roughly $9\%$ of the jump $\pi$ . This result is a manifestation of Gibbs's phenomenon which states that near a jump discontinuity, the Fourier series of a function overshoots (or undershoots) it by approximately $9\%$ of the jump.

证明

$$\max_{0< x\leq \pi /N}S_{N}(f)(x) - \frac{\pi}{2} = \int_{0}^{\pi}\frac{\sin t}{t} dt - \frac{\pi}{2},$$

这大约是跳跃量 $\pi$ 的 $9\%$。这个结果体现了吉布斯现象，它表明在跳跃间断点附近，函数的傅里叶级数会以大约跳跃量 $9\%$ 的幅度过冲（或下冲）。

[Hint: Use the expression for $S_{N}(f)$ given in Exercise 19. ]

[提示：使用练习 19 中给出的 $S_{N}(f)$ 表达式。]

===== Page 112 =====

## 4 Problems

## 4 问题

1. For each $0< \alpha < 1$ the series

$$\sum_{n = 1}^{\infty}\frac{\sin n x}{n^{\alpha}}$$

converges for every $x$ but is not the Fourier series of a Riemann integrable function.

1. 对于每个 $0< \alpha < 1$，级数

$$\sum_{n = 1}^{\infty}\frac{\sin n x}{n^{\alpha}}$$

对每个 $x$ 收敛，但不是黎曼可积函数的傅里叶级数。

(a) If the conjugate Dirichlet kernel is defined by

$$\tilde{D}_N(x) = \sum_{n = 1}^N \sin nx = \frac{\cos(x/2) - \cos((N+1/2)x)}{2\sin(x/2)},$$

(a) 如果共轭狄利克雷核定义为

$$\tilde{D}_N(x) = \sum_{n = 1}^N \sin nx = \frac{\cos(x/2) - \cos((N+1/2)x)}{2\sin(x/2)},$$

then show that

$$\tilde{D}_N(x) = \frac{\cos(x / 2) - \cos((N + 1 / 2)x)}{\sin(x / 2)},$$

and

$$\int_{-\pi}^{\pi}|\tilde{D}_N(x)|dx\leq c\log N.$$

那么证明

$$\tilde{D}_N(x) = \frac{\cos(x / 2) - \cos((N + 1 / 2)x)}{\sin(x / 2)},$$

并且

$$\int_{-\pi}^{\pi}|\tilde{D}_N(x)|dx\leq c\log N.$$

(b) As a result, if $f$ is Riemann integrable, then

$$(f*\tilde{D}_N)(0) = O(\log N).$$

(b) 因此，如果 $f$ 是黎曼可积的，那么

$$(f*\tilde{D}_N)(0) = O(\log N).$$

(c) In the present case, this leads to

$$\sum_{n = 1}^{N}\frac{1}{n^{\alpha}} = O(\log N),$$

which is a contradiction.

(c) 在当前情况下，这导致

$$\sum_{n = 1}^{N}\frac{1}{n^{\alpha}} = O(\log N),$$

这是一个矛盾。

2. An important fact we have proved is that the family $\{e^{inx}\}_{n\in \mathbb{Z}}$ is orthonormal in $\mathcal{R}$ and it is also complete, in the sense that the Fourier series of $f$ converges to $f$ in the norm. In this exercise, we consider another family possessing these same properties.

3. 我们已经证明的一个重要事实是，族 $\{e^{inx}\}_{n\in \mathbb{Z}}$ 在 $\mathcal{R}$ 中是正交归一的，并且也是完备的，即 $f$ 的傅里叶级数在范数意义下收敛到 $f$。在这个练习中，我们考虑另一个具有相同性质的族。

On $[- 1,1]$ define

$$L_{n}(x) = \frac{d^{n}}{dx^{n}} (x^{2} - 1)^{n},\qquad n = 0,1,2,\ldots$$

Then $L_{n}$ is a polynomial of degree $n$ which is called the $n^{\mathrm{th}}$ Legendre polynomial.

在 $[- 1,1]$ 上定义

$$L_{n}(x) = \frac{d^{n}}{dx^{n}} (x^{2} - 1)^{n},\qquad n = 0,1,2,\ldots$$

那么 $L_{n}$ 是一个 $n$ 次多项式，称为第 $n$ 个勒让德多项式。

===== Page 113 =====

(a) Show that if $f$ is indefinitely differentiable on $[-1,1]$ , then

$$\int_{-1}^{1}L_{n}(x)f(x)dx = (-1)^{n}\int_{-1}^{1}(x^{2} - 1)^{n}f^{(n)}(x)dx.$$

In particular, show that $L_{n}$ is orthogonal to $x^{m}$ whenever $m< n$ . Hence $\{L_{n}\}_{n = 0}^{\infty}$ is an orthogonal family.

(a) 证明如果 $f$ 在 $[-1,1]$ 上无限可微，那么

$$\int_{-1}^{1}L_{n}(x)f(x)dx = (-1)^{n}\int_{-1}^{1}(x^{2} - 1)^{n}f^{(n)}(x)dx.$$

特别地，证明当 $m< n$ 时，$L_{n}$ 与 $x^{m}$ 正交。因此 $\{L_{n}\}_{n = 0}^{\infty}$ 是一个正交族。

(b) Show that

$$\| L_{n}\|^{2} = \int_{-1}^{1}|L_{n}(x)|^{2}dx = \frac{(n!)^{2}2^{2n + 1}}{2n + 1}.$$

(b) 证明

$$\| L_{n}\|^{2} = \int_{-1}^{1}|L_{n}(x)|^{2}dx = \frac{(n!)^{2}2^{2n + 1}}{2n + 1}.$$

[Hint: First, note that $\| L_{n}\|^{2} = (- 1)^{n}(2n)! \int_{- 1}^{1}(x^{2} - 1)^{n}dx$ . Write $(x^{2} - 1)^{n} = (x - 1)^{n}(x + 1)^{n}$ and integrate by parts $n$ times to calculate this last integral.]

[提示：首先，注意 $\| L_{n}\|^{2} = (- 1)^{n}(2n)! \int_{- 1}^{1}(x^{2} - 1)^{n}dx$。将 $(x^{2} - 1)^{n} = (x - 1)^{n}(x + 1)^{n}$ 并分部积分 $n$ 次来计算这最后一个积分。]

(c) Prove that any polynomial of degree $n$ that is orthogonal to $1, x, x^{2}, \ldots , x^{n - 1}$ is a constant multiple of $L_{n}$ .

(c) 证明任何与 $1, x, x^{2}, \ldots , x^{n - 1}$ 正交的 $n$ 次多项式都是 $L_{n}$ 的常数倍。

(d) Let $\mathcal{L}_{n} = L_{n} / \| L_{n}\|$ , which are the normalized Legendre polynomials. Prove that $\{\mathcal{L}_{n}\}$ is the family obtained by applying the "Gram-Schmidt process" to $\{1, x, \ldots , x^{n}, \ldots \}$ , and conclude that every Riemann integrable function $f$ on $[-1,1]$ has a Legendre expansion

$$\sum_{n = 0}^{\infty}\langle f,\mathcal{L}_{n}\rangle \mathcal{L}_{n}$$

which converges to $f$ in the mean- square sense.

(d) 令 $\mathcal{L}_{n} = L_{n} / \| L_{n}\|$，它们是归一化的勒让德多项式。证明 $\{\mathcal{L}_{n}\}$ 是对 $\{1, x, \ldots , x^{n}, \ldots \}$ 应用“格拉姆-施密特过程”得到的族，并得出结论：$[-1,1]$ 上的每个黎曼可积函数 $f$ 都有一个勒让德展开式

$$\sum_{n = 0}^{\infty}\langle f,\mathcal{L}_{n}\rangle \mathcal{L}_{n}$$

该展开式在均方意义下收敛到 $f$。

3. Let $\alpha$ be a complex number not equal to an integer.

4. 设 $\alpha$ 是一个不等于整数的复数。

(a) Calculate the Fourier series of the $2\pi$ -periodic function defined on $[-\pi ,\pi ]$ by $f(x) = \cos (\alpha x)$ .

(a) 计算定义在 $[-\pi ,\pi]$ 上的 $2\pi$ 周期函数 $f(x) = \cos (\alpha x)$ 的傅里叶级数。

(b) Prove the following formulas due to Euler:

$$\sum_{n = 1}^{\infty}\frac{1}{n^{2} - \alpha^{2}} = \frac{1}{2\alpha^{2}} -\frac{\pi}{2\alpha\tan(\alpha\pi)}.$$

For all $u \in \mathbb{C} - \pi \mathbb{Z}$ ,

$$\cot u = \frac{1}{u} +2\sum_{n = 1}^{\infty}\frac{u}{u^{2} - n^{2}\pi^{2}}.$$

(b) 证明下列由欧拉给出的公式：

$$\sum_{n = 1}^{\infty}\frac{1}{n^{2} - \alpha^{2}} = \frac{1}{2\alpha^{2}} -\frac{\pi}{2\alpha\tan(\alpha\pi)}.$$

对所有 $u \in \mathbb{C} - \pi \mathbb{Z}$，

$$\cot u = \frac{1}{u} +2\sum_{n = 1}^{\infty}\frac{u}{u^{2} - n^{2}\pi^{2}}.$$

===== Page 114 =====

(c) Show that for all $\alpha \in \mathbb{C} - \mathbb{Z}$ we have

$$\frac{\alpha\pi}{\sin(\alpha\pi)} = 1 + 2\alpha^2\sum_{n = 1}^{\infty}\frac{(-1)^{n - 1}}{n^2 - \alpha^2}.$$

(c) 证明对所有 $\alpha \in \mathbb{C} - \mathbb{Z}$，有

$$\frac{\alpha\pi}{\sin(\alpha\pi)} = 1 + 2\alpha^2\sum_{n = 1}^{\infty}\frac{(-1)^{n - 1}}{n^2 - \alpha^2}.$$

(d) For all $0< \alpha < 1$ , show that

$$\int_{0}^{\infty}\frac{t^{\alpha - 1}}{t + 1} dt = \frac{\pi}{\sin(\alpha\pi)}.$$

(d) 对所有 $0< \alpha < 1$，证明

$$\int_{0}^{\infty}\frac{t^{\alpha - 1}}{t + 1} dt = \frac{\pi}{\sin(\alpha\pi)}.$$

[Hint: Split the integral as $\int_{0}^{1} + \int_{1}^{\infty}$ and change variables $t = 1 / u$ in the second integral. Now both integrals are of the form

$$\int_{0}^{1}\frac{t^{\gamma - 1}}{1 + t} dt,\qquad 0< \gamma < 1,$$

which one can show is equal to $\sum_{k = 0}^{\infty}\frac{(- 1)^{k}}{k + \gamma}$ . Use part (c) to conclude the proof.]

[提示：将积分拆分为 $\int_{0}^{1} + \int_{1}^{\infty}$，并在第二个积分中做变量替换 $t = 1 / u$。现在两个积分都具有形式

$$\int_{0}^{1}\frac{t^{\gamma - 1}}{1 + t} dt,\qquad 0< \gamma < 1,$$

可以证明它等于 $\sum_{k = 0}^{\infty}\frac{(- 1)^{k}}{k + \gamma}$。使用 (c) 部分得出结论。]

4. In this problem, we find the formula for the sum of the series

$$\sum_{n = 1}^{\infty}\frac{1}{n^k}$$

where $k$ is any even integer. These sums are expressed in terms of the Bernoulli numbers; the related Bernoulli polynomials are discussed in the next problem.

4. 在这个问题中，我们找出级数

$$\sum_{n = 1}^{\infty}\frac{1}{n^k}$$

的和的公式，其中 $k$ 是任何偶数。这些和用伯努利数表示；相关的伯努利多项式将在下一个问题中讨论。

Define the Bernoulli numbers $B_{n}$ by the formula

$$\frac{z}{e^z - 1} = \sum_{n = 0}^{\infty}\frac{B_n}{n!} z^n.$$

通过公式定义伯努利数 $B_{n}$

$$\frac{z}{e^z - 1} = \sum_{n = 0}^{\infty}\frac{B_n}{n!} z^n.$$

(a) Show that $B_{0} = 1$ , $B_{1} = -1 / 2$ , $B_{2} = 1 / 6$ , $B_{3} = 0$ , $B_{4} = -1 / 30$ , and $B_{5} = 0$ .

(a) 证明 $B_{0} = 1$，$B_{1} = -1 / 2$，$B_{2} = 1 / 6$，$B_{3} = 0$，$B_{4} = -1 / 30$，且 $B_{5} = 0$。

(b) Show that for $n \geq 1$ we have

$$B_{n} = -\frac{1}{n + 1}\sum_{k = 0}^{n - 1}\binom{n + 1}{k} B_{k}.$$

(b) 证明对于 $n \geq 1$，有

$$B_{n} = -\frac{1}{n + 1}\sum_{k = 0}^{n - 1}\binom{n + 1}{k} B_{k}.$$

(c) By writing

$$\frac{z}{e^z - 1} = 1 - \frac{z}{2} +\sum_{n = 2}^{\infty}\frac{B_n}{n!} z^n,$$

(c) 通过写成

$$\frac{z}{e^z - 1} = 1 - \frac{z}{2} +\sum_{n = 2}^{\infty}\frac{B_n}{n!} z^n,$$

===== Page 115 =====

show that $B_{n} = 0$ if $n$ is odd and $>1$ . Also prove that

$$z\cot z = 1 + \sum_{n = 1}^{\infty}(-1)^{n}\frac{2^{2n}B_{2n}}{(2n)!} z^{2n}.$$

证明若 $n$ 为奇数且 $>1$，则 $B_{n} = 0$。同时证明

$$z\cot z = 1 + \sum_{n = 1}^{\infty}(-1)^{n}\frac{2^{2n}B_{2n}}{(2n)!} z^{2n}.$$

(d) The zeta function is defined by

$$\zeta (s) = \sum_{n = 1}^{\infty}\frac{1}{n^{s}},\quad \mathrm{for~all~}s > 1.$$

(d) 泽塔函数定义为

$$\zeta (s) = \sum_{n = 1}^{\infty}\frac{1}{n^{s}},\quad \mathrm{对所有~}s > 1.$$

Deduce from the result in (c), and the expression for the cotangent function obtained in the previous problem, that

$$x\cot x = 1 - 2\sum_{m = 1}^{\infty}\frac{\zeta(2m)}{\pi^{2m}} x^{2m}.$$

从 (c) 的结果以及上一个问题中得到的余切函数表达式推导出

$$x\cot x = 1 - 2\sum_{m = 1}^{\infty}\frac{\zeta(2m)}{\pi^{2m}} x^{2m}.$$

(e) Conclude that

$$2\zeta (2m) = (-1)^{m + 1}\frac{(2\pi)^{2m}}{(2m)!} B_{2m}.$$

(e) 得出结论

$$2\zeta (2m) = (-1)^{m + 1}\frac{(2\pi)^{2m}}{(2m)!} B_{2m}.$$

5. Define the Bernoulli polynomials $B_{n}(x)$ by the formula

$$\frac{z e^{xz}}{e^{z} - 1} = \sum_{n = 0}^{\infty}\frac{B_{n}(x)}{n!} z^{n}.$$

5. 通过公式定义伯努利多项式 $B_{n}(x)$

$$\frac{z e^{xz}}{e^{z} - 1} = \sum_{n = 0}^{\infty}\frac{B_{n}(x)}{n!} z^{n}.$$

(a) The functions $B_{n}(x)$ are polynomials in $x$ and

$$B_{n}(x) = \sum_{k = 0}^{n}\binom{n}{k}B_{k}x^{n - k}.$$

Show that $B_{0}(x) = 1$ , $B_{1}(x) = x - 1 / 2$ , $B_{2}(x) = x^{2} - x + 1 / 6$ , and $B_{3}(x) = x^{3} - \frac{3}{2} x^{2} + \frac{1}{2} x$ .

(a) 函数 $B_{n}(x)$ 是 $x$ 的多项式，且

$$B_{n}(x) = \sum_{k = 0}^{n}\binom{n}{k}B_{k}x^{n - k}.$$

证明 $B_{0}(x) = 1$，$B_{1}(x) = x - 1 / 2$，$B_{2}(x) = x^{2} - x + 1 / 6$，且 $B_{3}(x) = x^{3} - \frac{3}{2} x^{2} + \frac{1}{2} x$。

(b) If $n \geq 1$ , then

$$B_{n}(x + 1) - B_{n}(x) = nx^{n - 1},$$

and if $n \geq 2$ , then

$$B_{n}(0) = B_{n}(1) = B_{n}.$$

(b) 如果 $n \geq 1$，那么

$$B_{n}(x + 1) - B_{n}(x) = nx^{n - 1},$$

并且如果 $n \geq 2$，那么

$$B_{n}(0) = B_{n}(1) = B_{n}.$$

(c) Define $S_{m}(n) = 1^{m} + 2^{m} + \dots +(n - 1)^{m}$ . Show that

$$(m + 1)S_{m}(n) = B_{m + 1}(n) - B_{m + 1}.$$

(c) 定义 $S_{m}(n) = 1^{m} + 2^{m} + \dots +(n - 1)^{m}$。证明

$$(m + 1)S_{m}(n) = B_{m + 1}(n) - B_{m + 1}.$$

===== Page 116 =====

(d) Prove that the Bernoulli polynomials are the only polynomials that satisfy

$$(i) B_0(x) = 1,$$ $$(ii) B_n'(x) = nB_{n - 1}(x) \text{for} n \geq 1,$$ $$(iii) \int_0^1 B_n(x)dx = 0 \text{for} n \geq 1, \text{and show that from (b) one obtains}$$ $$\int_x^{x + 1} B_n(t)dt = x^n.$$

(d) 证明伯努利多项式是唯一满足以下条件的多项式

$$(i) B_0(x) = 1,$$ $$(ii) B_n'(x) = nB_{n - 1}(x) \text{对于 } n \geq 1,$$ $$(iii) \int_0^1 B_n(x)dx = 0 \text{对于 } n \geq 1, \text{并从 (b) 得到}$$ $$\int_x^{x + 1} B_n(t)dt = x^n.$$

(e) Calculate the Fourier series of $B_{1}(x)$ to conclude that for $0 < x < 1$ we have

$$B_{1}(x) = x - 1 / 2 = \frac{-1}{\pi}\sum_{k = 1}^{\infty}\frac{\sin(2\pi kx)}{k}.$$

(e) 计算 $B_{1}(x)$ 的傅里叶级数，得出结论：对于 $0 < x < 1$，有

$$B_{1}(x) = x - 1 / 2 = \frac{-1}{\pi}\sum_{k = 1}^{\infty}\frac{\sin(2\pi kx)}{k}.$$

Integrate and conclude that

$$B_{2n}(x) = (-1)^{n + 1}\frac{2(2n)!}{(2\pi)^{2n}}\sum_{k = 1}^{\infty}\frac{\cos(2\pi kx)}{k^{2n}},$$ $$B_{2n + 1}(x) = (-1)^{n + 1}\frac{2(2n + 1)!}{(2\pi)^{2n + 1}}\sum_{k = 1}^{\infty}\frac{\sin(2\pi kx)}{k^{2n + 1}}.$$

积分并得出结论

$$B_{2n}(x) = (-1)^{n + 1}\frac{2(2n)!}{(2\pi)^{2n}}\sum_{k = 1}^{\infty}\frac{\cos(2\pi kx)}{k^{2n}},$$ $$B_{2n + 1}(x) = (-1)^{n + 1}\frac{2(2n + 1)!}{(2\pi)^{2n + 1}}\sum_{k = 1}^{\infty}\frac{\sin(2\pi kx)}{k^{2n + 1}}.$$

Finally, show that for $0 < x < 1$

$$B_{n}(x) = -\frac{n!}{(2\pi i)^{n}}\sum_{k\neq 0}e^{2\pi ikx}.$$

最后，证明对于 $0 < x < 1$

$$B_{n}(x) = -\frac{n!}{(2\pi i)^{n}}\sum_{k\neq 0}e^{2\pi ikx}.$$

We observe that the Bernoulli polynomials are, up to normalization, successive integrals of the sawtooth function.

我们注意到，伯努利多项式是锯齿函数在归一化意义下的逐次积分。