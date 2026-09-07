---
tags:
  - Real_analysis
  - Measure_Theorem
  - Topology
  - Set_Theory
---

## 1. 概念定义 (Definitions)

设 $X$ 为一基础集，$\{E_k\}_{k=1}^{\infty}$ 为 $X$ 中的一列子集。

### 1.1 渐增集合序列 (Increasing Sequence of Sets)

若序列满足：

1. $E_1 \subset E_2 \subset E_3 \subset \cdots \subset E_k \subset \cdots$
    
2. $E = \bigcup_{k=1}^{\infty} E_k$
    

则称 $\{E_k\}$ **渐增趋于** $E$，记作 **$E_k \nearrow E$**。

### 1.2 渐减集合序列 (Decreasing Sequence of Sets)

若序列满足：

1. $E_1 \supset E_2 \supset E_3 \supset \cdots \supset E_k \supset \cdots$
    
2. $E = \bigcap_{k=1}^{\infty} E_k$
    

则称 $\{E_k\}$ **渐减趋于** $E$，记作 **$E_k \searrow E$**。

## 2. 测度论中的核心作用：测度的连续性 (Continuity of Measure)

在测度空间 $(X, \mathcal{A}, \mu)$ 中，渐进序列是将**可列可加性**转化为**极限运算**的桥梁（即允许测度符号 $\mu$ 与极限符号 $\lim$ 交换顺序）。

### 定理：测度的连续性

1. **上连续性 (Continuity from Below)**：
    
    若 $E_k \nearrow E$，则：
    
    $$\mu(E) = \mu\left(\bigcup_{k=1}^{\infty} E_k\right) = \lim_{k \to \infty} \mu(E_k)$$
    
2. **下连续性 (Continuity from Above)**：
    
    若 $E_k \searrow E$，**且存在某一个 $k_0$ 使得 $\mu(E_{k_0}) < \infty$**，则：
    
    $$\mu(E) = \mu\left(\bigcap_{k=1}^{\infty} E_k\right) = \lim_{k \to \infty} \mu(E_k)$$
    

> **笔记埋点 (Warning)**:
> 
> 下连续性中 $\mu(E_{k_0}) < \infty$ 的条件不可或缺。
> **反例**：在 $(\mathbb{R}, \mathcal{L}, m)$ 勒贝格测度空间下，令 $E_k = [k, \infty)$。显然 $E_k \searrow \emptyset$，此时 $m(E_k) = \infty \to \infty$，而 $m(\emptyset) = 0$。

### 测度论基本证明中的主要用途

- **可列可加性与有限可加性的等价性**：在已知有限可加的前提下，单调集合序列的连续性与可列可加性（Countable Additivity）是完全等价的。证明全空间测度性质时经常以此为切入点。
    
- **逼近定理的基石**：在证明 $\sigma$-代数上的某些性质时，通常先对有限交/有限并的简单集合（如开集、紧集）成立，再利用 $E_k \nearrow E$ 或 $E_k \searrow E$ 逐步扩张到整个 $\sigma$-代数（如 Borel 集）。
    

## 3. 拓扑空间与分析中的应用 (Topological & Analytical Applications)

在拓扑学或带有拓扑结构的测度空间（如 Radon 测度空间）中，渐变序列（尤其是渐减序列）常用于论证**紧性 (Compactness)**与**逼近性 (Approximation)**。

### 3.1 闭区间套定理与 Cantor 交集定理 (Cantor's Intersection Theorem)

在完备度量空间（或紧拓扑空间）中，渐减的非空闭集序列的极限性质是分析的核心：

- 若 $F_k \searrow F$，且每个 $F_k$ 是非空紧集，则极限集 $F = \bigcap_{k=1}^{\infty} F_k$ **必非空且为紧集**。
    
- 若进一步满足直径 $\text{diam}(F_k) \to 0$，则 $F$ 恰好包含**一个点**。
    

### 3.2 勒贝格测度的正则性 (Regularity of Lebesgue Measure)

渐进序列用于展现拓扑结构（开集、闭集）与测度结构的深刻联系。

对于任意勒贝格可测集 $E \subset \mathbb{R}^n$，都可以通过单调序列从“外部”和“内部”进行拓扑逼近：

1. **外部开集逼近**：存在一列渐减的开集 $G_k \searrow G$，使得 $E \subset G$ 且 $m(G \setminus E) = 0$。此时：
    
    $$m(E) = \lim_{k \to \infty} m(G_k)$$
    
2. **内部紧集逼近**：存在一列渐增的紧集（有界闭集）$K_k \nearrow K$，使得 $K \subset E$ 且 $m(E \setminus K) = 0$。此时：
    
    $$m(E) = \lim_{k \to \infty} m(K_k)$$
    

## 4. 延伸：集合的上下极限 (Liminf & Limsup)

如果集合序列 $\{E_k\}$ 不是单调的（既不渐增也不渐减），可以通过构造单调序列来定义其广义极限：

- **上限集 (Limit Superior)**：
    
    $$\limsup_{k \to \infty} E_k = \bigcap_{n=1}^{\infty} \left( \bigcup_{k=n}^{\infty} E_k \right)$$
    
    _(注：内部 $U_n = \bigcup_{k=n}^{\infty} E_k$ 是一个渐减序列 $U_n \searrow \limsup E_k$)_
    
- **下限集 (Limit Inferior)**：
    
    $$\liminf_{k \to \infty} E_k = \bigcup_{n=1}^{\infty} \left( \bigcap_{k=n}^{\infty} E_k \right)$$
    
    _(注：内部 $V_n = \bigcap_{k=n}^{\infty} E_k$ 是一个渐增序列 $V_n \nearrow \liminf E_k$)_
    

当且仅当 $\limsup_{k \to \infty} E_k = \liminf_{k \to \infty} E_k = E$ 时，称集合序列收敛，且其极限为 $E$。