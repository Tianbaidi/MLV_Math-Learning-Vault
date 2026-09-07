---
tags:
  - Geometry
  - Differential_Geometry
  - Gauss_Equation
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §1–§2。论文反复用 Gauss 方程把 $S$ 与标量曲率挂钩:极小超曲面下 $R=n(n-1)-S$,于是 **"常数标量曲率 ⟺ 常数 $S$"**,这正是 Chern 猜想的表述。

> 相关笔记:[[Hypersurface_in_Sphere]]、[[Shape_Operator_Invariants]]、[[Codazzi_Equation]]。

## Gauss 方程(单位球面 $S^{n+1}$)

> [!ABSTRACT] Theorem(Gauss equation)
> 对 $X,Y,Z,W\in T\Sigma$,
> $$ R^{\Sigma}(X,Y,Z,W)=\bigl(\langle X,Z\rangle\langle Y,W\rangle-\langle X,W\rangle\langle Y,Z\rangle\bigr)+\bigl(h(X,Z)h(Y,W)-h(X,W)h(Y,Z)\bigr). $$
> 第一项来自环境球面截面曲率 $=1$,第二项来自嵌入 $\Sigma\subset S^{n+1}$(即 [[Hypersurface_in_Sphere]] 的 Gauss 公式中 $h$ 项)。

> [!NOTE] 主方向下的截面曲率
> 若 $e_i,e_j$ 是正交主方向($h(e_i,e_j)=0$ 当 $i\ne j$),取 $X=Z=e_i$、$Y=W=e_j$ 得
> $$ K(e_i,e_j)=1+\lambda_i\lambda_j. $$

## 标量曲率

> [!TIP] 标量曲率公式
> $$ R=n(n-1)+H^2-S,\qquad H=\mathrm{tr}A,\ S=\mathrm{tr}(A^2). $$
> 推导:$R=\sum_{i\ne j}K(e_i,e_j)=\sum_{i\ne j}(1+\lambda_i\lambda_j)=n(n-1)+\bigl((\textstyle\sum_i\lambda_i)^2-\sum_i\lambda_i^2\bigr)=n(n-1)+H^2-S$。
> 当 $\Sigma$ 极小($H=0$)时
> $$ R=n(n-1)-S. $$

> [!WARNING] 归一化约定提醒
> 若用 do Carmo 归一化 $H=\frac1n\mathrm{tr}A$,公式变为 $R=n(n-1)+n^2H^2-S$。本笔记与论文坚持**未归一化** $H=\mathrm{tr}A$,故为 $R=n(n-1)+H^2-S$。

## 关键推论:常数标量曲率 ⟺ 常数 $S$

> [!Danger] Corollary
> 对**极小**超曲面,$R=n(n-1)-S$ 为常数当且仅当 $S$ 为常数。因此 Chern 猜想的两种说法——"(常数标量曲率 + 极小)的 $S$ 值离散" 与 "(常数 $S$ + 极小)的 $S$ 值离散"——等价。

> [!NOTE] 本节关系
> $$ \boxed{R^{\Sigma}=\bar R+h\cdot h}\ \Longrightarrow\ \boxed{K_{ij}=1+\lambda_i\lambda_j}\ \Longrightarrow\ \boxed{R=n(n-1)+H^2-S}\ \xrightarrow{\ H=0\ }\ \boxed{R=n(n-1)-S}. $$
