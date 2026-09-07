---
tags:
  - Geometry
  - Differential_Geometry
  - Tubular_Neighborhood
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Lemma 5.1 及其后)。§5 要证明"**一族极小嵌入有无公共的、两侧一致的法向管状邻域**",从而获得面积界与正则收敛。这篇讲**球面法注射半径**与管状邻域。

> 相关笔记:[[Hypersurface_in_Sphere]]、[[Focal_Point_of_Hypersurface]]、[[Rolling_Radius]]、[[Normal_Jacobian]]、[[Smooth_Compactness_Minimal_Hypersurface]]、[[Hausdorff_Convergence_and_Blaschke_Selection]]。

## 球面法注射半径

> [!ABSTRACT] Definition(球形法注射半径)
> 对闭嵌入超曲面 $F:M\hookrightarrow S^{n+1}(1)$,定义其**球面法注射半径**为满足以下条件的 $r>0$ 的上确界:映射
> $$ E:M\times(-r,r)\to S^{n+1}(1),\qquad E(x,t)=\cos t\,F(x)+\sin t\,\nu(x), $$
> 是单射且非奇异(雅可比满秩)。也就是说,沿法向 $\nu$ 两侧各走 $r$ 长度,$F(M)$ 的**管状邻域** $E(M\times(-r,r))$ 不自我交叠、不坍缩。

## 引理 5.1:曲率界给出管径

> [!Success] Lemma(Lemma 5.1)
> 设 $F:M^n\hookrightarrow S^{n+1}(1)$ 是**闭连通嵌入极小**超曲面,且 $|A|\le K$。定义
> $$ r_K=\begin{cases}\arctan(K^{-1}),& K>0,\\ \pi/2,& K=0.\end{cases} $$
> 则 $F(M)$ 的球面法注射半径**至少为 $r_K$**。

> [!NOTE] 直观
> $K$ 越大(曲率越"弯"),允许的管径 $r_K=\arctan(1/K)$ 越小;当超曲面 totally geodesic($K=0$,如赤道)时,法向走到极点相遇前都不碰撞,管径取 $\pi/2$。

## 构造思路(需要"分离 + 滚动 = 焦点")

> [!NOTE] 三步逻辑
> 1. **分离**:闭嵌入超曲面把球面分成两个域 $\Omega_{\pm}$(见 [[Sphere_Orientability_and_TwoSided]]),取各侧内向单位法向,其 Ricci 为 $ng>0$,边界 $F(M)$ 平均曲率为零。
> 2. **滚动半径 = 焦点半径**:Roll(内向边界割距离)恒有 $\mathrm{Roll}\le\mathrm{Foc}$(首次内向焦点距离);Howard 滚动定理的刚性形式说严格 $\mathrm{Roll}<\mathrm{Foc}$ 只出现在圆柱/Möbius 带这类 Ricci 有零方向的情形,而 $\Omega_{\pm}$ Ricci>$0$,故 $\mathrm{Roll}=\mathrm{Foc}$(见 [[Rolling_Radius]])。
> 3. **焦点距离 ≥ $r_K$**:沿单位球面法向测地线,切向法 Jacobi 映射为 $J_t=\cos t\,I-\sin t\,A$(见 [[Focal_Point_of_Hypersurface]]);当 $\lambda>0$ 时其第一正零点为 $\arctan(1/\lambda)$,故 $|A|\le K$ 给出首焦点距离 $\ge\arctan(K^{-1})=r_K$。

 由 (2)(3),每侧法向指数映射在 $r<r_K$ 前单射且非奇异;法向段是到边界的唯一极短测地线并留在对应域内部,故两侧法向测地线(落在两个不相交域)不可能相遇。两侧估计合并即得**双侧**法注射界 $\ge r_K$。$\square$

> [!NOTE] 本节作用
> 这个统一的管径 $r_K$ 是后续一切的基础:它既给出面积界(见 [[Normal_Jacobian]]),又给出"图像是单层球面图"与收敛所需的均匀管状邻域(见 [[Smooth_Compactness_Minimal_Hypersurface]]、[[Hausdorff_Convergence_and_Blaschke_Selection]])。

> [!NOTE] 本节关系
> $$ \boxed{\text{嵌入分离}\Rightarrow\Omega_{\pm}}\ \xrightarrow{\ \mathrm{Roll=Foc}\ }\ \boxed{\text{双侧法注射半径}\ge r_K}\ \Longrightarrow\ \boxed{\text{均匀管状邻域}}\ \Longrightarrow\ \boxed{\text{面积界 + 单层图}}. $$
