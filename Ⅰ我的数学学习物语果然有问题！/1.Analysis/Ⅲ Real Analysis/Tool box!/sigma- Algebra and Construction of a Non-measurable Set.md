---
tags:
  - Real_analysis
  - Measure_Theorem
  - Set_Theory
  - Axiom_of_Choice
---
$\sigma$-代数是一个在结构上完备的子集系统，它为定义一个满足可列可加性的测度提供了必需且稳定的定义域，使得整个系统在标准的集合论运算下绝不越界。表示 $\mathbb{R}^d$ 的一个子集族，它在可列并、可列交以及补集运算下是封闭的。

**Borel $\sigma$-代数**，记作 $\mathcal{B}_{\mathbb{R}^d}$。根据定义，它是**包含所有开集的最小的 $\sigma$-代数**。这个 $\sigma$-代数中的元素被称为 **Borel 集** 。由于开集是可测的，我们得以断定：Borel $\sigma$-代数包含在可测集组成的 $\sigma$-代数之中。

从 Borel 集的角度来看，勒贝格可测集是通过对 Borel $\sigma$-代数进行完备化（completion）而产生的，也就是说，通过将 Borel 集里所有测度为零的子集添加进去。这是下面推论的直接推论。

从开集和闭集（它们是最简单的 Borel 集）开始，我们可以尝试按照复杂程度的顺序来列出 Borel 集。接下来按顺序排列的将是**开集的可列交集**；这样的集合被称为 **$G_\delta$ 集**。或者，我们也可以考虑它们的补集，即**闭集的可列并集**，被称为 **$F_\sigma$ 集**。

> [!Danger] Corollary
> $\mathbb{R}^d$ 的子集 $E$ 是可测的，当且仅当
> - $E$ 与某个 $G_{\delta}$ 集相差一个测度为 $0$ 的集合
> - $E$ 与某个 $F_{\delta}$ 集相差一个测度为 $0$ 的集合

这个推论一旦成立一个，由于 $F_{\sigma}$ , $G_{\sigma}$ , $m(o)=0$ 都是可测的，即 $E$ 是可测的。
反之，若 $E$ 是可测的，我们可以选择一个包含 $E$ 的开集，使得 $E \subset\mathcal{O}_{n}$ 且 $m(\mathcal{O}_{n}-E)< \frac{1}{n}$ . 我们令 $S=\bigcap_{n=1}^{\infty}$ 为包含 $E$ 的 $G_{\delta}$ 集，对所有的 $n$ ,我们都有 $(S-E)\subset(\mathcal{O}_{n}-E)$ ，对于所有的 $m(S-E)< \frac{1}{n}$ 故 $S-E$ 的外测度为 $0$ ,因此可测。如果我们讨论 $F_{\sigma}$ 可以利用 [[Lebesgue Measure and Measurable Sets#Properties of Sequences of Measurable Sets and Approximation Theorems]] 最后一个定理的 ii 部分利用 $\varepsilon=\frac{1}{n}$ 对得到的闭集取并即可 。

### Consruction of a Non-measurable Set
对不可测集 $\mathcal{N}$ 的构造我们用到 [[A-C]] 选择公理 . 从 $[0,1]$ 区间内实数间的一个简单等价关系 $x-y$ 来看：
若 $x-y$ 是有理数，我们称 $x\sim y$ .作为等价关系我们满足自反性，对称性，传递性 。这里对于任意两个等价关系，我们要么不交要么重合。 $[0,1]$ 是所有等价类的无并交，我们记为 
$$[0,1]=\bigcup_{\alpha} \mathcal{E}_{\alpha}$$
我们从每个等价类中恰好选取一个元素 $x_{\alpha}$ ,令其构成 $\{ x_{\alpha} \}=\mathcal{N}$ ，我们现在要知道其是否可测。

> [!NOTE] Theorem
> 集和 $\mathcal{N}$ 是不可测的

如果我们考虑反证法，我们假设 $\mathcal{N}$ 是可测的，令 $\{ r_{k} \}_{k=1}^{\infty}$ 是 $[-1,1]$ 中有理数的枚举,我们考虑平移 
$$\mathcal{N_{k}}=\mathcal{N}+r_{k}$$
我们声明 $\mathcal{N}_{k}$ 是无交的，且 
$$[0,1]\subset \bigcup_{k=1}^{\infty} \mathcal{N}_{k}\subset[-1,2]$$
我们设 $\mathcal{N}_{k} \cap \mathcal{N}_{k'}$ 是非空的，则存在 $r_{k}\neq r_{k'}$ 且 $\alpha$ 和 $\beta$ 满足 $x_{\alpha}+r_{k}=x_{\beta}+r_{k'}$ 因此 
$$x_{\alpha}-x_{\beta}=r_{k'}-r_{k}$$
