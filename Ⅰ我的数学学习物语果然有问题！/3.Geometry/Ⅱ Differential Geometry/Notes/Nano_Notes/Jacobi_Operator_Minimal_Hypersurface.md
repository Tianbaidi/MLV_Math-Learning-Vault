---
tags:
  - Geometry
  - Differential_Geometry
  - Jacobi_Operator
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §2–§4。核心是 **Jacobi 算子**
> $$ L=\Delta+n+S, $$
> 它同时是:极小超曲面法向变分的线性化 $L=DH(0)$、Jacobi 方程 $\Delta\phi+(n+S)\phi=0$ 的算子、以及 §4 里那个**自伴 Fredholm 算子**。

> 相关笔记:[[Shape_Operator_Invariants]]、[[Fredholm_Operator]]、[[Hölder_Space_and_Elliptic_Regularity]]、[[Path_Rigidity_of_S]]。

## 由来:法向变分的线性化

> [!ABSTRACT] Definition(Jacobi operator)
> 设 $F_t$ 是 $F$ 沿法向 $\phi\nu$ 的 $C^1$ 形变。论文 §2 的变分公式(Lemma 2.1, Eq. 4)给出平均曲率线性化
> $$ H'=\Delta\phi+(n+S)\phi=L\phi,\qquad L=\Delta+n+S. $$
> 故 $L=DH(0)$,即平均曲率算子 $H$ 在极小点处的 Fréchet 导数。

> [!NOTE] 为什么是 $\Delta+n+S$
> 单位球面里极小超曲面的**第二变分**由 $\Delta+n+S$ 控制;法向速度 $\phi$ 对应的 **Jacobi 方程**为
> $$ \Delta\phi+(n+S)\phi=0. $$

## 关键性质(§3 与 §4)

> [!TIP] 自伴、椭圆、Fredholm
> - **自伴**:$M$ 无边界时 $\int_M vLu\,d\mu=\int_M uLv\,d\mu$。
> - **椭圆**:主部是 $\Delta$。
> - **Fredholm**:由 Schauder 理论,$L:C^{k,\alpha}(M)\to C^{k-2,\alpha}(M)$ 是 Fredholm 的,且 $\operatorname{ind}L=0$(见 [[Fredholm_Operator]])。

> [!WARNING] Jacobi 核
> $\ker L=\ker(\Delta+n+S)$ **有限维**、元素光滑——这是 §4 做 Lyapunov–Schmidt 约化的立足点(见 [[Lyapunov_Schmidt_Reduction]])。

## 与论文 §2–§4 对接

- §3 Prop 3.1:沿"极小且 $S$、$f_3$ 空间常数"的 $C^1$ 族,法向速度 $\phi\in\ker L$,即满足 $\Delta\phi+(n+S)\phi=0$;因 $n+S>0$ 常数,积分得 $\int_M\phi\,d\mu=0$。
- §4:$L$ 的自伴 + 椭圆 + Fredholm 结构直接支撑 [[Lyapunov_Schmidt_Reduction]],把无穷维约束压到有限维 $K=\ker L$ 上。

> [!NOTE] 本节关系
> $$ \boxed{H'=\Delta\phi+(n+S)\phi}\ \Longrightarrow\ \boxed{L=\Delta+n+S}\ \Longrightarrow\ \boxed{\text{自伴+椭圆+Fredholm},\ \operatorname{ind}L=0}\ \Longrightarrow\ \boxed{\ker L\ \text{有限维}}. $$
