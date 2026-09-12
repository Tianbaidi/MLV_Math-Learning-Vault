---
tags:
  - Topology
  - Set_Theory
  - Exercises
---
>关于拓扑粗细的证明，本质上是比较一个集合上两个拓扑族（开集族）的包含关系。在拓扑学中，证明的思路通常分为全局判据、局部判据和映射判据三大类。下面从定义出发，系统梳理几种最核心的证明方法及其严格推导。

### 1. 基础定义

设 $X$ 为一个集合，$\mathcal{T}_1$ 和 $\mathcal{T}_2$ 是 $X$ 上的两个拓扑。

- 若 $\mathcal{T}_1 \subseteq \mathcal{T}_2$（即 $\mathcal{T}_1$ 的每个开集都在 $\mathcal{T}_2$ 中），则称 $\mathcal{T}_1$ 粗于（或弱于）$\mathcal{T}_2$，$\mathcal{T}_2$ 细于（或强于）$\mathcal{T}_1$。
    
- 若 $\mathcal{T}_1 \subsetneq \mathcal{T}_2$，则称 $\mathcal{T}_1$ 严格粗于 $\mathcal{T}_2$。
    

### 2. 最核心判据：恒等映射连续性（必考证明）

**定理：** 设 $(X, \mathcal{T}_1)$ 和 $(X, \mathcal{T}_2)$ 为同一底集上的两个拓扑空间，则

$$\mathcal{T}_1 \subseteq \mathcal{T}_2 \iff \text{恒等映射 } i:(X, \mathcal{T}_2) \to (X, \mathcal{T}_1) \text{ 是连续的.}$$

**证明（双向推导）：**

- **（必要性 $\Rightarrow$）：** 若 $\mathcal{T}_1 \subseteq \mathcal{T}_2$，取任意 $U \in \mathcal{T}_1$。由于恒等映射满足 $i^{-1}(U) = U$，又因为 $U \in \mathcal{T}_1 \subseteq \mathcal{T}_2$，所以 $i^{-1}(U) \in \mathcal{T}_2$。根据连续映射定义，$i$ 连续。
    
- **（充分性 $\Leftarrow$）：** 若 $i:(X, \mathcal{T}_2) \to (X, \mathcal{T}_1)$ 连续，则对任意 $U \in \mathcal{T}_1$，有 $i^{-1}(U) = U \in \mathcal{T}_2$。这说明 $\mathcal{T}_1$ 中的任意元素都属于 $\mathcal{T}_2$，故 $\mathcal{T}_1 \subseteq \mathcal{T}_2$。
    

证毕。 这个证明是证明拓扑粗细最简洁、最常用的工具。

### 3. 基于基（Basis）或邻域基的局部判据

当拓扑由基生成时，我们只需要检验基元素即可，无需检验全体开集。

**定理：** 设 $\mathcal{B}_1$ 和 $\mathcal{B}_2$ 分别是 $\mathcal{T}_1$ 和 $\mathcal{T}_2$ 的基，则 $\mathcal{T}_1 \subseteq \mathcal{T}_2$ 的充要条件是：

$$\forall x \in X, \quad \forall B_1 \in \mathcal{B}_1 \text{ 且 } x \in B_1, \quad \exists B_2 \in \mathcal{B}_2 \text{ 使得 } x \in B_2 \subseteq B_1.$$

**证明：**

- **（必要性）：** 因为 $B_1 \in \mathcal{T}_1 \subseteq \mathcal{T}_2$，所以 $B_1$ 是 $\mathcal{T}_2$ 中的开集。由基的定义，对于该开集 $B_1$ 和其中的点 $x$，必然存在基元素 $B_2 \in \mathcal{B}_2$ 满足 $x \in B_2 \subseteq B_1$。
    
- **（充分性）：** 取任意 $U \in \mathcal{T}_1$。对任意 $x \in U$，存在 $B_1 \in \mathcal{B}_1$ 使 $x \in B_1 \subseteq U$。由题设，存在 $B_2 \in \mathcal{B}_2$ 使 $x \in B_2 \subseteq B_1 \subseteq U$。因此 $U$ 可以表示为若干 $\mathcal{B}_2$ 元素的并集（即 $U = \bigcup_{x \in U} B_{2,x}$），所以 $U \in \mathcal{T}_2$。故 $\mathcal{T}_1 \subseteq \mathcal{T}_2$。
    

### 4. 基于闭包（Closure）的判据

拓扑越细，开集越多，点越“不容易”靠近一个集合，因此闭包越小。

**定理：** $\mathcal{T}_1 \subseteq \mathcal{T}_2$ 当且仅当对任意子集 $A \subseteq X$，都有 $\overline{A}^{\mathcal{T}_2} \subseteq \overline{A}^{\mathcal{T}_1}$（即在较细拓扑中的闭包包含在较粗拓扑的闭包中）。

**证明：**

- **（必要性 $\Rightarrow$）：** 设 $x \in \overline{A}^{\mathcal{T}_2}$，即 $x$ 的任意 $\mathcal{T}_2$-邻域都与 $A$ 相交。因为 $\mathcal{T}_1 \subseteq \mathcal{T}_2$，任意 $\mathcal{T}_1$-邻域 $U$ 也是 $\mathcal{T}_2$-邻域，故 $U \cap A \neq \emptyset$。因此 $x \in \overline{A}^{\mathcal{T}_1}$。得证 $\overline{A}^{\mathcal{T}_2} \subseteq \overline{A}^{\mathcal{T}_1}$。
    
- **（充分性 $\Leftarrow$）：** 取任意 $U \in \mathcal{T}_1$，令 $A = X \setminus U$（即 $A$ 是 $\mathcal{T}_1$-闭集）。在 $\mathcal{T}_1$ 中，$\overline{A}^{\mathcal{T}_1} = A$。由假设 $\overline{A}^{\mathcal{T}_2} \subseteq A$，而闭包必包含自身，故 $\overline{A}^{\mathcal{T}_2} = A$，说明 $A$ 也是 $\mathcal{T}_2$-闭集，因此其补集 $U \in \mathcal{T}_2$。故 $\mathcal{T}_1 \subseteq \mathcal{T}_2$。
    

同理，内部（Interior）的判据方向相反：$\mathcal{T}_1 \subseteq \mathcal{T}_2 \iff \operatorname{Int}_{\mathcal{T}_1}(A) \subseteq \operatorname{Int}_{\mathcal{T}_2}(A)$。

### 5. 基于序列/网收敛的判据（适用于第一可数空间）

虽然一般拓扑空间中序列收敛不能完全决定拓扑，但网（Net）可以。若拓扑越细，收敛的条件越苛刻（收敛的点越少）。

**定理：** 若 $\mathcal{T}_1 \subseteq \mathcal{T}_2$，则在 $\mathcal{T}_2$ 中收敛于 $x$ 的网（或序列）必然在 $\mathcal{T}_1$ 中也收敛于 $x$。

**证明：** 设网 $(x_\lambda)$ 在 $\mathcal{T}_2$ 中收敛于 $x$。取任意 $\mathcal{T}_1$-邻域 $U$ 包含 $x$，由于 $U \in \mathcal{T}_2$，由 $\mathcal{T}_2$-收敛性，存在 $\lambda_0$ 使得所有 $\lambda \ge \lambda_0$ 有 $x_\lambda \in U$。故在 $\mathcal{T}_1$ 中也收敛于 $x$。

_（注：反向不总是成立，除非拓扑可由收敛唯一确定，如第一可数空间。在一般证明中，若题目要求证明粗细，通常不用这个作为充要条件，但可作为必要性的辅助。）_

### 6. 泛性质（Universal Property）：最粗拓扑与最细拓扑

在构造拓扑时，常利用泛性质来证明其“最粗”或“最细”。

- **始拓扑（Initial Topology，如子空间、乘积拓扑）：** 设映射族 $f_\alpha: X \to Y_\alpha$，使得所有 $f_\alpha$ 连续的最粗拓扑 $\mathcal{T}$。
    
    - **证明思路：** 设 $\mathcal{T}'$ 是任意使所有 $f_\alpha$ 连续的另一拓扑。则对所有 $\alpha$ 和开集 $U_\alpha \subseteq Y_\alpha$，必须有 $f_\alpha^{-1}(U_\alpha) \in \mathcal{T}'$。而 $\mathcal{T}$ 正是由这些“子基”生成的拓扑，故 $\mathcal{T} \subseteq \mathcal{T}'$。因此 $\mathcal{T}$ 是最粗的。
        
- **终拓扑（Final Topology，如商拓扑）：** 设映射 $p: X \to Y$，商拓扑 $\mathcal{T}_q = \{ U \subseteq Y \mid p^{-1}(U) \in \mathcal{T}_X \}$ 是使 $p$ 连续的最细拓扑。
    
    - **证明思路：** 若另一拓扑 $\mathcal{T}'$ 使 $p$ 连续，则对任意 $V \in \mathcal{T}'$，有 $p^{-1}(V) \in \mathcal{T}_X$。根据商拓扑定义，$V \in \mathcal{T}_q$。故 $\mathcal{T}' \subseteq \mathcal{T}_q$。因此 $\mathcal{T}_q$ 是最细的。

Example.[[8 映射空间的拓扑#25#25]] #Mapping_Space 

证明“一致收敛拓扑 $\mathcal{T}_{\text{u.c.}}$ 细于乘积拓扑 $\mathcal{T}_{\text{prod}}$，且粗于箱拓扑 $\mathcal{T}_{\text{box}}$”，核心是证明以下包含链：

$$\mathcal{T}_{\text{prod}} \subseteq \mathcal{T}_{\text{u.c.}} \subseteq \mathcal{T}_{\text{box}}$$

为了逻辑清晰，我们分两步证明。关键技巧：利用你定义的一致度量 $d_u(f,g) = \sup_{x} \frac{d_Y(f(x),g(x))}{1+d_Y(f(x),g(x))}$ 的特殊性质（该比值始终 $\le 1$，且能控制逐点距离）。

### 第一步：证明 $\mathcal{T}_{\text{prod}} \subseteq \mathcal{T}_{\text{u.c.}}$（一致拓扑更细）

**思路：** 乘积拓扑由子基（Subbasis） $S(x_0, U) = \{f \in M(X,Y) \mid f(x_0) \in U\}$（其中 $x_0 \in X$，$U \subset Y$ 为开集）生成。只需证明每一个这样的子基元素在一致拓扑中都是开集。

**严格证明：**

取任意子基元素 $S = \{f \mid f(x_0) \in U\}$，其中 $x_0 \in X$，$U$ 是 $Y$ 中的开集。任取 $f \in S$，则 $f(x_0) \in U$。

因为 $U$ 是度量空间 $Y$ 中的开集，存在半径 $r > 0$，使得开球 $B_Y(f(x_0), r) \subset U$。

现在我们要找一个一致度量下的开球 $B_{d_u}(f, \alpha)$ 完全包含在 $S$ 中。

令 $\alpha = \frac{r}{1+r}$（注意 $0 < \alpha < 1$）。对于任意 $g \in B_{d_u}(f, \alpha)$，有：

$$d_u(f,g) = \sup_{x \in X} \frac{d_Y(f(x),g(x))}{1+d_Y(f(x),g(x))} < \alpha = \frac{r}{1+r}$$

特别地，对于点 $x_0$，代入可得：

$$\frac{d_Y(f(x_0),g(x_0))}{1+d_Y(f(x_0),g(x_0))} < \frac{r}{1+r}$$

解这个不等式（设 $t = d_Y(f(x_0),g(x_0))$，则 $\frac{t}{1+t} < \frac{r}{1+r} \implies t < r$），得到：

$$d_Y(f(x_0),g(x_0)) < r$$

因此 $g(x_0) \in B_Y(f(x_0), r) \subset U$，所以 $g \in S$。故 $B_{d_u}(f, \alpha) \subset S$。

因为任意 $f \in S$ 都有一个包含在 $S$ 内的一致开球，所以 $S$ 在 $\mathcal{T}_{\text{u.c.}}$ 中是开集。既然所有子基元素都是开的，生成它们的乘积拓扑自然包含于一致拓扑。得证 $\mathcal{T}_{\text{prod}} \subseteq \mathcal{T}_{\text{u.c.}}$。

### 第二步：证明 $\mathcal{T}_{\text{u.c.}} \subseteq \mathcal{T}_{\text{box}}$（一致拓扑更粗）

**思路：** 箱拓扑的基是所有笛卡尔积 $\prod_{x \in X} U_x$，其中每个 $U_x \subset Y$ 都是开集（对 $x$ 的选取没有限制）。只需证明一致拓扑的每一个度量开球，在箱拓扑中都是开集。

**严格证明：**

取任意一致开球 $B_{d_u}(f, \epsilon)$，其中 $f \in M(X,Y)$，$\epsilon > 0$。

不失一般性，我们可以取 $0 < \epsilon < 1$（因为若 $\epsilon \ge 1$，由于 $d_u \le 1$，开球就是全集，显然是箱开的）。

为了在箱拓扑中构造一个包含 $f$ 的小邻域，我们选取一个比 $\epsilon$ 更小的上界 $\delta$。令：

$$\delta = \frac{\epsilon}{1+\epsilon} \quad (\text{显然 } 0 < \delta < \epsilon < 1)$$

对于每一个指标 $x \in X$，定义 $Y$ 中的开集：

$$U_x := B_Y(f(x), \delta) = \{y \in Y \mid d_Y(y, f(x)) < \delta\}$$

现在考虑箱拓扑中的基本开集：

$$O := \prod_{x \in X} U_x$$

显然 $f \in O$（因为 $f(x) \in U_x$ 对所有 $x$ 成立）。接下来证明 $O \subset B_{d_u}(f, \epsilon)$：

任取 $g \in O$，则对每一个 $x \in X$，都有 $d_Y(f(x), g(x)) < \delta$。

因为函数 $t \mapsto \frac{t}{1+t}$ 是严格单调递增的，所以：

$$\frac{d_Y(f(x), g(x))}{1+d_Y(f(x), g(x))} < \frac{\delta}{1+\delta}$$

将 $\delta = \frac{\epsilon}{1+\epsilon}$ 代入右边：

$$\frac{\delta}{1+\delta} = \frac{\frac{\epsilon}{1+\epsilon}}{1 + \frac{\epsilon}{1+\epsilon}} = \frac{\epsilon}{1+2\epsilon} < \epsilon$$

因此，对所有 $x \in X$，都有 $\frac{d_Y(f(x), g(x))}{1+d_Y(f(x), g(x))} < \epsilon$。取上确界，得到：

$$d_u(f,g) = \sup_{x \in X} \frac{d_Y(f(x),g(x))}{1+d_Y(f(x),g(x))} \le \frac{\epsilon}{1+2\epsilon} < \epsilon$$

（注意这里严格小于 $\epsilon$，即使取上确界也不影响，因为所有项都被严格控制在 $\frac{\epsilon}{1+2\epsilon}$ 之下。）

所以 $g \in B_{d_u}(f, \epsilon)$，即 $O \subset B_{d_u}(f, \epsilon)$。

我们找到了一个包含 $f$ 的箱拓扑开集 $O$，且 $O$ 完全包含在一致开球内。因此该一致开球是箱拓扑中的开集。既然一致拓扑的基（所有开球）都是箱开集，则 $\mathcal{T}_{\text{u.c.}} \subseteq \mathcal{T}_{\text{box}}$ 得证。