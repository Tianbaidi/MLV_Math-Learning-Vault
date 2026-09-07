---
tags:
  - Geometry
  - Differential_Geometry
  - Rolling_Radius
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Lemma 5.1)。Howard 滚动定理的**刚性形式**把"滚动半径 $=$ 焦点半径"用于超曲面两侧,从而保证法向指数映射在管径内单射。

> 相关笔记:[[Tubular_Neighborhood]]、[[Focal_Point_of_Hypersurface]]、[[Normal_Jacobian]]。

## 滚动半径与焦点半径

> [!ABSTRACT] Definition(滚动半径 / 焦点半径)
> 对紧流形 $\Omega$ 与其边界 $\partial\Omega$,取内向单位法向。
> - **滚动半径** $\mathrm{Roll}$:内向边界割距离的下确界(从边界出发的内向法向测地线在"翻出"之前能走的最远距离)。
> - **焦点半径** $\mathrm{Foc}$:首次内向焦点距离的下确界(见 [[Focal_Point_of_Hypersurface]])。
>
> 恒有
> $$ \mathrm{Roll}\le\mathrm{Foc}. $$

## Howard 滚动定理(刚性形式)

> [!ABSTRACT] Theorem(Howard, 1999)
> 设 $M$ 是**完备连通、带光滑非空紧边界、Ricci 非负、边界内向平均曲率非负**的流形。若 $\mathrm{Roll}<\mathrm{Foc}$ **严格**成立,则 $M$ 必为 **Riemannian cylinder** 或 **广义 Möbius 带**。

> [!NOTE] 为什么 $\Omega_{\pm}$ 不是例外
> 每个例外空间都有**局部乘积区间方向,Ricci 为零**。而论文里 $\Omega_{\pm}$ 的 Ricci 是 $ng>0$(单位球面),边界 $F(M)$ 平均曲率为零,故不是例外。于是
> $$ \mathrm{Roll}=\mathrm{Foc}\quad(\text{在 }\Omega_{\pm}\text{ 两侧均成立}). $$

## 在 §5 中的角色

> [!NOTE] 滚动 = 焦点 ⟹ 管径
> $\mathrm{Roll}=\mathrm{Foc}$ 把"法向指数映射在首焦点之前单射"升级为"在滚动半径(即焦点半径)之前单射";配合焦点距离 $\ge r_K$(见 [[Focal_Point_of_Hypersurface]]),得每侧法注射半径 $\ge r_K$,再合并为双侧(见 [[Tubular_Neighborhood]])。

> [!NOTE] 本节关系
> $$ \boxed{\mathrm{Roll}\le\mathrm{Foc}}\ \xrightarrow{\ \text{Howard 刚性}\ (Ric>0)\ }\ \boxed{\mathrm{Roll}=\mathrm{Foc}}\ \Longrightarrow\ \boxed{\text{法向指数映射 }r_K\text{ 前单射}}\ \Longrightarrow\ \boxed{\text{双侧法注射半径}}. $$
