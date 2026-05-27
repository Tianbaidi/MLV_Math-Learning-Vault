---
tags:
  - Measure_Theorem
  - Real_analysis
---
> 自我们的测度，可测以及对可测集的定义之后，我们开始学习可测函数. 这一章节要知道的是可测函数的定义性质 (i) . 对 Simple Function 以及 Step Function 的逼近 (ii) . 以及最后的 Littlewood's Three Principles (iii) .在这些过程中，我们会接触到相关的证明工具。这一部分为 (i) 我们先进入定义和性质。

> [!ABSTRACT] Definition
> 设 $E$ 是 $\mathbb{R}^d$ 上的可测集，定义在 $E$ 上的函数被称为可测或者 **勒贝格可测** 的。即，对于实数域上的 $a$ 我们的集合满足 
> $$f^{-1}([-\infty,a))=\{ x\in E : f(x)<a \}$$ 
> 我们就称其是可测的，其中我们记 $E_{a}=\{ x \in E : f(x)<a \}$ .

此处我们要引入引理，对函数进行分类

> [!Success] Lemma
> - Extended Real Number
>  $$-\infty\leq x\leq+\infty$$
> - Finite-valued 
> $$-\infty<x<+\infty$$

	在可测函数的定义下，如果我们是取广义实值函数我们还需要证明 $f^{-1}(\infty)$ 是可测的。pp1
在这个定义下，不难发现，我们的符号其实的自由的 $a\geq>,x,< \leq a$ 这些都是可以的。等号互推的方法是
   $< \to \leq$ :
   $$\{ f\leq a \}=\bigcap_{k=1}^{\infty}\left\{  f\leq a-\frac{1}{k}  \right\}$$
   $\leq \to <$ : 
  $$\{ f<a \}=\bigcup_{k=1}^{\infty}\left\{  f<a-\frac{1}{k}  \right\}$$
对于取相反的符号，我们可以取其补集 $E_{a}^c$

对于可测函数，我们有以下性质：

> [!TIP] Proposition
> 1. 有限值函数 $f$ 是可测的当且仅当 $f^{-1}(\mathcal{O})$ 对任意开集 $\mathcal{O}$ 可测，再当且仅当 $f^{-1}(F)$ 对任意闭集 $F$ 可测
> 2. 若 $f$ 是 $\mathbb{R}^d$ 上的连续函数，那么 $f$ 是可测的。若 $f$ 是可测的且是有限值函数，$\Phi$ 是连续函数，那么 $\Phi \circ f$ 是可测的
> 3. 设 $\{ f_{n} \}_{n=1}^{\infty}$ 是一系列可测函数 . 有 
> $$\sup_{n}f_{n}(x),\quad \inf_{n}f_{n}(x),\quad \\lim_{ n \to \infty } \sup f_{n}(x) \  \text{~and~} \ \\lim_{ n \to \infty } \inf f_{n}(x)$$
> 是可测的
> 4. 若 $\{ f_{n} \}_{n=1}^{\infty}$ 是一系类可测函数，有 
> $$\lim_{ n \to \infty } f_{n}(x)=f(x)$$
> 这里 $f$ 是可测的
> 5. 若 $f$ 和 $g$ 都是可测的，那么有
> 	1. 整数次幂 $f^{k}$ , $k>1$ 也是可测的
> 	2. $f+g$ 以及 $fg$ 都是可测的若两函数是有限值函数
> 6. 设 $f$ 是 可测的，那么 $f(x)=g(x)$ a.e(几乎处处)$x$ ,于是 $g$ 也是可测的




