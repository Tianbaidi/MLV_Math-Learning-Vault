---
tags:
  - Geometry
  - Differential_Geometry
  - Shape_Operator
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §1–§2。论文的核心对象是**形状算子 $A$** 及其一组不变量
> $$ H=\mathrm{tr}\,A,\qquad S=|A|^2=\mathrm{tr}(A^2),\qquad f_3=\mathrm{tr}(A^3). $$
> 这篇把 $A$、主曲率、$h$ 与这些不变量一次讲清。

> 相关笔记:[[Hypersurface_in_Sphere]]、[[Symmetric_Functions_of_Principal_Curvatures]]、[[Gauss_Equation_Hypersurface]]、[[Codazzi_Equation]]。

## 形状算子

> [!ABSTRACT] Definition(shape operator)
> 设 $\Sigma^n\subset S^{n+1}$,单位法向量场 $\nu$。定义
> $$ A(X)=-\left(\nabla_X^{S}\nu\right)^{\top},\qquad X\in T\Sigma, $$
> 其中 $\nabla^S$ 是球面的 Levi-Civita 联络,$(\cdot)^{\top}$ 为到 $T\Sigma$ 的正交投影。(因 $\nabla_X^{S}\nu\perp\nu$ 且落在 $T_pS=T_p\Sigma\oplus\operatorname{span}\{\nu\}$ 的 $\nu$ 正交部分,它自动落在 $T\Sigma$。)
>
> 第二基本形式 $h(X,Y)=\langle A(X),Y\rangle$。

> [!TIP] 自伴性
> 对**超曲面**,$A$ 关于诱导度量 $g$ 自伴,$h$ 对称。于是 $A$ 可正交对角化,特征值 $\lambda_1,\dots,\lambda_n$ 即**主曲率**(见 [[Symmetric_Functions_of_Principal_Curvatures]])。

## 三个不变式

> [!NOTE] 论文用的三个量
> $$ H=\mathrm{tr}\,A=\sum_{i=1}^n\lambda_i,\qquad S=\mathrm{tr}(A^2)=|A|^2=\sum_i\lambda_i^2,\qquad f_3=\mathrm{tr}(A^3)=\sum_i\lambda_i^3. $$
> - $H$:平均曲率(采用**未归一化**约定;do Carmo 归一化为 $\frac1n\mathrm{tr}A$,见 [[Hypersurface_in_Sphere]])。
> - $S$:形状算子长度平方,$S\ge0$;对极小超曲面,$S$ 常数 ⟺ 常数标量曲率(见 [[Gauss_Equation_Hypersurface]])。
> - $f_3=\mathrm{tr}(A^3)$:论文的主角,是不变量族 $f_k=\mathrm{tr}(A^k)$ 的一员。

> [!WARNING] minimal 的条件
> 极小 ⟺ $H=0$ ⟺ $\mathrm{tr}\,A=0$。这是关于 $H$ 的独立条件,与 $S$、$f_3$ 无关。

## 与论文 §1–§2 对接

- Chern 猜想研究"闭极小超曲面、常数 $S$";$S=|A|^2$ 即为该领域标准主角。
- Simons 刚性不等式:$0\le S\le n\Rightarrow S=0$ 或 $S=n$;$S=n$ 时 $\Sigma$ 是 Clifford 环面。
- isoparametric(主曲率全体常数)给出主族,极小成员 $S=(g-1)n$,其中 $g\in\{1,2,3,4,6\}$ 为互异主曲率个数。

> [!NOTE] 本节关系
> $$ \boxed{A=-\left(\nabla_X^S\nu\right)^{\top}}\ \xrightarrow{\ \text{自伴}\ }\ \boxed{\text{实谱 }\lambda_i}\ \Longrightarrow\ \boxed{H=\mathrm{tr}A,\ S=\mathrm{tr}(A^2),\ f_3=\mathrm{tr}(A^3)}\ \Longrightarrow\ \boxed{\text{极小}\iff H=0}. $$
