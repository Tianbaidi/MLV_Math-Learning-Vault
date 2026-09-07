---
tags:
  - Geometry
  - Differential_Geometry
  - Focal_Point
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Lemma 5.1)。"焦点/焦距离"给出沿法向何处首次"聚焦"(法 Jacobi 映射退化),是决定法注射管径的关键。

> 相关笔记:[[Tubular_Neighborhood]]、[[Rolling_Radius]]、[[Normal_Jacobian]]、[[Hypersurface_in_Sphere]]。

## 法向测地线与法 Jacobi 映射

> [!ABSTRACT] Definition(法 Jacobi 映射)
> 沿单位球面 $S^{n+1}(1)$ 的法向测地线 $\gamma(t)=\cos t\,F(x)+\sin t\,\nu(x)$(见 [[Tubular_Neighborhood]] 的 $E(x,t)$),与 $\nu$ 正交的切向分量由
> $$ J_t=\cos t\,I-\sin t\,A $$
> 描述,其中 $A$ 是"内向"形状算子。

## 焦点与焦距离

> [!ABSTRACT] Definition(焦点、焦距离)
> 若 $\det J_t=0$,即某主曲率 $\lambda$ 使
> $$ \cos t-\lambda\sin t=0, $$
> 则称 $E(x,t)$ 为一个**焦点**(沿该法向"聚焦"的点)。首个内向焦距离
> $$ \mathrm{Foc}=\inf\{\ t>0:\det J_t=0\ \}. $$

> [!Success] Proposition(第一正零点)
> - 若 $\lambda>0$,$\cos t-\lambda\sin t$ 在 $\pi/2$ 之前的首正零点为 $t=\arctan(1/\lambda)$。
> - 若 $\lambda\le0$,在 $\pi/2$ 之前无正零点(分母/该因子恒为正)。
>
> 因而当 $|A|\le K$ 时,对 $\lambda_i>0$ 有 $\arctan(1/\lambda_i)\ge\arctan(1/K)$,首焦点距离 $\ge r_K$。当 $K=0$($A=0$,totally geodesic)时 $J_t=\cos t\,I$,首焦点距离为 $\pi/2$。

## 在 §5 中的角色

> [!NOTE] 焦点距离 → 管径
> 论文把"首焦点距离 $\ge r_K$"与"滚动半径 $=$ 焦点半径(见 [[Rolling_Radius]])"结合,得到每侧法向指数映射在 $r<r_K$ 前单射且非奇异,从而给出统一的法注射半径 $\ge r_K$(见 [[Tubular_Neighborhood]])。

> [!WARNING] 与 Jacobi 算子不要混淆
> 这里的 $J_t=\cos t\,I-\sin t\,A$ 是**沿法向测地线的切向 Jacobi 映射**(几何聚焦);而 §4 的 Jacobi 算子 $L=\Delta+n+S$ 是**变分/二次变分**算子(见 [[Jacobi_Operator_Minimal_Hypersurface]])。二者都叫 Jacobi,但用于不同层面。

> [!NOTE] 本节关系
> $$ \boxed{J_t=\cos t\,I-\sin t\,A}\ \Longrightarrow\ \boxed{\cos t-\lambda\sin t=0\Rightarrow t=\arctan(1/\lambda)}\ \Longrightarrow\ \boxed{\text{首焦点距离}\ge r_K}\ \Longrightarrow\ \boxed{\text{法注射半径}}. $$
