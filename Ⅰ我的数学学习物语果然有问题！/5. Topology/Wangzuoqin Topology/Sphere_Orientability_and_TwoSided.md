---
tags:
  - Topology
  - Orientability
  - Hypersurface
---

> 论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §2 规定超曲面是 **two-sided**(法线丛平凡),并说"在 $S^{n+1}$ 中,two-sided 等价于 $M$ 可定向";§5 又用到"嵌入超曲面把球面分成两个区域"和"度 1 覆盖"来保证收敛是一层(single-valued normal graph)。这篇把这几件事说清楚。

> 相关笔记:[[Hypersurface_in_Sphere]]、[[Hausdorff_Convergence_and_Blaschke_Selection]]。

## 超曲面的 two-sided 与可定向性

> [!ABSTRACT] Definition(two-sided)
> 浸入 $F:M^n\to S^{n+1}$ 称为 **two-sided**,如果它的法线丛 $N M$ 平凡(即存在**整体**连续单位法向量场 $\nu$)。
>
> 由于 $S^{n+1}$ 可定向,$M$ 的 two-sided 性**等价于** $M$ 可定向。对闭嵌入超曲面,若它分离球面(见下),two-sided 自动成立。

> [!NOTE] 直观
> "可定向"＝能在 $M$ 上一致地选择朝向;"two-sided"＝能在 $M$ 的一侧整体地选一个法向,不绕一圈后"翻面"。对超曲面(余维 1)二者一致。

## 嵌入超曲面分离球面

> [!Success] Lemma(分离)
> 设 $F:M^n\hookrightarrow S^{n+1}$( $n\ge2$ )是**闭连通嵌入**超曲面。则 $F(M)$ 把 $S^{n+1}$ 分成**两个**连通开区域 $\Omega_+$、$\Omega_-$,且 $\partial\Omega_\pm=F(M)$。
>
> 直觉:球面上的闭连通嵌入超曲面就像赤道,两侧各有一"半球"(这与 $\mathbb R^{n+1}$ 中的嵌入超曲面情形类似,由 Jordan–Brouwer 型的分离定理保证)。

于是每个 $\Omega_\pm$ 的闭包是以 $F(M)$ 为边界、带诱导度量的**紧流形**。论文 §5 正是对 $\Omega_\pm$ 用 Howard 滚动定理,得到两侧的滚动半径相等,从而给出双侧正常数注射半径。

## 度 1 覆盖论证(§5 的 single-valued graph)

> [!NOTE] 这一步在 §5 的作用
> 论文需要两件事:**收敛是 multiplicity-one**(不叠多层),且"最终 $\Sigma_j$ 是 $\Sigma_\infty$ 上的 **single-valued spherical normal graph**"。关键在于:
> 1. 因 $\Sigma_j$ 嵌入且分离球面,投影 $\pi_\infty|_{\Sigma_j}:\Sigma_j\to\Sigma_\infty$ 是局部微分同胚,像开且闭、又在连通的 $\Sigma_\infty$ 上,故为**有限覆盖**。
> 2. 在小的单层图坐标里,$D\Pi_j$ 逼近恒等( $\|D\Pi_j-I\|_{C^0}<1/2$ ),沿线段积分得 $|\Pi_j(v)-\Pi_j(w)|\ge\frac12|v-w|$,从而 $\Pi_j$ **单射**。
> 3. 因 $\Sigma_j$ 紧且 $\Sigma_j\to\Sigma_\infty$ 的 Hausdorff 距离趋于 0,纤维内每个点都在这个坐标球内,故纤维恰含一点——**覆盖度为 1**。
>
> 合起来,$\pi_\infty|_{\Sigma_j}$ 是微分同胚,$\Sigma_j$ 就可用一个整体法向 $\nu_\infty$ 写成 $F_j\circ\psi_j(x)=\cos v_j(x)\,F_\infty(x)+\sin v_j(x)\,\nu_\infty(x)$,其中 $v_j\to0$。

## 为什么"嵌入 + 分离"这么关键(对比浸入)

> [!WARNING] 嵌入 vs 浸入
> 只要求**浸入**时,可以对 Clifford 嵌入的 $S^1$ 因子做度 $d$ 覆盖,得到**同一** $|A|$、$S$、$f_3$ 而**面积与覆盖重数随 $d$ 增**的浸入族——没有度 1/单层性。论文 §5 的分离性 + 嵌入性正是用来排除这种"多层覆盖导致的散度(积累)的曲面"。见论文 Remark 5.5。

> [!NOTE] 本节关系
> $$ \boxed{S^{n+1}\text{ 可定向}}\ \Longleftrightarrow\ \boxed{M\text{ 可定向}\iff M\text{ two-sided}}\ \xrightarrow{\text{嵌入分离球面}}\ \boxed{\Omega_\pm\text{ 紧}}\ \Longrightarrow\ \boxed{\text{度1覆盖}\Rightarrow\text{single-valued graph}}. $$
