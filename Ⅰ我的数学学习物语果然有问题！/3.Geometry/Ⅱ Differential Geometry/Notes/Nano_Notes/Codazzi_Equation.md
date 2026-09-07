---
tags:
  - Geometry
  - Differential_Geometry
  - Codazzi_Equation
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §2–§3。论文用**收缩的 Codazzi 方程** $\mathrm{div}\,A=\nabla H$(极小超曲面下 $\mathrm{div}\,A=0$),在 §3 证明
> $$ \int_M\langle A,\nabla^2\phi\rangle\,d\mu=-\int_M\langle\mathrm{div}A,\nabla\phi\rangle\,d\mu=0, $$
> 这是路径刚性的关键一步。

> 相关笔记:[[Shape_Operator_Invariants]]、[[Gauss_Equation_Hypersurface]]、[[Jacobi_Operator_Minimal_Hypersurface]]。

## Codazzi 方程

> [!ABSTRACT] Theorem(Codazzi equation)
> 对超曲面 $\Sigma\subset S^{n+1}$,在局部正交标架 $\{e_i\}$ 下,第二基本形式的重协变导数满足
> $$ h_{ijk}=h_{ikj}, $$
> 即 $\nabla h$ 在**最后两个指标**上对称。(在平直环境/Ric=0 的情形它是"余维 1 + A 自伴 + 联络无挠"的结论。)

> [!Success] Theorem(收缩形式)
> 对超曲面,收缩 Codazzi 方程给出
> $$ \mathrm{div}\,A=\nabla H,\qquad H=\mathrm{tr}\,A. $$
> 特别地,当 $\Sigma$ **极小**($H=0$)时
> $$ \mathrm{div}\,A=0. $$
>
> 要点:单位球面是 Einstein($\mathrm{Ric}=ng$),故 $\mathrm{Ric}(\nu,X)=0$,收缩 Codazzi 只剩散度项,即得上式。

## 论文里的用法(§3, Eq. 9)

> [!NOTE] 关键积分
> 记 $\langle A,\nabla^2\phi\rangle=\sum_{i,j}h_{ij}\phi_{ij}$。由收缩 Codazzi + 极小性,分部积分得
> $$ \int_M\langle A,\nabla^2\phi\rangle\,d\mu=-\int_M\langle\mathrm{div}A,\nabla\phi\rangle\,d\mu=0. $$
> 这一项正是 $S'$ 变分(见 [[Path_Rigidity_of_S]])里想消掉的项。

> [!WARNING] 为什么需要"极小"
> 若 $H\ne0$,则 $\mathrm{div}A=\nabla H$ 一般非零,上面积分不会自动消失。**极小性是论文论证的硬前提之一**。

> [!NOTE] 本节关系
> $$ \boxed{h_{ijk}=h_{ikj}}\ \xrightarrow{\ \text{Einstein }(\mathrm{Ric}=ng)\ }\ \boxed{\mathrm{div}\,A=\nabla H}\ \xrightarrow{\ H=0\ }\ \boxed{\mathrm{div}\,A=0}\ \Longrightarrow\ \boxed{\int\langle A,\nabla^2\phi\rangle\,d\mu=0}. $$
