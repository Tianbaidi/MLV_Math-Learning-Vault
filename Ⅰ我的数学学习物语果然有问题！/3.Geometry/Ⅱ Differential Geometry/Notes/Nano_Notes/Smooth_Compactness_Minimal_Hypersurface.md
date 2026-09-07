---
tags:
  - Geometry
  - Differential_Geometry
  - Compactness
  - Minimal_Hypersurface
---

> 本文服务于论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §5(Prop 5.4)。这是把"一族闭连通嵌入极小超曲面"变成"一个光滑极小极限"的**全局紧致性定理**,也是 §6 证明主定理的最后一块拼图。

> 相关笔记:[[Tubular_Neighborhood]]、[[Focal_Point_of_Hypersurface]]、[[Rolling_Radius]]、[[Normal_Jacobian]]、[[Hausdorff_Convergence_and_Blaschke_Selection]]、[[Varifold_and_Stationarity]]、[[Hölder_Space_and_Elliptic_Regularity]]。

## 命题(Prop 5.4)

> [!ABSTRACT] Theorem(光滑嵌入紧致性)
> 设 $F_j:M_j^n\hookrightarrow S^{n+1}(1)$ 是一列**闭连通嵌入极小**超曲面,且 $\sup_{M_j}|A_j|\le K$。则(取子列后)存在闭连通光滑流形 $M_\infty$、光滑极小嵌入 $F_\infty:M_\infty\hookrightarrow S^{n+1}(1)$ 及微分同胚 $\psi_j:M_\infty\to M_j$,使
> $$ F_j\circ\psi_j\to F_\infty\quad\text{光滑}, $$
> 且对充分大的 $j$,像 $F_j(M_j)$ 是 $F_\infty(M_\infty)$ 上的 **single-valued 球面法图**。

## 三步走(§5)

> [!NOTE] 论证链条
> 1. **局部图 + Hausdorff 收敛**:由 [[Tubular_Neighborhood]] 得各点局部球面图(Lemma 5.3),再由 [[Hausdorff_Convergence_and_Blaschke_Selection]](Blaschke 选择)取 Hausdorff 极限 $\Sigma_\infty$,在图坐标上(平行移动套到固定切空间)用 Arzelà–Ascoli 得 $u_j^a\to u_\infty^a$ 在 $C^{1,\alpha}$ 收敛。
> 2. **varifold 收敛 + 度1单层**:由 [[Varifold_and_Stationarity]],从"有限单层图覆盖"得到 $\Sigma_j\to\Sigma_\infty$ 以**重数 1** 收敛,并把 stationarity 传给极限。
> 3. **椭圆提升到光滑**:stationary 的 $C^{1,1}$ 图函数 $u$ 弱满足面积泛函的 Euler–Lagrange 方程,经 Sobolev/Schauder(见 [[Hölder_Space_and_Elliptic_Regularity]])由 $C^{1,1}\Rightarrow C^{2,\alpha}\Rightarrow C^\infty$,故 $\Sigma_\infty$ 是光滑极小嵌入。
> 4. **度1覆盖**:投影 $\pi_\infty|_{\Sigma_j}:\Sigma_j\to\Sigma_\infty$ 是局部微分同胚、像开又闭、在连通 $\Sigma_\infty$ 上故为覆盖;单层图坐标里 $\|D\Pi_j-I\|_{C^0}<1/2$ 给单射,再因 $d(\cdot,\Sigma_\infty)\to0$ 得每纤维恰一点 ⟹ 覆盖度 1 ⟹ $\pi_\infty|_{\Sigma_j}$ 是微分同胚。于是 $F_j\circ\psi_j(x)=\cos v_j(x)F_\infty(x)+\sin v_j(x)\nu_\infty(x)$ 且 $v_j\to0$ 光滑。

> [!WARNING] 两个假设都必需(Remark 5.5)
> - **曲率界**排除 Wiygul"堆叠 Clifford 环面、颈缩"的行为(那会使 $\sup|A_j|$ 无界)。
> - **嵌入性**排除"对 Clifford 的 $S^1$ 因子取度 $d$ 覆盖"的浸入族(它们有相同 $|A|$、$S$、$f_3$ 但面积/覆盖重数随 $d$ 增大)。

> [!NOTE] 本节关系
> $$ \boxed{\sup|A_j|\le K}\ \xrightarrow{\text{Blaschke+Hausdorff}}\ \boxed{\text{局部 }C^{1,\alpha}\text{ 图收敛}}\ \xrightarrow{\text{varifold 重数1}}\ \boxed{\text{stationary}}\ \xrightarrow{\text{椭圆提升}}\ \boxed{\text{光滑极小极限 }F_\infty}. $$
