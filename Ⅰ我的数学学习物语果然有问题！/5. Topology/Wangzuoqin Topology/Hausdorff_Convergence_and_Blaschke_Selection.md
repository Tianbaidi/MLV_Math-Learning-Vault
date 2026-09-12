---
tags:
  - Topology
  - Metric_Geometry
  - Convergence
---

> 论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Prop 5.4)一开篇就用 **Blaschke 选择定理**从一族极小超曲面中挑出 Hausdorff 收敛子列,拿到极限 $\Sigma_\infty$;这是后面所有"局部图收敛 → varifold 收敛 → 光滑极限"的**起点**。这篇讲 Hausdorff 距离、Hausdorff 收敛与 Blaschke 选择定理。

> 相关笔记:[[Varifold_and_Stationarity]]、[[Sphere_Orientability_and_TwoSided]]、[[Hölder_Space_and_Elliptic_Regularity]]。

## Hausdorff 距离

> [!ABSTRACT] Definition(Hausdorff 距离)
> 设 $A,B\subset S^{n+1}$ 为非空紧子集。定义
> $$ d_H(A,B)=\max\Bigl\{\sup_{a\in A}d(a,B),\ \sup_{b\in B}d(b,A)\Bigr\}, $$
> 其中 $d(x,B)=\inf_{y\in B}d(x,y)$ 是球面距离。$d_H$ 构成紧子集族上的**度量**。

> [!TIP] 直观
> 用"把 $A$ 稍微"胀大"一点能否盖住 $B$,再把 $B$ 胀大能否盖住 $A$"来度量两个集合接近程度。$d_H(A,B)\le\epsilon$ 的意思是每个集合都落在另一个的 $\epsilon$-邻域内。

## Hausdorff 收敛

> [!ABSTRACT] Definition(Hausdorff 收敛)
> 一列紧集 $\Sigma_j$ 收敛到紧集 $\Sigma_\infty$,如果 $d_H(\Sigma_j,\Sigma_\infty)\to0$。这比点列收敛弱:它只保证"形状上接近",不一定给出可微的点对应(那是后面用局部图同化才有的)。

## Blaschke 选择定理

> [!Success] Theorem(Blaschke selection)
> 在**紧度量空间**(这里是 $S^{n+1}$)中,所有非空紧子集在 $d_H$ 下构成**紧度量空间**。因此任意一族紧子集都有 Hausdorff 收敛子列。
>
> 即:对闭连通嵌入极小子流形列 $\Sigma_j=F_j(M_j)$,Blaschke 选择定理给出子列与一非空紧集 $\Sigma_\infty\subset S^{n+1}$,使
> $$ \Sigma_j\xrightarrow{\ d_H\ }\Sigma_\infty. $$

> [!NOTE] 论文里的衔接(§5, Prop 5.4)
> 由 Blaschke 定理取 $\Sigma_\infty$ 后:
> 1. 取有限个点 $x_\infty^1,\dots,x_\infty^N$ 使 $B_{r/8}(x_\infty^a)$ 盖住 $\Sigma_\infty$,并在每个点选取 $\Sigma_j$ 中收敛的点 $x_j^a$;
> 2. 用平行移动把各切空间套到 $T_{x_\infty^a}S^{n+1}$,得 $T_{x_j^a}\Sigma_j\to P_\infty^a$;
> 3. 在每个局部图(见 [[Hölder_Space_and_Elliptic_Regularity]] Lemma 5.3 的球面图)上,用 Arzelà–Ascoli 得图函数 $u_j^a\to u_\infty^a$ 在 $C^{1,\alpha}$ 收敛,图极限正是 $\Sigma_\infty$ 在 $B_{r/2}(x_\infty^a)$ 中的一部分。
>
> 正因为 $\Sigma_j\to\Sigma_\infty$ **Hausdorff**,才能保证 $\Sigma_j$ 最终落入 $\Sigma_\infty$ 的管状邻域内、且与法向纤维横截,从而投影 $\pi_\infty|_{\Sigma_j}$ 是局部微分同胚(见 [[Sphere_Orientability_and_TwoSided]])。

> [!WARNING] 只有 Hausdorff 收敛还不足够
> 它给出"极限是紧集",但**不自动**给出"极限光滑"或"收敛是一层"。要做到这两点,论文还得靠 varifold + 椭圆正则性(见 [[Varifold_and_Stationarity]]、[[Hölder_Space_and_Elliptic_Regularity]])。Hausdorff 收敛只是把"有一串子流形"变成"有一个紧极限"的第一步。

> [!NOTE] 本节关系
> $$ \boxed{\Sigma_j\subset S^{n+1}\text{ 紧}}\ \xrightarrow{\ d_H\ }\ \boxed{\Sigma_\infty\text{ 紧}}\ \xrightarrow{\text{Blaschke}}\ \boxed{d_H(\Sigma_j,\Sigma_\infty)\to0}\ \Longrightarrow\ \boxed{\text{局部 }C^{1,\alpha}\text{ 图收敛}}. $$
