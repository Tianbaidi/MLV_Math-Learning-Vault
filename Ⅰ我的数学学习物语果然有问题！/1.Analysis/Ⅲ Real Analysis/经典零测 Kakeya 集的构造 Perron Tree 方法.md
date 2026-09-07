---
tags:
  - Real_analysis
  - Measure_Theorem
  - Kakeya_Problem
  - Grometric_Measure_Theory
---

> 本笔记为对南科大实分析暑期项目的预习，参考教材为 $\text{K. J. Falconer, }\textit{The Geometry of Fractal Sets}$ 的 96-99面。这一部分介绍了 $\text{Besicovitch}$ 集的起源以及 $\text{Kakeya}$ 问题的起源，随后我们引入一个工具称为 $\text{Perron Tree}$ 来构造这个经典的零测 $\text{Kakeya}$ 集。

## Background

我们要从 $\text{Besicovitch}$ 的想法出发，他构造出的 $\text{Besicovitch}$ 集在经过一定变化之后可以解决当时几乎同期提出的任意小测度的 $\text{Kakeya}$ 问题的解。

$\text{Besicovitch}$ 的出发点是为了研究以下问题：

> [!Question] 问题 1：黎曼可积函数的 Fubini 型问题
> 如果 $f$ 是定义在平面上的黎曼可积函数，是否总能找到一对正交的坐标轴，使得对于所有 $y$，$\displaystyle \int f(x,y)\,dx$ 都作为黎曼积分存在，并且关于 $y$ 的结果函数也是黎曼可积的？也就是说
> $$
> \int\left( \int f(x,y)\,dx \right)dy
> $$
> 在某种意义下是否总是良好？

$\text{Besicovitch}$ 想着构造一个极端的集合，来创造反例，满足 $F \subset \mathbb{R}^2$：

- $F$ 是紧致的；
- $\mathcal{L}^2 (F)=0$，但是 $F$ 含有每个方向的一条线段。

定义 $f(x,y)=\chi_{F_{0}}(x,y)$ 满足 $F_{0}=F \cap \mathbb{Q}^2$，于是就有：

- $f$ 只在"非常稀疏的点集上"为 $1$；
- 几乎处处为 $0$。

由于 $F$ 含有每一个方向的一条线段，于是对任意方向 $\theta$，都存在一条线段 $L_{\theta}\subset F$，在这条线段上 $F_{0}$ 与其补集呈现紧密且交错的形态出现。现在的形态很类似我们的狄利克雷函数。于是我们对其做横截积分的时候，每个方向都存在着切片不可黎曼积分的情况，就被他得逞了。这个集合就被称为 $\text{Besicovitch}$ 集，即 $\mathscr{L}^2 (F)=0$。

$\text{Kakeya}$ 问题则是来自一个几何运动问题：

> [!Question] 问题 2：Kakeya 旋转问题
> 在平面中，令一条单位线段可以在其中旋转 $180^{\circ}$ 回到原来位置但是方向相反的最小面积的集合是什么？

最初的直觉是等边三角形，如果我们不限定其凸性，得到凹的图形，得到更小的面积。$\text{Besicovitch}$ 集的构造经过一定的修改，可以得到任意小的面积的 $\text{Kakeya}$ 集。

## Main Tools & Construction

我们用到的核心工具为 $\text{Perron Tree}$。

> [!Success] Lemma 1 (Base Triangle Slide)
> 设 $T_{1}$ 和 $T_{2}$ 为底边在直线 $L$ 上的两个相邻的三角形，底边长为 $b$，高为 $h$。取 $\frac{1}{2}<\alpha<1$，如果 $T_{2}$ 沿着 $L$ 滑动 $2(1-\alpha)b$ 与 $T_{1}$ 重叠，则所得图形 $S$ 为 $T_{1}\cup T_{2}$ 的 **位似** 三角形 $T$ 以及辅助的两个三角形组成，我们有
> $$
> \mathcal{L}^2(T)=\alpha^2 \mathcal{L}^{2}(T_{1}\cup T_{2})
> $$
> 我们可以得到面积减少的值为
> $$
> \Delta = \mathcal{L}^{2}(T_{1}\cup T_{2})-\mathcal{L}^{2}(S)=\mathcal{L}^{2}(T_{1}\cup T_{2})(1-\alpha)(3\alpha-1)
> $$

> [!Success] Lemma 2 (Repeated Subdivision)
> 设 $T$ 为底边在直线 $L$ 上的一个三角形。将 $T$ 的底边分为 $2^k$ 个相等的线段，并将每个分点与对顶点相连，形成 $2^k$ 个基本三角形 $T_{1}\cdots T_{2^k}$。通过选取足够大的 $k$，可以沿 $L$ 平移这些基本三角形，使得所得（闭）图形 $S$ 的面积可以任意小。

### Area Reduction Tracking

 在合并基本三角形的树状级联过程中，第 $r$ 阶段的最小面积减少量随因子 $\alpha^{2(r-1)}$ 缩放：
 - **Stage 1:** $\ge (3\alpha - 1)(1 - \alpha)\mathcal{L}^2(T)$
 - **Stage 2:** $\ge (3\alpha - 1)(1 - \alpha)\alpha^2 \mathcal{L}^2(T)$
 - $\dots$
 - **Stage $k$:** $\ge (3\alpha - 1)(1 - \alpha)\alpha^{2(k-1)}\mathcal{L}^2(T)$

 将各个阶段的减少量作为等比级数求和，最终图形 $S$ 的面积满足：
 $$
 \mathcal{L}^2(S) \le \mathcal{L}^2(T) - (3\alpha - 1)(1 - \alpha)\sum_{r=1}^{k} \alpha^{2(r-1)} \mathcal{L}^2(T)
 $$

 由于
 $$
 \sum_{r=1}^{k} \alpha^{2(r-1)} = \frac{1 - \alpha^{2k}}{1 - \alpha^2} = \frac{1 - \alpha^{2k}}{(1-\alpha)(1+\alpha)}
$$
 代入上式消去 $(1-\alpha)$ 项，简化为：
 $$
 \mathcal{L}^2(S) \le \left( 1 - \frac{(3\alpha - 1)(1 - \alpha^{2k})}{1 + \alpha} \right) \mathcal{L}^2(T)
 $$

 令 $k \to \infty$（则 $\alpha^{2k} \to 0$），并令 $\alpha \to 1^-$（则 $\frac{3\alpha - 1}{1 + \alpha} \to 1$），乘数算子趋于 $0$：
 $$
 \mathcal{L}^2(S) \to 0
 $$

 即对于任意 $\epsilon > 0$，均可通过选取足够大的 $k$ 实现 $\mathcal{L}^2(S) < \epsilon$。

### Inductive Limit

 我们构造一个单调递减的紧致图形序列 $S_i$ 嵌套在开集序列 $V_i$ 中：
 - **Step 1:** 自 $T$ 得到 $S_1$ 满足 $\mathcal{L}^2(S_1) \le 2^{-2}$。选取开邻域 $V_1 \supset S_1$ 满足 $\mathcal{L}^2(\overline{V}_1) \le 2\mathcal{L}^2(S_1) \le 2^{-1}$。
 - **Step 2:** 在 $V_1$ 内对 $S_1$ 组件进行平移得到 $S_2$ 满足 $\mathcal{L}^2(S_2) \le 2^{-3}$。选取开邻域 $V_2$ 满足 $S_2 \subset V_2 \subset V_1$且 $\mathcal{L}^2(\overline{V}_2) \le 2\mathcal{L}^2(S_2) \le 2^{-2}$。
 - $\vdots$
 - **Step $i+1$:** 在 $V_i$ 内构造 $S_{i+1} \subset V_{i+1} \subset V_i$ 满足 $\mathcal{L}^2(\overline{V}_{i+1}) \le 2\mathcal{L}^2(S_{i+1}) \le 2^{-i}$。

 定义最终目标集 $F$ 为开集闭包的无穷交集：
 $$
 F = \bigcap_{i=1}^{\infty} \overline{V}_i
 $$

 由测度的连续性：
 $$
 \mathcal{L}^2(F) = \lim_{i \to \infty} \mathcal{L}^2(\overline{V}_i) = 0
 $$

### Directional Verification

 我们必须保证极限集 $F$ 仍然包含扇区内每个方向 $\theta$ 的单位线段。
 1. 对每个开集 $V_i$，由平移机制（不改变线段斜率），均存在方向为 $\theta$ 的单位线段 $M_i = [a_i, b_i] \subset V_i$。
 2. 即满足 $a_i, b_i \in V_i$，且 $|a_i - b_i| = 1$。
 3. 依据空间紧致性（标准选择定理），端点序列必有收敛子列：
    $$
    \{a_{i_j}\} \to a, \quad \{b_{i_j}\} \to b \implies M_i \to M
    $$
 4. 由于闭包序列单调嵌套（当 $i \ge j$ 时 $\overline{V}_i \subset \overline{V}_j$），故线段序列的极限点必留在每个固定的 $\overline{V}_j$ 内。
 5. 从而：
    $$
    a, b \in \bigcap_{i=1}^{\infty} \overline{V}_i = F \implies M \subset F
    $$

> [!NOTE] Theory（Kakeya 集的零测构造）
> 将该结构在平面上做三次旋转复制（$0^\circ, 60^\circ, 120^\circ$）并取并集，即得到一个包含平面所有方向单位线段的平面零测 $\text{Kakeya}$ 集。

