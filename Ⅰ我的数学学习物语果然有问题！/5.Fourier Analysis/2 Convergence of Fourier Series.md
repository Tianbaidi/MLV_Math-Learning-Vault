---
tags:
  - Fourier_Analysis
---
> 咕咕咕完了，这里重新开始写东西。我们已经了解了傅里叶级数的由来，在第二章接触了很多计算和新的概念，我们第三章虽然研究的是傅里叶级数的收敛性。但是我们还是会了解一些比较新鲜的东西。（哦，伟大的希尔伯特空间）

# Mean-square convergence of Forier Series


> [!NOTE] 主线
> 本章的主线在于证明以下这个定理
> **Theorem.1** 设 $f$ 是定义在圆上的可积函数，有 
> $$\frac{1}{2\pi}\int_{0}^{2\pi}|f(\theta)-S_{N}(f)(\theta)|^2d\theta \to 0\quad N\to \infty$$
> 总之看到这里，我有个疑问：为什么这里要有一个平方？我们能否在后面回答这个问题？

在此之前，我们来学高等🦘

## Vector space and inner products

> 我突然很不喜欢 stein 的书了，这里他写得很敷衍，我感觉这一章节直接加个 #Algebra  的 tag 我用来写袋鼠好了

向量空间（或者可以称为线性空间）我这里希望用我的方式来讲这个内容，但是stein的东西不会少。

### Fields 
对于层层的代数解构来看，域必定是非常严格的。对于很多运算封闭（+，-，$\times$ , / ,1）
> [!NOTE] 常见数域
> 有理数域 $\mathbb{Q}$-<font color="#c00000">最小数域</font>
> 实数域 $\mathbb{R}$
> 复数域 $\mathbb{C}$ -<font color="#c00000">最大数域</font>

在丘维声的高等代数教材中，他的定义相对精简：
复数集的一个非空子集 $\mathbb{K}$ ,如果满足：
    $(1)\ \ 0，1 \in \mathbb{K}$
    $(2)\ \ a,b \in \mathbb{K} \ \ \ \Rightarrow a+b,ab \in \mathbb{K}$
    $(3)\ \ a,b \in \mathbb{K} \ ,且b \not = 0\ \ \ \Rightarrow \frac{a}{b},\  a-b\in \mathbb{K}$
    则称 $\mathbb{K}$ 为一个数域
如果这三点展开，便是封闭、逆元、单位一

如果我们用笛卡尔积来表示，那就是 
$$F\times F\to^{+,\times} F$$
另外我们需要有一个加法交换群 $V$ ：$V\times V\to V$

向量空间特殊在我们能定义一个数乘运算： $F\times V\to V$    $(k,a)\mapsto ka$
我们选取元素 $X,Y,Z\in V$ 根据数乘运算和 $V$ 本身的定义（$\lambda\in F$） , 我们有以下非常显然的性质：
1. $X+Y=Y+X$ 
2. $X+(Y+Z)=(X+Y)+Z$
3. $\lambda_{1}(\lambda_{2} X)=\lambda_{1}\lambda_{2}X$
4. $\lambda(X+Y)=\lambda X+\lambda Y$
这里的我们一定要清楚 $X,Y$ 是 $V$ 中的元素，他们可以是任何神奇的形式，对于 so called 向量空间来看，我们的代表元素就是向量了

我们这里要介绍的运算叫做 **内积** ( inner product ) 

对于一个坐标，我们的点积是如何处理的？$A \cdot B=(a,b)\cdot(c,d)=ab+cd=\cos\langle {A,B} \rangle |A||B|$ 其实我们向量空间的内积也是类似 . 

**Definition.1** 我们将向量空间上的内积用 $(A,B)$ 表示，并且实数域 $\mathbb{R}$ 上内积既具有以下性质：

1. **对称** (Symmetric) : 或者我们称为可交换 $(X,Y)=(Y,X)$
2. **线性性** (Linear) : $(\alpha X+\beta Y,Z)=\alpha(X,Z)+\beta(Y,Z)$ 
3. **正定** (Positive-defind) : 有 $(X,X)\geq 0$ , 同时隐含着 $(X,X)=0$ 当且仅当 $X$ 为零

**Definition.1.1** 由于正定的性质，我们再度定义 $X$ 的**范数** ( norm ) 为 
$$||X||=(X,X)^{1/2}$$

我们以空间 $\mathbb{R}^d$ 为例，我们的内积为 
$$(X,Y)=x_{1}y_{1}+\cdots+x_{d}y_{d}$$
$X$ 的范数为 
$$||X||=(X,X)^{1/2}=\sqrt{ x_{1}^2+\cdots+x_{d}^2 }$$
> 这也被称为欧几里得距离 (Euclidean distance) ，范数也可以只用一个 $|X|$ 来表示

当我们将数域扩展到复数域 $\mathbb{C}$ 会是一种什么状况呢？

我们两个元素的内积也为复数，我们会有以下性质：

1. $(X,Y)=\overline{(Y,X)}$
2. **有共轭的线性性** ( Conjugate-linear ) : $(\alpha X+\beta Y,Z)=\alpha(X,Z)+\beta(Y,Z)$ and $(X,\alpha Y+\beta Z)=\overline{\alpha}(X,Y)+\overline{\beta}(X,Z)$ 

此外，这些内积被称为埃尔米特内积，我们会发现他**不符合**此前定义出来的**对称性** 

对于范数，我們的要求不會改變！必须有 $(X,X)\geq 0$，并且 $X$ 的范数仍然定义为 $\| X\| = (X,X)^{1 / 2}$。同样，如果 $\| X\| = 0$ 蕴含 $X = 0$，则内积是严格正定的。

$\mathbb{C}^{d}$ 中两个向量 $Z = (z_{1},\ldots ,z_{d})$ 和 $W = (w_{1},\ldots ,w_{d})$ 的内积定义为

$$(Z,W) = z_{1}\overline{w_{1}} +\dots +z_{d}\overline{w_{d}}.$$
向量 $Z$ 的范数为
$$\| Z\| = (Z,Z)^{1 / 2} = \sqrt{|z_1|^2 + \dots + |z_d|^2}.$$
![[Pasted image 20260402223646.png]]

**Definition.2** 我们定义 **正交性** 表示两个元素的内积有 $(A,B)=0$ 在几何直观上为两个向量垂直。我们可以写成 $A\perp B$ . 对此，我们有以下性质
1. The Pythagorean Theorem : 如果 $X$ 和 $Y$ 是正交的 
$$||X+Y||^{2}=||X||^{2}+||Y||^{2}$$
2. The Cauchy-Schwarz Inequality : 对任意 $X,Y \in V$ 我们有 
$$|(A,B)|\leq ||X||\cdot ||Y||$$
3. The Triangle Inequaloty : 对任意 $X.Y\in V$ 我们有 
$$||X+Y||\leq ||X||+||Y||$$
**proof .**  我们