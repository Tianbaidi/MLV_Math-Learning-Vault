---
tags:
  - Analysis
  - Geometric_Measure_Theory
  - Varifold
---

> 论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Prop 5.4)要证明"一族极小嵌入收敛到光滑极小嵌入、且是 multiplicity-one"。那里的工具是 **varifold**:把超曲面看成 **Grassmann 丛上的 Radon 测度**,从而可以用测度论的紧致性(Federer 型)得到"积分极限",再配合椭圆正则性把它提升为光滑解。这篇讲 varifold 与 stationarity 的最小必要内容。

> 相关笔记:[[Hausdorff_Convergence_and_Blaschke_Selection]]、[[Hölder_Space_and_Elliptic_Regularity]]、[[Sphere_Orientability_and_TwoSided]]。

## Varifold:把子流形当成测度

> [!ABSTRACT] Definition(varifold)
> 设 $\Sigma\subset S^{n+1}$ 是 $n$ 维(近似)子流形。把它的每个点 $x$ 连同其切平面 $T_x\Sigma$ 打包到 **Grassmann 丛** $G_n(TS^{n+1})$ 的一个点 $(x,T_x\Sigma)$ 上;$\Sigma$ 的面积密度在该丛上给出一个 **Radon 测度** $V$。这个"切平面 + 权"的抽象化就是 varifold,它让"一族曲面"能作为**测度**进行紧性论证。

> [!TIP] 关键好处
> 曲面是测度后,能对连续函数积分($\int f\,dV$),从而 $(x,P)\mapsto \operatorname{div}_P X(x)$ 这种量在**弱收敛**下保持。这使"极限仍是极小的"成为可能——见下面 stationarity。

## Stationarity:弱的"极小"

> [!ABSTRACT] Definition(stationarity)
> varifold $V$(或曲面 $\Sigma$)是 **stationary** 的,如果对任意光滑向量场 $X$,其第一变分为零:
> $$ \frac{d}{dt}\Big|_{t=0}\operatorname{Area}\bigl(\text{沿 }X\text{ 推移}\bigr)=0. $$
> 在闭情形下等价于散度形式
> $$ \int_\Sigma \operatorname{div}_{T\Sigma}X\,d\mu=0\qquad(\forall\, \text{光滑向量场 }X). $$
> "Stationary"是"极小"的**弱形式**(不求局部面积最小,只求一阶变分为零);它是极小曲面在积分/varifold 意义下的正确表述。

## 论文里的用法(§5, Prop 5.4)

> [!NOTE] 三步走
> 1. **局部图收敛**:由 [[Hausdorff_Convergence_and_Blaschke_Selection]] 得到 $\Sigma_j\to\Sigma_\infty$(Hausdorff),在各局部图上用 Arzelà–Ascoli 得图函数 $u_j^a\to u_\infty^a$ 在 $C^{1,\alpha}$ 收敛。
> 2. **varifold 收敛到 multiplicity-one**:因各图是一层的(见 [[Sphere_Orientability_and_TwoSided]] 的度1),$\Sigma_j\to\Sigma_\infty$ 作为 **varifold 以重数 1 收敛**。
> 3. **stationarity 传递**:由 $\operatorname{div}_{T\Sigma_j}X\,d\mu_j$ 的弱收敛,得极限 $\Sigma_\infty$ 满足 $\int\operatorname{div}_{T\Sigma_\infty}X\,d\mu_\infty=0$,故 $\Sigma_\infty$ **stationary**。再用椭圆正则性(见 [[Hölder_Space_and_Elliptic_Regularity]])把 stationary 解提升到 $C^\infty$,得光滑极小嵌入。

> [!WARNING] 为什么用 varifold 而不是直接的面积收敛
> 一族曲面可能无限接近(甚至逼近到"想重叠"),它们的面积可能收敛但几何"套叠"。用测度化(含切平面)的 varifold 收敛,能精确控制"每一层"的极限,再由度1图覆盖排除多层,保证 multiplicity-one。

> [!NOTE] 本节关系
> $$ \boxed{\Sigma\subset S^{n+1}}\ \longrightarrow\ \boxed{\text{Grassmann 丛上 Radon 测度 }V}\ \xrightarrow{\text{弱收敛}}\ \boxed{\text{varifold 极限}}\ \xrightarrow{\text{stationary}}\ \xrightarrow{\text{椭圆正则性}}\ \boxed{\text{光滑极小嵌入}}. $$
