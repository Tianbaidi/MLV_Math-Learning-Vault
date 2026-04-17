

===== Page 146 =====

5 The Fourier Transform on $\mathbb{R}$

# 5 实数轴上的傅里叶变换

The theory of Fourier series and integrals has always had major difficulties and necessitated a large mathematical apparatus in dealing with questions of convergence. It engendered the development of methods of summation, although these did not lead to a completely satisfactory solution of the problem.... For the Fourier transform, the introduction of distributions (hence the space $\mathcal{S}$ ) is inevitable either in an explicit or hidden form.... As a result one may obtain all that is desired from the point of view of the continuity and inversion of the Fourier transform.

L. Schwartz, 1950

傅里叶级数和积分理论在处理收敛问题时总是遇到重大困难，并且需要庞大的数学工具。它催生了求和方法的发展，尽管这些方法并未导致问题的完全令人满意的解决……对于傅里叶变换而言，引入分布（从而引入空间 $\mathcal{S}$ ）无论是显式还是隐式都是不可避免的……因此，从傅里叶变换的连续性和反演的角度，人们可以获得所有期望的结果。

L. 施瓦茨，1950年

The theory of Fourier series applies to functions on the circle, or equivalently, periodic functions on $\mathbb{R}$ . In this chapter, we develop an analogous theory for functions on the entire real line which are non- periodic. The functions we consider will be suitably "small" at infinity. There are several ways of defining an appropriate notion of "smallness," but it will nevertheless be vital to assume some sort of vanishing at infinity.

傅里叶级数理论适用于圆上的函数，等价地，适用于 $\mathbb{R}$ 上的周期函数。在本章中，我们为整个实轴上的非周期函数发展类似的理论。我们考虑的函数在无穷远处将适当地“小”。定义“小”的适当概念有几种方法，但无论如何，假设某种在无穷远处的消失是至关重要的。

On the one hand, recall that the Fourier series of a periodic function associates a sequence of numbers, namely the Fourier coefficients, to that function; on the other hand, given a suitable function $f$ on $\mathbb{R}$ , the analogous object associated to $f$ will in fact be another function $\hat{f}$ on $\mathbb{R}$ which is called the Fourier transform of $f$ . Since the Fourier transform of a function on $\mathbb{R}$ is again a function on $\mathbb{R}$ , one can observe a symmetry between a function and its Fourier transform, whose analogue is not as apparent in the setting of Fourier series.

一方面，回忆周期函数的傅里叶级数给该函数关联一个数列，即傅里叶系数；另一方面，给定 $\mathbb{R}$ 上的一个合适函数 $f$ ，与 $f$ 关联的类似对象实际上是 $\mathbb{R}$ 上的另一个函数 $\hat{f}$ ，称为 $f$ 的傅里叶变换。由于 $\mathbb{R}$ 上函数的傅里叶变换仍然是 $\mathbb{R}$ 上的函数，可以观察到函数与其傅里叶变换之间的对称性，这种对称性在傅里叶级数的背景下不那么明显。

Roughly speaking, the Fourier transform is a continuous version of the Fourier coefficients. Recall that the Fourier coefficients $a_{n}$ of a function $f$ defined on the circle are given by

$$a_{n} = \int_{0}^{1}f(x)e^{-2\pi inx}dx,$$

粗略地说，傅里叶变换是傅里叶系数的连续版本。回忆定义在圆上的函数 $f$ 的傅里叶系数 $a_{n}$ 由下式给出：

$$a_{n} = \int_{0}^{1}f(x)e^{-2\pi inx}dx,$$

===== Page 147 =====

and then in the appropriate sense we have

$$f(x) = \sum_{n = -\infty}^{\infty}a_{n}e^{2\pi inx}.$$

然后，在适当的意义下，我们有

$$f(x) = \sum_{n = -\infty}^{\infty}a_{n}e^{2\pi inx}.$$

Here we have replaced $\theta$ by $2\pi x$ , as we have frequently done previously.

这里我们将 $\theta$ 替换为 $2\pi x$ ，正如我们之前经常做的那样。

Now, consider the following analogy where we replace all of the discrete symbols (such as integers and sums) by their continuous counterparts (such as real numbers and integrals). In other words, given a function $f$ on all of $\mathbb{R}$ , we define its Fourier transform by changing the domain of integration from the circle to all of $\mathbb{R}$ , and by replacing $n \in \mathbb{Z}$ by $\xi \in \mathbb{R}$ in (1), that is, by setting

$$\hat{f} (\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}dx. \quad (3)$$

现在，考虑如下类比：将所有离散符号（如整数和求和）替换为它们的连续对应物（如实数和积分）。换句话说，给定整个 $\mathbb{R}$ 上的函数 $f$ ，我们通过将积分域从圆改为整个 $\mathbb{R}$ ，并将 (1) 中的 $n \in \mathbb{Z}$ 替换为 $\xi \in \mathbb{R}$ 来定义其傅里叶变换，即令

$$\hat{f} (\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}dx. \quad (3)$$

We push our analogy further, and consider the following continuous version of (2): replacing the sum by an integral, and $a_{n}$ by $\hat{f} (\xi)$ , leads to the Fourier inversion formula,

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi ix\xi}d\xi . \quad (4)$$

我们将类比推进一步，考虑 (2) 的如下连续版本：将求和替换为积分，并将 $a_{n}$ 替换为 $\hat{f} (\xi)$ ，得到傅里叶反演公式，

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi ix\xi}d\xi . \quad (4)$$

Under a suitable hypotheses on $f$ , the identity (4) actually holds, and much of the theory in this chapter aims at proving and exploiting this relation. The validity of the Fourier inversion formula is also suggested by the following simple observation. Suppose $f$ is supported in a finite interval contained in $I = [- L / 2, L / 2]$ , and we expand $f$ in a Fourier series on $I$ . Then, letting $L$ tend to infinity, we are led to (4) (see Exercise 1).

在对 $f$ 的适当假设下，等式 (4) 实际上成立，本章的大部分理论旨在证明和利用这一关系。傅里叶反演公式的有效性也由以下简单观察所提示。假设 $f$ 支集在包含于 $I = [- L / 2, L / 2]$ 的一个有限区间内，并且我们在 $I$ 上将 $f$ 展开为傅里叶级数。然后，令 $L$ 趋于无穷大，我们得到 (4)（见习题 1）。

The special properties of the Fourier transform make it an important tool in the study of partial differential equations. For instance, we shall see how the Fourier inversion formula allows us to analyze some equations that are modeled on the real line. In particular, following the ideas developed on the circle, we solve the time- dependent heat equation for an infinite rod and the steady- state heat equation in the upper half- plane.

傅里叶变换的特殊性质使其成为研究偏微分方程的重要工具。例如，我们将看到傅里叶反演公式如何使我们能够分析一些以实直线为模型的方程。特别地，遵循圆上发展的思想，我们求解无限长杆的时间相关热方程和上半平面的稳态热方程。

In the last part of the chapter we discuss further topics related to the Poisson summation formula,

$$\sum_{n\in \mathbb{Z}}f(n) = \sum_{n\in \mathbb{Z}}\hat{f} (n),$$

which gives another remarkable connection between periodic functions (and their Fourier series) and non- periodic functions on the line (and

在本章的最后部分，我们讨论与泊松求和公式相关的进一步主题，

$$\sum_{n\in \mathbb{Z}}f(n) = \sum_{n\in \mathbb{Z}}\hat{f} (n),$$

该公式给出了周期函数（及其傅里叶级数）与直线上非周期函数（及其傅里叶变换）之间的另一个非凡联系。

===== Page 148 =====

their Fourier transforms). This identity allows us to prove an assertion made in the previous chapter, namely, that the heat kernel $H_{t}(x)$ satisfies the properties of a good kernel. In addition, the Poisson summation formula arises in many other settings, in particular in parts of number theory, as we shall see in Book II.

这个恒等式使我们能够证明前一章中的一个断言，即热核 $H_{t}(x)$ 满足好核的性质。此外，泊松求和公式出现在许多其他场合，特别是在数论的某些部分，我们将在第二卷中看到。

We make a final comment about the approach we have chosen. In our study of Fourier series, we found it useful to consider Riemann integrable functions on the circle. In particular, this generality assured us that even functions that had certain discontinuities could be treated by the theory. In contrast, our exposition of the elementary properties of the Fourier transform is stated in terms of the Schwartz space $\mathcal{S}$ of testing functions. These are functions that are indefinitely differentiable and that, together with their derivatives, are rapidly decreasing at infinity. The reliance on this space of functions is a device that allows us to come quickly to the main conclusions, formulated in a direct and transparent fashion. Once this is carried out, we point out some easy extensions to a somewhat wider setting. The more general theory of Fourier transforms (which must necessarily be based on Lebesgue integration) will be treated in Book III.

我们对所选择的方法作最后的评论。在我们对傅里叶级数的研究中，我们发现考虑圆上的黎曼可积函数是有用的。特别地，这种一般性确保我们即使是具有某些不连续性的函数也能被理论处理。相比之下，我们对傅里叶变换基本性质的阐述是用测试函数空间 $\mathcal{S}$ 来表述的。这些函数是无限可微的，并且连同它们的导数在无穷远处快速递减。依赖这个函数空间是一种技巧，使我们能够迅速得出主要结论，并以直接透明的方式表述。完成这一步后，我们指出一些到更广泛情形的简单推广。更一般的傅里叶变换理论（必须基于勒贝格积分）将在第三卷中处理。

## 1 Elementary theory of the Fourier transform

## 1 傅里叶变换的基本理论

We begin by extending the notion of integration to functions that are defined on the whole real line.

我们首先将积分的概念推广到定义在整个实直线上的函数。

### 1.1 Integration of functions on the real line

### 1.1 实直线上函数的积分

Given the notion of the integral of a function on a closed and bounded interval, the most natural extension of this definition to continuous functions over $\mathbb{R}$ is

$$\int_{-\infty}^{\infty}f(x)dx = \lim_{N\to \infty}\int_{-N}^{N}f(x)dx.$$

给定闭区间上有界区间上函数积分的概念，将此定义推广到 $\mathbb{R}$ 上连续函数的最自然方式是

$$\int_{-\infty}^{\infty}f(x)dx = \lim_{N\to \infty}\int_{-N}^{N}f(x)dx.$$

Of course, this limit may not exist. For example, it is clear that if $f(x) = 1$ , or even if $f(x) = 1 / (1 + |x|)$ , then the above limit is infinite. A moment's reflection suggests that the limit will exist if we impose on $f$ enough decay as $|x|$ tends to infinity. A useful condition is as follows.

当然，这个极限可能不存在。例如，显然如果 $f(x) = 1$ ，或者即使 $f(x) = 1 / (1 + |x|)$ ，上述极限是无穷大。稍加思考表明，如果我们对 $f$ 施加足够的当 $|x|$ 趋于无穷大时的衰减，极限就会存在。一个有用的条件如下。

A function $f$ defined on $\mathbb{R}$ is said to be of moderate decrease if $f$ is continuous and there exists a constant $A > 0$ so that

$$|f(x)|\leq \frac{A}{1 + x^2}\quad \mathrm{for~all~}x\in \mathbb{R}.$$

定义在 $\mathbb{R}$ 上的函数 $f$ 被称为中度衰减的，如果 $f$ 连续且存在常数 $A > 0$ 使得

$$|f(x)|\leq \frac{A}{1 + x^2}\quad \mathrm{for~all~}x\in \mathbb{R}.$$

===== Page 149 =====

This inequality says that $f$ is bounded (by $A$ for instance), and also that it decays at infinity at least as fast as $1 / x^{2}$ , since $A / (1 + x^{2}) \leq A / x^{2}$ .

这个不等式表明 $f$ 是有界的（例如被 $A$ 界定），并且它在无穷远处至少以 $1 / x^{2}$ 的速度衰减，因为 $A / (1 + x^{2}) \leq A / x^{2}$ 。

For example, the function $f(x) = 1 / (1 + |x|^n)$ is of moderate decrease as long as $n \geq 2$ . Another example is given by the function $e^{- a|x|}$ for $a > 0$ .

例如，函数 $f(x) = 1 / (1 + |x|^n)$ 只要 $n \geq 2$ 就是中度衰减的。另一个例子是 $a > 0$ 时的函数 $e^{- a|x|}$ 。

We shall denote by $\mathcal{M}(\mathbb{R})$ the set of functions of moderate decrease on $\mathbb{R}$ . As an exercise, the reader can check that under the usual addition of functions and multiplication by scalars, $\mathcal{M}(\mathbb{R})$ forms a vector space over $\mathbb{C}$ .

我们用 $\mathcal{M}(\mathbb{R})$ 表示 $\mathbb{R}$ 上中度衰减函数的集合。作为练习，读者可以验证在通常的函数加法和数乘下，$\mathcal{M}(\mathbb{R})$ 构成 $\mathbb{C}$ 上的一个向量空间。

We next see that whenever $f$ belongs to $\mathcal{M}(\mathbb{R})$ , then we may define

$$\int_{-\infty}^{\infty}f(x)dx = \lim_{N\to \infty}\int_{-N}^{N}f(x)dx, \quad (5)$$

where the limit now exists. Indeed, for each $N$ the integral $I_{N} = \int_{- N}^{N}f(x)dx$ is well defined because $f$ is continuous. It now suffices to show that $\{I_{N}\}$ is a Cauchy sequence, and this follows because if $M > N$ , then

$$|I_M - I_N|\leq \left|\int_{N\leq |x|\leq M}f(x)dx\right|$$ $$\leq A\int_{N\leq |x|\leq M}\frac{dx}{x^2}$$ $$\leq \frac{2A}{N}\to 0\quad \mathrm{as}N\to \infty .$$

接下来我们看到，只要 $f$ 属于 $\mathcal{M}(\mathbb{R})$ ，我们就可以定义

$$\int_{-\infty}^{\infty}f(x)dx = \lim_{N\to \infty}\int_{-N}^{N}f(x)dx, \quad (5)$$

此时极限存在。实际上，对每个 $N$ ，积分 $I_{N} = \int_{- N}^{N}f(x)dx$ 是良好定义的，因为 $f$ 连续。现在只需证明 $\{I_{N}\}$ 是一个柯西序列，这是因为如果 $M > N$ ，则

$$|I_M - I_N|\leq \left|\int_{N\leq |x|\leq M}f(x)dx\right|$$ $$\leq A\int_{N\leq |x|\leq M}\frac{dx}{x^2}$$ $$\leq \frac{2A}{N}\to 0\quad \mathrm{as}N\to \infty .$$

Notice we have also proved that $\int_{|x|\geq N}f(x)dx\to 0$ as $N\to \infty$ .At this point, we remark that we may replace the exponent 2 in the definition of moderate decrease by $1 + \epsilon$ where $\epsilon >0$ ;that is,

$$|f(x)|\leq \frac{A}{1 + |x|^{1 + \epsilon}}\quad \mathrm{for~all~}x\in \mathbb{R}.$$

注意我们还证明了当 $N\to \infty$ 时 $\int_{|x|\geq N}f(x)dx\to 0$ 。此时，我们注意到可以用 $1 + \epsilon$（其中 $\epsilon >0$）替换中度衰减定义中的指数 2；即

$$|f(x)|\leq \frac{A}{1 + |x|^{1 + \epsilon}}\quad \mathrm{for~all~}x\in \mathbb{R}.$$

This definition would work just as well for the purpose of the theory developed in this chapter. We chose $\epsilon = 1$ merely as a matter of convenience.

这个定义对于本章发展的理论同样有效。我们选择 $\epsilon = 1$ 仅仅是出于方便。

We summarize some elementary properties of integration over $\mathbb{R}$ in a proposition.

我们将 $\mathbb{R}$ 上积分的一些基本性质总结在一个命题中。

Proposition 1.1 The integral of a function of moderate decrease defined by (5) satisfies the following properties:

命题 1.1 由 (5) 定义的中度衰减函数的积分满足以下性质：

===== Page 150 =====

(i) Linearity: if $f,g\in \mathcal{M}(\mathbb{R})$ and $a,b\in \mathbb{C}$ ,then

$$\int_{-\infty}^{\infty}(af(x) + bg(x))dx = a\int_{-\infty}^{\infty}f(x)dx + b\int_{-\infty}^{\infty}g(x)dx.$$

(i) 线性：若 $f,g\in \mathcal{M}(\mathbb{R})$ 且 $a,b\in \mathbb{C}$ ，则

$$\int_{-\infty}^{\infty}(af(x) + bg(x))dx = a\int_{-\infty}^{\infty}f(x)dx + b\int_{-\infty}^{\infty}g(x)dx.$$

(ii) Translation invariance: for every $h\in \mathbb{R}$ we have

$$\int_{-\infty}^{\infty}f(x - h)dx = \int_{-\infty}^{\infty}f(x)dx.$$

(ii) 平移不变性：对每个 $h\in \mathbb{R}$ 有

$$\int_{-\infty}^{\infty}f(x - h)dx = \int_{-\infty}^{\infty}f(x)dx.$$

(iii) Scaling under dilations: if $\delta >0$ ,then

$$\delta \int_{-\infty}^{\infty}f(\delta x)dx = \int_{-\infty}^{\infty}f(x)dx.$$

(iii) 伸缩变换下的缩放：若 $\delta >0$ ，则

$$\delta \int_{-\infty}^{\infty}f(\delta x)dx = \int_{-\infty}^{\infty}f(x)dx.$$

(iv) Continuity: if $f\in \mathcal{M}(\mathbb{R})$ ,then

$$\int_{-\infty}^{\infty}|f(x - h) - f(x)|dx\to 0\quad as h\to 0.$$

(iv) 连续性：若 $f\in \mathcal{M}(\mathbb{R})$ ，则当 $h\to 0$ 时

$$\int_{-\infty}^{\infty}|f(x - h) - f(x)|dx\to 0.$$

We say a few words about the proof. Property (i) is immediate. To verify property (ii), it suffices to see that

$$\int_{-N}^{N}f(x - h)dx - \int_{-N}^{N}f(x)dx\to 0\quad \mathrm{as}N\to \infty .$$

我们对证明说几句。性质 (i) 是直接的。要验证性质 (ii)，只需看到当 $N\to \infty$ 时

$$\int_{-N}^{N}f(x - h)dx - \int_{-N}^{N}f(x)dx\to 0.$$

Since $\int_{- N}^{N}f(x - h)dx = \int_{- N - h}^{N - h}f(x)dx$ , the above difference is majorized by

$$\left|\int_{-N - h}^{N}f(x)dx\right| + \left|\int_{N - h}^{N}f(x)dx\right|\leq \frac{A'}{1 + N^2}$$

for large $N$ , which tends to 0 as $N$ tends to infinity.

由于 $\int_{- N}^{N}f(x - h)dx = \int_{- N - h}^{N - h}f(x)dx$ ，上述差被

$$\left|\int_{-N - h}^{N}f(x)dx\right| + \left|\int_{N - h}^{N}f(x)dx\right|\leq \frac{A'}{1 + N^2}$$

（对大的 $N$）所控制，当 $N$ 趋于无穷大时趋于 0。

The proof of property (iii) is similar once we observe that $\delta \int_{- N}^{N}f(\delta x)dx =$ $\int_{-\delta N}^{N}f(x)dx$

性质 (iii) 的证明类似，一旦我们注意到 $\delta \int_{- N}^{N}f(\delta x)dx = \int_{-\delta N}^{N}f(x)dx$。

To prove property (iv) it suffices to take $|h|\leq 1$ . For a preassigned $\epsilon >0$ we first choose $N$ so large that

$$\int_{|x|\geq N}|f(x)|dx\leq \epsilon /4\quad \mathrm{and}\quad \int_{|x|\geq N}|f(x - h)|dx\leq \epsilon /4.$$

为证明性质 (iv)，只需取 $|h|\leq 1$。对于预先指定的 $\epsilon >0$，我们首先选取 $N$ 足够大使得

$$\int_{|x|\geq N}|f(x)|dx\leq \epsilon /4\quad \mathrm{and}\quad \int_{|x|\geq N}|f(x - h)|dx\leq \epsilon /4.$$

Now with $N$ fixed, we use the fact that since $f$ is continuous, it is uniformly continuous in the interval $[- N - 1,N + 1]$ . Hence

现在固定 $N$，我们利用以下事实：由于 $f$ 连续，它在区间 $[- N - 1,N + 1]$ 上一致连续。因此

===== Page 151 =====

$\sup_{|x|\leq N}|f(x - h) - f(x)|\to 0$ as $h$ tends to 0. So we can take $h$ so small that this supremum is less than $\epsilon /4N$ . Altogether, then,

$$\int_{-\infty}^{\infty}|f(x - h) - f(x)|dx\leq \int_{-N}^{N}|f(x - h) - f(x)|dx$$ $$+\int_{|x|\geq N}|f(x - h)|dx$$ $$+\int_{|x|\geq N}|f(x)|dx$$ $$\leq \epsilon /2 + \epsilon /4 + \epsilon /4 = \epsilon ,$$

and thus conclusion (iv) follows.

当 $h$ 趋于 0 时，$\sup_{|x|\leq N}|f(x - h) - f(x)|\to 0$。因此我们可以取 $h$ 足够小使得这个上确界小于 $\epsilon /4N$。于是，总的来说，

$$\int_{-\infty}^{\infty}|f(x - h) - f(x)|dx\leq \int_{-N}^{N}|f(x - h) - f(x)|dx$$ $$+\int_{|x|\geq N}|f(x - h)|dx$$ $$+\int_{|x|\geq N}|f(x)|dx$$ $$\leq \epsilon /2 + \epsilon /4 + \epsilon /4 = \epsilon ,$$

从而结论 (iv) 得证。

### 1.2 Definition of the Fourier transform

### 1.2 傅里叶变换的定义

If $f\in \mathcal{M}(\mathbb{R})$ , we define its Fourier transform for $\xi \in \mathbb{R}$ by

$$\hat{f} (\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}dx.$$

若 $f\in \mathcal{M}(\mathbb{R})$，我们定义其对 $\xi \in \mathbb{R}$ 的傅里叶变换为

$$\hat{f} (\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}dx.$$

Of course, $|e^{- 2\pi ix\xi}| = 1$ , so the integrand is of moderate decrease, and the integral makes sense.

当然，$|e^{- 2\pi ix\xi}| = 1$，所以被积函数是中度衰减的，积分有意义。

In fact, this last observation implies that $\hat{f}$ is bounded, and moreover, a simple argument shows that $\hat{f}$ is continuous and tends to 0 as $|\xi |\to \infty$ (Exercise 5). However, nothing in the definition above guarantees that $\hat{f}$ is of moderate decrease, or has a specific decay. In particular, it is not clear in this context how to make sense of the integral $\int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi ix\xi} d\xi$ and the resulting Fourier inversion formula. To remedy this, we introduce a more refined space of functions considered by Schwartz which is very useful in establishing the initial properties of the Fourier transform.

事实上，最后的观察意味着 $\hat{f}$ 是有界的，而且，一个简单的论证表明 $\hat{f}$ 是连续的并且当 $|\xi |\to \infty$ 时趋于 0（习题 5）。然而，上述定义中没有任何东西保证 $\hat{f}$ 是中度衰减的或具有特定的衰减。特别地，在这种背景下，如何理解积分 $\int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi ix\xi} d\xi$ 以及由此得到的傅里叶反演公式并不清楚。为了弥补这一点，我们引入施瓦茨考虑的一个更精细的函数空间，它在建立傅里叶变换的初步性质时非常有用。

The choice of the Schwartz space is motivated by an important principle which ties the decay of $\hat{f}$ to the continuity and differentiability properties of $f$ (and vice versa): the faster $\hat{f} (\xi)$ decreases as $|\xi |\to \infty$ the "smoother" $f$ must be. An example that reflects this principle is given in Exercise 3. We also note that this relationship between $f$ and $\hat{f}$ is reminiscent of a similar one between the smoothness of a function on the circle and the decay of its Fourier coefficients; see the discussion of Corollary 2.4 in Chapter 2.

施瓦茨空间的选择是由一个重要的原理所驱动的，该原理将 $\hat{f}$ 的衰减与 $f$ 的连续性和可微性联系起来（反之亦然）：$\hat{f} (\xi)$ 当 $|\xi |\to \infty$ 时衰减得越快，$f$ 就必须“越光滑”。反映这一原理的例子见习题 3。我们还注意到，$f$ 和 $\hat{f}$ 之间的这种关系让人联想到圆上函数的光滑性与其傅里叶系数衰减之间的类似关系；见第 2 章推论 2.4 的讨论。

### 1.3 The Schwartz space

### 1.3 施瓦茨空间

The Schwartz space on $\mathbb{R}$ consists of the set of all indefinitely differentiable functions $f$ so that $f$ and all its derivatives $f^{\prime},f^{\prime \prime},\ldots ,f^{(\ell)},\ldots$

$\mathbb{R}$ 上的施瓦茨空间由所有无限可微函数 $f$ 组成，使得 $f$ 及其所有导数 $f^{\prime},f^{\prime \prime},\ldots ,f^{(\ell)},\ldots$

===== Page 152 =====

are rapidly decreasing, in the sense that

$$\sup_{x\in \mathbb{R}}|x|^k |f^{(\ell)}(x)|< \infty \quad \text{for every} k, \ell \geq 0.$$

是快速递减的，即对每个 $k, \ell \geq 0$ 有

$$\sup_{x\in \mathbb{R}}|x|^k |f^{(\ell)}(x)|< \infty.$$

We denote this space by $\mathcal{S} = \mathcal{S}(\mathbb{R})$ , and again, the reader should verify that $\mathcal{S}(\mathbb{R})$ is a vector space over $\mathbb{C}$ . Moreover, if $f \in \mathcal{S}(\mathbb{R})$ , we have

$$f^{\prime}(x) = \frac{df}{dx}\in \mathcal{S}(\mathbb{R})\quad \mathrm{and}\quad xf(x)\in \mathcal{S}(\mathbb{R}).$$

我们将此空间记为 $\mathcal{S} = \mathcal{S}(\mathbb{R})$，读者应再次验证 $\mathcal{S}(\mathbb{R})$ 是 $\mathbb{C}$ 上的向量空间。此外，若 $f \in \mathcal{S}(\mathbb{R})$，则

$$f^{\prime}(x) = \frac{df}{dx}\in \mathcal{S}(\mathbb{R})\quad \mathrm{and}\quad xf(x)\in \mathcal{S}(\mathbb{R}).$$

This expresses the important fact that the Schwartz space is closed under differentiation and multiplication by polynomials.

这表达了施瓦茨空间在微分和乘以多项式下封闭的重要事实。

A simple example of a function in $\mathcal{S}(\mathbb{R})$ is the Gaussian defined by

$$f(x) = e^{-x^2},$$

which plays a central role in the theory of the Fourier transform, as well as other fields (for example, probability theory and physics). The reader can check that the derivatives of $f$ are of the form $P(x)e^{- x^2}$ where $P$ is a polynomial, and this immediately shows that $f \in \mathcal{S}(\mathbb{R})$ . In fact, $e^{- ax^2}$ belongs to $\mathcal{S}(\mathbb{R})$ whenever $a > 0$ . Later, we will normalize the Gaussian by choosing $a = \pi$ .

$\mathcal{S}(\mathbb{R})$ 中函数的一个简单例子是由下式定义的高斯函数

$$f(x) = e^{-x^2},$$

它在傅里叶变换理论以及其他领域（例如概率论和物理学）中起着核心作用。读者可以验证 $f$ 的导数是 $P(x)e^{- x^2}$ 的形式，其中 $P$ 是多项式，这立即表明 $f \in \mathcal{S}(\mathbb{R})$。实际上，只要 $a > 0$，$e^{- ax^2}$ 就属于 $\mathcal{S}(\mathbb{R})$。稍后，我们将通过选择 $a = \pi$ 来归一化高斯函数。

<center>Figure 1. The Gaussian $e^{-x^2}$ </center>

<center>图 1. 高斯函数 $e^{-x^2}$</center>

An important class of other examples in $\mathcal{S}(\mathbb{R})$ are the "bump functions" which vanish outside bounded intervals (Exercise 4).

$\mathcal{S}(\mathbb{R})$ 中其他例子的一个重要类别是“钟形函数”，它们在有限区间外消失（习题 4）。

As a final remark, note that although $e^{- |x|}$ decreases rapidly at infinity, it is not differentiable at 0 and therefore does not belong to $\mathcal{S}(\mathbb{R})$ .

最后一点说明，注意尽管 $e^{- |x|}$ 在无穷远处快速递减，但它在 0 处不可微，因此不属于 $\mathcal{S}(\mathbb{R})$。

===== Page 153 =====

### 1.4 The Fourier transform on $\mathcal{S}$

### 1.4 $\mathcal{S}$ 上的傅里叶变换

The Fourier transform of a function $f \in \mathcal{S}(\mathbb{R})$ is defined by

$$\hat{f} (\xi) = \int_{-\infty}^{\infty} f(x)e^{-2\pi ix\xi} dx.$$

函数 $f \in \mathcal{S}(\mathbb{R})$ 的傅里叶变换定义为

$$\hat{f} (\xi) = \int_{-\infty}^{\infty} f(x)e^{-2\pi ix\xi} dx.$$

Some simple properties of the Fourier transform are gathered in the following proposition. We use the notation

$$f(x)\longrightarrow \hat{f} (\xi)$$

to mean that $\hat{f}$ denotes the Fourier transform of $f$ .

傅里叶变换的一些简单性质汇集在下面的命题中。我们使用记号

$$f(x)\longrightarrow \hat{f} (\xi)$$

表示 $\hat{f}$ 是 $f$ 的傅里叶变换。

Proposition 1.2 If $f \in \mathcal{S}(\mathbb{R})$ then:

$$(i) f(x + h)\longrightarrow \hat{f} (\xi)e^{2\pi ih\xi}\mathrm{~whenever~}h\in \mathbb{R}.$$ $$(ii) f(x)e^{-2\pi ixh}\longrightarrow \hat{f} (\xi +h)\mathrm{~whenever~}h\in \mathbb{R}.$$ $$(iii) f(\delta x)\longrightarrow \delta^{-1}\hat{f} (\delta^{-1}\xi)\mathrm{~whenever~}\delta >0.$$ $$(iv) f^{\prime}(x)\longrightarrow 2\pi i\xi \hat{f} (\xi).$$ $$(v) -2\pi ixf(x)\longrightarrow \frac{d}{d\xi}\hat{f} (\xi).$$

命题 1.2 若 $f \in \mathcal{S}(\mathbb{R})$，则：

$$(i) f(x + h)\longrightarrow \hat{f} (\xi)e^{2\pi ih\xi}\mathrm{~whenever~}h\in \mathbb{R}.$$ $$(ii) f(x)e^{-2\pi ixh}\longrightarrow \hat{f} (\xi +h)\mathrm{~whenever~}h\in \mathbb{R}.$$ $$(iii) f(\delta x)\longrightarrow \delta^{-1}\hat{f} (\delta^{-1}\xi)\mathrm{~whenever~}\delta >0.$$ $$(iv) f^{\prime}(x)\longrightarrow 2\pi i\xi \hat{f} (\xi).$$ $$(v) -2\pi ixf(x)\longrightarrow \frac{d}{d\xi}\hat{f} (\xi).$$

In particular, except for factors of $2\pi i$ , the Fourier transform interchanges differentiation and multiplication by $x$ . This is the key property that makes the Fourier transform a central object in the theory of differential equations. We shall return to this point later.

特别地，除了 $2\pi i$ 的因子外，傅里叶变换交换了微分和乘以 $x$ 的操作。这是使傅里叶变换成为微分方程理论核心对象的关键性质。我们稍后将回到这一点。

Proof. Property (i) is an immediate consequence of the translation invariance of the integral, and property (ii) follows from the definition. Also, the third property of Proposition 1.1 establishes (iii).

证明。性质 (i) 是积分平移不变性的直接推论，性质 (ii) 由定义得出。另外，命题 1.1 的第三个性质确立了 (iii)。

Integrating by parts gives

$$\int_{-N}^{N}f^{\prime}(x)e^{-2\pi ix\xi}dx = \left[f(x)e^{-2\pi ix\xi}\right]_{-N}^{N} + 2\pi i\xi \int_{-N}^{N}f(x)e^{-2\pi ix\xi}dx,$$

分部积分给出

$$\int_{-N}^{N}f^{\prime}(x)e^{-2\pi ix\xi}dx = \left[f(x)e^{-2\pi ix\xi}\right]_{-N}^{N} + 2\pi i\xi \int_{-N}^{N}f(x)e^{-2\pi ix\xi}dx,$$

so letting $N$ tend to infinity gives (iv).

因此令 $N$ 趋于无穷大给出 (iv)。

Finally, to prove property (v), we must show that $\hat{f}$ is differentiable and find its derivative. Let $\epsilon > 0$ and consider

$$\frac{\hat{f}(\xi + h) - \hat{f}(\xi)}{h} -(-\widehat{2\pi ixf})(\xi) =$$ $$\int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}\left[\frac{e^{-2\pi ixh} - 1}{h} +2\pi ix\right]dx.$$

最后，要证明性质 (v)，我们必须证明 $\hat{f}$ 可微并找到其导数。令 $\epsilon > 0$，考虑

$$\frac{\hat{f}(\xi + h) - \hat{f}(\xi)}{h} -(-\widehat{2\pi ixf})(\xi) =$$ $$\int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}\left[\frac{e^{-2\pi ixh} - 1}{h} +2\pi ix\right]dx.$$

===== Page 154 =====

Since $f(x)$ and $xf(x)$ are of rapid decrease, there exists an integer $N$ so that $\begin{array}{r}\int_{|x|\geq N}|f(x)|dx\leq \epsilon \end{array}$ and $\begin{array}{r}\int_{|x|\geq N}|x||f(x)|dx\leq \epsilon \end{array}$ . Moreover, for $|x|\leq N$ , there exists $h_0$ so that $|h|< h_0$ implies

$$\left|\frac{e^{-2\pi i x h} - 1}{h} +2\pi i x\right|\leq \frac{\epsilon}{N}.$$

由于 $f(x)$ 和 $xf(x)$ 是快速递减的，存在整数 $N$ 使得 $\int_{|x|\geq N}|f(x)|dx\leq \epsilon$ 和 $\int_{|x|\geq N}|x||f(x)|dx\leq \epsilon$。此外，对于 $|x|\leq N$，存在 $h_0$ 使得 $|h|< h_0$ 蕴含

$$\left|\frac{e^{-2\pi i x h} - 1}{h} +2\pi i x\right|\leq \frac{\epsilon}{N}.$$

Hence for $|h|< h_0$ we have

$$\left|\frac{\hat{f}(\xi + h) - \hat{f}(\xi)}{h} -(-\overline{2\pi i x} f)(\xi)\right|$$ $$\qquad \leq \int_{-N}^{N}\left|f(x)e^{-2\pi i x\xi}\left[\frac{e^{-2\pi i x h} - 1}{h} +2\pi i x\right]\right|dx + C\epsilon$$ $$\qquad \leq C^{\prime}\epsilon .$$

因此对于 $|h|< h_0$，我们有

$$\left|\frac{\hat{f}(\xi + h) - \hat{f}(\xi)}{h} -(-\overline{2\pi i x} f)(\xi)\right|$$ $$\qquad \leq \int_{-N}^{N}\left|f(x)e^{-2\pi i x\xi}\left[\frac{e^{-2\pi i x h} - 1}{h} +2\pi i x\right]\right|dx + C\epsilon$$ $$\qquad \leq C^{\prime}\epsilon .$$

Theorem 1.3 If $f\in \mathcal{S}(\mathbb{R})$ , then $\hat{f}\in \mathcal{S}(\mathbb{R})$ .

定理 1.3 若 $f\in \mathcal{S}(\mathbb{R})$，则 $\hat{f}\in \mathcal{S}(\mathbb{R})$。

The proof is an easy application of the fact that the Fourier transform interchanges differentiation and multiplication. In fact, note that if $f\in \mathcal{S}(\mathbb{R})$ , its Fourier transform $\hat{f}$ is bounded; then also, for each pair of non- negative integers $\ell$ and $k$ , the expression

$$\xi^k\left(\frac{d}{d\xi}\right)^\ell \hat{f} (\xi)$$

is bounded, since by the last proposition, it is the Fourier transform of

$$\frac{1}{(2\pi i)^k}\left(\frac{d}{dx}\right)^k [(-2\pi i x)^\ell f(x)].$$

证明是傅里叶变换交换微分和乘法这一事实的简单应用。实际上，注意若 $f\in \mathcal{S}(\mathbb{R})$，其傅里叶变换 $\hat{f}$ 有界；然后，对每一对非负整数 $\ell$ 和 $k$，表达式

$$\xi^k\left(\frac{d}{d\xi}\right)^\ell \hat{f} (\xi)$$

是有界的，因为根据上一个命题，它是

$$\frac{1}{(2\pi i)^k}\left(\frac{d}{dx}\right)^k [(-2\pi i x)^\ell f(x)]$$

的傅里叶变换。

The proof of the inversion formula

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i x\xi}d\xi \quad \mathrm{for} f\in \mathcal{S}(\mathbb{R}),$$

which we give in the next section, is based on a careful study of the function $e^{- ax^2}$ , which, as we have already observed, is in $\mathcal{S}(\mathbb{R})$ if $a > 0$ .

反演公式

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i x\xi}d\xi \quad \mathrm{for} f\in \mathcal{S}(\mathbb{R}),$$

的证明（我们将在下一节给出）基于对函数 $e^{- ax^2}$ 的仔细研究，正如我们已经注意到的，当 $a > 0$ 时它在 $\mathcal{S}(\mathbb{R})$ 中。

===== Page 155 =====

## The Gaussians as good kernels

## 作为好核的高斯函数

We begin by considering the case $a = \pi$ because of the normalization:

$$\int_{-\infty}^{\infty}e^{-\pi x^{2}}dx = 1. \quad (6)$$

我们从考虑 $a = \pi$ 的情形开始，这是因为归一化：

$$\int_{-\infty}^{\infty}e^{-\pi x^{2}}dx = 1. \quad (6)$$

To see why (6) is true, we use the multiplicative property of the exponential to reduce the calculation to a two- dimensional integral. More precisely, we can argue as follows:

$$\left(\int_{-\infty}^{\infty}e^{-\pi x^{2}}dx\right)^{2} = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}e^{-\pi (x^{2} + y^{2})}dxdy$$ $$\qquad = \int_{0}^{2\pi}\int_{0}^{\infty}e^{-\pi r^{2}}rdrd\theta$$ $$\qquad = \int_{0}^{\infty}2\pi re^{-\pi r^{2}}dr$$ $$\qquad = \left[-e^{-\pi r^{2}}\right]_{0}^{\infty}$$ $$\qquad = 1,$$

要看出 (6) 为什么成立，我们使用指数的乘法性质将计算归结为二维积分。更精确地说，我们可以论证如下：

$$\left(\int_{-\infty}^{\infty}e^{-\pi x^{2}}dx\right)^{2} = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}e^{-\pi (x^{2} + y^{2})}dxdy$$ $$\qquad = \int_{0}^{2\pi}\int_{0}^{\infty}e^{-\pi r^{2}}rdrd\theta$$ $$\qquad = \int_{0}^{\infty}2\pi re^{-\pi r^{2}}dr$$ $$\qquad = \left[-e^{-\pi r^{2}}\right]_{0}^{\infty}$$ $$\qquad = 1,$$

where we have evaluated the two- dimensional integral using polar coordinates.

其中我们使用极坐标计算了二维积分。

The fundamental property of the Gaussian which is of interest to us, and which actually follows from (6), is that $e^{- \pi x^{2}}$ equals its Fourier transform! We isolate this important result in a theorem.

我们感兴趣的高斯函数的基本性质，实际上可以从 (6) 推出，即 $e^{- \pi x^{2}}$ 等于其傅里叶变换！我们将这一重要结果单独列为定理。

Theorem 1.4 If $f(x) = e^{- \pi x^{2}}$ , then $\hat{f} (\xi) = f(\xi)$ .

定理 1.4 若 $f(x) = e^{- \pi x^{2}}$，则 $\hat{f} (\xi) = f(\xi)$。

Proof. Define

$$F(\xi) = \hat{f} (\xi) = \int_{-\infty}^{\infty}e^{-\pi x^{2}}e^{-2\pi ix\xi}dx,$$

证明。定义

$$F(\xi) = \hat{f} (\xi) = \int_{-\infty}^{\infty}e^{-\pi x^{2}}e^{-2\pi ix\xi}dx,$$

and observe that $F(0) = 1$ , by our previous calculation. By property (v) in Proposition 1.2, and the fact that $f^{\prime}(x) = - 2\pi x f(x)$ , we obtain

$$F^{\prime}(\xi) = \int_{-\infty}^{\infty}f(x)(-2\pi ix)e^{-2\pi ix\xi}dx = i\int_{-\infty}^{\infty}f^{\prime}(x)e^{-2\pi ix\xi}dx.$$

并注意到根据之前的计算 $F(0) = 1$。由命题 1.2 中的性质 (v) 以及 $f^{\prime}(x) = - 2\pi x f(x)$ 的事实，我们得到

$$F^{\prime}(\xi) = \int_{-\infty}^{\infty}f(x)(-2\pi ix)e^{-2\pi ix\xi}dx = i\int_{-\infty}^{\infty}f^{\prime}(x)e^{-2\pi ix\xi}dx.$$

By (iv) of the same proposition, we find that

$$F^{\prime}(\xi) = i(2\pi i\xi)\hat{f} (\xi) = -2\pi \xi F(\xi).$$

根据同一命题的 (iv)，我们发现

$$F^{\prime}(\xi) = i(2\pi i\xi)\hat{f} (\xi) = -2\pi \xi F(\xi).$$

===== Page 156 =====

If we define $G(\xi) = F(\xi)e^{\pi \xi^2}$ , then from what we have seen above, it follows that $G^{\prime}(\xi) = 0$ , hence $G$ is constant. Since $F(0) = 1$ , we conclude that $G$ is identically equal to 1, therefore $F(\xi) = e^{-\pi \xi^2}$ , as was to be shown.

若定义 $G(\xi) = F(\xi)e^{\pi \xi^2}$，则从上面我们看到 $G^{\prime}(\xi) = 0$，因此 $G$ 是常数。由于 $F(0) = 1$，我们得出结论 $G$ 恒等于 1，因此 $F(\xi) = e^{-\pi \xi^2}$，证毕。

The scaling properties of the Fourier transform under dilations yield the following important transformation law, which follows from (iii) in Proposition 1.2 (with $\delta$ replaced by $\delta^{- 1 / 2}$ ).

傅里叶变换在伸缩变换下的缩放性质给出以下重要的变换律，它由命题 1.2 中的 (iii) 得出（将 $\delta$ 替换为 $\delta^{- 1 / 2}$）。

Corollary 1.5 If $\delta >0$ and $K_{\delta}(x) = \delta^{- 1 / 2}e^{-\pi x^{2} / \delta}$ , then $\widehat{K_{\delta}} (\xi) = e^{-\pi \delta \xi^{2}}$ .

推论 1.5 若 $\delta >0$ 且 $K_{\delta}(x) = \delta^{- 1 / 2}e^{-\pi x^{2} / \delta}$，则 $\widehat{K_{\delta}} (\xi) = e^{-\pi \delta \xi^{2}}$。

We pause to make an important observation. As $\delta$ tends to 0, the function $K_{\delta}$ peaks at the origin, while its Fourier transform $\widehat{K_{\delta}}$ gets flatter. So in this particular example, we see that $K_{\delta}$ and $\widehat{K_{\delta}}$ cannot both be localized (that is, concentrated) at the origin. This is an example of a general phenomenon called the Heisenberg uncertainty principle, which we will discuss at the end of this chapter.

我们停下来做一个重要的观察。当 $\delta$ 趋于 0 时，函数 $K_{\delta}$ 在原点处达到峰值，而其傅里叶变换 $\widehat{K_{\delta}}$ 变得更平坦。因此在这个特例中，我们看到 $K_{\delta}$ 和 $\widehat{K_{\delta}}$ 不能同时集中在原点。这是一个被称为海森堡不确定性原理的普遍现象的例子，我们将在本章末尾讨论。

We have now constructed a family of good kernels on the real line, analogous to those on the circle considered in Chapter 2. Indeed, with

$$K_{\delta}(x) = \delta^{-1 / 2}e^{-\pi x^{2} / \delta},$$

我们现在已经构造了实直线上一族好核，类似于第 2 章中考虑的圆上的好核。确实，取

$$K_{\delta}(x) = \delta^{-1 / 2}e^{-\pi x^{2} / \delta},$$

we have:

$$\mathrm{i)}\int_{-\infty}^{\infty}K_{\delta}(x)dx = 1.$$ $$\mathrm{ii)}\int_{-\infty}^{\infty}|K_{\delta}(x)|dx\leq M.$$ $$\mathrm{iii)}\mathrm{For~every~}\eta >0,\mathrm{we~have~}\int_{|x| > \eta}|K_{\delta}(x)|dx\to 0\mathrm{~as~}\delta \to 0.$$

我们有：

$$\mathrm{i)}\int_{-\infty}^{\infty}K_{\delta}(x)dx = 1.$$ $$\mathrm{ii)}\int_{-\infty}^{\infty}|K_{\delta}(x)|dx\leq M.$$ $$\mathrm{iii)}\mathrm{对每个~}\eta >0,\mathrm{有~}\int_{|x| > \eta}|K_{\delta}(x)|dx\to 0\mathrm{~当~}\delta \to 0.$$

To prove (i), we may change variables and use (6), or note that the integral equals $\widehat{K_{\delta}} (0)$ , which is 1 by Corollary 1.5. Since $K_{\delta} \geq 0$ , it is clear that property (ii) is also true. Finally we can again change variables to get

$$\int_{|x| > \eta}|K_{\delta}(x)|dx = \int_{|y| > \eta /\delta^{1 / 2}}e^{-\pi y^{2}}dy\to 0$$

as $\delta$ tends to 0. We have thus proved the following result.

为证明 (i)，我们可以变换变量并利用 (6)，或者注意到积分等于 $\widehat{K_{\delta}} (0)$，由推论 1.5 知为 1。由于 $K_{\delta} \geq 0$，性质 (ii) 显然也成立。最后我们可以再次变换变量得到

$$\int_{|x| > \eta}|K_{\delta}(x)|dx = \int_{|y| > \eta /\delta^{1 / 2}}e^{-\pi y^{2}}dy\to 0$$

当 $\delta$ 趋于 0 时。因此我们证明了以下结果。

Theorem 1.6 The collection $\{K_{\delta}\}_{\delta >0}$ is a family of good kernels as $\delta \to 0$ .

定理 1.6 集合 $\{K_{\delta}\}_{\delta >0}$ 当 $\delta \to 0$ 时是一族好核。

We next apply these good kernels via the operation of convolution, which is given as follows. If $f,g \in \mathcal{S}(\mathbb{R})$ , their convolution is defined by

$$(f*g)(x) = \int_{-\infty}^{\infty}f(x - t)g(t)dt. \quad (7)$$

接下来我们通过卷积运算应用这些好核，卷积定义如下。若 $f,g \in \mathcal{S}(\mathbb{R})$，它们的卷积定义为

$$(f*g)(x) = \int_{-\infty}^{\infty}f(x - t)g(t)dt. \quad (7)$$

===== Page 157 =====

For a fixed value of $x$ , the function $f(x - t)g(t)$ is of rapid decrease in $t$ , hence the integral converges.

对于固定的 $x$，函数 $f(x - t)g(t)$ 关于 $t$ 是快速递减的，因此积分收敛。

By the argument in Section 4 of Chapter 2 (with a slight modification), we get the following corollary.

通过第 2 章第 4 节的论证（稍作修改），我们得到以下推论。

Corollary 1.7 If $f \in \mathcal{S}(\mathbb{R})$ , then

$$(f * K_{\delta})(x) \to f(x) \quad \text{uniformly in } x \text{ as } \delta \to 0.$$

推论 1.7 若 $f \in \mathcal{S}(\mathbb{R})$，则当 $\delta \to 0$ 时

$$(f * K_{\delta})(x) \to f(x) \quad \text{在 } x \text{ 上一致}.$$

Proof. First, we claim that $f$ is uniformly continuous on $\mathbb{R}$ . Indeed, given $\epsilon > 0$ there exists $R > 0$ so that $|f(x)| < \epsilon /4$ whenever $|x| \geq R$ . Moreover, $f$ is continuous, hence uniformly continuous on the compact interval $[- R, R]$ , and together with the previous observation, we can find $\eta > 0$ so that $|f(x) - f(y)| < \epsilon$ whenever $|x - y| < \eta$ . Now we argue as usual. Using the first property of good kernels, we can write

$$(f * K_{\delta})(x) - f(x) = \int_{-\infty}^{\infty} K_{\delta}(t) [f(x - t) - f(x)] dt,$$

证明。首先，我们断言 $f$ 在 $\mathbb{R}$ 上一致连续。实际上，给定 $\epsilon > 0$，存在 $R > 0$ 使得当 $|x| \geq R$ 时 $|f(x)| < \epsilon /4$。此外，$f$ 连续，因此在紧区间 $[- R, R]$ 上一致连续，结合之前的观察，我们可以找到 $\eta > 0$ 使得当 $|x - y| < \eta$ 时 $|f(x) - f(y)| < \epsilon$。现在我们照常论证。使用好核的第一个性质，我们可以写

$$(f * K_{\delta})(x) - f(x) = \int_{-\infty}^{\infty} K_{\delta}(t) [f(x - t) - f(x)] dt,$$

and since $K_{\delta} \geq 0$ , we find

$$|(f * K_{\delta})(x) - f(x)| \leq \int_{|t| > \eta} + \int_{|t| \leq \eta} K_{\delta}(t) |f(x - t) - f(x)| dt.$$

并且由于 $K_{\delta} \geq 0$，我们发现

$$|(f * K_{\delta})(x) - f(x)| \leq \int_{|t| > \eta} + \int_{|t| \leq \eta} K_{\delta}(t) |f(x - t) - f(x)| dt.$$

The first integral is small by the third property of good kernels, and the fact that $f$ is bounded, while the second integral is also small since $f$ is uniformly continuous and $\int K_{\delta} = 1$ . This concludes the proof of the corollary.

第一个积分由好核的第三个性质以及 $f$ 有界而很小，而第二个积分由于 $f$ 一致连续且 $\int K_{\delta} = 1$ 也很小。这就完成了推论的证明。

### 1.5 The Fourier inversion

### 1.5 傅里叶反演

The next result is an identity sometimes called the multiplication formula.

下一个结果是一个恒等式，有时称为乘法公式。

Proposition 1.8 If $f, g \in \mathcal{S}(\mathbb{R})$ , then

$$\int_{-\infty}^{\infty} f(x) \hat{g}(x) dx = \int_{-\infty}^{\infty} \hat{f}(y) g(y) dy.$$

命题 1.8 若 $f, g \in \mathcal{S}(\mathbb{R})$，则

$$\int_{-\infty}^{\infty} f(x) \hat{g}(x) dx = \int_{-\infty}^{\infty} \hat{f}(y) g(y) dy.$$

To prove the proposition, we need to digress briefly to discuss the interchange of the order of integration for double integrals. Suppose $F(x, y)$ is a continuous function in the plane $(x, y) \in \mathbb{R}^{2}$ . We will assume the following decay condition on $F$ :

$$|F(x,y)| \leq A / (1 + x^{2})(1 + y^{2}).$$

为证明该命题，我们需要简短地离题讨论二重积分中积分次序的交换。假设 $F(x, y)$ 是平面 $(x, y) \in \mathbb{R}^{2}$ 上的连续函数。我们将对 $F$ 假设以下衰减条件：

$$|F(x,y)| \leq A / (1 + x^{2})(1 + y^{2}).$$

===== Page 158 =====

Then, we can state that for each $x$ the function $F(x,y)$ is of moderate decrease in $y$ , and similarly for each fixed $y$ the function $F(x,y)$ is of moderate decrease in $x$ . Moreover, the function $F_{1}(x) = \int_{-\infty}^{\infty}F(x,y)dy$ is continuous and of moderate decrease; similarly for the function $F_{2}(y) = \int_{-\infty}^{\infty}F(x,y)dx$ . Finally

$$\int_{-\infty}^{\infty}F_{1}(x)dx = \int_{-\infty}^{\infty}F_{2}(y)dy.$$

于是，我们可以断言：对每个 $x$，函数 $F(x,y)$ 关于 $y$ 是中度衰减的；类似地，对每个固定的 $y$，函数 $F(x,y)$ 关于 $x$ 是中度衰减的。此外，函数 $F_{1}(x) = \int_{-\infty}^{\infty}F(x,y)dy$ 连续且中度衰减；函数 $F_{2}(y) = \int_{-\infty}^{\infty}F(x,y)dx$ 亦然。最后，

$$\int_{-\infty}^{\infty}F_{1}(x)dx = \int_{-\infty}^{\infty}F_{2}(y)dy.$$

The proof of these facts may be found in the appendix.

这些事实的证明可以在附录中找到。

We now apply this to $F(x,y) = f(x)g(y)e^{- 2\pi ixy}$ . Then $F_{1}(x) = f(x)\hat{g} (x)$ , and $F_{2}(y) = \hat{f} (y)g(y)$ so

$$\int_{-\infty}^{\infty}f(x)\hat{g} (x)dx = \int_{-\infty}^{\infty}\hat{f} (y)g(y)dy,$$

现在将其应用于 $F(x,y) = f(x)g(y)e^{- 2\pi ixy}$。则 $F_{1}(x) = f(x)\hat{g} (x)$，且 $F_{2}(y) = \hat{f} (y)g(y)$，所以

$$\int_{-\infty}^{\infty}f(x)\hat{g} (x)dx = \int_{-\infty}^{\infty}\hat{f} (y)g(y)dy,$$

which is the assertion of the proposition.

这就是命题的断言。

The multiplication formula and the fact that the Gaussian is its own Fourier transform lead to a proof of the first major theorem.

乘法公式和高斯函数是其自身傅里叶变换的事实导致第一个主要定理的证明。

Theorem 1.9 (Fourier inversion) If $f\in \mathcal{S}(\mathbb{R})$ , then

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i x\xi}d\xi .$$

定理 1.9（傅里叶反演）若 $f\in \mathcal{S}(\mathbb{R})$，则

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i x\xi}d\xi .$$

Proof. We first claim that

$$f(0) = \int_{-\infty}^{\infty}\hat{f} (\xi)d\xi .$$

证明。我们首先断言

$$f(0) = \int_{-\infty}^{\infty}\hat{f} (\xi)d\xi .$$

Let $G_{\delta}(x) = e^{-\pi \delta x^{2}}$ so that $\hat{G}_{\delta}(\xi) = K_{\delta}(\xi)$ . By the multiplication formula we get

$$\int_{-\infty}^{\infty}f(x)K_{\delta}(x)dx = \int_{-\infty}^{\infty}\hat{f} (\xi)G_{\delta}(\xi)d\xi .$$

令 $G_{\delta}(x) = e^{-\pi \delta x^{2}}$，使得 $\hat{G}_{\delta}(\xi) = K_{\delta}(\xi)$。由乘法公式得到

$$\int_{-\infty}^{\infty}f(x)K_{\delta}(x)dx = \int_{-\infty}^{\infty}\hat{f} (\xi)G_{\delta}(\xi)d\xi .$$

Since $K_{\delta}$ is a good kernel, the first integral goes to $f(0)$ as $\delta$ tends to 0. Since the second integral clearly converges to $\int_{-\infty}^{\infty}\hat{f} (\xi)d\xi$ as $\delta$ tends to 0, our claim is proved. In general, let $F(y) = f(y + x)$ so that

$$f(x) = F(0) = \int_{-\infty}^{\infty}\hat{F} (\xi)d\xi = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i x\xi}d\xi .$$

由于 $K_{\delta}$ 是好核，当 $\delta$ 趋于 0 时第一个积分趋于 $f(0)$。由于第二个积分当 $\delta$ 趋于 0 时显然收敛到 $\int_{-\infty}^{\infty}\hat{f} (\xi)d\xi$，我们的断言得证。一般情况下，令 $F(y) = f(y + x)$，则

$$f(x) = F(0) = \int_{-\infty}^{\infty}\hat{F} (\xi)d\xi = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i x\xi}d\xi .$$

As the name of Theorem 1.9 suggests, it provides a formula that inverts the Fourier transform; in fact we see that the Fourier transform is its own

正如定理 1.9 的名称所示，它提供了一个反演傅里叶变换的公式；事实上我们看到傅里叶变换是其自身的

===== Page 159 =====

inverse except for the change of $x$ to $- x$ . More precisely, we may define two mappings $\mathcal{F}:\mathcal{S}(\mathbb{R})\to \mathcal{S}(\mathbb{R})$ and $\mathcal{F}^{*}:\mathcal{S}(\mathbb{R})\to \mathcal{S}(\mathbb{R})$ by

$$\mathcal{F}(f)(\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi i x\xi}dx\quad \mathrm{and}\quad \mathcal{F}^{*}(g)(x) = \int_{-\infty}^{\infty}g(\xi)e^{2\pi i x\xi} d\xi .$$

逆，除了将 $x$ 改为 $- x$。更精确地说，我们可以定义两个映射 $\mathcal{F}:\mathcal{S}(\mathbb{R})\to \mathcal{S}(\mathbb{R})$ 和 $\mathcal{F}^{*}:\mathcal{S}(\mathbb{R})\to \mathcal{S}(\mathbb{R})$ 如下：

$$\mathcal{F}(f)(\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi i x\xi}dx\quad \mathrm{and}\quad \mathcal{F}^{*}(g)(x) = \int_{-\infty}^{\infty}g(\xi)e^{2\pi i x\xi} d\xi .$$

Thus $\mathcal{F}$ is the Fourier transform, and Theorem 1.9 guarantees that $\mathcal{F}^{*}\circ \mathcal{F} = I$ on $\mathcal{S}(\mathbb{R})$ , where $I$ is the identity mapping. Moreover, since the definitions of $\mathcal{F}$ and $\mathcal{F}^{*}$ differ only by a sign in the exponential, we see that $\mathcal{F}(f)(y) = \mathcal{F}^{*}(f)(- y)$ , so we also have $\mathcal{F}\circ \mathcal{F}^{*} = I$ . As a consequence, we conclude that $\mathcal{F}^{*}$ is the inverse of the Fourier transform on $\mathcal{S}(\mathbb{R})$ , and we get the following result.

因此 $\mathcal{F}$ 是傅里叶变换，定理 1.9 保证在 $\mathcal{S}(\mathbb{R})$ 上 $\mathcal{F}^{*}\circ \mathcal{F} = I$，其中 $I$ 是恒等映射。此外，由于 $\mathcal{F}$ 和 $\mathcal{F}^{*}$ 的定义仅在指数符号上不同，我们看到 $\mathcal{F}(f)(y) = \mathcal{F}^{*}(f)(- y)$，因此也有 $\mathcal{F}\circ \mathcal{F}^{*} = I$。作为推论，我们得出结论 $\mathcal{F}^{*}$ 是 $\mathcal{S}(\mathbb{R})$ 上傅里叶变换的逆，并得到以下结果。

Corollary 1.10 The Fourier transform is a bijective mapping on the Schwartz space.

推论 1.10 傅里叶变换是施瓦茨空间上的双射。

### 1.6 The Plancherel formula

### 1.6 普朗歇尔公式

We need a few further results about convolutions of Schwartz functions. The key fact is that the Fourier transform interchanges convolutions with pointwise products, a result analogous to the situation for Fourier series.

我们需要一些关于施瓦茨函数卷积的进一步结果。关键事实是傅里叶变换交换卷积和逐点乘积，这与傅里叶级数的情况类似。

Proposition 1.11 If $f,g\in \mathcal{S}(\mathbb{R})$ then:

(i) $f*g\in \mathcal{S}(\mathbb{R})$ (ii) $f*g = g*f$ (iii) $\widehat{(f*g)}(\xi) = \hat{f} (\xi)\hat{g} (\xi)$

命题 1.11 若 $f,g\in \mathcal{S}(\mathbb{R})$，则：

(i) $f*g\in \mathcal{S}(\mathbb{R})$ (ii) $f*g = g*f$ (iii) $\widehat{(f*g)}(\xi) = \hat{f} (\xi)\hat{g} (\xi)$

Proof. To prove that $f*g$ is rapidly decreasing, observe first that for any $\ell \geq 0$ we have $\sup_{x}|x|^{\ell}|g(x - y)|\leq A_{\ell}(1 + |y|)^{\ell}$ , because $g$ is rapidly decreasing (to check this assertion, consider separately the two cases $|x|\leq 2|y|$ and $|x|\geq 2|y|$ ). From this, we see that

$$\sup_{x}|x^{\ell}(f*g)(x)|\leq A_{\ell}\int_{-\infty}^{\infty}|f(y)|(1 + |y|)^{\ell}dy,$$

证明。为证明 $f*g$ 是快速递减的，首先注意到对任意 $\ell \geq 0$，有 $\sup_{x}|x|^{\ell}|g(x - y)|\leq A_{\ell}(1 + |y|)^{\ell}$，因为 $g$ 是快速递减的（要验证这一断言，请分别考虑 $|x|\leq 2|y|$ 和 $|x|\geq 2|y|$ 两种情形）。由此我们看到

$$\sup_{x}|x^{\ell}(f*g)(x)|\leq A_{\ell}\int_{-\infty}^{\infty}|f(y)|(1 + |y|)^{\ell}dy,$$

so that $x^{\ell}(f*g)(x)$ is a bounded function for every $\ell \geq 0$ . These estimates carry over to the derivatives of $f*g$ , thereby proving that $f*g\in \mathcal{S}(\mathbb{R})$ because

$$\left(\frac{d}{dx}\right)^{k}(f*g)(x) = (f*\left(\frac{d}{dx}\right)^{k}g)(x)\quad \mathrm{for}k = 1,2,\ldots$$

因此对每个 $\ell \geq 0$，$x^{\ell}(f*g)(x)$ 是有界函数。这些估计可以推广到 $f*g$ 的导数，从而证明 $f*g\in \mathcal{S}(\mathbb{R})$，因为

$$\left(\frac{d}{dx}\right)^{k}(f*g)(x) = (f*\left(\frac{d}{dx}\right)^{k}g)(x)\quad \mathrm{for}k = 1,2,\ldots$$

===== Page 160 =====

This identity is proved first for $k = 1$ by differentiating under the integral defining $f*g$ . The interchange of differentiation and integration is justified in this case by the rapid decrease of $dg / dx$ . The identity then follows for every $k$ by iteration.

这个恒等式首先对 $k = 1$ 通过在定义 $f*g$ 的积分下微分来证明。在这种情况下，微分和积分的交换由 $dg / dx$ 的快速递减得到证明。然后通过迭代，该恒等式对每个 $k$ 都成立。

For fixed $x$ , the change of variables $x - y = u$ shows that

$$(f*g)(x) = \int_{-\infty}^{\infty}f(x - u)g(u)du = (g*f)(x).$$

对于固定的 $x$，变量替换 $x - y = u$ 表明

$$(f*g)(x) = \int_{-\infty}^{\infty}f(x - u)g(u)du = (g*f)(x).$$

This change of variables is a composition of two changes, $y\mapsto - y$ and $y\mapsto y - h$ (with $h = x$ ). For the first one we use the observation that $\begin{array}{r}\int_{-\infty}^{\infty}F(x)dx = \int_{-\infty}^{\infty}F(- x)dx \end{array}$ for any Schwartz function $F$ , and for the second, we apply (ii) of Proposition 1.1

这个变量替换是两次变换的复合：$y\mapsto - y$ 和 $y\mapsto y - h$（其中 $h = x$）。对于第一次变换，我们利用观察：对任何施瓦茨函数 $F$，有 $\int_{-\infty}^{\infty}F(x)dx = \int_{-\infty}^{\infty}F(- x)dx$；对于第二次，我们应用命题 1.1 的 (ii)。

Finally, consider $F(x,y) = f(y)g(x - y)e^{- 2\pi i x\xi}$ . Since $f$ and $g$ are rapidly decreasing, considering separately the two cases $|x|\leq 2|y|$ and $|x|\geq 2|y|$ , we see that the discussion of the change of order of integration after Proposition 1.8 applies to $F$ . In this case $F_{1}(x) = (f*g)(x)e^{- 2\pi i x\xi}$ , and $F_{2}(y) = f(y)e^{- 2\pi i y\xi}\hat{g} (\xi)$ . Thus $\begin{array}{r}\int_{-\infty}^{\infty}F_{1}(x)dx = \int_{-\infty}^{\infty}F_{2}(y)dy \end{array}$ , which implies (iii). The proposition is therefore proved.

最后，考虑 $F(x,y) = f(y)g(x - y)e^{- 2\pi i x\xi}$。由于 $f$ 和 $g$ 是快速递减的，分别考虑 $|x|\leq 2|y|$ 和 $|x|\geq 2|y|$ 两种情形，我们看到命题 1.8 之后关于积分次序交换的讨论适用于 $F$。在此情形下，$F_{1}(x) = (f*g)(x)e^{- 2\pi i x\xi}$，而 $F_{2}(y) = f(y)e^{- 2\pi i y\xi}\hat{g} (\xi)$。因此 $\int_{-\infty}^{\infty}F_{1}(x)dx = \int_{-\infty}^{\infty}F_{2}(y)dy$，这意味着 (iii)。于是命题得证。

We now use the properties of convolutions of Schwartz functions to prove the main result of this section. The result we have in mind is the analogue for functions on $\mathbb{R}$ of Parseval's identity for Fourier series.

现在我们使用施瓦茨函数卷积的性质来证明本节的主要结果。我们想到的结果是傅里叶级数的帕塞瓦尔恒等式在 $\mathbb{R}$ 上函数的类似物。

The Schwartz space can be equipped with a Hermitian inner product

$$(f,g) = \int_{-\infty}^{\infty}f(x)\overline{g(x)} dx$$

施瓦茨空间可以装备一个埃尔米特内积

$$(f,g) = \int_{-\infty}^{\infty}f(x)\overline{g(x)} dx$$

whose associated norm is

$$\| f\| = \left(\int_{-\infty}^{\infty}|f(x)|^2 dx\right)^{1 / 2}.$$

其关联的范数为

$$\| f\| = \left(\int_{-\infty}^{\infty}|f(x)|^2 dx\right)^{1 / 2}.$$

The second major theorem in the theory states that the Fourier transform is a unitary transformation on $\mathcal{S}(\mathbb{R})$ .

该理论中的第二个主要定理指出，傅里叶变换是 $\mathcal{S}(\mathbb{R})$ 上的酉变换。

Theorem 1.12 (Plancherel) If $f\in \mathcal{S}(\mathbb{R})$ then $\| \hat{f}\| = \| f\|$ .

定理 1.12（普朗歇尔）若 $f\in \mathcal{S}(\mathbb{R})$，则 $\| \hat{f}\| = \| f\|$。

Proof. If $f\in \mathcal{S}(\mathbb{R})$ define $f^{p}(x) = \overline{f(- x)}$ . Then $\widehat{f^{p}} (\xi) = \overline{\hat{f} (\xi)}$ . Now let $h = f*f^{p}$ . Clearly, we have

$$\hat{h} (\xi) = |\hat{f} (\xi)|^{2}\quad \mathrm{and}\quad h(0) = \int_{-\infty}^{\infty}|f(x)|^{2}dx.$$

证明。若 $f\in \mathcal{S}(\mathbb{R})$，定义 $f^{p}(x) = \overline{f(- x)}$。则 $\widehat{f^{p}} (\xi) = \overline{\hat{f} (\xi)}$。现在令 $h = f*f^{p}$。显然，我们有

$$\hat{h} (\xi) = |\hat{f} (\xi)|^{2}\quad \mathrm{and}\quad h(0) = \int_{-\infty}^{\infty}|f(x)|^{2}dx.$$

===== Page 161 =====

The theorem now follows from the inversion formula applied with $x = 0$ that is,

$$\int_{-\infty}^{\infty}\hat{h} (\xi)d\xi = h(0).$$

现在定理由反演公式在 $x = 0$ 时的应用得出，即

$$\int_{-\infty}^{\infty}\hat{h} (\xi)d\xi = h(0).$$

### 1.7 Extension to functions of moderate decrease

### 1.7 推广到中度衰减函数

In the previous sections, we have limited our assertion of the Fourier inversion and Plancherel formulas to the case when the function involved belonged to the Schwartz space. It does not really involve further ideas to extend these results to functions of moderate decrease, once we make the additional assumption that the Fourier transform of the function under consideration is also of moderate decrease. Indeed, the key observation, which is easy to prove, is that the convolution $f*g$ of two functions $f$ and $g$ of moderate decrease is again a function of moderate decrease (Exercise 7); also $\widehat{f*g} = \hat{f}\hat{g}$ . Moreover, the multiplication formula continues to hold, and we deduce the Fourier inversion and Plancherel formulas when $f$ and $\hat{f}$ are both of moderate decrease.

在前面的章节中，我们将傅里叶反演和普朗歇尔公式的断言限制在所涉函数属于施瓦茨空间的情形。一旦我们额外假设所考虑函数的傅里叶变换也是中度衰减的，将这些结果推广到中度衰减函数并不需要引入更多的新思想。事实上，容易证明的关键观察是，两个中度衰减函数 $f$ 和 $g$ 的卷积 $f*g$ 仍然是中度衰减函数（习题 7）；并且 $\widehat{f*g} = \hat{f}\hat{g}$。此外，乘法公式仍然成立，并且当 $f$ 和 $\hat{f}$ 都是中度衰减时，我们推导出傅里叶反演和普朗歇尔公式。

This generalization, although modest in scope, is nevertheless useful in some circumstances.

这种推广虽然在范围上有限，但在某些情况下是有用的。

### 1.8 The Weierstrass approximation theorem

### 1.8 魏尔斯特拉斯逼近定理

We now digress briefly by further exploiting our good kernels to prove the Weierstrass approximation theorem. This result was already alluded to in Chapter 2.

我们现在简短地离题，进一步利用我们的好核来证明魏尔斯特拉斯逼近定理。这个结果在第 2 章中已经提到过。

Theorem 1.13 Let $f$ be a continuous function on the closed and bounded interval $[a,b]\subset \mathbb{R}$ . Then, for any $\epsilon >0$ , there exists a polynomial $P$ such that

$$\sup_{x\in [a,b]}|f(x) - P(x)|< \epsilon .$$

定理 1.13 设 $f$ 是闭有界区间 $[a,b]\subset \mathbb{R}$ 上的连续函数。则对任意 $\epsilon >0$，存在多项式 $P$ 使得

$$\sup_{x\in [a,b]}|f(x) - P(x)|< \epsilon .$$

In other words, $f$ can be uniformly approximated by polynomials.

换句话说，$f$ 可以被多项式一致逼近。

Proof. Let $[- M,M]$ denote any interval that contains $[a,b]$ in its interior, and let $g$ be a continuous function on $\mathbb{R}$ that equals 0 outside $[- M,M]$ and equals $f$ in $[a,b]$ . For example, extend $f$ as follows: from $b$ to $M$ define $g$ by a straight line segment going from $f(b)$ to 0, and from $a$ to $- M$ by a straight line segment from $f(a)$ also to 0. Let $B$ be a

证明。令 $[- M,M]$ 表示任一包含 $[a,b]$ 在其内部的区间，并令 $g$ 是 $\mathbb{R}$ 上的连续函数，在 $[- M,M]$ 外等于 0，在 $[a,b]$ 上等于 $f$。例如，如下延拓 $f$：从 $b$ 到 $M$，用从 $f(b)$ 到 0 的直线段定义 $g$；从 $a$ 到 $- M$，用从 $f(a)$ 到 0 的直线段定义 $g$。令 $B$ 是

===== Page 162 =====

bound for $g$ , that is, $|g(x)| \leq B$ for all $x$ . Then, since $\{K_{\delta}\}$ is a family of good kernels, and $g$ is continuous with compact support, we may argue as in the proof of Corollary 1.7 to see that $g * K_{\delta}$ converges uniformly to $g$ as $\delta$ tends to 0. In fact, we choose $\delta_{0}$ so that

$$|g(x) - (g * K_{\delta_0})(x)| < \epsilon /2 \quad \text{for all } x \in \mathbb{R}.$$

$g$ 的一个界，即对所有 $x$ 有 $|g(x)| \leq B$。然后，由于 $\{K_{\delta}\}$ 是一族好核，且 $g$ 连续且具有紧支集，我们可以像推论 1.7 的证明那样论证，看到当 $\delta$ 趋于 0 时 $g * K_{\delta}$ 一致收敛到 $g$。实际上，我们选择 $\delta_{0}$ 使得

$$|g(x) - (g * K_{\delta_0})(x)| < \epsilon /2 \quad \text{for all } x \in \mathbb{R}.$$

Now, we recall that $e^{x}$ is given by the power series expansion $e^{x} = \sum_{n = 0}^{\infty} x^{n} / n!$ which converges uniformly in every compact interval of $\mathbb{R}$ . Therefore, there exists an integer $N$ so that

$$|K_{\delta_0}(x) - R(x)| \leq \frac{\epsilon}{4MB} \quad \text{for all } x \in [-2M, 2M]$$

现在，我们回忆 $e^{x}$ 由幂级数展开 $e^{x} = \sum_{n = 0}^{\infty} x^{n} / n!$ 给出，该级数在 $\mathbb{R}$ 的每个紧区间上一致收敛。因此，存在整数 $N$ 使得

$$|K_{\delta_0}(x) - R(x)| \leq \frac{\epsilon}{4MB} \quad \text{for all } x \in [-2M, 2M]$$

where $\begin{array}{r}R(x) = \delta_0^{- 1 / 2}\sum_{n = 0}^{N}\frac{(- \pi x^2 / \delta_0)^n}{n!} \end{array}$ Then, recalling that $g$ vanishes outside the interval $[- M, M]$ , we have that for all $x \in [- M, M]$

$$|(g * K_{\delta_0})(x) - (g * R)(x)| = \left|\int_{-M}^{M} g(t) [K_{\delta_0}(x - t) - R(x - t)] dt\right|$$ $$\qquad \leq \int_{-M}^{M} |g(t)| |K_{\delta_0}(x - t) - R(x - t)| dt$$ $$\qquad \leq 2MB \sup_{z \in [-2M, 2M]} |K_{\delta_0}(z) - R(z)|$$ $$\qquad < \epsilon /2.$$

其中 $R(x) = \delta_0^{- 1 / 2}\sum_{n = 0}^{N}\frac{(- \pi x^2 / \delta_0)^n}{n!}$。然后，回忆 $g$ 在区间 $[- M, M]$ 外为零，我们有对所有 $x \in [- M, M]$

$$|(g * K_{\delta_0})(x) - (g * R)(x)| = \left|\int_{-M}^{M} g(t) [K_{\delta_0}(x - t) - R(x - t)] dt\right|$$ $$\qquad \leq \int_{-M}^{M} |g(t)| |K_{\delta_0}(x - t) - R(x - t)| dt$$ $$\qquad \leq 2MB \sup_{z \in [-2M, 2M]} |K_{\delta_0}(z) - R(z)|$$ $$\qquad < \epsilon /2.$$

Therefore, the triangle inequality implies that $|g(x) - (g * R)(x)| < \epsilon$ whenever $x \in [- M, M]$ , hence $|f(x) - (g * R)(x)| < \epsilon$ when $x \in [a, b]$ .

因此，三角不等式表明，当 $x \in [- M, M]$ 时 $|g(x) - (g * R)(x)| < \epsilon$，从而当 $x \in [a, b]$ 时 $|f(x) - (g * R)(x)| < \epsilon$。

Finally, note that $g * R$ is a polynomial in the $x$ variable. Indeed, by definition we have $(g * R)(x) = \int_{- M}^{M} g(t) R(x - t) dt$ , and $R(x - t)$ is a polynomial in $x$ since it can be expressed, after several expansions, as $R(x - t) = \sum_{n} a_{n}(t) x^{n}$ where the sum is finite. This concludes the proof of the theorem.

最后，注意 $g * R$ 是 $x$ 变量的多项式。实际上，根据定义我们有 $(g * R)(x) = \int_{- M}^{M} g(t) R(x - t) dt$，而 $R(x - t)$ 是 $x$ 的多项式，因为经过若干展开后它可以表示为 $R(x - t) = \sum_{n} a_{n}(t) x^{n}$，其中求和是有限的。这就完成了定理的证明。

## 2 Applications to some partial differential equations

## 2 在一些偏微分方程中的应用

We mentioned earlier that a crucial property of the Fourier transform is that it interchanges differentiation and multiplication by polynomials. We now use this crucial fact together with the Fourier inversion theorem to solve some specific partial differential equations.

我们之前提到，傅里叶变换的一个关键性质是它交换微分和乘以多项式。现在我们利用这一关键事实以及傅里叶反演定理来求解一些特定的偏微分方程。

### 2.1 The time-dependent heat equation on the real line

### 2.1 实直线上的时间相关热方程

In Chapter 4 we considered the heat equation on the circle. Here we study the analogous problem on the real line.

在第 4 章中，我们考虑了圆上的热方程。这里我们研究实直线上的类似问题。

===== Page 163 =====

Consider an infinite rod, which we model by the real line, and suppose that we are given an initial temperature distribution $f(x)$ on the rod at time $t = 0$ .We wish now to determine the temperature $u(x,t)$ at a point $x$ at time $t > 0$ .Considerations similar to the ones given in Chapter 1 show that when $u$ is appropriately normalized, it solves the following partial differential equation:

$$\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2}, \quad (8)$$

考虑一根无限长的杆，我们将其模型化为实直线，并假设在时间 $t = 0$ 时杆上有一个初始温度分布 $f(x)$。我们现在希望确定在时间 $t > 0$ 时点 $x$ 处的温度 $u(x,t)$。与第 1 章中类似的考虑表明，当 $u$ 被适当归一化时，它满足以下偏微分方程：

$$\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2}, \quad (8)$$

called the heat equation. The initial condition we impose is $u(x,0) = f(x)$ .

称为热方程。我们施加的初始条件是 $u(x,0) = f(x)$。

Just as in the case of the circle, the solution is given in terms of a convolution. Indeed, define the heat kernel of the line by

$$\mathcal{H}_t(x) = K_\delta (x),\quad \mathrm{with}\delta = 4\pi t,$$

正如圆上的情形，解由卷积给出。实际上，定义直线的热核为

$$\mathcal{H}_t(x) = K_\delta (x),\quad \mathrm{with}\delta = 4\pi t,$$

so that

$$\mathcal{H}_t(x) = \frac{1}{(4\pi t)^{1 / 2}} e^{-x^2 /4t}\quad \mathrm{and}\quad \hat{\mathcal{H}}_t(\xi) = e^{-4\pi^2 t\xi^2}.$$

于是

$$\mathcal{H}_t(x) = \frac{1}{(4\pi t)^{1 / 2}} e^{-x^2 /4t}\quad \mathrm{and}\quad \hat{\mathcal{H}}_t(\xi) = e^{-4\pi^2 t\xi^2}.$$

Taking the Fourier transform of equation (8) in the $x$ variable (formally) leads to

$$\frac{\partial\hat{u}}{\partial t} (\xi ,t) = -4\pi^2 \xi^2 \hat{u} (\xi ,t).$$

对方程 (8) 关于 $x$ 变量（形式地）取傅里叶变换，得到

$$\frac{\partial\hat{u}}{\partial t} (\xi ,t) = -4\pi^2 \xi^2 \hat{u} (\xi ,t).$$

Fixing $\xi$ , this is an ordinary differential equation in the variable $t$ (with unknown $\hat{u} (\xi ,\cdot)$ ), so there exists a constant $A(\xi)$ so that

$$\hat{u} (\xi ,t) = A(\xi)e^{-4\pi^2 \xi^2 t}.$$

固定 $\xi$，这是关于变量 $t$ 的常微分方程（未知函数为 $\hat{u} (\xi ,\cdot)$），因此存在常数 $A(\xi)$ 使得

$$\hat{u} (\xi ,t) = A(\xi)e^{-4\pi^2 \xi^2 t}.$$

We may also take the Fourier transform of the initial condition and obtain $\hat{u} (\xi ,0) = \hat{f} (\xi)$ , hence $A(\xi) = \hat{f} (\xi)$ . This leads to the following theorem.

我们也可以对初始条件取傅里叶变换，得到 $\hat{u} (\xi ,0) = \hat{f} (\xi)$，因此 $A(\xi) = \hat{f} (\xi)$。这就引出了以下定理。

Theorem 2.1 Given $f\in \mathcal{S}(\mathbb{R})$ ,let

$$u(x,t) = (f*\mathcal{H}_t)(x)\quad for t > 0$$

where $\mathcal{H}_t$ is the heat kernel. Then:

定理 2.1 给定 $f\in \mathcal{S}(\mathbb{R})$，令

$$u(x,t) = (f*\mathcal{H}_t)(x)\quad for t > 0$$

其中 $\mathcal{H}_t$ 是热核。则：

(i) The function $u$ is $C^2$ when $x\in \mathbb{R}$ and $t > 0$ ,and $u$ solves the heat equation.

(i) 当 $x\in \mathbb{R}$ 且 $t > 0$ 时，函数 $u$ 是 $C^2$ 的，并且 $u$ 满足热方程。

===== Page 164 =====

(ii) $u(x,t)\to f(x)$ uniformly in $x$ as $t\to 0$ .Hence if we set $u(x,0) =$ $f(x)$ ,then $u$ is continuous on the closure of the upper half- plane

$$\overline{\mathbb{R}_+^2} = \{(x,t):x\in \mathbb{R},t\geq 0\} .$$

(ii) 当 $t\to 0$ 时，$u(x,t)\to f(x)$ 在 $x$ 上一致。因此如果我们设 $u(x,0) = f(x)$，则 $u$ 在上半平面的闭包上连续

$$\overline{\mathbb{R}_+^2} = \{(x,t):x\in \mathbb{R},t\geq 0\} .$$

(iii) Moreover, $\int_{-\infty}^{\infty}|u(x,t) - f(x)|^{2}d x\to 0$ as $t\to 0$.

(iii) 此外，当 $t\to 0$ 时，$\int_{-\infty}^{\infty}|u(x,t) - f(x)|^{2}d x\to 0$。

Proof. Because $u = f*\mathcal{H}_t$ , taking the Fourier transform in the $x$ variable gives $\hat{u} = \hat{f}\hat{\mathcal{H}}_t$ , and so $\hat{u} (\xi ,t) = \hat{f} (\xi)e^{- 4\pi^2 \xi^2 t}$ . The Fourier inversion formula gives

$$u(x,t) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{-4\pi^2 t\xi^2}e^{2\pi i\xi x}d\xi .$$

证明。由于 $u = f*\mathcal{H}_t$，关于 $x$ 变量取傅里叶变换得到 $\hat{u} = \hat{f}\hat{\mathcal{H}}_t$，因此 $\hat{u} (\xi ,t) = \hat{f} (\xi)e^{- 4\pi^2 \xi^2 t}$。傅里叶反演公式给出

$$u(x,t) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{-4\pi^2 t\xi^2}e^{2\pi i\xi x}d\xi .$$

By differentiating under the integral sign, one verifies (i). In fact, one observes that $u$ is indefinitely differentiable. Note that (ii) is an immediate consequence of Corollary 1.7. Finally, by Plancherel's formula, we have

$$\int_{-\infty}^{\infty}|u(x,t) - f(x)|^{2}d x = \int_{-\infty}^{\infty}|\hat{u} (\xi ,t) - \hat{f} (\xi)|^{2}d\xi$$ $$= \int_{-\infty}^{\infty}|\hat{f} (\xi)|^{2}|e^{-4\pi^{2}t\xi^{2}} - 1|d\xi .$$

通过在积分号下求导，可以验证 (i)。实际上，观察到 $u$ 是无限可微的。注意 (ii) 是推论 1.7 的直接结果。最后，由普朗歇尔公式，我们有

$$\int_{-\infty}^{\infty}|u(x,t) - f(x)|^{2}d x = \int_{-\infty}^{\infty}|\hat{u} (\xi ,t) - \hat{f} (\xi)|^{2}d\xi$$ $$= \int_{-\infty}^{\infty}|\hat{f} (\xi)|^{2}|e^{-4\pi^{2}t\xi^{2}} - 1|d\xi .$$

To see that this last integral goes to 0 as $t\to 0$ , we argue as follows: since $|e^{- 4\pi^2 t\xi^2} - 1|\leq 2$ and $f\in \mathcal{S}(\mathbb{R})$ , we can find $N$ so that

$$\int_{|\xi |\geq N}|\hat{f} (\xi)|^{2}|e^{-4\pi^{2}t\xi^{2}} - 1|d\xi < \epsilon ,$$

要看出最后一个积分当 $t\to 0$ 时趋于 0，我们论证如下：由于 $|e^{- 4\pi^2 t\xi^2} - 1|\leq 2$ 且 $f\in \mathcal{S}(\mathbb{R})$，我们可以找到 $N$ 使得

$$\int_{|\xi |\geq N}|\hat{f} (\xi)|^{2}|e^{-4\pi^{2}t\xi^{2}} - 1|d\xi < \epsilon ,$$

and for all small $t$ we have $\sup_{|\xi |\leq N}|\hat{f} (\xi)|^{2}|e^{- 4\pi^{2}t\xi^{2}} - 1|< \epsilon /2N$ since $\hat{f}$ is bounded. Thus

$$\int_{|\xi |\leq N}|\hat{f} (\xi)|^{2}|e^{-4\pi^{2}t\xi^{2}} - 1|d\xi < \epsilon \quad \mathrm{for~all~small~}t.$$

并且对所有小的 $t$，由于 $\hat{f}$ 有界，我们有 $\sup_{|\xi |\leq N}|\hat{f} (\xi)|^{2}|e^{- 4\pi^{2}t\xi^{2}} - 1|< \epsilon /2N$。因此

$$\int_{|\xi |\leq N}|\hat{f} (\xi)|^{2}|e^{-4\pi^{2}t\xi^{2}} - 1|d\xi < \epsilon \quad \mathrm{for~all~small~}t.$$

This completes the proof of the theorem.

这就完成了定理的证明。

The above theorem guarantees the existence of a solution to the heat equation with initial data $f$ . This solution is also unique, if uniqueness is formulated appropriately. In this regard, we note that $u = f*\mathcal{H}_t$ , $f\in \mathcal{S}(\mathbb{R})$ , satisfies the following additional property.

上述定理保证了具有初始数据 $f$ 的热方程解的存在性。如果适当地表述唯一性，该解也是唯一的。在这方面，我们注意到 $u = f*\mathcal{H}_t$（$f\in \mathcal{S}(\mathbb{R})$）满足以下附加性质。

Corollary 2.2 $u(\cdot ,t)$ belongs to $\mathcal{S}(\mathbb{R})$ uniformly in $t$ , in the sense that for any $T > 0$

$$\sup_{x\in \mathbb{R}\atop 0< t< T}|x|^k\left|\frac{\partial^\ell}{\partial x^\ell}u(x,t)\right|< \infty \quad \text{for each} k,\ell \geq 0. \quad (9)$$

推论 2.2 $u(\cdot ,t)$ 属于 $\mathcal{S}(\mathbb{R})$ 且关于 $t$ 一致，即对任意 $T > 0$ 和每个 $k,\ell \geq 0$，

$$\sup_{x\in \mathbb{R}\atop 0< t< T}|x|^k\left|\frac{\partial^\ell}{\partial x^\ell}u(x,t)\right|< \infty. \quad (9)$$

===== Page 165 =====

Proof. This result is a consequence of the following estimate:

$$\begin{array}{rl} & {|u(x,t)|\leq \int_{|y|\leq |x| / 2}|f(x - y)|\mathcal{H}_t(y)dy + \int_{|y|\geq |x| / 2}|f(x - y)|\mathcal{H}_t(y)}\\ & {\qquad \leq \frac{C_N}{(1 + |x|)^N} +\frac{C}{\sqrt{t}} e^{-cx^2 /t}.} \end{array} \quad (1)$$

证明。这个结果是以下估计的推论：

$$\begin{array}{rl} & {|u(x,t)|\leq \int_{|y|\leq |x| / 2}|f(x - y)|\mathcal{H}_t(y)dy + \int_{|y|\geq |x| / 2}|f(x - y)|\mathcal{H}_t(y)}\\ & {\qquad \leq \frac{C_N}{(1 + |x|)^N} +\frac{C}{\sqrt{t}} e^{-cx^2 /t}.} \end{array} \quad (1)$$

Indeed, since $f$ is rapidly decreasing, we have $|f(x - y)|\leq C_N / (1 + |x|)^N$ when $|y|\leq |x| / 2$ . Also, if $|y|\geq |x| / 2$ then $\mathcal{H}_t(y)\leq Ct^{- 1 / 2}e^{- cx^2 /t}$ , and we obtain the above inequality. Consequently, we see that $u(x,t)$ is rapidly decreasing uniformly for $0< t< T$ .

实际上，由于 $f$ 是快速递减的，当 $|y|\leq |x| / 2$ 时我们有 $|f(x - y)|\leq C_N / (1 + |x|)^N$。此外，若 $|y|\geq |x| / 2$，则 $\mathcal{H}_t(y)\leq Ct^{- 1 / 2}e^{- cx^2 /t}$，我们得到上述不等式。因此，我们看到 $u(x,t)$ 在 $0< t< T$ 上一致快速递减。

The same argument can be applied to the derivatives of $u$ in the $x$ variable since we may differentiate under the integral sign and apply the above estimate with $f$ replaced by $f^{\prime}$ , and so on.

同样的论证可以应用于 $u$ 关于 $x$ 变量的导数，因为我们可以在积分号下求导，并将上述估计中的 $f$ 替换为 $f^{\prime}$，依此类推。

This leads to the following uniqueness theorem.

这导致以下唯一性定理。

Theorem 2.3 Suppose $u(x,t)$ satisfies the following conditions:

(i) $u$ is continuous on the closure of the upper half-plane. (ii) $u$ satisfies the heat equation for $t > 0$ . (iii) $u$ satisfies the boundary condition $u(x,0) = 0$ . (iv) $u(\cdot ,t)\in \mathcal{S}(\mathbb{R})$ uniformly in $t$ , as in (9).

Then, we conclude that $u = 0$ .

定理 2.3 假设 $u(x,t)$ 满足以下条件：

(i) $u$ 在上半平面的闭包上连续。(ii) $u$ 对 $t > 0$ 满足热方程。(iii) $u$ 满足边界条件 $u(x,0) = 0$。(iv) $u(\cdot ,t)\in \mathcal{S}(\mathbb{R})$ 且关于 $t$ 一致，如 (9) 所示。

于是我们得出结论 $u = 0$。

Below we use the abbreviations $\partial_{x}^{t}u$ and $\partial_{t}u$ to denote $\partial^{t}u / \partial x^{t}$ and $\partial u / \partial t$ , respectively.

下面我们使用缩写 $\partial_{x}^{t}u$ 和 $\partial_{t}u$ 分别表示 $\partial^{t}u / \partial x^{t}$ 和 $\partial u / \partial t$。

Proof. We define the energy at time $t$ of the solution $u(x,t)$ by

$$E(t) = \int_{\mathbb{R}}|u(x,t)|^{2}dx.$$

证明。我们定义解 $u(x,t)$ 在时间 $t$ 的能量为

$$E(t) = \int_{\mathbb{R}}|u(x,t)|^{2}dx.$$

Clearly $E(t)\geq 0$ . Since $E(0) = 0$ it suffices to show that $E$ is a decreasing function, and this is achieved by proving that $dE / dt\leq 0$ . The assumptions on $u$ allow us to differentiate $E(t)$ under the integral sign

$$\frac{dE}{dt} = \int_{\mathbb{R}}[\partial_{t}u(x,t)\overline{u} (x,t) + u(x,t)\partial_{t}\overline{u} (x,t)]dx.$$

显然 $E(t)\geq 0$。由于 $E(0) = 0$，只需证明 $E$ 是递减函数，这通过证明 $dE / dt\leq 0$ 来实现。对 $u$ 的假设允许我们在积分号下对 $E(t)$ 求导

$$\frac{dE}{dt} = \int_{\mathbb{R}}[\partial_{t}u(x,t)\overline{u} (x,t) + u(x,t)\partial_{t}\overline{u} (x,t)]dx.$$

But $u$ satisfies the heat equation, therefore $\partial_{t}u = \partial_{x}^{2}u$ and $\partial_{t}\overline{u} = \partial_{x}^{2}\overline{u}$ , so that after an integration by parts, where we use the fact that $u$ and its

但 $u$ 满足热方程，因此 $\partial_{t}u = \partial_{x}^{2}u$ 且 $\partial_{t}\overline{u} = \partial_{x}^{2}\overline{u}$，所以在分部积分之后（利用 $u$ 及其

===== Page 166 =====

$x$ derivatives decrease rapidly as $|x|\to \infty$ , we find

$$\frac{dE}{dt} = \int_{\mathbb{R}}\left[\partial_x^2 u(x,t)\overline{u} (x,t) + u(x,t)\partial_x^2\overline{u} (x,t)\right]dx$$ $$= -\int_{\mathbb{R}}\left[\partial_xu(x,t)\partial_x\overline{u} (x,t) + \partial_xu(x,t)\partial_x\overline{u} (x,t)\right]dx$$ $$= -2\int_{\mathbb{R}}|\partial_xu(x,t)|^2 dx$$ $$\leq 0,$$

$x$ 导数当 $|x|\to \infty$ 时快速递减），我们发现

$$\frac{dE}{dt} = \int_{\mathbb{R}}\left[\partial_x^2 u(x,t)\overline{u} (x,t) + u(x,t)\partial_x^2\overline{u} (x,t)\right]dx$$ $$= -\int_{\mathbb{R}}\left[\partial_xu(x,t)\partial_x\overline{u} (x,t) + \partial_xu(x,t)\partial_x\overline{u} (x,t)\right]dx$$ $$= -2\int_{\mathbb{R}}|\partial_xu(x,t)|^2 dx$$ $$\leq 0,$$

as claimed. Thus $E(t) = 0$ for all $t$ , hence $u = 0$ .

如所述。因此对所有 $t$ 有 $E(t) = 0$，从而 $u = 0$。

Another uniqueness theorem for the heat equation, with a less restrictive assumption than (9), can be found in Problem 6. Examples when uniqueness fails are given in Exercise 12 and Problem 4.

热方程的另一个唯一性定理（其假设比 (9) 更弱）可以在问题 6 中找到。唯一性失效的例子在习题 12 和问题 4 中给出。

### 2.2 The steady-state heat equation in the upper half-plane

### 2.2 上半平面中的稳态热方程

The equation we are now concerned with is

$$\triangle u = \frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2} = 0 \quad (10)$$

我们现在关注的方程是

$$\triangle u = \frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2} = 0 \quad (10)$$

in the upper half- plane $\mathbb{R}_+^2 = \{(x,y):x\in \mathbb{R},y > 0\}$ . The boundary condition we require is $u(x,0) = f(x)$ . The operator $\triangle$ is the Laplacian and the above partial differential equation describes the steady- state heat distribution in $\mathbb{R}_+^2$ subject to $u = f$ on the boundary. The kernel that solves this problem is called the Poisson kernel for the upper half- plane, and is given by

$$\mathcal{P}_y(x) = \frac{1}{\pi}\frac{y}{x^2 + y^2}\quad \mathrm{where~}x\in \mathbb{R}\mathrm{~and~}y > 0.$$

在上半平面 $\mathbb{R}_+^2 = \{(x,y):x\in \mathbb{R},y > 0\}$ 中。我们要求的边界条件是 $u(x,0) = f(x)$。算子 $\triangle$ 是拉普拉斯算子，上述偏微分方程描述了 $\mathbb{R}_+^2$ 中满足边界上 $u = f$ 的稳态热分布。解决这个问题的核称为上半平面的泊松核，由下式给出：

$$\mathcal{P}_y(x) = \frac{1}{\pi}\frac{y}{x^2 + y^2}\quad \mathrm{where~}x\in \mathbb{R}\mathrm{~and~}y > 0.$$

This is the analogue of the Poisson kernel for the disc discussed in Section 5.4 of Chapter 2.

这是第 2 章第 5.4 节中讨论的圆盘泊松核的类比。

Note that for each fixed $y$ the kernel $\mathcal{P}_y$ is only of moderate decrease as a function of $x$ , so we will use the theory of the Fourier transform appropriate for these types of functions (see Section 1.7).

注意，对每个固定的 $y$，核 $\mathcal{P}_y$ 作为 $x$ 的函数只是中度衰减的，因此我们将使用适用于这些类型函数的傅里叶变换理论（见第 1.7 节）。

We proceed as in the case of the time- dependent heat equation, by taking the Fourier transform of equation (10) (formally) in the $x$ variable, thereby obtaining

$$-4\pi^2 \xi^2 \hat{u}(\xi , y) + \frac{\partial^2 \hat{u}}{\partial y^2} (\xi , y) = 0$$

我们按照时间相关热方程的情形进行，对方程 (10) 关于 $x$ 变量（形式地）取傅里叶变换，从而得到

$$-4\pi^2 \xi^2 \hat{u}(\xi , y) + \frac{\partial^2 \hat{u}}{\partial y^2} (\xi , y) = 0$$

===== Page 167 =====

with the boundary condition $\hat{u} (\xi ,0) = \hat{f} (\xi)$ . The general solution of this ordinary differential equation in $y$ (with $\xi$ fixed) takes the form

$$\hat{u} (\xi ,y) = A(\xi)e^{-2\pi |\xi |y} + B(\xi)e^{2\pi |\xi |y}.$$

带有边界条件 $\hat{u} (\xi ,0) = \hat{f} (\xi)$。这个关于 $y$ 的常微分方程（$\xi$ 固定）的通解形式为

$$\hat{u} (\xi ,y) = A(\xi)e^{-2\pi |\xi |y} + B(\xi)e^{2\pi |\xi |y}.$$

If we disregard the second term because of its rapid exponential increase we find, after setting $y = 0$ , that

$$\hat{u} (\xi ,y) = \hat{f} (\xi)e^{-2\pi |\xi |y}.$$

如果我们因为第二项指数增长过快而忽略它，则在设 $y = 0$ 后发现

$$\hat{u} (\xi ,y) = \hat{f} (\xi)e^{-2\pi |\xi |y}.$$

Therefore $u$ is given in terms of the convolution of $f$ with a kernel whose Fourier transform is $e^{- 2\pi |\xi |y}$ . This is precisely the Poisson kernel given above, as we prove next.

因此 $u$ 由 $f$ 与一个其傅里叶变换为 $e^{- 2\pi |\xi |y}$ 的核的卷积给出。正如我们接下来证明的，这正是上面给出的泊松核。

Lemma 2.4 The following two identities hold:

$$\int_{-\infty}^{\infty}e^{-2\pi |\xi |y}e^{2\pi i\xi x}d\xi = \mathcal{P}_y(x),$$ $$\int_{-\infty}^{\infty}\mathcal{P}_y(x)e^{-2\pi i\xi x}d x = e^{-2\pi |\xi |y}.$$

引理 2.4 以下两个恒等式成立：

$$\int_{-\infty}^{\infty}e^{-2\pi |\xi |y}e^{2\pi i\xi x}d\xi = \mathcal{P}_y(x),$$ $$\int_{-\infty}^{\infty}\mathcal{P}_y(x)e^{-2\pi i\xi x}d x = e^{-2\pi |\xi |y}.$$

Proof. The first formula is fairly straightforward since we can split the integral from $- \infty$ to 0 and 0 to $\infty$ . Then, since $y > 0$ we have

$$\int_{0}^{\infty}e^{-2\pi \xi y}e^{2\pi i\xi x}d\xi = \int_{0}^{\infty}e^{2\pi i(x + iy)\xi}d\xi = \left[\frac{e^{2\pi i(x + iy)\xi}}{2\pi i(x + iy)}\right]_{0}^{\infty} =$$ $$\qquad -\frac{1}{2\pi i(x + iy)},$$

证明。第一个公式相当直接，因为我们可以将积分从 $- \infty$ 到 0 和从 0 到 $\infty$ 分开。然后，由于 $y > 0$，我们有

$$\int_{0}^{\infty}e^{-2\pi \xi y}e^{2\pi i\xi x}d\xi = \int_{0}^{\infty}e^{2\pi i(x + iy)\xi}d\xi = \left[\frac{e^{2\pi i(x + iy)\xi}}{2\pi i(x + iy)}\right]_{0}^{\infty} =$$ $$\qquad -\frac{1}{2\pi i(x + iy)},$$

and similarly,

$$\int_{-\infty}^{0}e^{2\pi \xi y}e^{2\pi i\xi x}d\xi = \frac{1}{2\pi i(x - iy)}.$$

类似地，

$$\int_{-\infty}^{0}e^{2\pi \xi y}e^{2\pi i\xi x}d\xi = \frac{1}{2\pi i(x - iy)}.$$

Therefore

$$\int_{-\infty}^{\infty}e^{-2\pi |\xi |y}e^{2\pi i\xi x}d\xi = \frac{1}{2\pi i(x - iy)} -\frac{1}{2\pi i(x + iy)} = \frac{y}{\pi(x^{2} + y^{2})}.$$

因此

$$\int_{-\infty}^{\infty}e^{-2\pi |\xi |y}e^{2\pi i\xi x}d\xi = \frac{1}{2\pi i(x - iy)} -\frac{1}{2\pi i(x + iy)} = \frac{y}{\pi(x^{2} + y^{2})}.$$

The second formula is now a consequence of the Fourier inversion theorem applied in the case when $f$ and $\hat{f}$ are of moderate decrease.

第二个公式现在是傅里叶反演定理在 $f$ 和 $\hat{f}$ 都是中度衰减情形下的推论。

Lemma 2.5 The Poisson kernel is a good kernel on $\mathbb{R}$ as $y \to 0$ .

引理 2.5 当 $y \to 0$ 时，泊松核是 $\mathbb{R}$ 上的好核。

===== Page 168 =====

Proof. Setting $\xi = 0$ in the second formula of the lemma shows that $\int_{-\infty}^{\infty}\mathcal{P}_{y}(x)dx = 1$ , and clearly $\mathcal{P}_{y}(x)\geq 0$ , so it remains to check the last property of good kernels. Given a fixed $\delta >0$ , we may change variables $u = x / y$ so that

$$\int_{\delta}^{\infty}\frac{y}{x^{2} + y^{2}} dx = \int_{\delta /y}^{\infty}\frac{du}{1 + u^{2}} = [\arctan u]_{\delta /y}^{\infty} = \pi /2 - \arctan (\delta /y),$$

证明。在引理的第二个公式中设 $\xi = 0$ 表明 $\int_{-\infty}^{\infty}\mathcal{P}_{y}(x)dx = 1$，并且显然 $\mathcal{P}_{y}(x)\geq 0$，因此只需检查好核的最后一个性质。给定固定的 $\delta >0$，我们可以变换变量 $u = x / y$，使得

$$\int_{\delta}^{\infty}\frac{y}{x^{2} + y^{2}} dx = \int_{\delta /y}^{\infty}\frac{du}{1 + u^{2}} = [\arctan u]_{\delta /y}^{\infty} = \pi /2 - \arctan (\delta /y),$$

and this quantity goes to 0 as $y\rightarrow 0$ . Since $\mathcal{P}_{y}(x)$ is an even function, the proof is complete.

这个量当 $y\rightarrow 0$ 时趋于 0。由于 $\mathcal{P}_{y}(x)$ 是偶函数，证明完成。

The following theorem establishes the existence of a solution to our problem.

以下定理确立了我们的问题解的存在性。

Theorem 2.6 Given $f\in \mathcal{S}(\mathbb{R})$ , let $u(x,y) = (f*\mathcal{P}_{y})(x)$ . Then:

(i) $u(x,y)$ is $C^2$ in $\mathbb{R}_+^2$ and $\Delta u = 0$ . (ii) $u(x,y)\rightarrow f(x)$ uniformly as $y\rightarrow 0$ . (iii) $\int_{-\infty}^{\infty}|u(x,y) - f(x)|^2 dx\rightarrow 0$ as $y\rightarrow 0$ . (iv) If $u(x,0) = f(x)$ , then $u$ is continuous on the closure $\overline{\mathbb{R}_+^2}$ of the upper half-plane, and vanishes at infinity in the sense that $u(x,y)\rightarrow 0$ as $|x|\rightarrow \infty$ .

$$u(x,y)\rightarrow 0\quad as|x| + y\rightarrow \infty .$$

定理 2.6 给定 $f\in \mathcal{S}(\mathbb{R})$，令 $u(x,y) = (f*\mathcal{P}_{y})(x)$。则：

(i) $u(x,y)$ 在 $\mathbb{R}_+^2$ 中是 $C^2$ 的，且 $\Delta u = 0$。(ii) 当 $y\rightarrow 0$ 时 $u(x,y)\rightarrow f(x)$ 一致。(iii) 当 $y\rightarrow 0$ 时 $\int_{-\infty}^{\infty}|u(x,y) - f(x)|^2 dx\rightarrow 0$。(iv) 若设 $u(x,0) = f(x)$，则 $u$ 在上半平面的闭包 $\overline{\mathbb{R}_+^2}$ 上连续，并且在无穷远处消失，即当 $|x|\rightarrow \infty$ 时 $u(x,y)\rightarrow 0$，且

$$u(x,y)\rightarrow 0\quad as|x| + y\rightarrow \infty .$$

Proof. The proofs of parts (i), (ii), and (iii) are similar to the case of the heat equation, and so are left to the reader. Part (iv) is a consequence of two easy estimates whenever $f$ is of moderate decrease. First, we have

$$|(f*\mathcal{P}_y)(x)|\leq C\left(\frac{1}{(1 + x^2)} +\frac{y}{x^2 + y^2}\right)$$

证明。(i)、(ii) 和 (iii) 部分的证明与热方程的情形类似，因此留给读者。第 (iv) 部分是当 $f$ 中度衰减时两个简单估计的推论。首先，我们有

$$|(f*\mathcal{P}_y)(x)|\leq C\left(\frac{1}{(1 + x^2)} +\frac{y}{x^2 + y^2}\right)$$

which is proved (as in the case of the heat equation) by splitting the integral $\int_{-\infty}^{\infty}f(x - t)\mathcal{P}_y(t)dt$ into the part where $|t|\leq |x| / 2$ and the part where $|t|\geq |x| / 2$ . Also, we have $|(f*\mathcal{P}_y)(x)|\leq C / y$ , since $\sup_{x}\mathcal{P}_{y}(x)\leq$ $c / y$ .

这通过将积分 $\int_{-\infty}^{\infty}f(x - t)\mathcal{P}_y(t)dt$ 分成 $|t|\leq |x| / 2$ 和 $|t|\geq |x| / 2$ 两部分来证明（如热方程的情形）。此外，由于 $\sup_{x}\mathcal{P}_{y}(x)\leq c / y$，我们有 $|(f*\mathcal{P}_y)(x)|\leq C / y$。

Using the first estimate when $|x|\geq |y|$ and the second when $|x|\leq |y|$ gives the desired decrease at infinity.

当 $|x|\geq |y|$ 时使用第一个估计，当 $|x|\leq |y|$ 时使用第二个估计，就得到了在无穷远处的所需衰减。

We next show that the solution is essentially unique.

接下来我们证明解本质上是唯一的。

Theorem 2.7 Suppose $u$ is continuous on the closure of the upper half- plane $\mathbb{R}_+^2$ , satisfies $\Delta u = 0$ for $(x,y)\in \mathbb{R}_+^2$ , $u(x,0) = 0$ , and $u(x,y)$ vanishes at infinity. Then $u = 0$ .

定理 2.7 假设 $u$ 在上半平面 $\mathbb{R}_+^2$ 的闭包上连续，对 $(x,y)\in \mathbb{R}_+^2$ 满足 $\Delta u = 0$，$u(x,0) = 0$，并且 $u(x,y)$ 在无穷远处消失。则 $u = 0$。

===== Page 169 =====

A simple example shows that a condition concerning the decay of $u$ at infinity is needed: take $u(x,y) = y$ . Clearly $u$ satisfies the steady- state heat equation and vanishes on the real line, yet $u$ is not identically zero.

一个简单的例子表明，关于 $u$ 在无穷远处衰减的条件是必要的：取 $u(x,y) = y$。显然 $u$ 满足稳态热方程并在实直线上消失，但 $u$ 不恒为零。

The proof of the theorem relies on a basic fact about harmonic functions, which are functions satisfying $\triangle u = 0$ . The fact is that the value of a harmonic function at a point equals its average value around any circle centered at that point.

该定理的证明依赖于调和函数（即满足 $\triangle u = 0$ 的函数）的一个基本事实。这个事实是：调和函数在一点的值等于它在该点为中心的任何圆上的平均值。

Lemma 2.8 (Mean- value property) Suppose $\Omega$ is an open set in $\mathbb{R}^2$ and let $u$ be a function of class $C^2$ with $\triangle u = 0$ in $\Omega$ . If the closure of the disc centered at $(x,y)$ and of radius $R$ is contained in $\Omega$ , then

$$u(x,y) = \frac{1}{2\pi}\int_{0}^{2\pi}u(x + r\cos \theta ,y + r\sin \theta)d\theta$$

for all $0\leq r\leq R$

引理 2.8（平均值性质）设 $\Omega$ 是 $\mathbb{R}^2$ 中的开集，且 $u$ 是 $C^2$ 类函数，在 $\Omega$ 中满足 $\triangle u = 0$。如果以 $(x,y)$ 为中心、半径为 $R$ 的圆的闭包包含在 $\Omega$ 中，则对所有 $0\leq r\leq R$，

$$u(x,y) = \frac{1}{2\pi}\int_{0}^{2\pi}u(x + r\cos \theta ,y + r\sin \theta)d\theta$$

Proof. Let $U(r,\theta) = u(x + r\cos \theta ,y + r\sin \theta)$ . Expressing the Laplacian in polar coordinates, the equation $\triangle u = 0$ then implies

$$0 = \frac{\partial^2U}{\partial\theta^2} +r\frac{\partial}{\partial r}\left(r\frac{\partial U}{\partial r}\right).$$

证明。令 $U(r,\theta) = u(x + r\cos \theta ,y + r\sin \theta)$。将拉普拉斯算子用极坐标表示，方程 $\triangle u = 0$ 蕴含

$$0 = \frac{\partial^2U}{\partial\theta^2} +r\frac{\partial}{\partial r}\left(r\frac{\partial U}{\partial r}\right).$$

If we define $F(r) = \frac{1}{2\pi}\int_{0}^{2\pi}U(r,\theta)d\theta$ , the above gives

$$r\frac{\partial}{\partial r}\left(r\frac{\partial F}{\partial r}\right) = \frac{1}{2\pi}\int_{0}^{2\pi} - \frac{\partial^2U}{\partial\theta^2} (r,\theta)d\theta .$$

如果我们定义 $F(r) = \frac{1}{2\pi}\int_{0}^{2\pi}U(r,\theta)d\theta$，则上式给出

$$r\frac{\partial}{\partial r}\left(r\frac{\partial F}{\partial r}\right) = \frac{1}{2\pi}\int_{0}^{2\pi} - \frac{\partial^2U}{\partial\theta^2} (r,\theta)d\theta .$$

The integral of $\partial^2 U / \partial \theta^2$ over the circle vanishes since $\partial U / \partial \theta$ is periodic, hence $r\frac{\partial}{\partial r}\left(r\frac{\partial F}{\partial r}\right) = 0$ , and consequently $r\partial F / \partial r$ must be constant. Evaluating this expression at $r = 0$ we find that $\partial F / \partial r = 0$ . Thus $F$ is constant, but since $F(0) = u(x,y)$ , we finally find that $F(r) = u(x,y)$ for all $0\leq r\leq R$ , which is the mean- value property.

$\partial^2 U / \partial \theta^2$ 在圆上的积分为零，因为 $\partial U / \partial \theta$ 是周期的，因此 $r\frac{\partial}{\partial r}\left(r\frac{\partial F}{\partial r}\right) = 0$，从而 $r\partial F / \partial r$ 必须是常数。在 $r = 0$ 处计算该表达式，我们发现 $\partial F / \partial r = 0$。因此 $F$ 是常数，但由于 $F(0) = u(x,y)$，我们最终得到对所有 $0\leq r\leq R$ 有 $F(r) = u(x,y)$，这就是平均值性质。

Finally, note that the argument above is implicit in the proof of Theorem 5.7, Chapter 2.

最后，注意上述论证隐含在第 2 章定理 5.7 的证明中。

To prove Theorem 2.7 we argue by contradiction. Considering separately the real and imaginary parts of $u$ , we may suppose that $u$ itself is real- valued, and is somewhere strictly positive, say $u(x_0,y_0) > 0$ for some $x_0\in \mathbb{R}$ and $y_0 > 0$ . We shall see that this leads to a contradiction. First, since $u$ vanishes at infinity, we can find a large semi- disc of radius $R$ $D_{R}^{+} = \{(x,y):x^{2} + y^{2}\leq R,y\geq 0\}$ outside of which $u(x,y)\leq$ $\textstyle {\frac{1}{2}}u(x_0,y_0)$ . Next, since $u$ is continuous in $D_{R}^{+}$ , it attains its maximum $M$ there, so there exists a point $(x_{1},y_{1})\in D_{R}^{+}$ with $u(x_{1},y_{1}) = M$ , while

为了证明定理 2.7，我们采用反证法。分别考虑 $u$ 的实部和虚部，我们可以假设 $u$ 本身是实值的，并且在某处严格为正，例如存在 $x_0\in \mathbb{R}$ 和 $y_0 > 0$ 使得 $u(x_0,y_0) > 0$。我们将看到这导致矛盾。首先，由于 $u$ 在无穷远处消失，我们可以找到一个半径为 $R$ 的大半圆盘 $D_{R}^{+} = \{(x,y):x^{2} + y^{2}\leq R,y\geq 0\}$，在其外部有 $u(x,y)\leq \frac{1}{2}u(x_0,y_0)$。其次，由于 $u$ 在 $D_{R}^{+}$ 上连续，它在某处达到最大值 $M$，因此存在点 $(x_{1},y_{1})\in D_{R}^{+}$ 使得 $u(x_{1},y_{1}) = M$，而

===== Page 170 =====

$u(x,y)\leq M$ in the semi- disc; also, since $u(x,y)\leq \textstyle {\frac{1}{2}}u(x_0,y_0)\leq M / 2$ outside of the semi- disc, we have $u(x,y)\leq M$ throughout the entire upper half- plane. Now the mean- value property for harmonic functions implies

$$u(x_1,y_1) = \frac{1}{2\pi}\int_0^{2\pi}u(x_1 + \rho \cos \theta ,y_1 + \rho \sin \theta)d\theta$$

在半圆盘内 $u(x,y)\leq M$；此外，由于在半圆盘外 $u(x,y)\leq \frac{1}{2}u(x_0,y_0)\leq M / 2$，在整个上半平面有 $u(x,y)\leq M$。现在调和函数的平均值性质蕴含

$$u(x_1,y_1) = \frac{1}{2\pi}\int_0^{2\pi}u(x_1 + \rho \cos \theta ,y_1 + \rho \sin \theta)d\theta$$

whenever the circle of integration lies in the upper half- plane. In particular, this equation holds if $0< \rho < y_{1}$ . Since $u(x_{1},y_{1})$ equals the maximum value $M$ , and $u(x_{1} + \rho \cos \theta ,y_{1} + \rho \sin \theta)\leq M$ , it follows by continuity that $u(x_{1} + \rho \cos \theta ,y_{1} + \rho \sin \theta) = M$ on the whole circle. For otherwise $u(x,y)\leq M - \epsilon$ , on an arc of length $\delta >0$ on the circle, and this would give

$$\frac{1}{2\pi}\int_0^{2\pi}u(x_1 + \rho \cos \theta ,y_1 + \rho \sin \theta)d\theta \leq M - \frac{\epsilon\delta}{2\pi} < M,$$

只要积分圆位于上半平面内。特别地，如果 $0< \rho < y_{1}$，这个方程成立。由于 $u(x_{1},y_{1})$ 等于最大值 $M$，且 $u(x_{1} + \rho \cos \theta ,y_{1} + \rho \sin \theta)\leq M$，由连续性可知，在整个圆上 $u(x_{1} + \rho \cos \theta ,y_{1} + \rho \sin \theta) = M$。否则，在圆上某个长度为 $\delta >0$ 的弧上 $u(x,y)\leq M - \epsilon$，这将导致

$$\frac{1}{2\pi}\int_0^{2\pi}u(x_1 + \rho \cos \theta ,y_1 + \rho \sin \theta)d\theta \leq M - \frac{\epsilon\delta}{2\pi} < M,$$

contradicting the fact that $u(x_{1},y_{1}) = M$ . Now letting $\rho \rightarrow y_{1}$ , and using the continuity of $u$ again, we see that this implies $u(x_{1},0) = M > 0$ which contradicts the fact that $u(x,0) = 0$ for all $x$ .

这与 $u(x_{1},y_{1}) = M$ 的事实矛盾。现在令 $\rho \rightarrow y_{1}$，并再次使用 $u$ 的连续性，我们看到这意味着 $u(x_{1},0) = M > 0$，这与对所有 $x$ 有 $u(x,0) = 0$ 的事实矛盾。

## 3 The Poisson summation formula

## 3 泊松求和公式

The definition of the Fourier transform was motivated by the desire for a continuous version of Fourier series, applicable to functions defined on the real line. We now show that there exists a further remarkable connection between the analysis of functions on the circle and related functions on $\mathbb{R}$ .

傅里叶变换的定义是由对傅里叶级数的连续版本的需求所驱动的，该版本适用于定义在实直线上的函数。现在我们展示，在圆上函数的分析与 $\mathbb{R}$ 上相关函数之间存在另一个非凡的联系。

Given a function $f\in \mathcal{S}(\mathbb{R})$ on the real line, we can construct a new function on the circle by the recipe

$$F_{1}(x) = \sum_{n = -\infty}^{\infty}f(x + n).$$

给定实直线上的函数 $f\in \mathcal{S}(\mathbb{R})$，我们可以通过以下方式在圆上构造一个新函数

$$F_{1}(x) = \sum_{n = -\infty}^{\infty}f(x + n).$$

Since $f$ is rapidly decreasing, the series converges absolutely and uniformly on every compact subset of $\mathbb{R}$ , so $F_{1}$ is continuous. Note that $F_{1}(x + 1) = F_{1}(x)$ because passage from $n$ to $n + 1$ in the above sum merely shifts the terms on the series defining $F_{1}(x)$ . Hence $F_{1}$ is periodic with period 1. The function $F_{1}$ is called the periodization of $f$ .

由于 $f$ 是快速递减的，该级数在 $\mathbb{R}$ 的每个紧子集上绝对且一致收敛，因此 $F_{1}$ 连续。注意 $F_{1}(x + 1) = F_{1}(x)$，因为上述求和中从 $n$ 到 $n + 1$ 只是移动了定义 $F_{1}(x)$ 的级数中的项。因此 $F_{1}$ 是周期为 1 的周期函数。函数 $F_{1}$ 称为 $f$ 的周期化。

There is another way to arrive at a "periodic version" of $f$ , this time by Fourier analysis. Start with the identity

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i\xi x}d\xi ,$$

还有另一种方法可以得到 $f$ 的“周期版本”，这次是通过傅里叶分析。从恒等式开始

$$f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi i\xi x}d\xi ,$$

===== Page 171 =====

and consider its discrete analogue, where the integral is replaced by a sum

$$F_{2}(x) = \sum_{n = -\infty}^{\infty}\hat{f} (n)e^{2\pi inx}.$$

并考虑其离散模拟，其中积分被求和取代

$$F_{2}(x) = \sum_{n = -\infty}^{\infty}\hat{f} (n)e^{2\pi inx}.$$

Once again, the sum converges absolutely and uniformly since $\hat{f}$ belongs to the Schwartz space, hence $F_{2}$ is continuous. Moreover, $F_{2}$ is also periodic of period 1 since this is the case for each one of the exponentials $e^{2\pi inx}$ .

同样，由于 $\hat{f}$ 属于施瓦茨空间，该求和绝对且一致收敛，因此 $F_{2}$ 连续。此外，$F_{2}$ 也是周期为 1 的周期函数，因为每个指数 $e^{2\pi inx}$ 都是如此。

The fundamental fact is that these two approaches, which produce $F_{1}$ and $F_{2}$ , actually lead to the same function.

基本事实是，这两种产生 $F_{1}$ 和 $F_{2}$ 的方法实际上导致相同的函数。

Theorem 3.1 (Poisson summation formula) If $f \in \mathcal{S}(\mathbb{R})$ , then

$$\sum_{n = -\infty}^{\infty}f(x + n) = \sum_{n = -\infty}^{\infty}\hat{f} (n)e^{2\pi inx}.$$

定理 3.1（泊松求和公式）若 $f \in \mathcal{S}(\mathbb{R})$，则

$$\sum_{n = -\infty}^{\infty}f(x + n) = \sum_{n = -\infty}^{\infty}\hat{f} (n)e^{2\pi inx}.$$

In particular, setting $x = 0$ we have

$$\sum_{n = -\infty}^{\infty}f(n) = \sum_{n = -\infty}^{\infty}\hat{f} (n).$$

特别地，令 $x = 0$ 得到

$$\sum_{n = -\infty}^{\infty}f(n) = \sum_{n = -\infty}^{\infty}\hat{f} (n).$$

In other words, the Fourier coefficients of the periodization of $f$ are given precisely by the values of the Fourier transform of $f$ on the integers.

换句话说，$f$ 的周期化的傅里叶系数恰好由 $f$ 的傅里叶变换在整数上的值给出。

Proof. To check the first formula it suffices, by Theorem 2.1 in Chapter 2, to show that both sides (which are continuous) have the same Fourier coefficients (viewed as functions on the circle). Clearly, the $m^{\mathrm{th}}$ Fourier coefficient of the right- hand side is $\hat{f} (m)$ . For the left- hand side we have

$$\int_{0}^{1}\left(\sum_{n = -\infty}^{\infty}f(x + n)\right)e^{-2\pi imx}dx = \sum_{n = -\infty}^{\infty}\int_{0}^{1}f(x + n)e^{-2\pi imx}dx$$ $$\qquad = \sum_{n = -\infty}^{\infty}\int_{n}^{n + 1}f(y)e^{-2\pi imy}dy$$ $$\qquad = \int_{-\infty}^{\infty}f(y)e^{-2\pi imy}dy$$ $$\qquad = \hat{f} (m),$$

证明。为了验证第一个公式，根据第 2 章定理 2.1，只需证明两边（都是连续的）具有相同的傅里叶系数（视为圆上的函数）。显然，右边的第 $m$ 个傅里叶系数是 $\hat{f} (m)$。对于左边，我们有

$$\int_{0}^{1}\left(\sum_{n = -\infty}^{\infty}f(x + n)\right)e^{-2\pi imx}dx = \sum_{n = -\infty}^{\infty}\int_{0}^{1}f(x + n)e^{-2\pi imx}dx$$ $$\qquad = \sum_{n = -\infty}^{\infty}\int_{n}^{n + 1}f(y)e^{-2\pi imy}dy$$ $$\qquad = \int_{-\infty}^{\infty}f(y)e^{-2\pi imy}dy$$ $$\qquad = \hat{f} (m),$$

where the interchange of the sum and integral is permissible since $f$ is rapidly decreasing. This completes the proof of the theorem.

其中求和与积分的交换是允许的，因为 $f$ 是快速递减的。这就完成了定理的证明。

===== Page 172 =====

We observe that the theorem extends to the case when we merely assume that both $f$ and $\hat{f}$ are of moderate decrease; the proof is in fact unchanged.

我们注意到，该定理可以推广到仅假设 $f$ 和 $\hat{f}$ 都是中度衰减的情形；证明实际上不变。

It turns out that the operation of periodization is important in a number of questions, even when the Poisson summation formula does not apply. We give an example by considering the elementary function $f(x) = 1/x, x \neq 0$. The result is that $\sum_{n=-\infty}^{\infty}1/(x + n)$, when summed symmetrically, gives the partial fraction decomposition of the cotangent function.

事实证明，即使泊松求和公式不适用，周期化运算在许多问题中也很重要。我们考虑初等函数 $f(x) = 1/x, x \neq 0$ 来给出一个例子。结果是，当对称求和时，$\sum_{n=-\infty}^{\infty}1/(x + n)$ 给出了余切函数的部分分式分解。

In fact this sum equals $\pi \cot \pi x$, when $x$ is not an integer. Similarly with $f(x) = 1/x^2$, we get $\sum_{n=-\infty}^{\infty}1/(x + n)^2 = \pi^2/(\sin \pi x)^2$, whenever $x \notin \mathbb{Z}$ (see Exercise 15).

事实上，当 $x$ 不是整数时，该和等于 $\pi \cot \pi x$。类似地，对于 $f(x) = 1/x^2$，当 $x \notin \mathbb{Z}$ 时，我们得到 $\sum_{n=-\infty}^{\infty}1/(x + n)^2 = \pi^2/(\sin \pi x)^2$（见习题 15）。

### 3.1 Theta and zeta functions

### 3.1 Theta 函数和 zeta 函数

We define the theta function $\vartheta(s)$ for $s > 0$ by

$$\vartheta(s) = \sum_{n = -\infty}^{\infty}e^{-\pi n^2 s}.$$

我们对 $s > 0$ 定义 theta 函数 $\vartheta(s)$ 为

$$\vartheta(s) = \sum_{n = -\infty}^{\infty}e^{-\pi n^2 s}.$$

The condition on $s$ ensures the absolute convergence of the series. A crucial fact about this special function is that it satisfies the following functional equation.

对 $s$ 的条件保证了级数的绝对收敛。这个特殊函数的一个关键事实是它满足以下函数方程。

Theorem 3.2 $s^{-1/2}\vartheta(1/s) = \vartheta(s)$ whenever $s > 0$.

定理 3.2 当 $s > 0$ 时，$s^{-1/2}\vartheta(1/s) = \vartheta(s)$。

The proof of this identity consists of a simple application of the Poisson summation formula to the pair

$$f(x) = e^{-\pi s x^2}$$

and

$$\hat{f}(\xi) = s^{-1/2}e^{-\pi \xi^2 / s}.$$

这个恒等式的证明是泊松求和公式对以下函数对的简单应用

$$f(x) = e^{-\pi s x^2}$$

和

$$\hat{f}(\xi) = s^{-1/2}e^{-\pi \xi^2 / s}.$$

The theta function $\vartheta(s)$ also extends to complex values of $s$ when $\operatorname{Re}(s) > 0$, and the functional equation is still valid then.

当 $\operatorname{Re}(s) > 0$ 时，theta 函数 $\vartheta(s)$ 也可以推广到复数 $s$，此时函数方程仍然成立。

The theta function is intimately connected with an important function in number theory, the zeta function $\zeta(s)$ defined for $\operatorname{Re}(s) > 1$ by

$$\zeta(s) = \sum_{n = 1}^{\infty}\frac{1}{n^s}.$$

theta 函数与数论中的一个重要函数——zeta 函数 $\zeta(s)$ 密切相关，后者对 $\operatorname{Re}(s) > 1$ 定义为

$$\zeta(s) = \sum_{n = 1}^{\infty}\frac{1}{n^s}.$$

Later we will see that this function carries essential information about the prime numbers (see Chapter 8).

稍后我们将看到，这个函数承载着关于素数的重要信息（见第 8 章）。

It also turns out that $\zeta$, $\vartheta$, and another important function $\Gamma$ are related by the following identity:

$$\pi^{-s/2}\Gamma(s/2)\zeta(s) = \frac{1}{2}\int_0^{\infty} t^{s/2-1}(\vartheta(t) - 1) dt,$$

此外，$\zeta$、$\vartheta$ 和另一个重要函数 $\Gamma$ 通过以下恒等式相关联：

$$\pi^{-s/2}\Gamma(s/2)\zeta(s) = \frac{1}{2}\int_0^{\infty} t^{s/2-1}(\vartheta(t) - 1) dt,$$

===== Page 173 =====

which is valid for $s > 1$ (Exercises 17 and 18). Returning to the function $\theta$ , define the generalization $\Theta(z|\tau)$ given by

$$\Theta(z|\tau) = \sum_{n = -\infty}^{\infty}e^{i\pi n^2\tau}e^{2\pi inz}$$

这对 $s > 1$ 成立（习题 17 和 18）。回到函数 $\theta$，定义推广 $\Theta(z|\tau)$ 为

$$\Theta(z|\tau) = \sum_{n = -\infty}^{\infty}e^{i\pi n^2\tau}e^{2\pi inz}$$

whenever $\operatorname{Im}(\tau) > 0$ and $z\in \mathbb{C}$ . Taking $z = 0$ and $\tau = is$ we get $\Theta(z|\tau) =$ $\theta(s)$

只要 $\operatorname{Im}(\tau) > 0$ 且 $z\in \mathbb{C}$。取 $z = 0$ 和 $\tau = is$ 得到 $\Theta(z|\tau) = \theta(s)$。

### 3.2 Heat kernels

### 3.2 热核

Another application related to the Poisson summation formula and the theta function is the time- dependent heat equation on the circle. A solution to the equation

$$\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2}$$

另一个与泊松求和公式和 theta 函数相关的应用是圆上的时间相关热方程。方程

$$\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2}$$

subject to $u(x,0) = f(x)$ , where $f$ is periodic of period 1, was given in the previous chapter by

$$u(x,t) = (f*H_t)(x)$$

的解，满足 $u(x,0) = f(x)$，其中 $f$ 是周期为 1 的周期函数，在上一章中由下式给出

$$u(x,t) = (f*H_t)(x)$$

where $H_{t}(x)$ is the heat kernel on the circle, that is,

$$H_{t}(x) = \sum_{n = -\infty}^{\infty}e^{-4\pi^{2}n^{2}t}e^{2\pi inx}.$$

其中 $H_{t}(x)$ 是圆上的热核，即

$$H_{t}(x) = \sum_{n = -\infty}^{\infty}e^{-4\pi^{2}n^{2}t}e^{2\pi inx}.$$

Note in particular that with our definition of the generalized theta function in the previous section, we have $\Theta(x|4\pi it) = H_t(x)$ . Also, recall that the heat equation on $\mathbb{R}$ gave rise to the heat kernel

$$\mathcal{H}_t(x) = \frac{1}{(4\pi t)^{1 / 2}} e^{-x^2 /4t}$$

特别地，根据上一节中广义 theta 函数的定义，我们有 $\Theta(x|4\pi it) = H_t(x)$。此外，回忆 $\mathbb{R}$ 上的热方程产生了热核

$$\mathcal{H}_t(x) = \frac{1}{(4\pi t)^{1 / 2}} e^{-x^2 /4t}$$

where $\hat{\mathcal{H}}_t(\xi) = e^{- 4\pi^2 \xi^2 t}$ . The fundamental relation between these two objects is an immediate consequence of the Poisson summation formula:

其中 $\hat{\mathcal{H}}_t(\xi) = e^{- 4\pi^2 \xi^2 t}$。这两个对象之间的基本关系是泊松求和公式的直接推论：

Theorem 3.3 The heat kernel on the circle is the periodization of the heat kernel on the real line:

$$H_{t}(x) = \sum_{n = -\infty}^{\infty}\mathcal{H}_{t}(x + n).$$

定理 3.3 圆上的热核是实直线上热核的周期化：

$$H_{t}(x) = \sum_{n = -\infty}^{\infty}\mathcal{H}_{t}(x + n).$$

===== Page 174 =====

Although the proof that $\mathcal{H}_t$ is a good kernel on $\mathbb{R}$ was fairly straightforward, we left open the harder problem that $H_{t}$ is a good kernel on the circle. The above results allow us to resolve this matter.

尽管证明 $\mathcal{H}_t$ 是 $\mathbb{R}$ 上的好核相当直接，但我们留下了更困难的问题：$H_{t}$ 是圆上的好核。上述结果使我们能够解决这个问题。

Corollary 3.4 The kernel $H_{t}(x)$ is a good kernel for $t \to 0$ .

推论 3.4 核 $H_{t}(x)$ 当 $t \to 0$ 时是好核。

Proof. We already observed that $\int_{|x| \leq 1 / 2} H_{t}(x) dx = 1$ . Now note that $H_{t} \geq 0$ , which is immediate from the above formula since $\mathcal{H}_{t} \geq 0$ . Finally, we claim that when $|x| \leq 1 / 2$ ,

$$H_{t}(x) = \mathcal{H}_{t}(x) + \mathcal{E}_{t}(x),$$

证明。我们已经观察到 $\int_{|x| \leq 1 / 2} H_{t}(x) dx = 1$。现在注意 $H_{t} \geq 0$，这从上述公式立即可得，因为 $\mathcal{H}_{t} \geq 0$。最后，我们断言当 $|x| \leq 1 / 2$ 时，

$$H_{t}(x) = \mathcal{H}_{t}(x) + \mathcal{E}_{t}(x),$$

where the error satisfies $|\mathcal{E}_{t}(x)| \leq c_{1} e^{- c_{2} / t}$ with $c_{1}, c_{2} > 0$ and $0 < t \leq 1$ . To see this, note again that the formula in the theorem gives

$$H_{t}(x) = \mathcal{H}_{t}(x) + \sum_{|n| \geq 1} \mathcal{H}_{t}(x + n);$$

其中误差满足 $|\mathcal{E}_{t}(x)| \leq c_{1} e^{- c_{2} / t}$，其中 $c_{1}, c_{2} > 0$ 且 $0 < t \leq 1$。要看到这一点，再次注意定理中的公式给出

$$H_{t}(x) = \mathcal{H}_{t}(x) + \sum_{|n| \geq 1} \mathcal{H}_{t}(x + n);$$

therefore, since $|x| \leq 1 / 2$

$$\mathcal{E}_{t}(x) = \frac{1}{\sqrt{4\pi t}} \sum_{|n| \geq 1} e^{-(x + n)^{2} / 4t} \leq C t^{-1 / 2} \sum_{n \geq 1} e^{-c n^{2} / t}.$$

因此，由于 $|x| \leq 1 / 2$

$$\mathcal{E}_{t}(x) = \frac{1}{\sqrt{4\pi t}} \sum_{|n| \geq 1} e^{-(x + n)^{2} / 4t} \leq C t^{-1 / 2} \sum_{n \geq 1} e^{-c n^{2} / t}.$$

Note that $n^{2} / t \geq n^{2}$ and $n^{2} / t \geq 1 / t$ whenever $0 < t \leq 1$ , so $e^{- c n^{2} / t} \leq e^{- \frac{c}{2} n^{2}} e^{- \frac{c}{2} t}$ . Hence

$$|\mathcal{E}_{t}(x)| \leq C t^{-1 / 2} e^{-\frac{c}{2} t} \sum_{n \geq 1} e^{-\frac{c}{2} n^{2}} \leq c_{1} e^{-c_{2} / t}.$$

注意，只要 $0 < t \leq 1$，就有 $n^{2} / t \geq n^{2}$ 和 $n^{2} / t \geq 1 / t$，因此 $e^{- c n^{2} / t} \leq e^{- \frac{c}{2} n^{2}} e^{- \frac{c}{2} t}$。于是

$$|\mathcal{E}_{t}(x)| \leq C t^{-1 / 2} e^{-\frac{c}{2} t} \sum_{n \geq 1} e^{-\frac{c}{2} n^{2}} \leq c_{1} e^{-c_{2} / t}.$$

The proof of the claim is complete, and as a result $\int_{|x| \leq 1 / 2} |\mathcal{E}_{t}(x)| dx \to 0$ as $t \to 0$ . It is now clear that $H_{t}$ satisfies

$$\int_{\eta < |x| \leq 1 / 2} |H_{t}(x)| dx \to 0 \quad \text{as} \quad t \to 0,$$

断言的证明完成，因此当 $t \to 0$ 时 $\int_{|x| \leq 1 / 2} |\mathcal{E}_{t}(x)| dx \to 0$。现在显然 $H_{t}$ 满足

$$\int_{\eta < |x| \leq 1 / 2} |H_{t}(x)| dx \to 0 \quad \text{as} \quad t \to 0,$$

because $\mathcal{H}_{t}$ does.

因为 $\mathcal{H}_{t}$ 满足。

### 3.3 Poisson kernels

### 3.3 泊松核

In a similar manner to the discussion above about the heat kernels, we state the relation between the Poisson kernels for the disc and the upper half- plane where

$$P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r \cos \theta + r^{2}} \quad \text{and} \quad \mathcal{P}_{y}(x) = \frac{1}{\pi} \frac{y}{y^{2} + x^{2}}.$$

与上述关于热核的讨论类似，我们陈述圆盘和上半平面的泊松核之间的关系，其中

$$P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r \cos \theta + r^{2}} \quad \text{and} \quad \mathcal{P}_{y}(x) = \frac{1}{\pi} \frac{y}{y^{2} + x^{2}}.$$

===== Page 175 =====

$$\mathrm{Theorem~3.5~}P_{r}(2\pi x) = \sum_{n\in \mathbb{Z}}\mathcal{P}_{y}(x + n)\mathrm{~where~}r = e^{-2\pi y}.$$

$$\mathrm{定理~3.5~}P_{r}(2\pi x) = \sum_{n\in \mathbb{Z}}\mathcal{P}_{y}(x + n)\mathrm{~其中~}r = e^{-2\pi y}.$$

This is again an immediate corollary of the Poisson summation formula applied to $f(x) = \mathcal{P}_y(x)$ and $\hat{f} (\xi) = e^{- 2\pi |\xi |y}$ . Of course, here we use the Poisson summation formula under the assumptions that $f$ and $\hat{f}$ are of moderate decrease.

这再次是泊松求和公式应用于 $f(x) = \mathcal{P}_y(x)$ 和 $\hat{f} (\xi) = e^{- 2\pi |\xi |y}$ 的直接推论。当然，这里我们在假设 $f$ 和 $\hat{f}$ 中度衰减的情况下使用泊松求和公式。

## 4 The Heisenberg uncertainty principle

## 4 海森堡不确定性原理

The mathematical thrust of the principle can be formulated in terms of a relation between a function and its Fourier transform. The basic underlying law, formulated in its vaguest and most general form, states that a function and its Fourier transform cannot both be essentially localized. Somewhat more precisely, if the "preponderance" of the mass of a function is concentrated in an interval of length $L$ , then the preponderance of the mass of its Fourier transform cannot lie in an interval of length essentially smaller than $L^{- 1}$ . The exact statement is as follows.

该原理的数学要点可以用函数与其傅里叶变换之间的关系来表述。基本定律，以其最模糊和最一般的形式表述，指出一个函数及其傅里叶变换不能同时本质上是局部的。更精确地说，如果一个函数的“质量主体”集中在一个长度为 $L$ 的区间内，那么其傅里叶变换的质量主体就不能位于一个长度本质上小于 $L^{- 1}$ 的区间内。精确陈述如下。

Theorem 4.1 Suppose $\psi$ is a function in $\mathcal{S}(\mathbb{R})$ which satisfies the normalizing condition $\int_{-\infty}^{\infty}|\psi (x)|^{2}dx = 1$ . Then

$$\left(\int_{-\infty}^{\infty}x^{2}|\psi (x)|^{2}dx\right)\left(\int_{-\infty}^{\infty}\xi^{2}|\hat{\psi} (\xi)|^{2}d\xi\right)\geq \frac{1}{16\pi^{2}},$$

定理 4.1 假设 $\psi$ 是 $\mathcal{S}(\mathbb{R})$ 中的函数，满足归一化条件 $\int_{-\infty}^{\infty}|\psi (x)|^{2}dx = 1$。则

$$\left(\int_{-\infty}^{\infty}x^{2}|\psi (x)|^{2}dx\right)\left(\int_{-\infty}^{\infty}\xi^{2}|\hat{\psi} (\xi)|^{2}d\xi\right)\geq \frac{1}{16\pi^{2}},$$

and equality holds if and only if $\psi (x) = Ae^{- Bx^{2}}$ where $B > 0$ and $|A|^{2} = \sqrt{2B / \pi}$ .

等号成立当且仅当 $\psi (x) = Ae^{- Bx^{2}}$，其中 $B > 0$ 且 $|A|^{2} = \sqrt{2B / \pi}$。

In fact, we have

$$\left(\int_{-\infty}^{\infty}(x - x_{0})^{2}|\psi (x)|^{2}dx\right)\left(\int_{-\infty}^{\infty}(\xi -\xi_{0})^{2}|\hat{\psi} (\xi)|^{2}d\xi\right)\geq \frac{1}{16\pi^{2}}$$

for every $x_0, \xi_0 \in \mathbb{R}$ .

实际上，对每个 $x_0, \xi_0 \in \mathbb{R}$，有

$$\left(\int_{-\infty}^{\infty}(x - x_{0})^{2}|\psi (x)|^{2}dx\right)\left(\int_{-\infty}^{\infty}(\xi -\xi_{0})^{2}|\hat{\psi} (\xi)|^{2}d\xi\right)\geq \frac{1}{16\pi^{2}}.$$

Proof. The second inequality actually follows from the first by replacing $\psi (x)$ by $e^{- 2\pi ix\xi_0}\psi (x + x_0)$ and changing variables. To prove the first inequality, we argue as follows. Beginning with our normalizing assumption $\int |\psi |^2 = 1$ , and recalling that $\psi$ and $\psi '$ are rapidly decreasing, an integration by parts gives

$$1 = \int_{-\infty}^{\infty}|\psi (x)|^{2}dx$$ $$= -\int_{-\infty}^{\infty}x\frac{d}{dx} |\psi (x)|^{2}dx$$ $$= -\int_{-\infty}^{\infty}\left(x\psi '(x)\overline{\psi (x)} +x\overline{\psi '(x)}\psi (x)\right)dx.$$

证明。第二个不等式实际上可以通过将 $\psi (x)$ 替换为 $e^{- 2\pi ix\xi_0}\psi (x + x_0)$ 并变换变量从第一个不等式推出。为了证明第一个不等式，我们论证如下。从归一化假设 $\int |\psi |^2 = 1$ 开始，并回忆 $\psi$ 和 $\psi '$ 是快速递减的，分部积分给出

$$1 = \int_{-\infty}^{\infty}|\psi (x)|^{2}dx$$ $$= -\int_{-\infty}^{\infty}x\frac{d}{dx} |\psi (x)|^{2}dx$$ $$= -\int_{-\infty}^{\infty}\left(x\psi '(x)\overline{\psi (x)} +x\overline{\psi '(x)}\psi (x)\right)dx.$$

===== Page 176 =====

The last identity follows because $|\psi |^2 = \psi \bar{\psi}$ . Therefore

$$1\leq 2\int_{-\infty}^{\infty}|x||\psi (x)||\psi '(x)|dx$$ $$\leq 2\left(\int_{-\infty}^{\infty}x^2 |\psi (x)|^2 dx\right)^{1 / 2}\left(\int_{-\infty}^{\infty}|\psi '(x)|^2 dx\right)^{1 / 2},$$

最后一个恒等式成立是因为 $|\psi |^2 = \psi \bar{\psi}$。因此

$$1\leq 2\int_{-\infty}^{\infty}|x||\psi (x)||\psi '(x)|dx$$ $$\leq 2\left(\int_{-\infty}^{\infty}x^2 |\psi (x)|^2 dx\right)^{1 / 2}\left(\int_{-\infty}^{\infty}|\psi '(x)|^2 dx\right)^{1 / 2},$$

where we have used the Cauchy- Schwarz inequality. The identity

$$\int_{-\infty}^{\infty}|\psi '(x)|^2 dx = 4\pi^2\int_{-\infty}^{\infty}\xi^2 |\hat{\psi} (\xi)|^2 d\xi ,$$

其中我们使用了柯西-施瓦茨不等式。恒等式

$$\int_{-\infty}^{\infty}|\psi '(x)|^2 dx = 4\pi^2\int_{-\infty}^{\infty}\xi^2 |\hat{\psi} (\xi)|^2 d\xi ,$$

which holds because of the properties of the Fourier transform and the Plancherel formula, concludes the proof of the inequality in the theorem.

由于傅里叶变换的性质和普朗歇尔公式而成立，从而完成了定理中不等式的证明。

If equality holds, then we must also have equality where we applied the Cauchy- Schwarz inequality, and as a result we find that $\psi '(x) = \beta x\psi (x)$ for some constant $\beta$ . The solutions to this equation are $\psi (x) = Ae^{\beta x^2 /2}$ , where $A$ is constant. Since we want $\psi$ to be a Schwartz function, we must take $\beta = - 2B < 0$ , and since we impose the condition $\int_{-\infty}^{\infty}|\psi (x)|^2 dx = 1$ we find that $|A|^2 = \sqrt{2B / \pi}$ , as was to be shown.

如果等号成立，那么我们在应用柯西-施瓦茨不等式的地方也必须取等号，结果我们发现存在常数 $\beta$ 使得 $\psi '(x) = \beta x\psi (x)$。该方程的解为 $\psi (x) = Ae^{\beta x^2 /2}$，其中 $A$ 是常数。因为我们希望 $\psi$ 是施瓦茨函数，必须取 $\beta = - 2B < 0$，并且由于我们施加了条件 $\int_{-\infty}^{\infty}|\psi (x)|^2 dx = 1$，我们发现 $|A|^2 = \sqrt{2B / \pi}$，如所述。

The precise assertion contained in Theorem 4.1 first came to light in the study of quantum mechanics. It arose when one considered the extent to which one could simultaneously locate the position and momentum of a particle. Assuming we are dealing with (say) an electron that travels along the real line, then according to the laws of physics, matters are governed by a "state function" $\psi$ , which we can assume to be in $\mathcal{S}(\mathbb{R})$ , and which is normalized according to the requirement that

$$\int_{-\infty}^{\infty}|\psi (x)|^2 dx = 1.$$

定理 4.1 中的精确断言最初出现在量子力学研究中。它出现在考虑一个粒子的位置和动量能够同时被定位到什么程度的时候。假设我们正在处理（例如）一个沿实直线运动的电子，那么根据物理定律，事情由一个“态函数” $\psi$ 支配，我们可以假设 $\psi \in \mathcal{S}(\mathbb{R})$，并且它根据以下要求归一化：

$$\int_{-\infty}^{\infty}|\psi (x)|^2 dx = 1.$$

The position of the particle is then determined not as a definite point $x$ ; instead its probable location is given by the rules of quantum mechanics as follows:

粒子的位置不是被确定为一个确定的点 $x$；相反，它的可能位置由量子力学的规则给出如下：

The probability that the particle is located in the interval $(a,b)$ is $\int_{a}^{b}|\psi (x)|^{2}dx$ .

粒子位于区间 $(a,b)$ 中的概率是 $\int_{a}^{b}|\psi (x)|^{2}dx$。

According to this law we can calculate the probable location of the particle with the aid of $\psi$ : in fact, there may be only a small probability that the particle is located in a given interval $(a',b')$ , but nevertheless it is somewhere on the real line since $\int_{-\infty}^{\infty}|\psi (x)|^2 dx = 1$ .

根据这个定律，我们可以借助 $\psi$ 计算粒子的可能位置：事实上，粒子位于给定区间 $(a',b')$ 的概率可能很小，但无论如何它位于实直线上的某处，因为 $\int_{-\infty}^{\infty}|\psi (x)|^2 dx = 1$。

===== Page 177 =====

In addition to the probability density $|\psi (x)|^2 dx$ , there is the expectation of where the particle might be. This expectation is the best guess of the position of the particle, given its probability distribution determined by $|\psi (x)|^2 dx$ , and is the quantity defined by

$$\overline{x} = \int_{-\infty}^{\infty}x|\psi (x)|^2 dx. \quad (12)$$

除了概率密度 $|\psi (x)|^2 dx$ 之外，还有粒子可能在哪里的期望。这个期望是在给定由 $|\psi (x)|^2 dx$ 确定的概率分布下对粒子位置的最佳猜测，它是由下式定义的量

$$\overline{x} = \int_{-\infty}^{\infty}x|\psi (x)|^2 dx. \quad (12)$$

Why is this our best guess? Consider the simpler (idealized) situation where we are given that the particle can be found at only finitely many different points, $x_{1},x_{2},\ldots ,x_{N}$ on the real axis, with $p_i$ the probability that the particle is at $x_{i}$ , and $p_1 + p_2 + \dots +p_N = 1$ . Then, if we knew nothing else, and were forced to make one choice as to the position of the particle, we would naturally take $\overline{x} = \sum_{i = 1}^{N}x_{i}p_{i}$ , which is the appropriate weighted average of the possible positions. The quantity (12) is clearly the general (integral) version of this.

为什么这是我们的最佳猜测？考虑更简单（理想化）的情况：已知粒子只能出现在实轴上的有限多个不同点 $x_{1},x_{2},\ldots ,x_{N}$ 处，$p_i$ 是粒子在 $x_i$ 处的概率，且 $p_1 + p_2 + \dots +p_N = 1$。那么，如果我们一无所知，并且被迫对粒子的位置做出一个选择，我们自然会取 $\overline{x} = \sum_{i = 1}^{N}x_{i}p_{i}$，这是可能位置的适当加权平均。量 (12) 显然是这个的通用（积分）版本。

We next come to the notion of variance, which in our terminology is the uncertainty attached to our expectation. Having determined that the expected position of the particle is $\overline{x}$ (given by (12)), the resulting uncertainty is the quantity

$$\int_{-\infty}^{\infty}(x - \overline{x})^2 |\psi (x)|^2 dx. \quad (13)$$

接下来我们讨论方差的概念，用我们的术语来说，就是与期望相关的不确定性。在确定粒子的期望位置为 $\overline{x}$（由 (12) 给出）之后，由此产生的不确定性是量

$$\int_{-\infty}^{\infty}(x - \overline{x})^2 |\psi (x)|^2 dx. \quad (13)$$

Notice that if $\psi$ is highly concentrated near $\overline{x}$ , it means that there is a high probability that $x$ is near $\overline{x}$ , and so (13) is small, because most of the contribution to the integral takes place for values of $x$ near $\overline{x}$ . Here we have a small uncertainty. On the other hand, if $\psi (x)$ is rather flat (that is, the probability distribution $|\psi (x)|^2 dx$ is not very concentrated), then the integral (13) is rather big, because large values of $(x - \overline{x})^2$ will come into play, and as a result the uncertainty is relatively large.

注意，如果 $\psi$ 高度集中在 $\overline{x}$ 附近，这意味着 $x$ 接近 $\overline{x}$ 的概率很高，因此 (13) 很小，因为积分的主要贡献来自 $x$ 接近 $\overline{x}$ 的值。这里我们有一个小的不确定性。另一方面，如果 $\psi (x)$ 相当平坦（即概率分布 $|\psi (x)|^2 dx$ 不是很集中），那么积分 (13) 相当大，因为 $(x - \overline{x})^2$ 的大值会起作用，结果不确定性相对较大。

It is also worthwhile to observe that the expectation $\overline{x}$ is that choice for which the uncertainty $\int_{-\infty}^{\infty}(x - \overline{x})^2 |\psi (x)|^2 dx$ is the smallest. Indeed, if we try to minimize this quantity by equating to 0 its derivative with respect to $\overline{x}$ , we find that $2\int_{-\infty}^{\infty}(x - \overline{x})|\psi (x)|^2 dx = 0$ , which gives (12).

还值得注意，期望 $\overline{x}$ 是使得不确定性 $\int_{-\infty}^{\infty}(x - \overline{x})^2 |\psi (x)|^2 dx$ 最小的选择。实际上，如果我们试图通过将其关于 $\overline{x}$ 的导数设为 0 来最小化这个量，我们得到 $2\int_{-\infty}^{\infty}(x - \overline{x})|\psi (x)|^2 dx = 0$，这给出 (12)。

So far, we have discussed the "expectation" and "uncertainty" related to the position of the particle. Of equal relevance are the corresponding notions regarding its momentum. The corresponding rule of quantum mechanics is:

到目前为止，我们已经讨论了与粒子位置相关的“期望”和“不确定性”。同样相关的是关于其动量的相应概念。量子力学的相应规则是：

The probability that the momentum $\xi$ of the particle belongs to the interval $(a,b)$ is $\int_{a}^{b}|\hat{\psi} (\xi)|^{2} d\xi$ where $\hat{\psi}$ is the Fourier transform of $\psi$ .

粒子的动量 $\xi$ 属于区间 $(a,b)$ 的概率是 $\int_{a}^{b}|\hat{\psi} (\xi)|^{2} d\xi$，其中 $\hat{\psi}$ 是 $\psi$ 的傅里叶变换。

===== Page 178 =====

Combining these two laws with Theorem 4.1 gives $1 / 16\pi^2$ as the lower bound for the product of the uncertainty of the position and the uncertainty of the momentum of a particle. So the more certain we are about the location of the particle, the less certain we can be about its momentum, and vice versa. However, we have simplified the statement of the two laws by rescaling to change the units of measurement. Actually, there enters a fundamental but small physical number $\hbar$ called Planck's constant. When properly taken into account, the physical conclusion is

(uncertainty of position) $\times$ (uncertainty of momentum) $\geq \hbar /16\pi^2$ .

将这两个定律与定理 4.1 结合起来，得到 $1 / 16\pi^2$ 作为粒子位置不确定性与动量不确定性乘积的下界。因此，我们对粒子的位置越确定，对其动量就越不确定，反之亦然。然而，我们通过重新缩放改变测量单位简化了两个定律的表述。实际上，这里引入了一个基本但很小的物理常数 $\hbar$，称为普朗克常数。适当考虑后，物理结论是

（位置不确定性）$\times$（动量不确定性）$\geq \hbar /16\pi^2$。

---
# 海森堡不确定性原理：从傅里叶分析到量子力学  
## —— 一份数学详尽的讲义  

本讲义基于 Elias M. Stein 所著《傅里叶分析导论》（Fourier Analysis: An Introduction）第 4 章的内容，完整补全了定理 4.1 的证明过程中省略的细节，并系统阐述了其物理意义。我/们将从函数与其傅里叶变换的局域性矛盾出发，推导出量子力学中最核心的不确定性关系。

---

## 1. 直观背景：函数与傅里叶变换不能同时局部化  

在信号处理中，一个时域信号若高度集中在某段时间内，其频谱必定展宽；反之，纯单频信号（频谱集中在单一频率）必定在时域无限延伸。这种“时宽–带宽积”的下界正是海森堡不确定性原理的数学本质。  

对于复值函数 $\psi(x)$，其傅里叶变换定义为  
$$
\hat{\psi}(\xi)=\int_{-\infty}^{\infty}\psi(x)e^{-2\pi i x\xi}\,dx .
$$  
若 $|\psi(x)|^2$ 的“质量主体”集中在长度为 $L$ 的区间内，则 $|\hat{\psi}(\xi)|^2$ 的质量主体不可能集中在长度远小于 $L^{-1}$ 的区间内。下面用精确的方差形式给出定量描述。

---

## 2. 预备知识  

- **Schwartz 空间 $\mathcal{S}(\mathbb{R})$**：所有无穷可导且自身及其各阶导数均快速衰减（衰减速度超过任意幂次）的函数。在该空间上傅里叶变换是双射，且满足 Plancherel 定理。  
- **归一化条件**：  
  $$
  \int_{-\infty}^{\infty}|\psi(x)|^2\,dx = 1 .
  $$  
  此时 $|\psi(x)|^2dx$ 可解释为概率密度。  
- **傅里叶变换的基本性质**：  
  $$
  \widehat{\psi'}(\xi)=2\pi i\xi\,\hat{\psi}(\xi),\qquad
  \int_{-\infty}^{\infty}|\psi'(x)|^2dx = 4\pi^2\int_{-\infty}^{\infty}\xi^2|\hat{\psi}(\xi)|^2d\xi .
  $$  
  第二式即 Plancherel 定理（或帕塞瓦尔恒等式）的直接推论。  
- **柯西–施瓦茨不等式**：  
  $$
  \left|\int f\bar{g}\right| \le \left(\int|f|^2\right)^{1/2}\left(\int|g|^2\right)^{1/2}.
  $$

---

## 3. 定理的精确陈述  

**定理 4.1**  
设 $\psi\in\mathcal{S}(\mathbb{R})$ 满足 $\int_{-\infty}^{\infty}|\psi(x)|^2dx=1$。则  
$$
\left(\int_{-\infty}^{\infty}x^2|\psi(x)|^2dx\right)\left(\int_{-\infty}^{\infty}\xi^2|\hat{\psi}(\xi)|^2d\xi\right)\ge\frac{1}{16\pi^2},
\tag{1}
$$  
且等号成立当且仅当 $\psi(x)=Ae^{-Bx^2}$（$B>0$），其中 $|A|^2=\sqrt{2B/\pi}$。  

更一般地，对任意实数 $x_0,\xi_0$ 有  
$$
\left(\int_{-\infty}^{\infty}(x-x_0)^2|\psi(x)|^2dx\right)\left(\int_{-\infty}^{\infty}(\xi-\xi_0)^2|\hat{\psi}(\xi)|^2d\xi\right)\ge\frac{1}{16\pi^2}.
\tag{2}
$$

---

## 4. 证明 (1) 的完整推导  

### 4.1 从归一化条件出发，利用分部积分  

首先注意到  
$$
1 = \int_{-\infty}^{\infty}|\psi(x)|^2dx = \int_{-\infty}^{\infty}\psi(x)\overline{\psi(x)}\,dx .
$$  
对 $\frac{d}{dx}\bigl(x|\psi(x)|^2\bigr)$ 进行分部积分。因为 $\psi$ 快速衰减，边界项为零：  
$$
0 = \int_{-\infty}^{\infty}\frac{d}{dx}\bigl(x|\psi(x)|^2\bigr)dx
   = \int_{-\infty}^{\infty}|\psi(x)|^2dx + \int_{-\infty}^{\infty}x\frac{d}{dx}|\psi(x)|^2dx .
$$  
从而  
$$
1 = -\int_{-\infty}^{\infty}x\frac{d}{dx}|\psi(x)|^2dx .
\tag{3}
$$  

接下来计算导数：  
$$
\frac{d}{dx}|\psi(x)|^2 = \frac{d}{dx}\bigl(\psi(x)\overline{\psi(x)}\bigr)
= \psi'(x)\overline{\psi(x)} + \psi(x)\overline{\psi'(x)} .
$$  
代入 (3)：  
$$
1 = -\int_{-\infty}^{\infty}x\Bigl(\psi'(x)\overline{\psi(x)} + \psi(x)\overline{\psi'(x)}\Bigr)dx .
$$  
将两项分开：  
$$
1 = -\int_{-\infty}^{\infty}x\psi'(x)\overline{\psi(x)}\,dx \;-\; \int_{-\infty}^{\infty}x\psi(x)\overline{\psi'(x)}\,dx .
\tag{4}
$$  

### 4.2 利用共轭对称性简化  

注意第二项是第一个积分的复共轭（因为 $\overline{x\psi'(x)\overline{\psi(x)}} = x\psi(x)\overline{\psi'(x)}$，而 $x$ 为实数）。设  
$$
I = \int_{-\infty}^{\infty}x\psi'(x)\overline{\psi(x)}\,dx ,
$$  
则第二项即为 $\overline{I}$。于是 (4) 成为  
$$
1 = -I - \overline{I} = -2\,\operatorname{Re}(I).
$$  
因此  
$$
\operatorname{Re}(I) = -\frac12 .
\tag{5}
$$  

### 4.3 用绝对值放大得到不等式  

由绝对值不等式，  
$$
|I| \ge |\operatorname{Re}(I)| = \frac12 .
$$  
另一方面，  
$$
|I| \le \int_{-\infty}^{\infty}|x||\psi'(x)||\psi(x)|\,dx .
$$  
因此  
$$
\frac12 \le \int_{-\infty}^{\infty}|x||\psi'(x)||\psi(x)|\,dx .
\tag{6}
$$  

### 4.4 应用柯西–施瓦茨不等式  

将被积函数写成 $(|x||\psi(x)|)\cdot|\psi'(x)|$，由柯西–施瓦茨不等式：  
$$
\int_{-\infty}^{\infty}|x||\psi'(x)||\psi(x)|\,dx
\le \left(\int_{-\infty}^{\infty}x^2|\psi(x)|^2dx\right)^{1/2}
   \left(\int_{-\infty}^{\infty}|\psi'(x)|^2dx\right)^{1/2}.
$$  
结合 (6) 得到  
$$
\frac12 \le \left(\int x^2|\psi|^2\right)^{1/2}
           \left(\int |\psi'|^2\right)^{1/2}.
\tag{7}
$$  

### 4.5 将 $\int|\psi'|^2$ 用 $\hat{\psi}$ 表示  

由傅里叶变换的性质：$\widehat{\psi'}(\xi)=2\pi i\xi\,\hat{\psi}(\xi)$。根据 Plancherel 定理，  
$$
\int_{-\infty}^{\infty}|\psi'(x)|^2dx = \int_{-\infty}^{\infty}|\widehat{\psi'}(\xi)|^2d\xi
= \int_{-\infty}^{\infty}|2\pi i\xi\,\hat{\psi}(\xi)|^2d\xi
= 4\pi^2\int_{-\infty}^{\infty}\xi^2|\hat{\psi}(\xi)|^2d\xi .
\tag{8}
$$  

将 (8) 代入 (7)：  
$$
\frac12 \le \left(\int x^2|\psi|^2\right)^{1/2}
           \left(4\pi^2\int\xi^2|\hat{\psi}|^2\right)^{1/2}
= 2\pi \left(\int x^2|\psi|^2\right)^{1/2}
        \left(\int\xi^2|\hat{\psi}|^2\right)^{1/2}.
$$  
两边除以 $2\pi$ 并平方，即得  
$$
\left(\int x^2|\psi|^2\right)\left(\int\xi^2|\hat{\psi}|^2\right)
\ge \frac{1}{16\pi^2}.
$$  
这就完成了不等式 (1) 的证明。

---

## 5. 等号成立条件的详细分析  

若 (1) 取等号，则推导过程中的两个不等式必须同时取等号：  

1. **柯西–施瓦茨不等式取等号**：存在常数 $\lambda$ 使得  
   $$
   |\psi'(x)| = \lambda\,|x||\psi(x)|\quad\text{几乎处处}.
   \tag{9}
   $$  
   并且，在应用 $|I|\ge|\operatorname{Re} I|$ 时也需取等号，这意味着 $I$ 为负实数（因为 $\operatorname{Re}I=-1/2$，且 $|I|=1/2$ 迫使 $I$ 为实数且为负）。回忆 $I=\int x\psi'\bar\psi\,dx$。由 (9) 和相位条件可以证明 $\psi'(x)/\psi(x)$ 是 $x$ 的实系数线性函数。  

   实际上，从 Cauchy–Schwarz 等号条件出发，存在常数 $\beta$（可为复数）使得  
   $$
   x\,\overline{\psi(x)} = \beta\,\overline{\psi'(x)}\quad\text{几乎处处},
   $$  
   或其等价形式 $\psi'(x) = \beta x\,\psi(x)$。但为了 $I$ 是负实数，需要 $\beta$ 为负实数。记 $\beta = -2B$，$B>0$，则  
   $$
   \psi'(x) = -2B x\,\psi(x).
   \tag{10}
   $$  

2. **微分方程的解**：方程 (10) 的通解为  
   $$
   \psi(x) = A e^{-B x^2},
   $$  
   其中 $A$ 为复常数。为保证 $\psi$ 属于 Schwartz 空间，要求 $B>0$。  

3. **归一化条件确定 $A$**：  
   $$
   1 = \int_{-\infty}^{\infty}|A|^2 e^{-2B x^2}dx = |A|^2\sqrt{\frac{\pi}{2B}} .
   $$  
   故 $|A|^2 = \sqrt{\frac{2B}{\pi}}$。等号成立时 $\psi$ 正是高斯函数（可带有任意相位因子 $e^{i\theta}$，不影响概率密度和方差）。

---

## 6. 平移不变性：证明 (2)  

对于任意固定的 $x_0,\xi_0\in\mathbb{R}$，定义  
$$
\tilde{\psi}(x) = e^{-2\pi i x\xi_0}\,\psi(x+x_0).
$$  
直接验证可知 $\tilde{\psi}\in\mathcal{S}(\mathbb{R})$ 且满足归一化条件。其傅里叶变换为  
$$
\hat{\tilde{\psi}}(\xi) = \int e^{-2\pi i x\xi} e^{-2\pi i x\xi_0}\psi(x+x_0)dx
= e^{2\pi i x_0(\xi+\xi_0)} \int e^{-2\pi i y(\xi+\xi_0)}\psi(y)dy
= e^{2\pi i x_0(\xi+\xi_0)}\,\hat{\psi}(\xi+\xi_0).
$$  
于是  
$$
|\tilde{\psi}(x)|^2 = |\psi(x+x_0)|^2,\qquad
|\hat{\tilde{\psi}}(\xi)|^2 = |\hat{\psi}(\xi+\xi_0)|^2.
$$  
计算方差：  
$$
\int x^2|\tilde{\psi}(x)|^2dx = \int (x-x_0)^2|\psi(x)|^2dx,
$$  
$$
\int \xi^2|\hat{\tilde{\psi}}(\xi)|^2d\xi = \int (\xi-\xi_0)^2|\hat{\psi}(\xi)|^2d\xi.
$$  
将不等式 (1) 应用于 $\tilde{\psi}$ 即得 (2)。  

---

## 7. 量子力学诠释  

在量子力学中，一维粒子的状态由波函数 $\psi(x)$ 描述（取 $\psi\in\mathcal{S}(\mathbb{R})$，归一化 $\int|\psi|^2=1$）。  

- **位置概率密度**：$|\psi(x)|^2dx$ 表示粒子在 $x$ 附近出现的概率。  
- **动量概率密度**：动量 $p$ 与波数 $\xi$ 的关系为 $p = h\xi = 2\pi\hbar\xi$（其中 $h$ 为普朗克常数，$\hbar = h/(2\pi)$）。更常用的是：$\hat{\psi}(\xi)$ 的模平方 $|\hat{\psi}(\xi)|^2d\xi$ 给出动量在 $p = h\xi$ 附近的概率。  
- **期望值**：位置期望 $\langle x\rangle = \int x|\psi|^2dx$；动量期望 $\langle p\rangle = h\int\xi|\hat{\psi}|^2d\xi$。  
- **不确定性（方差）**：  
  $$
  (\Delta x)^2 = \int (x-\langle x\rangle)^2|\psi|^2dx,\qquad
  (\Delta p)^2 = \int (p-\langle p\rangle)^2|\hat{\psi}|^2dp.
  $$  
  利用 $\xi = p/h$，有  
  $$
  (\Delta p)^2 = h^2\int (\xi-\langle\xi\rangle)^2|\hat{\psi}|^2d\xi.
  $$  

将不等式 (2) 中的 $x_0,\xi_0$ 分别取为 $\langle x\rangle$ 和 $\langle\xi\rangle$，并代入物理常数，得到  
$$
(\Delta x)^2 \cdot (\Delta p)^2 \ge h^2\cdot\frac{1}{16\pi^2}
= \frac{\hbar^2}{4},
$$  
即  
$$
\Delta x \cdot \Delta p \ge \frac{\hbar}{2}.
$$  
这就是著名的海森堡不确定性原理。其物理含义：不可能同时精确测量一个粒子的位置和动量；对位置测量越精确（$\Delta x$ 越小），动量的不确定性 $\Delta p$ 必然越大，反之亦然。等号成立时波函数为高斯波包（相干态）。

---

## 8. 补充注释  

- **为什么忽略边界项**：由于 $\psi\in\mathcal{S}(\mathbb{R})$，当 $|x|\to\infty$ 时，$x|\psi(x)|^2\to0$，因此分部积分产生的边界项 $\left.x|\psi(x)|^2\right|_{-\infty}^{\infty}=0$。  
- **Plancherel 定理**：$\int |f|^2 = \int |\hat{f}|^2$，这保证了能量守恒。  
- **高斯函数的最小性**：高斯函数是唯一使不确定性乘积达到最小值的波函数，称为**最小不确定态**。  
- **其他形式的不确定性原理**：例如熵测不准原理（Hirschman 不等式）、硬不确定性原理（Hardy 定理）等，但上述方差形式是最常用的一种。  

---

## 9. 总结  

我们从傅里叶分析的基本不等式出发，通过分部积分、柯西–施瓦茨不等式和 Plancherel 定理，严格证明了函数与其傅里叶变换的方差乘积至少为 $1/(16\pi^2)$，等号仅对高斯函数成立。通过引入普朗克常数，这一数学结论立即转化为量子力学中的海森堡不确定性原理。这不仅揭示了波粒二象性的深层结构，也奠定了现代量子理论的基本框架。

---

**参考文献**  
E. M. Stein & R. Shakarchi, *Fourier Analysis: An Introduction*, Princeton University Press, 2003, Chapter 4.

---



## 5 Exercises

## 5 习题

1. Corollary 2.3 in Chapter 2 leads to the following simplified version of the Fourier inversion formula. Suppose $f$ is a continuous function supported on an interval $[-M, M]$ , whose Fourier transform $\hat{f}$ is of moderate decrease.

2. 第 2 章推论 2.3 导致傅里叶反演公式的以下简化版本。假设 $f$ 是支集在区间 $[-M, M]$ 上的连续函数，其傅里叶变换 $\hat{f}$ 是中度衰减的。

(a) Fix $L$ with $L / 2 > M$ , and show that $f(x) = \sum a_n(L)e^{2\pi inx / L}$ where

$$a_n(L) = \frac{1}{L}\int_{-L / 2}^{L / 2}f(x)e^{-2\pi inx / L}dx = \frac{1}{L}\hat{f}(n / L).$$

(a) 固定 $L$ 使得 $L / 2 > M$，并证明 $f(x) = \sum a_n(L)e^{2\pi inx / L}$，其中

$$a_n(L) = \frac{1}{L}\int_{-L / 2}^{L / 2}f(x)e^{-2\pi inx / L}dx = \frac{1}{L}\hat{f}(n / L).$$

Alternatively, we may write $f(x) = \delta \sum_{n = -\infty}^{\infty}\hat{f} (n\delta)e^{2\pi in\delta x}$ with $\delta = 1 / L$ .

或者，我们可以写 $f(x) = \delta \sum_{n = -\infty}^{\infty}\hat{f} (n\delta)e^{2\pi in\delta x}$，其中 $\delta = 1 / L$。

(b) Prove that if $F$ is continuous and of moderate decrease, then

$$\int_{-\infty}^{\infty}F(\xi)d\xi = \lim_{\delta \to 0\atop \delta >0}\delta \sum_{n = -\infty}^{\infty}F(\delta n).$$

(b) 证明如果 $F$ 连续且中度衰减，则

$$\int_{-\infty}^{\infty}F(\xi)d\xi = \lim_{\delta \to 0\atop \delta >0}\delta \sum_{n = -\infty}^{\infty}F(\delta n).$$

(c) Conclude that $f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi ix\xi}d\xi$ .

(c) 得出结论 $f(x) = \int_{-\infty}^{\infty}\hat{f} (\xi)e^{2\pi ix\xi}d\xi$。

[Hint: For (a), note that the Fourier series of $f$ on $[- L / 2, L / 2]$ converges absolutely. For (b), first approximate the integral by $\int_{- N}^{N}F$ and the sum by $\delta \sum_{|n| \leq N / \delta}F(n\delta)$ . Then approximate the second integral by Riemann sums.]

[提示：对于 (a)，注意 $f$ 在 $[- L / 2, L / 2]$ 上的傅里叶级数绝对收敛。对于 (b)，首先用 $\int_{- N}^{N}F$ 逼近积分，用 $\delta \sum_{|n| \leq N / \delta}F(n\delta)$ 逼近和。然后用黎曼和逼近第二个积分。]

2. Let $f$ and $g$ be the functions defined by

3. 设 $f$ 和 $g$ 是由下式定义的函数

$$f(x) = \begin{cases} 1 & \text{if } |x| \leq 1/2, \\ 0 & \text{otherwise}, \end{cases} \quad g(x) = \begin{cases} 1 - |x| & \text{if } |x| \leq 1, \\ 0 & \text{otherwise}. \end{cases}$$

$$f(x) = \begin{cases} 1 & \text{if } |x| \leq 1/2, \\ 0 & \text{otherwise}, \end{cases} \quad g(x) = \begin{cases} 1 - |x| & \text{if } |x| \leq 1, \\ 0 & \text{otherwise}. \end{cases}$$

Although $f$ is not continuous, the integral defining its Fourier transform still makes sense. Show that

$$\hat{f} (\xi) = \frac{\sin 2\pi\xi}{\pi\xi}\quad \mathrm{and}\quad \hat{g} (\xi) = \left(\frac{\sin\pi\xi}{\pi\xi}\right)^2,$$

尽管 $f$ 不连续，但定义其傅里叶变换的积分仍然有意义。证明

$$\hat{f} (\xi) = \frac{\sin 2\pi\xi}{\pi\xi}\quad \mathrm{and}\quad \hat{g} (\xi) = \left(\frac{\sin\pi\xi}{\pi\xi}\right)^2,$$

===== Page 179 =====

with the understanding that $\hat{f} (0) = 2$ and $\hat{g} (0) = 1$ .

其中约定 $\hat{f} (0) = 2$ 且 $\hat{g} (0) = 1$。

3. The following exercise illustrates the principle that the decay of $\hat{f}$ is related to the continuity properties of $f$ .

4. 以下习题说明了 $\hat{f}$ 的衰减与 $f$ 的连续性质相关的原理。

(a) Suppose that $f$ is a function of moderate decrease on $\mathbb{R}$ whose Fourier transform $\hat{f}$ is continuous and satisfies

$$\hat{f} (\xi) = O\left(\frac{1}{|\xi|^{1 + \alpha}}\right)\quad \mathrm{as} |\xi |\to \infty$$

(a) 假设 $f$ 是 $\mathbb{R}$ 上的中度衰减函数，其傅里叶变换 $\hat{f}$ 连续且满足当 $|\xi |\to \infty$ 时

$$\hat{f} (\xi) = O\left(\frac{1}{|\xi|^{1 + \alpha}}\right)$$

for some $0< \alpha < 1$ . Prove that $f$ satisfies a Hölder condition of order $\alpha$ that is, that

$$|f(x + h) - f(x)|\leq M|h|^{\alpha}\quad \mathrm{for~some~}M > 0\mathrm{~and~all~}x,h\in \mathbb{R}.$$

对某个 $0< \alpha < 1$。证明 $f$ 满足 $\alpha$ 阶 Hölder 条件，即存在 $M > 0$ 使得对所有 $x,h\in \mathbb{R}$ 有

$$|f(x + h) - f(x)|\leq M|h|^{\alpha}.$$

(b) Let $f$ be a continuous function on $\mathbb{R}$ which vanishes for $|x|\geq 1$ , with $f(0) = 0$ , and which is equal to $1 / \log (1 / |x|)$ for all $x$ in a neighborhood of the origin. Prove that $\hat{f}$ is not of moderate decrease. In fact, there is no $\epsilon >0$ so that $\hat{f} (\xi) = O(1 / |\xi |^{1 + \epsilon})$ as $|\xi |\to \infty$ .

(b) 设 $f$ 是 $\mathbb{R}$ 上的连续函数，当 $|x|\geq 1$ 时为零，$f(0) = 0$，并且在原点的一个邻域内对所有 $x$ 有 $f(x) = 1 / \log (1 / |x|)$。证明 $\hat{f}$ 不是中度衰减的。事实上，不存在 $\epsilon >0$ 使得当 $|\xi |\to \infty$ 时 $\hat{f} (\xi) = O(1 / |\xi |^{1 + \epsilon})$。

[Hint: For part (a), use the Fourier inversion formula to express $f(x + h) - f(x)$ as an integral involving $\hat{f}$ , and estimate this integral separately for $\xi$ in the two ranges $|\xi |\leq 1 / |h|$ and $|\xi |\geq 1 / |h|$ .]

[提示：对于 (a) 部分，使用傅里叶反演公式将 $f(x + h) - f(x)$ 表示为涉及 $\hat{f}$ 的积分，并分别对 $|\xi |\leq 1 / |h|$ 和 $|\xi |\geq 1 / |h|$ 两个范围估计该积分。]

4. Bump functions. Examples of compactly supported functions in $\mathcal{S}(\mathbb{R})$ are very handy in many applications in analysis. Some examples are:

5. 钟形函数。$\mathcal{S}(\mathbb{R})$ 中具有紧支集的函数在分析的许多应用中非常方便。一些例子是：

(a) Suppose $a< b$ , and $f$ is the function such that $f(x) = 0$ if $x\leq a$ or $x\geq b$ and

$$f(x) = e^{-1 / (x - a)}e^{-1 / (b - x)}\quad \mathrm{if~}a< x< b.$$

(a) 假设 $a< b$，且 $f$ 是满足以下条件的函数：若 $x\leq a$ 或 $x\geq b$ 则 $f(x) = 0$，且若 $a< x< b$ 则

$$f(x) = e^{-1 / (x - a)}e^{-1 / (b - x)}.$$

Show that $f$ is indefinitely differentiable on $\mathbb{R}$ .

证明 $f$ 在 $\mathbb{R}$ 上无限可微。

(b) Prove that there exists an indefinitely differentiable function $F$ on $\mathbb{R}$ such that $F(x) = 0$ if $x\leq a$ , $F(x) = 1$ if $x\geq b$ , and $F$ is strictly increasing on $[a,b]$ .

(b) 证明存在 $\mathbb{R}$ 上的无限可微函数 $F$，使得当 $x\leq a$ 时 $F(x) = 0$，当 $x\geq b$ 时 $F(x) = 1$，且 $F$ 在 $[a,b]$ 上严格递增。

(c) Let $\delta >0$ be so small that $a + \delta < b - \delta$ . Show that there exists an indefinitely differentiable function $g$ such that $g$ is 0 if $x\leq a$ or $x\geq b$ , $g$ is 1 on $[a + \delta ,b - \delta ]$ , and $g$ is strictly monotonic on $[a,a + \delta ]$ and $[b - \delta ,b]$ .

(c) 令 $\delta >0$ 足够小使得 $a + \delta < b - \delta$。证明存在无限可微函数 $g$，使得当 $x\leq a$ 或 $x\geq b$ 时 $g = 0$，$g$ 在 $[a + \delta ,b - \delta ]$ 上为 1，且 $g$ 在 $[a,a + \delta ]$ 和 $[b - \delta ,b]$ 上严格单调。

[Hint: For (b) consider $F(x) = c\int_{- \infty}^{x}f(t)dt$ where $c$ is an appropriate constant.]

[提示：对于 (b)，考虑 $F(x) = c\int_{- \infty}^{x}f(t)dt$，其中 $c$ 是适当的常数。]

5. Suppose $f$ is continuous and of moderate decrease.

6. 假设 $f$ 连续且中度衰减。

(a) Prove that $\hat{f}$ is continuous and $\hat{f} (\xi)\to 0$ as $|\xi |\to \infty$ .

(a) 证明 $\hat{f}$ 连续且当 $|\xi |\to \infty$ 时 $\hat{f} (\xi)\to 0$。

===== Page 180 =====

(b) Show that if $\hat{f} (\xi) = 0$ for all $\xi$ , then $f$ is identically 0.

(b) 证明如果对所有 $\xi$ 有 $\hat{f} (\xi) = 0$，则 $f$ 恒为 0。

[Hint: For part (a), show that $\begin{array}{r}{\hat{f} (\xi) = \frac{1}{2}\int_{-\infty}^{\infty}[f(x) - f(x - 1 / (2\xi))]e^{- 2\pi i x\xi}dx.} \end{array}$ For part (b), verify that the multiplication formula $\begin{array}{r}{\int f(x)\hat{g} (x)d x = \int \hat{f} (y)g(y)d y} \end{array}$ still holds whenever $g\in \mathcal{S}(\mathbb{R}).$ ]

[提示：对于 (a) 部分，证明 $\hat{f} (\xi) = \frac{1}{2}\int_{-\infty}^{\infty}[f(x) - f(x - 1 / (2\xi))]e^{- 2\pi i x\xi}dx$。对于 (b) 部分，验证乘法公式 $\int f(x)\hat{g} (x)d x = \int \hat{f} (y)g(y)d y$ 在 $g\in \mathcal{S}(\mathbb{R})$ 时仍然成立。]

6. The function $e^{- \pi x^{2}}$ is its own Fourier transform. Generate other functions that (up to a constant multiple) are their own Fourier transforms. What must the constant multiples be? To decide this, prove that $\mathcal{F}^{4} = I$ . Here $\mathcal{F}(f) = \hat{f}$ is the Fourier transform, $\mathcal{F}^{4} = \mathcal{F}\circ \mathcal{F}\circ \mathcal{F}\circ \mathcal{F}$ , and $I$ is the identity operator $(I f)(x) = f(x)$ (see also Problem 7).

7. 函数 $e^{- \pi x^{2}}$ 是其自身的傅里叶变换。生成其他（至多相差常数倍）是其自身傅里叶变换的函数。常数倍必须是什么？为了确定这一点，证明 $\mathcal{F}^{4} = I$。这里 $\mathcal{F}(f) = \hat{f}$ 是傅里叶变换，$\mathcal{F}^{4} = \mathcal{F}\circ \mathcal{F}\circ \mathcal{F}\circ \mathcal{F}$，且 $I$ 是恒等算子 $(I f)(x) = f(x)$（另见问题 7）。

8. Prove that the convolution of two functions of moderate decrease is a function of moderate decrease.

9. 证明两个中度衰减函数的卷积是中度衰减函数。

[Hint: Write

$$\int f(x - y)g(y)dy = \int_{|y|\leq |x| / 2} + \int_{|y|\geq |x| / 2}.$$

[提示：写出

$$\int f(x - y)g(y)dy = \int_{|y|\leq |x| / 2} + \int_{|y|\geq |x| / 2}.$$

In the first integral $f(x - y) = O(1 / (1 + x^{2}))$ while in the second integral $g(y) = O(1 / (1 + x^{2}))$ .]

在第一个积分中 $f(x - y) = O(1 / (1 + x^{2}))$，而在第二个积分中 $g(y) = O(1 / (1 + x^{2}))$。]

8. Prove that $f$ is continuous, of moderate decrease, and $\int_{-\infty}^{\infty}f(y)e^{-y^{2}}e^{2xy}dy = 0$ for all $x\in \mathbb{R}$ , then $f = 0$ .

9. 证明如果 $f$ 连续、中度衰减，且对所有 $x\in \mathbb{R}$ 有 $\int_{-\infty}^{\infty}f(y)e^{-y^{2}}e^{2xy}dy = 0$，则 $f = 0$。

[Hint: Consider $f\ast e^{- x^{2}}$ .]

[提示：考虑 $f\ast e^{- x^{2}}$。]

9. If $f$ is of moderate decrease, then

$$\int_{-R}^{R}\left(1 - \frac{|\xi|}{R}\right)\hat{f} (\xi)e^{2\pi i x\xi}d\xi = (f*\mathcal{F}_{R})(x), \quad (14)$$

9. 如果 $f$ 中度衰减，则

$$\int_{-R}^{R}\left(1 - \frac{|\xi|}{R}\right)\hat{f} (\xi)e^{2\pi i x\xi}d\xi = (f*\mathcal{F}_{R})(x), \quad (14)$$

where the Fejer kernel on the real line is defined by

$$\mathcal{F}_{R}(t) = \left\{ \begin{array}{ll}R\left(\frac{\sin\pi tR}{\pi tR}\right)^{2} & \mathrm{if} t\neq 0,\\ R & \mathrm{if} t = 0. \end{array} \right.$$

其中实直线上的 Fejér 核定义为

$$\mathcal{F}_{R}(t) = \left\{ \begin{array}{ll}R\left(\frac{\sin\pi tR}{\pi tR}\right)^{2} & \mathrm{if} t\neq 0,\\ R & \mathrm{if} t = 0. \end{array} \right.$$

Show that $\{\mathcal{F}_{R}\}$ is a family of good kernels as $R\rightarrow \infty$ , and therefore (14) tends uniformly to $f(x)$ as $R\rightarrow \infty$ . This is the analogue of Fejer's theorem for Fourier series in the context of the Fourier transform.

证明 $\{\mathcal{F}_{R}\}$ 当 $R\rightarrow \infty$ 时是一族好核，因此当 $R\rightarrow \infty$ 时 (14) 一致趋于 $f(x)$。这是在傅里叶变换背景下 Fejér 定理对于傅里叶级数的模拟。

10. Below is an outline of a different proof of the Weierstrass approximation theorem.

11. 以下是魏尔斯特拉斯逼近定理的另一个证明的概要。

===== Page 181 =====

Define the Landau kernels by

定义 Landau 核为

$$L_n(x) = \begin{cases} c_n (1 - x^2)^n & \text{if } |x| \leq 1, \\ 0 & \text{if } |x| > 1, \end{cases}$$

$$L_n(x) = \begin{cases} c_n (1 - x^2)^n & \text{if } |x| \leq 1, \\ 0 & \text{if } |x| > 1, \end{cases}$$

where $c_{n}$ is chosen so that $\int_{-\infty}^{\infty}L_{n}(x)dx = 1$ . Prove that $\{L_{n}\}_{n\geq 0}$ is a family of good kernels as $n\to \infty$ . As a result, show that if $f$ is a continuous function supported in $[- 1 / 2,1 / 2]$ , then $(f*L_{n})(x)$ is a sequence of polynomials on $[- 1 / 2,1 / 2]$ which converges uniformly to $f$ .

其中 $c_{n}$ 选择使得 $\int_{-\infty}^{\infty}L_{n}(x)dx = 1$。证明 $\{L_{n}\}_{n\geq 0}$ 当 $n\to \infty$ 时是一族好核。结果，证明如果 $f$ 是支集在 $[- 1 / 2,1 / 2]$ 中的连续函数，则 $(f*L_{n})(x)$ 是 $[- 1 / 2,1 / 2]$ 上的一列多项式，一致收敛到 $f$。

[Hint: First show that $c_{n}\geq 2 / (n + 1)$ .]

[提示：首先证明 $c_{n}\geq 2 / (n + 1)$。]

11. Suppose that $u$ is the solution to the heat equation given by $u = f*\mathcal{H}_{t}$ where $f\in \mathcal{S}(\mathbb{R})$ . If we also set $u(x,0) = f(x)$ , prove that $u$ is continuous on the closure of the upper half-plane, and vanishes at infinity, that is,

$$u(x,t)\to 0\quad \mathrm{as}|x| + t\to \infty .$$

11. 假设 $u$ 是由 $u = f*\mathcal{H}_{t}$ 给出的热方程的解，其中 $f\in \mathcal{S}(\mathbb{R})$。如果我们还设 $u(x,0) = f(x)$，证明 $u$ 在上半平面的闭包上连续，且在无穷远处消失，即

$$u(x,t)\to 0\quad \mathrm{as}|x| + t\to \infty .$$

[Hint: To prove that $u$ vanishes at infinity, show that (i) $|u(x,t)|\leq C / \sqrt{t}$ and (ii) $|u(x,t)|\leq C / (1 + |x|^2) + Ct^{- 1 / 2}e^{- cx^2 /t}$ . Use (i) when $|x|\leq t$ , and (ii) otherwise.]

[提示：为了证明 $u$ 在无穷远处消失，证明 (i) $|u(x,t)|\leq C / \sqrt{t}$ 和 (ii) $|u(x,t)|\leq C / (1 + |x|^2) + Ct^{- 1 / 2}e^{- cx^2 /t}$。当 $|x|\leq t$ 时使用 (i)，否则使用 (ii)。]

12. Show that the function defined by

$$u(x,t) = \frac{x}{t}\mathcal{H}_t(x)$$

12. 证明由下式定义的函数

$$u(x,t) = \frac{x}{t}\mathcal{H}_t(x)$$

satisfies the heat equation for $t > 0$ and $\lim_{t\to 0}u(x,t) = 0$ for every $x$ , but $u$ is not continuous at the origin.

满足当 $t > 0$ 时的热方程，且对每个 $x$ 有 $\lim_{t\to 0}u(x,t) = 0$，但 $u$ 在原点不连续。

[Hint: Approach the origin with $(x,t)$ on the parabola $x^{2} / 4t = c$ where $c$ is a constant.]

[提示：沿着抛物线 $x^{2} / 4t = c$（其中 $c$ 是常数）上的点 $(x,t)$ 趋近原点。]

13. Prove the following uniqueness theorem for harmonic functions in the strip $\{(x,y):0< y< 1, - \infty < x< \infty \}$ : if $u$ is harmonic in the strip, continuous on its closure with $u(x,0) = u(x,1) = 0$ for all $x\in \mathbb{R}$ , and $u$ vanishes at infinity, then $u = 0$ .

14. 证明带形区域 $\{(x,y):0< y< 1, - \infty < x< \infty \}$ 中调和函数的以下唯一性定理：如果 $u$ 在带形区域中调和，在其闭包上连续，对所有 $x\in \mathbb{R}$ 有 $u(x,0) = u(x,1) = 0$，且 $u$ 在无穷远处消失，则 $u = 0$。

15. Prove that the periodization of the Fejer kernel $\mathcal{F}_{N}$ on the real line (Exercise 9) is equal to the Fejer kernel for periodic functions of period 1. In other words,

$$\sum_{n = -\infty}^{\infty}\mathcal{F}_N(x + n) = F_N(x),$$

14. 证明实直线上 Fejér 核 $\mathcal{F}_{N}$（习题 9）的周期化等于周期为 1 的周期函数的 Fejér 核。换句话说，

$$\sum_{n = -\infty}^{\infty}\mathcal{F}_N(x + n) = F_N(x),$$

when $N\geq 1$ is an integer, and where

$$F_{N}(x) = \sum_{n = -N}^{N}\left(1 - \frac{|n|}{N}\right)e^{2\pi inx} = \frac{1}{N}\frac{\sin^{2}(N\pi x)}{\sin^{2}(\pi x)}.$$

当 $N\geq 1$ 是整数时，且其中

$$F_{N}(x) = \sum_{n = -N}^{N}\left(1 - \frac{|n|}{N}\right)e^{2\pi inx} = \frac{1}{N}\frac{\sin^{2}(N\pi x)}{\sin^{2}(\pi x)}.$$

===== Page 182 =====

15. This exercise provides another example of periodization.

16. 本习题提供了周期化的另一个例子。

(a) Apply the Poisson summation formula to the function $g$ in Exercise 2 to obtain

$$\sum_{n = -\infty}^{\infty}\frac{1}{(n + \alpha)^2} = \frac{\pi^2}{(\sin\pi\alpha)^2}$$

(a) 将泊松求和公式应用于习题 2 中的函数 $g$，得到

$$\sum_{n = -\infty}^{\infty}\frac{1}{(n + \alpha)^2} = \frac{\pi^2}{(\sin\pi\alpha)^2}$$

whenever $\alpha$ is real, but not equal to an integer.

只要 $\alpha$ 是实数但不等于整数。

(b) Prove as a consequence that

$$\sum_{n = -\infty}^{\infty}\frac{1}{(n + \alpha)} = \frac{\pi}{\tan\pi\alpha} \quad (15)$$

(b) 作为推论，证明

$$\sum_{n = -\infty}^{\infty}\frac{1}{(n + \alpha)} = \frac{\pi}{\tan\pi\alpha} \quad (15)$$

whenever $\alpha$ is real but not equal to an integer. [Hint: First prove it when $0< \alpha < 1$ . To do so, integrate the formula in (b). What is the precise meaning of the series on the left- hand side of (15)? Evaluate at $\alpha = 1 / 2$ .]

只要 $\alpha$ 是实数但不等于整数。[提示：首先在 $0< \alpha < 1$ 时证明它。为此，对 (b) 中的公式积分。(15) 左边的级数的确切含义是什么？在 $\alpha = 1 / 2$ 处求值。]

16. The Dirichlet kernel on the real line is defined by

$$\int_{-R}^{R}\hat{f} (\xi)e^{2\pi i x\xi}d\xi = (f*\mathcal{D}_{R})(x)\mathrm{so that}\mathcal{D}_{R}(x) = \overline{\chi_{[-R,R]}}(x) = \frac{\sin(2\pi R x)}{\pi x}.$$

16. 实直线上的 Dirichlet 核定义为

$$\int_{-R}^{R}\hat{f} (\xi)e^{2\pi i x\xi}d\xi = (f*\mathcal{D}_{R})(x)\mathrm{so that}\mathcal{D}_{R}(x) = \overline{\chi_{[-R,R]}}(x) = \frac{\sin(2\pi R x)}{\pi x}.$$

Also, the modified Dirichlet kernel for periodic functions of period 1 is defined by

$$D_{N}^{*}(x) = \sum_{|n|\leq N - 1}e^{2\pi inx} + \frac{1}{2} (e^{-2\pi inx} + e^{2\pi inx}).$$

此外，周期为 1 的周期函数的修正 Dirichlet 核定义为

$$D_{N}^{*}(x) = \sum_{|n|\leq N - 1}e^{2\pi inx} + \frac{1}{2} (e^{-2\pi inx} + e^{2\pi inx}).$$

Show that the result in Exercise 15 gives

$$\sum_{n = -\infty}^{\infty}\mathcal{D}_N(x + n) = D_N^* (x),$$

证明习题 15 的结果给出

$$\sum_{n = -\infty}^{\infty}\mathcal{D}_N(x + n) = D_N^* (x),$$

where $N\geq 1$ is an integer, and the infinite series must be summed symmetrically. In other words, the periodization of $\mathcal{D}_N$ is the modified Dirichlet kernel $D_N^*$ .

其中 $N\geq 1$ 是整数，且无穷级数必须对称求和。换句话说，$\mathcal{D}_N$ 的周期化是修正的 Dirichlet 核 $D_N^*$。

17. The gamma function is defined for $s > 0$ by

$$\Gamma (s) = \int_{0}^{\infty}e^{-x}x^{s - 1}dx.$$

17. Gamma 函数对 $s > 0$ 定义为

$$\Gamma (s) = \int_{0}^{\infty}e^{-x}x^{s - 1}dx.$$

(a) Show that for $s > 0$ the above integral makes sense, that is, that the following two limits exist:

$$\lim_{\delta \to 0}\int_{\delta}^{1}e^{-x}x^{s - 1}dx\quad \mathrm{and}\quad \lim_{A\to \infty}\int_{1}^{A}e^{-x}x^{s - 1}dx.$$

(a) 证明对 $s > 0$ 上述积分有意义，即以下两个极限存在：

$$\lim_{\delta \to 0}\int_{\delta}^{1}e^{-x}x^{s - 1}dx\quad \mathrm{and}\quad \lim_{A\to \infty}\int_{1}^{A}e^{-x}x^{s - 1}dx.$$

===== Page 183 =====

(b) Prove that $\Gamma (s + 1) = s\Gamma (s)$ whenever $s > 0$ , and conclude that for every integer $n \geq 1$ we have $\Gamma (n + 1) = n!$ .

(b) 证明当 $s > 0$ 时 $\Gamma (s + 1) = s\Gamma (s)$，并得出结论：对每个整数 $n \geq 1$，有 $\Gamma (n + 1) = n!$。

(c) Show that

$$\Gamma \left(\frac{1}{2}\right) = \sqrt{\pi}\quad \mathrm{and}\quad \Gamma \left(\frac{3}{2}\right) = \frac{\sqrt{\pi}}{2}.$$

(c) 证明

$$\Gamma \left(\frac{1}{2}\right) = \sqrt{\pi}\quad \mathrm{and}\quad \Gamma \left(\frac{3}{2}\right) = \frac{\sqrt{\pi}}{2}.$$

[Hint: For (c), use $\int_{-\infty}^{\infty} e^{-\pi x^2} dx = 1$ .]

[提示：对于 (c)，使用 $\int_{-\infty}^{\infty} e^{-\pi x^2} dx = 1$。]

18. The zeta function is defined for $s > 1$ by $\zeta (s) = \sum_{n = 1}^{\infty} 1 / n^s$ . Verify the identity

$$\pi^{-s / 2}\Gamma (s / 2)\zeta (s) = \frac{1}{2}\int_{0}^{\infty}t^{\frac{s}{2} -1}(\theta (t) - 1)dt\qquad \mathrm{whenever} s > 1$$

18. Zeta 函数对 $s > 1$ 定义为 $\zeta (s) = \sum_{n = 1}^{\infty} 1 / n^s$。验证恒等式

$$\pi^{-s / 2}\Gamma (s / 2)\zeta (s) = \frac{1}{2}\int_{0}^{\infty}t^{\frac{s}{2} -1}(\theta (t) - 1)dt\qquad \mathrm{whenever} s > 1$$

where $\Gamma$ and $\theta$ are the gamma and theta functions, respectively:

$$\Gamma (s) = \int_{0}^{\infty}e^{-t}t^{s - 1}dt\quad \mathrm{and}\quad \theta (s) = \sum_{n = -\infty}^{\infty}e^{-n\pi^{2}s}.$$

其中 $\Gamma$ 和 $\theta$ 分别是 gamma 函数和 theta 函数：

$$\Gamma (s) = \int_{0}^{\infty}e^{-t}t^{s - 1}dt\quad \mathrm{and}\quad \theta (s) = \sum_{n = -\infty}^{\infty}e^{-n\pi^{2}s}.$$

More about the zeta function and its relation to the prime number theorem can be found in Book II.

关于 zeta 函数及其与素数定理的关系的更多内容可以在第二卷中找到。

19. The following is a variant of the calculation of $\zeta (2m) = \sum_{n = 1}^{\infty} 1 / n^{2m}$ found in Problem 4, Chapter 3.

20. 以下是第 3 章问题 4 中 $\zeta (2m) = \sum_{n = 1}^{\infty} 1 / n^{2m}$ 计算的一个变体。

(a) Apply the Poisson summation formula to $f(x) = t / (\pi (x^2 + t^2))$ and $\hat{f} (\xi) = e^{-2\pi t|\xi|}$ where $t > 0$ in order to get

$$\frac{1}{\pi}\sum_{n = -\infty}^{\infty}\frac{t}{t^2 + n^2} = \sum_{n = -\infty}^{\infty}e^{-2\pi t|n|}.$$

(a) 将泊松求和公式应用于 $f(x) = t / (\pi (x^2 + t^2))$ 和 $\hat{f} (\xi) = e^{-2\pi t|\xi|}$，其中 $t > 0$，以得到

$$\frac{1}{\pi}\sum_{n = -\infty}^{\infty}\frac{t}{t^2 + n^2} = \sum_{n = -\infty}^{\infty}e^{-2\pi t|n|}.$$

(b) Prove the following identity valid for $0 < t < 1$ :

$$\frac{1}{\pi}\sum_{n = -\infty}^{\infty}\frac{t}{t^2 + n^2} = \frac{1}{\pi t} +\frac{2}{\pi}\sum_{m = 1}^{\infty}(-1)^{m + 1}\zeta (2m)t^{2m - 1}$$

(b) 证明以下对 $0 < t < 1$ 成立的恒等式：

$$\frac{1}{\pi}\sum_{n = -\infty}^{\infty}\frac{t}{t^2 + n^2} = \frac{1}{\pi t} +\frac{2}{\pi}\sum_{m = 1}^{\infty}(-1)^{m + 1}\zeta (2m)t^{2m - 1}$$

as well as

$$\sum_{n = -\infty}^{\infty}e^{-2\pi t|n|} = \frac{2}{1 - e^{-2\pi t}} -1.$$

以及

$$\sum_{n = -\infty}^{\infty}e^{-2\pi t|n|} = \frac{2}{1 - e^{-2\pi t}} -1.$$

===== Page 184 =====

(c) Use the fact that

$$\frac{z}{e^z - 1} = 1 - \frac{z}{2} +\sum_{m = 1}^{\infty}\frac{B_{2m}}{(2m)!} z^{2m},$$

(c) 利用以下事实

$$\frac{z}{e^z - 1} = 1 - \frac{z}{2} +\sum_{m = 1}^{\infty}\frac{B_{2m}}{(2m)!} z^{2m},$$

where $B_{k}$ are the Bernoulli numbers to deduce from the above formula,

$$2\zeta (2m) = (-1)^{m + 1}\frac{(2\pi)^{2m}}{(2m)!} B_{2m}.$$

其中 $B_{k}$ 是伯努利数，从上述公式推导出

$$2\zeta (2m) = (-1)^{m + 1}\frac{(2\pi)^{2m}}{(2m)!} B_{2m}.$$

20. The following results are relevant in information theory when one tries to recover a signal from its samples.

21. 以下结果在信息论中与试图从样本中恢复信号相关。

Suppose $f$ is of moderate decrease and that its Fourier transform $\hat{f}$ is supported in $I = [- 1 / 2,1 / 2]$ . Then, $f$ is entirely determined by its restriction to $\mathbb{Z}$ . This means that if $g$ is another function of moderate decrease whose Fourier transform is supported in $I$ and $f(n) = g(n)$ for all $n\in \mathbb{Z}$ , then $f = g$ . More precisely:

假设 $f$ 中度衰减，且其傅里叶变换 $\hat{f}$ 支集在 $I = [- 1 / 2,1 / 2]$ 中。那么，$f$ 完全由其到 $\mathbb{Z}$ 的限制决定。这意味着，如果 $g$ 是另一个中度衰减的函数，其傅里叶变换支集在 $I$ 中，且对所有 $n\in \mathbb{Z}$ 有 $f(n) = g(n)$，则 $f = g$。更精确地说：

(a) Prove that the following reconstruction formula holds:

$$f(x) = \sum_{n = -\infty}^{\infty}f(n)K(x - n)\quad \mathrm{where}K(y) = \frac{\sin\pi y}{\pi y}.$$

(a) 证明以下重构公式成立：

$$f(x) = \sum_{n = -\infty}^{\infty}f(n)K(x - n)\quad \mathrm{where}K(y) = \frac{\sin\pi y}{\pi y}.$$

Note that $K(y) = O(1 / |y|)$ as $|y|\to \infty$

注意当 $|y|\to \infty$ 时 $K(y) = O(1 / |y|)$。

(b) If $\lambda >1$ , then

$$f(x) = \sum_{n = -\infty}^{\infty}\frac{1}{\lambda} f\left(\frac{n}{\lambda}\right)K_{\lambda}\left(x - \frac{n}{\lambda}\right)\quad \mathrm{where}K_{\lambda}(y) = \frac{\cos\pi y - \cos\pi\lambda y}{\pi^{2}(\lambda - 1)y^{2}}.$$

(b) 如果 $\lambda >1$，则

$$f(x) = \sum_{n = -\infty}^{\infty}\frac{1}{\lambda} f\left(\frac{n}{\lambda}\right)K_{\lambda}\left(x - \frac{n}{\lambda}\right)\quad \mathrm{where}K_{\lambda}(y) = \frac{\cos\pi y - \cos\pi\lambda y}{\pi^{2}(\lambda - 1)y^{2}}.$$

Thus, if one samples $f$ "more often," the series in the reconstruction formula converges faster since $K_{\lambda}(y) = O(1 / |y|^2)$ as $|y|\to \infty$ . Note that $K_{\lambda}(y)\to K(y)$ as $\lambda \to 1$ .

因此，如果人们“更频繁地”采样 $f$，重构公式中的级数收敛得更快，因为当 $|y|\to \infty$ 时 $K_{\lambda}(y) = O(1 / |y|^2)$。注意当 $\lambda \to 1$ 时 $K_{\lambda}(y)\to K(y)$。

(c) Prove that $\int_{-\infty}^{\infty}|f(x)|^{2}dx = \sum_{n = -\infty}^{\infty}|f(n)|^{2}$ .

(c) 证明 $\int_{-\infty}^{\infty}|f(x)|^{2}dx = \sum_{n = -\infty}^{\infty}|f(n)|^{2}$。

[Hint: For part (a) show that if $\chi$ is the characteristic function of $I$ , then $\hat{f} (\xi) = \chi (\xi)\sum_{n = -\infty}^{\infty}f(n)e^{- 2\pi in\xi}$ . For (b) use the function in Figure 2 instead of $\chi (\xi)$ .]

[提示：对于 (a) 部分，证明如果 $\chi$ 是 $I$ 的特征函数，则 $\hat{f} (\xi) = \chi (\xi)\sum_{n = -\infty}^{\infty}f(n)e^{- 2\pi in\xi}$。对于 (b)，使用图 2 中的函数代替 $\chi (\xi)$。]

21. Suppose that $f$ is continuous on $\mathbb{R}$ . Show that $f$ and $\hat{f}$ cannot both be compactly supported unless $f = 0$ . This can be viewed in the same spirit as the uncertainty principle.

22. 假设 $f$ 在 $\mathbb{R}$ 上连续。证明 $f$ 和 $\hat{f}$ 不能同时具有紧支集，除非 $f = 0$。这可以与不确定性原理的精神相同地看待。

===== Page 185 =====

<center>Figure 2. The function in Exercise 20 </center>

<center>图 2. 习题 20 中的函数</center>

[Hint: Assume $f$ is supported in $[0,1 / 2]$ . Expand $f$ in a Fourier series in the interval $[0,1]$ , and note that as a result, $f$ is a trigonometric polynomial.]

[提示：假设 $f$ 支集在 $[0,1 / 2]$ 中。在区间 $[0,1]$ 上将 $f$ 展开为傅里叶级数，并注意结果，$f$ 是一个三角多项式。]

22. The heuristic assertion stated before Theorem 4.1 can be made precise as follows. If $F$ is a function on $\mathbb{R}$ , then we say that the preponderance of its mass is contained in an interval $I$ (centered at the origin) if

$$\int_{I}x^{2}|F(x)|^{2}dx\geq \frac{1}{2}\int_{\mathbb{R}}x^{2}|F(x)|^{2}dx. \quad (16)$$

22. 定理 4.1 之前的启发式断言可以精确表述如下。如果 $F$ 是 $\mathbb{R}$ 上的函数，我们说其质量的主体包含在区间 $I$（以原点为中心）中，如果

$$\int_{I}x^{2}|F(x)|^{2}dx\geq \frac{1}{2}\int_{\mathbb{R}}x^{2}|F(x)|^{2}dx. \quad (16)$$

Now suppose $f\in \mathcal{S}$ , and (16) holds with $F = f$ and $I = I_{1}$ ; also with $F = \hat{f}$ and $I = I_{2}$ . Then if $L_{j}$ denotes the length of $I_{j}$ , we have

$$L_{1}L_{2}\geq \frac{1}{2\pi}.$$

现在假设 $f\in \mathcal{S}$，且 (16) 对 $F = f$ 和 $I = I_{1}$ 成立；也对 $F = \hat{f}$ 和 $I = I_{2}$ 成立。那么如果 $L_{j}$ 表示 $I_{j}$ 的长度，我们有

$$L_{1}L_{2}\geq \frac{1}{2\pi}.$$

A similar conclusion holds if the intervals are not necessarily centered at the origin.

如果区间不一定以原点为中心，类似的结论也成立。

23. The Heisenberg uncertainty principle can be formulated in terms of the operator $L = -\frac{d^{2}}{dx^{2}} +x^{2}$ , which acts on Schwartz functions by the formula

$$L(f) = -\frac{d^{2}f}{dx^{2}} +x^{2}f.$$

23. 海森堡不确定性原理可以用算子 $L = -\frac{d^{2}}{dx^{2}} +x^{2}$ 来表述，该算子通过公式作用于施瓦茨函数

$$L(f) = -\frac{d^{2}f}{dx^{2}} +x^{2}f.$$

This operator, sometimes called the Hermite operator, is the quantum analogue of the harmonic oscillator. Consider the usual inner product on $\mathcal{S}$ given by

$$(f,g) = \int_{-\infty}^{\infty}f(x)\overline{g(x)} dx\qquad \mathrm{whenever} f,g\in \mathcal{S}.$$

这个算子有时称为 Hermite 算子，是量子力学中谐振子的模拟。考虑 $\mathcal{S}$ 上通常的内积：

$$(f,g) = \int_{-\infty}^{\infty}f(x)\overline{g(x)} dx\qquad \mathrm{whenever} f,g\in \mathcal{S}.$$

===== Page 186 =====

(a) Prove that the Heisenberg uncertainty principle implies

$$(Lf,f)\geq (f,f)\quad \mathrm{for~all~}f\in \mathcal{S}.$$

(a) 证明海森堡不确定性原理蕴含

$$(Lf,f)\geq (f,f)\quad \mathrm{for~all~}f\in \mathcal{S}.$$

This is usually denoted by $L\geq I$ . [Hint: Integrate by parts.]

这通常记为 $L\geq I$。[提示：分部积分。]

(b) Consider the operators $A$ and $A^{*}$ defined on $\mathcal{S}$ by

$$A(f) = \frac{df}{dx} +xf\quad \mathrm{and}\quad A^{*}(f) = -\frac{df}{dx} +xf.$$

(b) 考虑定义在 $\mathcal{S}$ 上的算子 $A$ 和 $A^{*}$：

$$A(f) = \frac{df}{dx} +xf\quad \mathrm{and}\quad A^{*}(f) = -\frac{df}{dx} +xf.$$

The operators $A$ and $A^{*}$ are sometimes called the annihilation and creation operators, respectively. Prove that for all $f,g\in \mathcal{S}$ we have

(i) $(Af,g) = (f,A^{*}g)$ (ii) $(Af,Af) = (A^{*}Af,f)\geq 0$ (iii) $A^{*}A = L - I.$

算子 $A$ 和 $A^{*}$ 有时分别称为湮灭算子和产生算子。证明对所有 $f,g\in \mathcal{S}$，有

(i) $(Af,g) = (f,A^{*}g)$ (ii) $(Af,Af) = (A^{*}Af,f)\geq 0$ (iii) $A^{*}A = L - I.$

In particular, this again shows that $L\geq I$

特别地，这再次表明 $L\geq I$。

(c) Now for $t\in \mathbb{R}$ , let

$$A_{t}(f) = \frac{df}{dx} +txf\quad \mathrm{and}\quad A_{t}^{*}(f) = -\frac{df}{dx} +txf.$$

(c) 现在对 $t\in \mathbb{R}$，令

$$A_{t}(f) = \frac{df}{dx} +txf\quad \mathrm{and}\quad A_{t}^{*}(f) = -\frac{df}{dx} +txf.$$

Use the fact that $(A_{t}^{*}A_{t}f,f)\geq 0$ to give another proof of the Heisenberg uncertainty principle which says that whenever $\int_{-\infty}^{\infty}|f(x)|^{2}dx = 1$ then

$$\left(\int_{-\infty}^{\infty}x^{2}|f(x)|^{2}dx\right)\left(\int_{-\infty}^{\infty}\left|\frac{df}{dx}\right|^{2}dx\right)\geq 1 / 4.$$

利用 $(A_{t}^{*}A_{t}f,f)\geq 0$ 的事实给出海森堡不确定性原理的另一个证明，该原理表明只要 $\int_{-\infty}^{\infty}|f(x)|^{2}dx = 1$，就有

$$\left(\int_{-\infty}^{\infty}x^{2}|f(x)|^{2}dx\right)\left(\int_{-\infty}^{\infty}\left|\frac{df}{dx}\right|^{2}dx\right)\geq 1 / 4.$$

[Hint: Think of $(A_{t}^{*}A_{t}f,f)$ as a quadratic polynomial in $t$ .]

[提示：将 $(A_{t}^{*}A_{t}f,f)$ 视为 $t$ 的二次多项式。]

## 6 Problems

## 6 问题

1. The equation

$$x^{2}\frac{\partial^{2}u}{\partial x^{2}} +ax\frac{\partial u}{\partial x} = \frac{\partial u}{\partial t} \quad (17)$$

1. 方程

$$x^{2}\frac{\partial^{2}u}{\partial x^{2}} +ax\frac{\partial u}{\partial x} = \frac{\partial u}{\partial t} \quad (17)$$

with $u(x,0) = f(x)$ for $0< x< \infty$ and $t > 0$ is a variant of the heat equation which occurs in a number of applications. To solve (17), make the change of variables $x = e^{- y}$ so that $- \infty < y< \infty$ . Set $U(y,t) = u(e^{- y},t)$ and $F(y) = f(e^{- y})$ . Then the problem reduces to the equation

$$\frac{\partial^2U}{\partial y^2} +(1 - a)\frac{\partial U}{\partial y} = \frac{\partial U}{\partial t},$$

其中 $u(x,0) = f(x)$，$0< x< \infty$，$t > 0$，是热方程的一个变体，出现在许多应用中。为了求解 (17)，作变量替换 $x = e^{- y}$，使得 $- \infty < y< \infty$。设 $U(y,t) = u(e^{- y},t)$ 和 $F(y) = f(e^{- y})$。则问题简化为方程

$$\frac{\partial^2U}{\partial y^2} +(1 - a)\frac{\partial U}{\partial y} = \frac{\partial U}{\partial t},$$

===== Page 187 =====

with $U(y,0) = F(y)$ . This can be solved like the usual heat equation (the case $a = 1$ ) by taking the Fourier transform in the $y$ variable. One must then compute the integral $\int_{-\infty}^{\infty}e^{(- 4\pi^{2}\xi^{2} + (1 - a)2\pi i\xi t)}e^{2\pi i\xi v}d\xi$ . Show that the solution of the original problem is then given by

$$u(x,t) = \frac{1}{(4\pi t)^{1 / 2}}\int_{0}^{\infty}e^{-(\log (v / x) + (1 - a)t)^{2} / (4t)}f(v)\frac{dv}{v}.$$

满足 $U(y,0) = F(y)$。这可以像通常的热方程（$a = 1$ 的情形）一样，通过对 $y$ 变量取傅里叶变换来求解。然后必须计算积分 $\int_{-\infty}^{\infty}e^{(- 4\pi^{2}\xi^{2} + (1 - a)2\pi i\xi t)}e^{2\pi i\xi v}d\xi$。证明原问题的解然后由下式给出

$$u(x,t) = \frac{1}{(4\pi t)^{1 / 2}}\int_{0}^{\infty}e^{-(\log (v / x) + (1 - a)t)^{2} / (4t)}f(v)\frac{dv}{v}.$$

2. The Black-Scholes equation from finance theory is

$$\frac{\partial V}{\partial t} +rs\frac{\partial V}{\partial s} +\frac{\sigma^2s^2}{2}\frac{\partial^2V}{\partial s^2} -rV = 0,\qquad 0< t< T, \quad (18)$$

2. 金融理论中的 Black-Scholes 方程是

$$\frac{\partial V}{\partial t} +rs\frac{\partial V}{\partial s} +\frac{\sigma^2s^2}{2}\frac{\partial^2V}{\partial s^2} -rV = 0,\qquad 0< t< T, \quad (18)$$

subject to the "final" boundary condition $V(s,T) = F(s)$ . An appropriate change of variables reduces this to the equation in Problem 1. Alternatively, the substitution $V(s,t) = e^{ax + br}U(x,\tau)$ where $x = \log s$ $\tau = \frac{\sigma^2}{2} (T - t)$ $a = \frac{1}{2} - \frac{r}{\sigma^2}$ , and $b = -\left(\frac{1}{2} +\frac{r}{\sigma^2}\right)^2$ reduces (18) to the one- dimensional heat equation with the initial condition $U(x,0) = e^{- ax}F(e^x)$ . Thus a solution to the Black- Scholes equation is

$$V(s,t) = \frac{e^{-r(T - t)}}{\sqrt{2\pi\sigma^2(T - t)}}\int_0^\infty e^{-\frac{(\log(s / s^*) + (r - \sigma^2 / 2)(T - t))^2}{2\sigma^2(T - t)}} F(s^*)ds^*.$$

满足“最终”边界条件 $V(s,T) = F(s)$。适当的变量替换将其简化为问题 1 中的方程。或者，代入 $V(s,t) = e^{ax + br}U(x,\tau)$，其中 $x = \log s$，$\tau = \frac{\sigma^2}{2} (T - t)$，$a = \frac{1}{2} - \frac{r}{\sigma^2}$，且 $b = -\left(\frac{1}{2} +\frac{r}{\sigma^2}\right)^2$，将 (18) 简化为一维热方程，初始条件为 $U(x,0) = e^{- ax}F(e^x)$。因此，Black-Scholes 方程的一个解是

$$V(s,t) = \frac{e^{-r(T - t)}}{\sqrt{2\pi\sigma^2(T - t)}}\int_0^\infty e^{-\frac{(\log(s / s^*) + (r - \sigma^2 / 2)(T - t))^2}{2\sigma^2(T - t)}} F(s^*)ds^*.$$

3. \* The Dirichlet problem in a strip. Consider the equation $\triangle u = 0$ in the horizontal strip

$$\{(x,y):0< y< 1, - \infty < x< \infty \}$$

3. \* 带形区域中的 Dirichlet 问题。考虑水平带形区域中的方程 $\triangle u = 0$

$$\{(x,y):0< y< 1, - \infty < x< \infty \}$$

with boundary conditions $u(x,0) = f_0(x)$ and $u(x,1) = f_1(x)$ , where $f_0$ and $f_1$ are both in the Schwartz space.

带有边界条件 $u(x,0) = f_0(x)$ 和 $u(x,1) = f_1(x)$，其中 $f_0$ 和 $f_1$ 都在施瓦茨空间中。

(a) Show (formally) that if $u$ is a solution to this problem, then

$$\hat{u} (\xi ,y) = A(\xi)e^{2\pi \xi y} + B(\xi)e^{-2\pi \xi y}.$$

(a) （形式地）证明如果 $u$ 是这个问题的解，则

$$\hat{u} (\xi ,y) = A(\xi)e^{2\pi \xi y} + B(\xi)e^{-2\pi \xi y}.$$

Express $A$ and $B$ in terms of $\widehat{f}_0$ and $\widehat{f}_1$ , and show that

$$\hat{u} (\xi ,y) = \frac{\sinh(2\pi(1 - y)\xi)}{\sinh(2\pi\xi)}\widehat{f}_0(\xi) + \frac{\sinh(2\pi y\xi)}{\sinh(2\pi\xi)}\widehat{f}_0(\xi).$$

用 $\widehat{f}_0$ 和 $\widehat{f}_1$ 表示 $A$ 和 $B$，并证明

$$\hat{u} (\xi ,y) = \frac{\sinh(2\pi(1 - y)\xi)}{\sinh(2\pi\xi)}\widehat{f}_0(\xi) + \frac{\sinh(2\pi y\xi)}{\sinh(2\pi\xi)}\widehat{f}_0(\xi).$$

(b) Prove as a result that

$$\int_{-\infty}^{\infty}|u(x,y) - f_0(x)|^2 dx\to 0\quad \mathrm{as} y\to 0$$

(b) 作为结果证明

$$\int_{-\infty}^{\infty}|u(x,y) - f_0(x)|^2 dx\to 0\quad \mathrm{as} y\to 0$$

and

$$\int_{-\infty}^{\infty}|u(x,y) - f_1(x)|^2 dx\to 0\quad \mathrm{as} y\to 1.$$

和

$$\int_{-\infty}^{\infty}|u(x,y) - f_1(x)|^2 dx\to 0\quad \mathrm{as} y\to 1.$$

===== Page 188 =====

(c) If $\Phi (\xi) = (\sinh 2\pi a\xi) / (\sinh 2\pi \xi)$ , with $0\leq a< 1$ , then $\Phi$ is the Fourier transform of $\phi$ where

$$\phi (x) = \frac{\sin\pi a}{2}\cdot \frac{1}{\cosh\pi x + \cos\pi a}.$$

(c) 如果 $\Phi (\xi) = (\sinh 2\pi a\xi) / (\sinh 2\pi \xi)$，其中 $0\leq a< 1$，则 $\Phi$ 是 $\phi$ 的傅里叶变换，其中

$$\phi (x) = \frac{\sin\pi a}{2}\cdot \frac{1}{\cosh\pi x + \cos\pi a}.$$

This can be shown, for instance, by using contour integration and the residue formula from complex analysis (see Book II, Chapter 3).

这可以通过例如使用复分析中的围道积分和留数公式来证明（见第二卷，第 3 章）。

(d) Use this result to express $u$ in terms of Poisson-like integrals involving $f_{0}$ and $f_{1}$ as follows:

$$u(x,y) = \frac{\sin\pi y}{2}\left(\int_{-\infty}^{\infty}\frac{f_0(x - t)}{\cosh\pi t - \cos\pi y} dt + \int_{-\infty}^{\infty}\frac{f_1(x - t)}{\cosh\pi t + \cos\pi y} dt\right).$$

(d) 利用这一结果，将 $u$ 表示为涉及 $f_{0}$ 和 $f_{1}$ 的类似泊松的积分如下：

$$u(x,y) = \frac{\sin\pi y}{2}\left(\int_{-\infty}^{\infty}\frac{f_0(x - t)}{\cosh\pi t - \cos\pi y} dt + \int_{-\infty}^{\infty}\frac{f_1(x - t)}{\cosh\pi t + \cos\pi y} dt\right).$$

(e) Finally, one can check that the function $u(x,y)$ defined by the above expression is harmonic in the strip, and converges uniformly to $f_{0}(x)$ as $y\rightarrow 0$ , and to $f_{1}(x)$ as $y\rightarrow 1$ . Moreover, one sees that $u(x,y)$ vanishes at infinity, that is, $\lim_{|x|\rightarrow \infty}u(x,y) = 0$ , uniformly in $y$ .

(e) 最后，可以验证由上述表达式定义的函数 $u(x,y)$ 在带形区域中是调和的，并且当 $y\rightarrow 0$ 时一致收敛到 $f_{0}(x)$，当 $y\rightarrow 1$ 时一致收敛到 $f_{1}(x)$。此外，人们看到 $u(x,y)$ 在无穷远处消失，即 $\lim_{|x|\rightarrow \infty}u(x,y) = 0$，在 $y$ 上一致。

In Exercise 12, we gave an example of a function that satisfies the heat equation in the upper half- plane, with boundary value 0, but which was not identically 0. We observed in this case that $u$ was in fact not continuous up to the boundary.

在习题 12 中，我们给出了一个满足上半平面热方程、边界值为 0 但不恒为 0 的函数的例子。我们注意到在这种情况下 $u$ 实际上直到边界都不连续。

In Problem 4 we exhibit examples illustrating non- uniqueness, but this time with continuity up to the boundary $t = 0$ . These examples satisfy a growth condition at infinity, namely $|u(x,t)|\leq C e^{cx^{2 + \epsilon}}$ , for any $\epsilon >0$ . Problems 5 and 6 show that under the more restrictive growth condition $|u(x,t)|\leq C e^{cx^{2}}$ , uniqueness does hold.

在问题 4 中，我们展示了说明非唯一性的例子，但这次是直到边界 $t = 0$ 都连续。这些例子满足在无穷远处的增长条件，即对任何 $\epsilon >0$ 有 $|u(x,t)|\leq C e^{cx^{2 + \epsilon}}$。问题 5 和 6 表明，在更严格的增长条件 $|u(x,t)|\leq C e^{cx^{2}}$ 下，唯一性确实成立。

4. \* If $g$ is a smooth function on $\mathbb{R}$ , define the formal power series

$$u(x,t) = \sum_{n = 0}^{\infty}g^{(n)}(t)\frac{x^{2n}}{(2n)!}.$$

4. \* 如果 $g$ 是 $\mathbb{R}$ 上的光滑函数，定义形式幂级数

$$u(x,t) = \sum_{n = 0}^{\infty}g^{(n)}(t)\frac{x^{2n}}{(2n)!}.$$

(a) Check formally that $u$ solves the heat equation.

(a) 形式地验证 $u$ 满足热方程。

(b) For $a > 0$ , consider the function defined by

$$g(t) = \begin{cases} e^{-t^{-a}} & \text{if } t > 0, \\ 0 & \text{if } t \leq 0. \end{cases}$$

(b) 对于 $a > 0$，考虑由下式定义的函数

$$g(t) = \begin{cases} e^{-t^{-a}} & \text{if } t > 0, \\ 0 & \text{if } t \leq 0. \end{cases}$$

One can show that there exists $0< \theta < 1$ depending on $a$ so that

$$|g^{(k)}(t)|\leq \frac{k!}{(\theta t)^k} e^{-\frac{1}{2} t^{-a}}\quad \mathrm{for} t > 0.$$

可以证明存在依赖于 $a$ 的 $0< \theta < 1$ 使得对 $t > 0$ 有

$$|g^{(k)}(t)|\leq \frac{k!}{(\theta t)^k} e^{-\frac{1}{2} t^{-a}}.$$

===== Page 189 =====

(c) As a result, for each $x$ and $t$ the series (19) converges; $u$ solves the heat equation; $u$ vanishes for $t = 0$ ; and $u$ satisfies the estimate $|u(x,t)|\leq Ce^{c|x|^{2a/(a - 1)}}$ for some constants $C,c > 0$ .

(c) 结果，对每个 $x$ 和 $t$，级数 (19) 收敛；$u$ 满足热方程；当 $t = 0$ 时 $u$ 消失；并且 $u$ 满足估计 $|u(x,t)|\leq Ce^{c|x|^{2a/(a - 1)}}$，其中 $C,c > 0$ 是常数。

(d) Conclude that for every $\epsilon >0$ there exists a non-zero solution to the heat equation which is continuous for $x\in \mathbb{R}$ and $t\geq 0$ , which satisfies $u(x,0) =$ 0 and $|u(x,t)|\leq Ce^{c|x|^{2 + \epsilon}}$ .

(d) 得出结论：对每个 $\epsilon >0$，存在一个非零的热方程解，该解对 $x\in \mathbb{R}$ 和 $t\geq 0$ 连续，满足 $u(x,0) = 0$ 和 $|u(x,t)|\leq Ce^{c|x|^{2 + \epsilon}}$。

5. \* The following "maximum principle" for solutions of the heat equation will be used in the next problem.

6. \* 热方程解的以下“最大值原理”将在下一个问题中使用。

Theorem. Suppose that $u(x,t)$ is a real- valued solution of the heat equation in the upper half- plane, which is continuous on its closure. Let $R$ denote the rectangle

$$R = \{(x,y)\in \mathbb{R}^{2}:a\leq x\leq b,0\leq t\leq c\}$$

定理。假设 $u(x,t)$ 是上半平面中热方程的实值解，在其闭包上连续。令 $R$ 表示矩形

$$R = \{(x,y)\in \mathbb{R}^{2}:a\leq x\leq b,0\leq t\leq c\}$$

and $\partial^{\prime}R$ be the part of the boundary of $R$ which consists of the two vertical sides and its base on the line $t = 0$ see Figure 3).Then

$$\min_{(x,t)\in \partial^{\prime}R}u(x,t) = \min_{(x,t)\in R}u(x,t)\qquad \mathrm{and}\qquad \max_{(x,t)\in \partial^{\prime}R}u(x,t) = \max_{(x,t)\in R}u(x,t).$$

且 $\partial^{\prime}R$ 是 $R$ 的边界的一部分，由两条垂直边和其在直线 $t = 0$ 上的底边组成（见图 3）。则

$$\min_{(x,t)\in \partial^{\prime}R}u(x,t) = \min_{(x,t)\in R}u(x,t)\qquad \mathrm{and}\qquad \max_{(x,t)\in \partial^{\prime}R}u(x,t) = \max_{(x,t)\in R}u(x,t).$$

<center>Figure 3. The rectangle $R$ and part of its boundary $\partial^{\prime}R$ </center>

<center>图 3. 矩形 $R$ 及其边界的一部分 $\partial^{\prime}R$</center>

The steps leading to a proof of this result are outlined below.

导致这一结果证明的步骤概述如下。

(a) Show that it suffices to prove that if $u\geq 0$ on $\partial^{\prime}R$ ,then $u\geq 0$ in $R$

(a) 证明只需证明：如果在 $\partial^{\prime}R$ 上 $u\geq 0$，则在 $R$ 中 $u\geq 0$。

(b) For $\epsilon >0$ ,let

$$v(x,t) = u(x,t) + \epsilon t.$$

(b) 对于 $\epsilon >0$，令

$$v(x,t) = u(x,t) + \epsilon t.$$

Then, $v$ has a minimum on $R$ ,say at $(x_{1},t_{1})$ .Show that $x_{1} = a$ or $b$ or else $t_1 = 0$ .To do so, suppose on the contrary that $a< x_{1}< b$ and $0< t_{1}\leq c$ ,and prove that $v_{xx}(x_{1},t_{1}) - v_{t}(x_{1},t_{1})\leq - \epsilon$ .However, show also that the left- hand side must be non- negative.

然后，$v$ 在 $R$ 上有一个最小值，比如说在 $(x_{1},t_{1})$ 处。证明 $x_{1} = a$ 或 $b$ 或者 $t_1 = 0$。为此，反设 $a< x_{1}< b$ 且 $0< t_{1}\leq c$，并证明 $v_{xx}(x_{1},t_{1}) - v_{t}(x_{1},t_{1})\leq - \epsilon$。然而，也要证明左边必须是非负的。

(c) Deduce from (b) that $u(x,t)\geq \epsilon (t_1 - t)$ for any $(x,t)\in R$ and let $\epsilon \rightarrow 0$

(c) 从 (b) 推导出对任何 $(x,t)\in R$ 有 $u(x,t)\geq \epsilon (t_1 - t)$，并令 $\epsilon \rightarrow 0$。

6. \* The examples in Problem 4 are optimal in the sense of the following uniqueness theorem due to Tychonoff.

7. \* 问题 4 中的例子在以下由 Tychonoff 提出的唯一性定理的意义上是最优的。

===== Page 190 =====

Theorem. Suppose $u(x,t)$ satisfies the following conditions:

(i) $u(x,t)$ solves the heat equation for all $x\in \mathbb{R}$ and and all $t > 0$

(ii) $u(x,t)$ is continuous for all $x\in \mathbb{R}$ and $0\leq t\leq c$

(iii) $u(x,0) = 0$

(iv) $|u(x,t)|\leq Me^{ax^2}$ for some $M$ , $a$ , and all $x\in \mathbb{R}$ , $0\leq t< c$

定理。假设 $u(x,t)$ 满足以下条件：

(i) $u(x,t)$ 对所有 $x\in \mathbb{R}$ 和所有 $t > 0$ 满足热方程

(ii) $u(x,t)$ 对所有 $x\in \mathbb{R}$ 和 $0\leq t\leq c$ 连续

(iii) $u(x,0) = 0$

(iv) 存在 $M$、$a$，使得对所有 $x\in \mathbb{R}$、$0\leq t< c$ 有 $|u(x,t)|\leq Me^{ax^2}$

Then $u$ is identically equal to 0.

则 $u$ 恒等于 0。

7. \* The Hermite functions $h_k(x)$ are defined by the generating identity

$$\sum_{k = 0}^{\infty}h_k(x)\frac{t^k}{k!} = e^{-(x^2 /2 - 2tx + t^2)}.$$

7. \* Hermite 函数 $h_k(x)$ 由生成恒等式定义

$$\sum_{k = 0}^{\infty}h_k(x)\frac{t^k}{k!} = e^{-(x^2 /2 - 2tx + t^2)}.$$

(a) Show that an alternate definition of the Hermite functions is given by the formula

$$h_k(x) = (-1)^k e^{x^2 /2}\left(\frac{d}{dx}\right)^k e^{-x^2}.$$

(a) 证明 Hermite 函数的另一个定义由公式给出

$$h_k(x) = (-1)^k e^{x^2 /2}\left(\frac{d}{dx}\right)^k e^{-x^2}.$$

[Hint: Write $e^{- (x^2 / 2 - 2tx + t^2)} = e^{x^2 /2}e^{- (x - t)^2}$ and use Taylor's formula.] Conclude from the above expression that each $h_k(x)$ is of the form $P_k(x)e^{- x^2 /2}$ , where $P_k$ is a polynomial of degree $k$ . In particular, the Hermite functions belong to the Schwartz space and $h_0(x) = e^{- x^2 /2}$ , $h_1(x) = 2xe^{- x^2 /2}$ .

[提示：写出 $e^{- (x^2 / 2 - 2tx + t^2)} = e^{x^2 /2}e^{- (x - t)^2}$ 并使用泰勒公式。] 从上述表达式得出结论：每个 $h_k(x)$ 形如 $P_k(x)e^{- x^2 /2}$，其中 $P_k$ 是 $k$ 次多项式。特别地，Hermite 函数属于施瓦茨空间，且 $h_0(x) = e^{- x^2 /2}$，$h_1(x) = 2xe^{- x^2 /2}$。

(b) Prove that the family $\{h_k\}_{k = 0}^{\infty}$ is complete in the sense that if $f$ is a Schwartz function, and

$$(f,h_k) = \int_{-\infty}^{\infty}f(x)h_k(x)dx = 0\quad \mathrm{for~all~}k\geq 0,$$

(b) 证明族 $\{h_k\}_{k = 0}^{\infty}$ 是完备的，即如果 $f$ 是施瓦茨函数，且对所有 $k\geq 0$ 有

$$(f,h_k) = \int_{-\infty}^{\infty}f(x)h_k(x)dx = 0,$$

then $f = 0$ . [Hint: Use Exercise 8. ]

则 $f = 0$。[提示：使用习题 8。]

(c) Define $h_k^*(x) = h_k((2\pi)^{1 / 2}x)$ . Then

$$\widehat{h_k^*}(\xi) = (-i)^k h_k^* (\xi).$$

(c) 定义 $h_k^*(x) = h_k((2\pi)^{1 / 2}x)$。则

$$\widehat{h_k^*}(\xi) = (-i)^k h_k^* (\xi).$$

Therefore, each $h_k^*$ is an eigenfunction for the Fourier transform.

因此，每个 $h_k^*$ 是傅里叶变换的特征函数。

(d) Show that $h_k$ is an eigenfunction for the operator defined in Exercise 23, and in fact, prove that

$$Lh_k = (2k + 1)h_k.$$

(d) 证明 $h_k$ 是习题 23 中定义的算子的特征函数，并且实际上证明

$$Lh_k = (2k + 1)h_k.$$

In particular, we conclude that the functions $h_k$ are mutually orthogonal for the $L^2$ inner product on the Schwartz space.

特别地，我们得出结论：函数 $h_k$ 对于施瓦茨空间上的 $L^2$ 内积是相互正交的。

(e) Finally, show that $\int_{-\infty}^{\infty}[h_k(x)]^2 dx = \pi^{1 / 2}2^k k!$ . [Hint: Square the generating relation.]

(e) 最后，证明 $\int_{-\infty}^{\infty}[h_k(x)]^2 dx = \pi^{1 / 2}2^k k!$。[提示：将生成关系平方。]

===== Page 191 =====

8.\* To refine the results in Chapter 4, and to prove that

$$f_{\alpha}(x) = \sum_{n = 0}^{\infty}2^{-n\alpha}e^{2\pi i2^{n}x}$$

8.\* 为了改进第 4 章的结果，并证明

$$f_{\alpha}(x) = \sum_{n = 0}^{\infty}2^{-n\alpha}e^{2\pi i2^{n}x}$$

is nowhere differentiable even in the case $\alpha = 1$ , we need to consider a variant of the delayed means $\Delta_{N}$ , which in turn will be analyzed by the Poisson summation formula.

即使在 $\alpha = 1$ 的情况下也无处可微，我们需要考虑延迟平均 $\Delta_{N}$ 的一个变体，这又将被泊松求和公式分析。

(a) Fix an indefinitely differentiable function $\Phi$ satisfying

$$\Phi(\xi) = \begin{cases} 1 & \text{if } |\xi| \leq 1/2, \\ 0 & \text{if } |\xi| \geq 1, \end{cases}$$

(a) 固定一个无限可微函数 $\Phi$ 满足

$$\Phi(\xi) = \begin{cases} 1 & \text{if } |\xi| \leq 1/2, \\ 0 & \text{if } |\xi| \geq 1, \end{cases}$$

and $0 \leq \Phi(\xi) \leq 1$ otherwise.

且在其他情况下 $0 \leq \Phi(\xi) \leq 1$。

By the Fourier inversion formula, there exists $\phi \in \mathcal{S}$ so that $\hat{\phi} (\xi) = \Phi (\xi)$ Let $\phi_{N}(x) = N\phi (Nx)$ so that $\hat{\phi_{N}} (\xi) = \Phi (\xi /N)$ . Finally, set

$$\tilde{\Delta}_{N}(x) = \sum_{n = -\infty}^{\infty}\phi_{N}(x + n).$$

由傅里叶反演公式，存在 $\phi \in \mathcal{S}$ 使得 $\hat{\phi} (\xi) = \Phi (\xi)$。令 $\phi_{N}(x) = N\phi (Nx)$，使得 $\hat{\phi_{N}} (\xi) = \Phi (\xi /N)$。最后，设

$$\tilde{\Delta}_{N}(x) = \sum_{n = -\infty}^{\infty}\phi_{N}(x + n).$$

Observe by the Poisson summation formula that $\tilde{\Delta}_{N}(x) = \sum_{n = -\infty}^{\infty}\Phi (n / N)e^{2\pi inx}$ , thus $\tilde{\Delta}_{N}$ is a trigonometric polynomial of degree $\leq 2N$ , with terms whose coefficients are 1 when $|n|\leq N$ . Let

$$\tilde{\Delta}_{N}(f) = f*\tilde{\Delta}_{N}.$$

通过泊松求和公式观察到 $\tilde{\Delta}_{N}(x) = \sum_{n = -\infty}^{\infty}\Phi (n / N)e^{2\pi inx}$，因此 $\tilde{\Delta}_{N}$ 是次数 $\leq 2N$ 的三角多项式，其项当 $|n|\leq N$ 时系数为 1。令

$$\tilde{\Delta}_{N}(f) = f*\tilde{\Delta}_{N}.$$

Note that

$$S_{N}(f_{\alpha}) = \tilde{\Delta}_{N}(f_{\alpha})$$

注意

$$S_{N}(f_{\alpha}) = \tilde{\Delta}_{N}(f_{\alpha})$$

where $N^{\prime}$ is the largest integer of the form $2^{k}$ with $N^{\prime}\leq N$

其中 $N^{\prime}$ 是形如 $2^{k}$ 且 $N^{\prime}\leq N$ 的最大整数。

(b) If we set $\tilde{\Delta}_{N}(x) = \phi_{N}(x) + E_{N}(x)$ where

$$E_{N}(x) = \sum_{|n|\geq 1}\phi_{N}(x + n),$$

(b) 如果我们设 $\tilde{\Delta}_{N}(x) = \phi_{N}(x) + E_{N}(x)$，其中

$$E_{N}(x) = \sum_{|n|\geq 1}\phi_{N}(x + n),$$

then one sees that:

$$\sup_{|x|\leq 1 / 2}|E_{N}^{\prime}(x)|\to 0\mathrm{~as~}N\to \infty .$$

则人们看到：

$$\sup_{|x|\leq 1 / 2}|E_{N}^{\prime}(x)|\to 0\mathrm{~as~}N\to \infty .$$

$$|\tilde{\Delta}_{N}^{\prime}(x)|\leq cN^{2}.$$

$$|\tilde{\Delta}_{N}^{\prime}(x)|\leq c / (N|x|^{3}),\mathrm{~for~}|x|\leq 1 / 2.$$

$$|\tilde{\Delta}_{N}^{\prime}(x)|\leq cN^{2}.$$

$$|\tilde{\Delta}_{N}^{\prime}(x)|\leq c / (N|x|^{3}),\mathrm{~for~}|x|\leq 1 / 2.$$

Moreover, $\int_{|x|\leq 1 / 2}\tilde{\Delta}_{N}^{\prime}(x)dx = 0$ , and $-\int_{|x|\leq 1 / 2}x\tilde{\Delta}_{N}^{\prime}(x)dx\to 1$ as $N\to$ $\infty$

此外，$\int_{|x|\leq 1 / 2}\tilde{\Delta}_{N}^{\prime}(x)dx = 0$，且当 $N\to \infty$ 时 $-\int_{|x|\leq 1 / 2}x\tilde{\Delta}_{N}^{\prime}(x)dx\to 1$。

(c) The above estimates imply that if $f^{\prime}(x_{0})$ exists, then

$$(f*\tilde{\Delta}_{N}^{\prime})(x_{0} + h_{N})\to f^{\prime}(x_{0})\quad \mathrm{as}N\to \infty ,$$

(c) 上述估计表明，如果 $f^{\prime}(x_{0})$ 存在，则当 $N\to \infty$ 时

$$(f*\tilde{\Delta}_{N}^{\prime})(x_{0} + h_{N})\to f^{\prime}(x_{0}),$$

whenever $|h_{N}|\leq C / N$ . Then, conclude that both the real and imaginary parts of $f_{1}$ are nowhere differentiable, as in the proof given in Section 3, Chapter 4.

只要 $|h_{N}|\leq C / N$。然后，得出结论：$f_{1}$ 的实部和虚部都无处可微，如第 4 章第 3 节给出的证明所述。