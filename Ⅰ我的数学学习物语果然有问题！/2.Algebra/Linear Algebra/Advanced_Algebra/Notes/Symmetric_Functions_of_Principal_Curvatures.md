---
tags:
  - Linear_Algebra
  - Symmetric_Function
  - Spectrum
---

> 论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 通篇用
> $$ S=\operatorname{tr}(A^2),\qquad f_3=\operatorname{tr}(A^3),\qquad H=\operatorname{tr}A, $$
> 其中 $A$ 是形状算子。这篇整理"主曲率的对称函数"所需的线性代数:为什么这些迹量只看主曲率这个**无序集合**、如何用幂和与初等对称函数互相表达,以及 $S$ 的几何含义。

> 相关笔记:[[Shape_Operator_Invariants]]、[[Hypersurface_in_Sphere]]。

## 自伴算子的谱分解

> [!ABSTRACT] Definition(形状算子与主曲率)
> 设 $A:T_p\Sigma\to T_p\Sigma$ 是对诱导度量 $g$ 自伴的线性算子(超曲面的形状算子满足 $\langle AX,Y\rangle=\langle X,AY\rangle$,见 [[Shape_Operator_Invariants]])。由谱定理,$A$ 可正交对角化,其特征值 $\lambda_1,\dots,\lambda_n$( **主曲率** )皆为实数,存在单位正交基 $\{e_i\}$ 使 $Ae_i=\lambda_ie_i$。

## 幂和(迹)作为对称函数

> [!NOTE] 为什么"迹"只看主曲率的无序集合
> $$ \operatorname{tr}A=\sum_i\lambda_i,\quad \operatorname{tr}A^2=\sum_i\lambda_i^2,\quad \operatorname{tr}A^3=\sum_i\lambda_i^3. $$
> 这些量对主曲率的**排列不变**、对特征向量的选取无关,因此只依赖于 $A$ 的谱——是主曲率的 **对称函数**。这正是论文把它们当作超曲面的"内蕴不变量"的理由。

## 幂和与初等对称函数(牛顿恒等式)

记 $p_k=\sum_i\lambda_i^k$(幂和),$e_k=\sum_{i_1<\cdots<i_k}\lambda_{i_1}\cdots\lambda_{i_k}$(初等对称函数,特征多项式系数)。

> [!Success] Theorem(牛顿恒等式)
> $$ ke_k=\sum_{i=1}^{k}(-1)^{i-1}e_{k-i}\,p_i,\qquad k=1,\dots,n. $$
> 例如
> $$ p_1=e_1,\qquad p_2=e_1p_1-2e_2,\qquad p_3=e_2p_1-e_1p_2+3e_3. $$
> 所以给定的 $p_1,p_2,p_3$(即 $H,S,f_3$)可反解出 $e_1,e_2,e_3$,也就是主曲率的全套低阶对称信息。这解释了为何"形状算子的迹量"这一族是自然的分类不变量。

## $S$ 的几何含义:形状算子长度平方

> [!TIP] $S=|A|^2$
> 采用内积 $\langle A,B\rangle=\operatorname{tr}(A^\top B)$,有
> $$ S=\operatorname{tr}(A^2)=|A|^2=\sum_{i=1}^n\lambda_i^2. $$
> 论文里 $S$ 与"常数标量曲率"等价(经 Gauss 方程 $R=n(n−1)−S$ 当 $H=0$),见 [[Gauss_Equation_Hypersurface]]。于是"极小 + 常数 $S$"就是"主曲率平方和恒定"。

> [!WARNING] $H$ 的约定
> 本文与论文都采用**未归一化** $H=\operatorname{tr}A=\sum_i\lambda_i$。若别的书用归一化 $H=\frac1n\operatorname{tr}A$,它们相差因子 $\tfrac1n$。读论文时务必用未归一化版本(见 [[Hypersurface_in_Sphere]] 的约定声明)。

> [!NOTE] 本节关系
> $$ \boxed{A\text{ 自伴}\Rightarrow\text{ 实谱 }\lambda_i}\ \Longrightarrow\ \boxed{p_k=\operatorname{tr}A^k}\ \xleftrightarrow{\text{牛顿恒等式}}\ \boxed{e_k}\ \Longrightarrow\ \boxed{S=\sum\lambda_i^2,\ f_3=\sum\lambda_i^3}. $$
