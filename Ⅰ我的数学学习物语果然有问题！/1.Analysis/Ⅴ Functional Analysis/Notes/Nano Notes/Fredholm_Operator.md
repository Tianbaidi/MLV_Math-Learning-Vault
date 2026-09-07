---
tags:
  - Analysis
  - Functional_Analysis
  - Fredholm_Operator
---

> [!NOTE] 本文用途
> 这篇原子笔记服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §4。论文把 Jacobi 算子
> $$L=\Delta+n+S$$
> 当作 $C^{k,\alpha}(M)\to C^{k-2,\alpha}(M)$ 的**自伴 Fredholm 算子**来用。要读懂 §4 的 "range condition"、$\operatorname{codim}\operatorname{Ran}L=\dim\ker L$、$\operatorname{ind}L=0$ 与 $K\oplus X$ 分解,就需要这里的 Fredholm 理论。配套看 [[Lyapunov_Schmidt_Reduction]]、[[Hölder_Space_and_Elliptic_Regularity]]。

## 什么是 Fredholm 算子

> [!ABSTRACT] 定义:Fredholm 算子
> 设 $X,Y$ 为 Banach 空间,有界线性算子 $T:X\to Y$ 称为 **Fredholm** 的,如果
> 1. $\ker T$ 有限维;
> 2. $\operatorname{Ran} T$ 闭;
> 3. $\operatorname{Ran} T$ 在 $Y$ 中余维有限。
>
> 此时定义 **Fredholm 指标**
> $$ \operatorname{ind} T=\dim\ker T-\operatorname{codim}\operatorname{Ran} T. $$

> [!TIP] 关键:自伴 + 椭圆 ⟹ Fredholm 且指标为 0
> 论文里的关键事实是:在闭流形 $M$ 上,$L=\Delta+n+S$ 的**主部是 $\Delta$**,故椭圆;又因为 $M$ 无边界、$n+S$ 是实值函数,$L$ **形式上自伴(对称)**。于是有:
> $$ \int_M v\,Lu\,d\mu = -\int_M\langle\nabla v,\nabla u\rangle\,d\mu+\int_M(n+S)uv\,d\mu = \int_M u\,Lv\,d\mu. $$
> 由标准 **Schauder 椭圆理论**(见 [[Hölder_Space_and_Elliptic_Regularity]]),$L:C^{k,\alpha}(M)\to C^{k-2,\alpha}(M)$ 是 Fredholm 的,且由自伴性推出
> $$ \operatorname{codim}\operatorname{Ran} L=\dim\ker L, \qquad\text{即}\quad \operatorname{ind} L=0. $$

## Fredholm 交替定理(自伴版)

> [!NOTE] Fredholm 交替定理
> 对自伴 Fredholm 算子 $L$,椭圆正则性保证 $\ker L$ 中元素皆光滑。于是
> $$ f\in\operatorname{Ran}L\ \iff\ \int_M f\,\varphi\,d\mu=0\quad(\forall\,\varphi\in\ker L). $$
> 也就是说,$\operatorname{Ran}L$ 恰是 $\ker L$ 在 $L^2$ 意义下的**正交补**。

## 这里的 $K\oplus X$ 分解

设 $\ker L=K$,$K^{\perp_{L^2}}$ 为 $K$ 在 $L^2(M,g)$ 内积下的正交补。论文取

$$ X=C^{k,α}(M)\cap K^{\perp_{L^2}},\qquad Y=C^{k−2,α}(M)\cap K^{\perp_{L^2}}, $$

于是有直和分解

$$ C^{k,α}(M)=K\oplus X,\qquad C^{k−2,α}(M)=K\oplus Y. $$

> [!WARNING] 这里的一句话总结
> 由于 $L$ 在 $K$ 上为零、又自伴,上面的交替定理表明 **$L:X\to Y$ 是双射**,Schauder 估计给出有界逆 $L^{-1}:Y\to X$。这正是 §4 做 Lyapunov–Schmidt 约化前的基石。

## 与论文 §4 的对接

- $L=DH(0)=\Delta+n+S$ 是平均曲率算子 $H$ 在极小超曲面处的**线性化**(§2 的变分公式给出 $H'=\Delta\phi+(n+S)\phi$)。
- $\ker L=\ker(\Delta+n+S)$ 就是 §3 里 Jacobi 方程的**解空间**($\Delta\phi+(n+S)\phi=0$),也是 §4 里那个有限维的 Jacobi 核。
- 用 $L$ 在 $K\oplus X$ 上的可逆性,配合解析隐函数定理,才能把"极小且 $S$、$f_3$ 常数"这一个无穷维约束"约化"到有限个生成元上去——见 [[Lyapunov_Schmidt_Reduction]]。

> [!NOTE] 本节关系
> $$ \boxed{L=\Delta+n+S}\ \xrightarrow{\text{椭圆+自伴}}\ \boxed{\operatorname{ind}L=0}\ \Longrightarrow\ \boxed{K\oplus X\text{ 上双射 }}\ \Longrightarrow\ \boxed{\text{Lyapunov–Schmidt 约化}}. $$
