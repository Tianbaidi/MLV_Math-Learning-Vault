---
tags:
  - Geometry
  - Differential_Geometry
  - Path_Rigidity
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §3(Prop 3.1)与 Remark 3.3。这是全文的"**路径刚性**"——它对 §4 的解析论证和 §6 的组合起着关键作用。

> 相关笔记:[[Jacobi_Operator_Minimal_Hypersurface]]、[[Codazzi_Equation]]、[[Fredholm_Operator]]、[[Lyapunov_Schmidt_Reduction]]。

## 命题陈述(Prop 3.1)

> [!ABSTRACT] Theorem(路径刚性; Path rigidity)
> 设 $I\subset\mathbb R$ 为区间,$t\mapsto F_t$ 是从 $I$ 到 $C^{3}(M,S^{n+1}(1))$ 的 $C^1$ 映射(把 $F_t$ 视为 $\mathbb R^{n+2}$ 值映射)。设每个 $F_t$ 是 **two-sided 极小浸入**,且 $S_t$ 与 $f_{3,t}$ 都是空间常数。则
> $$ t\mapsto S_t\ \text{ 在 }I\text{ 上为常数}. $$
> 即"约束族上的 $S$ 值不漂移"。

## 证明要点(§3)

> [!NOTE] 推导链条
> 写 $\partial_tF_t=dF_t(V)+\phi\nu=:W+\phi\nu$,$\phi$ 为法向速度($V$ 为切向分量,只改参数化,由 Remark 2.2 可弃去其 transport 项)。于是:
> 1. **Jacobi 方程(极小)**:由 $\Delta\phi+(n+S)\phi=0$(见 [[Jacobi_Operator_Minimal_Hypersurface]]),因 $n+S>0$ 常数,积分得
>    $$ \int_M\phi\,d\mu=0. \tag{7} $$
> 2. **$S$ 变分**:因 $S_t$ 空间常数,
>    $$ \frac12\frac{dS_t}{dt}=\langle A,\nabla^2\phi\rangle+f_3\phi=:c(t). \tag{8} $$
> 3. **Codazzi 消项**:由 [[Codazzi_Equation]] 的 $\mathrm{div}A=0$(极小),
>    $$ \int_M\langle A,\nabla^2\phi\rangle\,d\mu=-\int_M\langle\mathrm{div}A,\nabla\phi\rangle\,d\mu=0. \tag{9} $$
> 4. **积分(8)**:用 (9)、$f_3$ 的空间常数性、(7),得
>    $$ c(t)\,\mathrm{Vol}(M)=f_3\int_M\phi\,d\mu=0. $$
>    因此 $c(t)=0$ 对每个 $t$ 成立,故 $S_t$ 在 $I$ 上为常数。$\square$

## 为什么需要"常数 $f_3$"(Remark 3.2)

> [!WARNING] 没有常数 $f_3$ 就失败
> 若 $f_3$ **不**空间常数,同一计算只给出
> $$ \frac12S'\,\mathrm{Vol}(M)=\int_M\phi f_3\,d\mu, $$
> 此时 Jacobi 方程与 $\int_M\phi\,d\mu=0$ **都不**迫使右边为零。这正是"常数 $f_3$"假设进入局部论证的确切位置。

## 谱形式的重述(Remark 3.3)

> [!TIP] Fredholm / range 条件视角
> 固定 $t$,令 $L_t=\Delta_t+n+S_t$ 为 Jacobi 算子。$\phi\in\ker L_t$。由 $L_t$ 自伴 + Fredholm 的交替定理:
> $$ f_{3,t}\perp\ker L_t\ (\text{在 }L^2(M,g_t)\text{ 内积下})\ \iff\ f_{3,t}\in\operatorname{Ran}L_t=\operatorname{Ran}(\Delta_t+n+S_t). $$
> 若 $f_{3,t}$ 空间常数,则 $f_{3,t}=L_t f_{3,t}/(n+S_t)$,故"常数 $f_3$"推出 range 条件;而 range 条件是比常数 $f_3$ **更弱**的充分条件(见 [[Fredholm_Operator]])。

> [!NOTE] 本节关系
> $$ \boxed{\Delta\phi+(n+S)\phi=0}\ \Longrightarrow\ \boxed{\int\phi\,d\mu=0}\ \xrightarrow{\ \mathrm{div}A=0\ }\ \boxed{\int\langle A,\nabla^2\phi\rangle d\mu=0}\ \Longrightarrow\ \boxed{S_t\ \text{常数}}. $$
