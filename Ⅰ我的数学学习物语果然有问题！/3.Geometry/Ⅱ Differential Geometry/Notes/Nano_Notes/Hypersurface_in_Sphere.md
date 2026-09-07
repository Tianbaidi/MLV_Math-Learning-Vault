---
tags:
  - Geometry
  - Differential_Geometry
  - Minimal_Hypersurface
  - Hypersurface
---

> 这篇是"球面中的超曲面"的**根笔记**:定义对象、切/法分解、以及作为论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 前置的一组不变式与三个规范模型。更细的机制(shape operator 性质、Gauss / Codazzi 方程、Jacobi 算子)各自成篇,这里只给出整体并交叉引用。

> 相关笔记:[[Shape_Operator_Invariants]]、[[Gauss_Equation_Hypersurface]]、[[Codazzi_Equation]]、[[Jacobi_Operator_Minimal_Hypersurface]]、[[Symmetric_Functions_of_Principal_Curvatures]]、[[Sphere_Orientability_and_TwoSided]]。

> [!WARNING] 本笔记 / 论文的约定(与 do Carmo 归一化不同)
> 本笔记**跟随论文与其所属领域(极小超曲面 / Chern 猜想 / 几何测度论)**的主流约定:
> $$ H=\mathrm{tr}\,A=\sum_{i=1}^n\lambda_i,\qquad S=\mathrm{tr}(A^2)=|A|^2=\sum_i\lambda_i^2,\qquad f_3=\mathrm{tr}(A^3)=\sum_i\lambda_i^3. $$
> 注意经典微分几何(do Carmo 曲面论/《Riemannian Geometry》)常取**归一化** $H_{\text{do Carmo}}=\frac1n\,\mathrm{tr}A$。二者只差因子 $n$:例如 Gauss 方程在未归一化下是 $R=n(n-1)+H^2-S$,在归一化下是 $R=n(n-1)+n^2H^2-S$。跨书阅读时务必留意。

## 定义:球面中的超曲面

> [!ABSTRACT] Definition(hypersurface)
> 设单位球面
> $$ S^{n+1}=\{x\in\mathbb R^{n+2}:|x|=1\}. $$
> 若 $\Sigma^n\subset S^{n+1}$ 是一个 $n$-维光滑子流形,则称 $\Sigma$ 为 $S^{n+1}$ 中的 **hypersurface**。
>
> 等价地 $\operatorname{codim}_{S^{n+1}}\Sigma=1$;而在环境空间里 $\operatorname{codim}_{\mathbb R^{n+2}}\Sigma=2$。

## 切空间与法空间

> [!ABSTRACT] Definition(切/法分解)
> 对 $p\in\Sigma$,有 $T_p\Sigma\subset T_pS^{n+1}$。因为
> $$ T_pS^{n+1}=\{v\in\mathbb R^{n+2}:\langle v,p\rangle=0\}, $$
> 所以位置向量 $p$ 是球面的法向量。若 $\nu$ 是 $\Sigma\subset S^{n+1}$ 的局部单位法向量,则 $\nu\in T_pS^{n+1}$,从而 $\langle\nu,p\rangle=0$。于是有正交分解
> $$ \mathbb R^{n+2}=T_p\Sigma\oplus\operatorname{span}\{\nu,p\}. $$

这里的关键:**有两个法方向**——一个是环境空间里的位置向量 $p$(垂垂于球面),一个是曲面在球面内的法向 $\nu$(与 $p$ 正交)。论文 §5 的管状/焦点构造正是用 $(p,\nu)$ 这两个方向。

## 不变式:形状算子派生的一组量

把 shape operator $A=-\nabla^S_X\nu$ 视为自伴算子(细节见 [[Shape_Operator_Invariants]]),主曲率 $\lambda_1,\dots,\lambda_n$ 是其特征值。论文用的三个不变式是

> [!NOTE] 三个不变式
> $$ H=\mathrm{tr}\,A=\sum_i\lambda_i,\qquad S=\mathrm{tr}(A^2)=|A|^2=\sum_i\lambda_i^2,\qquad f_3=\mathrm{tr}(A^3)=\sum_i\lambda_i^3. $$
> 其中 $S$ 即"形状算子长度平方",$f_3$ 是论文的主角(trace of $A^3$);它们都是主曲率的**对称函数**(见 [[Symmetric_Functions_of_Principal_Curvatures]])。

## 极小超曲面

> [!ABSTRACT] Definition(minimal hypersurface)
> 若 $H\equiv 0$,即 $\mathrm{tr}\,A=0$(等价地 $\sum_i\lambda_i=0$),则称 $\Sigma^n\subset S^{n+1}$ 为 **minimal hypersurface**。
>
> 在 $H=0$ 时,由 Gauss 方程([[Gauss_Equation_Hypersurface]])
> $$ R=n(n-1)-S, $$
> 所以 **"常数标量曲率" ⟺ "常数 $S$"**——这正是 Chern 猜想的表述形式。

## 三个规范模型

> [!Example] 赤道 Equator
> $$ \Sigma=\{x\in S^{n+1}:x_{n+2}=0\}\cong S^n. $$
> 它是 totally geodesic:$A=0$,$H=0$。因此赤道是最基本的极小超曲面。

> [!Example] 测地球面 Geodesic sphere
> 取常值 $c\in(-1,1)$,
> $$ \Sigma_c=\{x\in S^{n+1}:x_{n+2}=c\}\cong S^n(\sqrt{1-c^2}). $$
> 其所有主曲率相等,是 totally umbilical。当且仅当 $c=0$ 时它是极小(即赤道)。主曲率的**符号**取决于 $\nu$ 的选取。

> [!Example] Clifford 超曲面
> 设 $p+q=n$,则
> $$ \mathbb S^p\textstyle\Bigl(\sqrt{\frac{p}{n}}\Bigr)\times\mathbb S^q\Bigl(\sqrt{\frac{q}{n}}\Bigr)\subset S^{n+1} $$
> 是极小超曲面。两个主曲率为 $\sqrt{\frac{q}{p}}$ (重数 $p$)与 $-\sqrt{\frac{p}{q}}$ (重数 $q$),从而
> $$ p\sqrt{\frac{q}{p}}-q\sqrt{\frac{p}{q}}=\sqrt{pq}-\sqrt{pq}=0. $$
> 极小超曲面的"极小"靠零平均曲率;当 $S$ 常数且取 $S=n$ 时,Clifford 环面是首个刚性模型(见 [[Shape_Operator_Invariants]] 与 [[Gauss_Equation_Hypersurface]])。

## 本节关系

$$ \boxed{\Sigma^n\subset S^{n+1},\ \operatorname{codim}=1}\ \Longrightarrow\ \boxed{\mathbb R^{n+2}=T_p\Sigma\oplus\operatorname{span}\{\nu,p\},\ \nu\perp p}\ \Longrightarrow\ \boxed{H,S,f_3}\ \Longrightarrow\ \boxed{\text{极小}\iff H=0\iff R=n(n-1)-S}. $$
