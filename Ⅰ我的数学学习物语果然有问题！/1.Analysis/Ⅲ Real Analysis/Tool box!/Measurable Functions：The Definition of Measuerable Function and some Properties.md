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

第一条就涉及我们此前提到的关于广义实值函数下的的验证问题，对于 **2.** 我们知道 $\Phi$ 是连续函数，则 $\Phi^{-1}((-\infty,a))$ 必然为开集，记为 $\mathcal{O}$ ,因此，我们有 $(\Phi \circ f)^{-1}((-\infty,a))=f^{-1}(\mathcal{O})$ 是可测的

	这里我们不能随意调整连续和可测的条件！

对于 **3.** 我们要注意到一个观察 $\{ \sup_{n }f_{n}>a \}=\bigcup_{n}\{ f_{n}>a \}$ 我们又有 $\inf_{n} f_{n}(x)=-\sup_{n}(-f_{n}(x))$ . 有 $\limsup_{ n \to \infty } f_{n}(x)=\inf_{k} \{ \sup_{n>k} f_{n} \}$ 和 $\liminf_{ n \to \infty } f_{n}(x)=\sup_{k} \{ \inf_{n>k} f_{n} \}$ .

对于 **4.** 我们可以从 **3.** 推得。**5.** 我们先讨论 **1** ，若 $k$ 是奇数，有 $\{ f^k >a\}=\left\{  f> \frac{1}{a^k}  \right\}$ 若 $k$ 是偶的，则有 $\{ f^k >a\}=\left\{  f> \frac{1}{a^k}  \right\}\cap \left\{  f<- \frac{1}{a^k}  \right\}$ . 对 **2.** 我们有 $f+g$ 是可测的，由于 
$$\{ f+g>a \}=\bigcup_{r\in \mathbb{Q}}\{ f>a-r \}\cap \{ g>r \}$$
这里的 $\mathbb{Q}$ 是有理数。随后，我们解决 $fg$ 是可测的问题 , 注意到 
$$fg= \frac{1}{4}[(f+g)^{2}-(f-g)^{2}]$$
可测是显然的。对于定义在 $E$ 上的函数满足 $f(x)\neq g(x)$ 的 $x$ 构成的集合测度为 $0$ ，我们就称 $f(x)=g(x)\quad \text{a.e}\quad x\in E$  a.e : Almost everywhere
至此，对于此前的讨论，我们可以将处处要求减弱，要求几乎处处即可

其总结即为 **6** 。