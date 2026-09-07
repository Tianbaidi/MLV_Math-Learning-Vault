---
tags:
  - Analysis
  - Functional_Analysis
  - Lyapunov_Schmidt
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §4。Lyapunov–Schmidt 约化把**无穷维**的约束方程(极小,且 $S$、$f_3$ 为空间常数)投影到 Jacobi 核 $K$ 这个**有限维**子空间上,得到有限个变量的障碍映射 $\kappa$,再对 $Z$ 做实解析处理。

> 相关笔记:[[Fredholm_Operator]]、[[Real_Analytic_and_Subanalytic_Sets]]、[[Path_Rigidity_of_S]]、[[Hölder_Space_and_Elliptic_Regularity]]。

## 目标:把无穷维方程压到有限维

设 $H(u)=0$ 刻画"$F_u$ 是极小"($H$ 是平均曲率算子),同时要管住 $S$ 与 $f_3$ 的空间常数性。$H$ 在 $u=0$ 处实解析,线性化是

$$ DH(0)=L=\Delta+n+S. $$

用 [[Fredholm_Operator]] 的分解,把 $u$ 拆成 $u=z+w$,其中 $z\in K=\ker L$(有限维)、$w\in X$( $K$ 的 $L^2$ 正交补):

> [!TIP] 分解
> $$ C^{k,α}(M)=K\oplus X. $$
> 给定"Jacobi 核方向" $z$,【极小】这个约束将唯一确定正交补部分 $w$。

## 解析隐函数定理给出 $\Psi$

记 $P$ 为到 $K$ 的投影,$Q=I-P$ 为到 $X$ 的投影。由于 $L:X\to Y$ 是双射(见 [[Fredholm_Operator]])且 $H$ 实解析,**解析隐函数定理**给出:存在 $0$ 的邻域 $U_K\subset K$、$U_X\subset X$ 及实解析映射

$$ \Psi:U_K\to U_X,\qquad \Psi(0)=0,\quad D\Psi(0)=0, $$

使得

$$ QH(z+w)=0\ \iff\ w=\Psi(z), $$

只要 $z+w$ 足够小。即在给定的 $z$ 下,极小性唯一解出 $w$。

## 有限维障碍映射 $\kappa$

> [!ABSTRACT] Definition(障碍映射)
> $$ \kappa:U_K\to K,\qquad \kappa(z)=P\,H\bigl(z+\Psi(z)\bigr). $$
> 由构造,$\kappa(z)=0$ **当且仅当**对应的小极小图 $F_{u(z)}$ 存在。于是"极小超曲面族"局部编码为有限维实解析集合
> $$ Z_0=\{z\in U_K:\kappa(z)=0\}. $$

再把常数性约束写成 $V_S(u)=0$、$V_3(u)=0$,其中

$$ V_S(u)=\int_M\bigl(S_u-\overline S(u)\bigr)^2\,d\mu_u,\qquad V_3(u)=\int_M\bigl(f_{3,u}-\overline{f_3}(u)\bigr)^2\,d\mu_u, $$

$\overline S(u)$、$\overline{f_3}(u)$ 分别是 $S_u$、$f_{3,u}$ 的 $d\mu_u$-平均。于是完整约束集为

$$ Z=\bigl\{z\in U_K:\kappa(z)=0,\ V_S(u(z))=0,\ V_3(u(z))=0\bigr\}. $$

## 为什么要这一步

> [!NOTE] 关键作用
> 没有约化,我们面对的是无限维空间上的约束方程;约化后 $Z$ 是**有限维实解析集**。论文 §4 正是对 $Z$ 使用 [[Real_Analytic_and_Subanalytic_Sets]] 里的 Hironaka 曲线选择引理,把"S 的取值若有聚点"化为一条**实解析路径**,再用 §3 的 [[Path_Rigidity_of_S]] 得出矛盾。

> [!NOTE] 本节关系
> $$ \boxed{L\text{ 双射于 }X\to Y}\ \Longrightarrow\ \boxed{\exists\,\Psi:U_K\to U_X}\ \Longrightarrow\ \boxed{\kappa(z)=P\,H(z+\Psi(z))}\ \Longrightarrow\ \boxed{\text{有限维实解析集 }Z}. $$
