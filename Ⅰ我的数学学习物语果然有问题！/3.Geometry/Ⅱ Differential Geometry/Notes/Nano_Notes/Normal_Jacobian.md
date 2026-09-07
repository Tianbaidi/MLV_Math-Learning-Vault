---
tags:
  - Geometry
  - Differential_Geometry
  - Normal_Jacobian
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Prop 5.2)。在拿到统一管径后,**法 Jacobian** 给出与拓扑无关的一致面积上界。

> 相关笔记:[[Tubular_Neighborhood]]、[[Focal_Point_of_Hypersurface]]、[[Smooth_Compactness_Minimal_Hypersurface]]。

## 法 Jacobian

> [!ABSTRACT] Definition(法 Jacobian)
> 在 $(x,t)\in M\times(-r,r)$ 处,法向指数映射 $E(x,t)=\cos t\,F(x)+\sin t\,\nu(x)$ 的 Jacobian 行列式为
> $$ J(x,t)=\det\bigl(\cos t\,I-\sin t\,A_x\bigr)=\prod_{i=1}^n\bigl(\cos t-\lambda_i(x)\sin t\bigr). $$

## 面积上界(Prop 5.2)

> [!Success] Proposition(Prop 5.2)
> 在 Lemma 5.1 的假设下,取 $\delta_K=r_K/2$、$b_K=\cos\delta_K-K\sin\delta_K>0$,则
> $$ \mathrm{Vol}(M)\le\frac{\mathrm{Vol}(S^{n+1}(1))}{2\delta_K\,b_K^{\,n}}. $$

> [!NOTE] 推导要点
> 1. 对 $|t|\le\delta_K$、$|\lambda_i|\le K$,每个因子 $\cos t-\lambda_i\sin t\ge b_K>0$。
> 2. Lemma 5.1 保证 $E$ 在 $M\times[-\delta_K,\delta_K]$ 上**单射**,故换元得
>    $$ \mathrm{Vol}(S^{n+1}(1))\ge\int_{-\delta_K}^{\delta_K}\int_M J(x,t)\,d\mu(x)\,dt\ge 2\delta_K\,b_K^{\,n}\,\mathrm{Vol}(M). $$
> 3. 移项即得面积上界。$\square$

## 在 §5 中的角色

> [!NOTE] 一致面积界
> 这个界只依赖 $n$ 与 $K$($\Lambda$),**不依赖**流形 $M$ 的拓扑。它保证闭极小超曲面族的质量一致有界,是 [[Smooth_Compactness_Minimal_Hypersurface]] 里 varifold 紧致性/测度收敛的前提。

> [!NOTE] 本节关系
> $$ \boxed{J=\det(\cos t\,I-\sin t\,A)=\prod_i(\cos t-\lambda_i\sin t)}\ \xrightarrow{\ |A|\le K\ }\ \boxed{J\ge b_K^{\,n}}\ \Longrightarrow\ \boxed{\mathrm{Vol}(M)\le\frac{\mathrm{Vol}(S^{n+1}(1))}{2\delta_K b_K^{\,n}}}. $$
