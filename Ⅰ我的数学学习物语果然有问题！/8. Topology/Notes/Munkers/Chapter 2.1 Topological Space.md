---
tags:
  - Topology
  - Munkres
  - Set_Theory
---


> [!QUOTE] Definition 1
> 集合 $X$ 上的一个 拓扑（topology）是 $X$ 的一个子集族 $\mathcal{T}$ 有以下性质：
> 1. $\varnothing$ 和 $X$ 在 $\mathcal{T}$ 上
> 2. $\mathcal{T}$ 的任意子族元素的并在 $\mathcal{T}$ 中
> 3. $\mathcal{T}$ 的任意有限子族的交在 $\mathcal{T}$ 中
> 一个指定拓扑 $\mathcal{T}$ 的集合 $X$ 就称为一个 **拓扑空间** （Topological Space）

如果 $X$ 是一个带有拓扑 $\mathcal{T}$ 的拓扑空间， $X$ 的子集 $U$ 若为集族 $\mathcal{T}$ 元素 , 则称 $U$ 是 $X$ 中的 **开集** (Open set) 。拓扑空间是集合 X 连同其子集的一个族（称为开集族），使得 $\varnothing$ 和 $X$ 在其中，且该族对任意并和有限交封闭。

我们也用有序偶对来表示拓扑 $(X,\mathcal{T})$ .


> [!Example] 拓扑的几个个类型
> 1. 如果 $X$ 为任意一个集合 ，$X$ 的所有子集的族是 $X$ 的一个拓扑 —— 我们称为 **离散拓扑** (Discrete Topology) 
> 2. 仅仅由 $X$ 和 $\varnothing$ 组成的族也是一个拓扑，称之为 **密着拓扑** (Indiscrete Topology)  或者 **平庸拓扑** (Trivial Topology) 
> 3. 设 $X$ 是一个集合， $\mathcal{T}_{f}$ 是一个使得 $X-U$ 或者是有限集或者是等于 $X$ 的那些 $X$ 的子集 $U$ 的全体。那么  $\mathcal{T}_{f}$ 是 $X$ 上的一个拓扑，我们称为 **有限维拓扑** (Finite complement Topology) . 由于 $X-X=\varnothing$ 是有限集， $X-\varnothing=X$ , 所以 $X$ 与 $\varnothing$ 都在 $\mathcal{T}_{f}$ 中 .  
> 4. 设 $X$ 是一个集合， $\mathcal{T}_{c}$ 是使得 $X-U$ 是可数集或者等于 $X$ 的所有 $X$ 的子集 $U$ 的全体。容易验证， $\mathcal{T}_{c}$ 是 $X$ 上的一个拓扑

对于 3. 若 $\{ U_{\alpha} \}$ 是 $\mathcal{T}_{f}$ 中非空元素的一个**加标族** (indexed family) ，为了证明 $\cup U_{\alpha}$ 在 $\mathcal{T}_{f}$ 中，只要确定 
$$X-\cup U_{\alpha}=\cap(X-U_{\alpha})$$
每个集合 $X-U_{\alpha}$ 是有限集，所以右边的集合也是有限集 . 如果 $U_{1},U_{2},\dots,U_{n}$ 是 $\mathcal{T}_{f}$ 的非空元素，为了证明 $\cap U_{i}$ 在 $\mathcal{T}_f$ 中，只要确定

$$X-\bigcap_{i=1}^n U_{i}=\bigcup_{i=1}^{n}(X-U_{\alpha})$$
右边是有限集的有限并，所以是有限集

> [!QUOTE] Definition 2
> 设 $\mathcal{T}$ 和 $\mathcal{T'}$ 是集和 $X$ 上的两个拓扑，如果 $\mathcal{T}'\supset \mathcal{T}$ 我们就称 $\mathcal{T}'$ **细于** (finer) $\mathcal{T}$ ——若为真包含，则为**严格细于** （strictly finer）。反之，则为 **粗于** (coarser) 与 **严格粗于** （strictly coarser）

从这个定义来看，我们知道有些拓扑是可以比较的
——但是就是可以有拓扑不能比较！好像 
$$\mathcal{T}_{1}=\{ \varnothing,\{ 1 \},\{ 2,3 \},X \}$$
$$\mathcal{T}_{2}=\{ \varnothing,\{ 1 \},\{ 1,3 \},\{ 2 \},X \}$$
这两个拓扑没有什么包含关系，那么就是无法比较的。我们对能否包含的想法，可以想这从一个拓扑再次打碎。如 $\mathcal{T}_{1}'=\{ \varnothing,\{ 1 \},\{ 2,3 \},\{ 3 \},\{ 1,3 \},X \}$

