---
tags:
  - Topology
  - Set_Theory
  - Munkres
---
# Rule of assignment

函数其实我们早就有了解过了，但是我们现在想让函数的描述更加精确，于是我们给出 **指派法则** 的定义
**Def.** **指派法则** 是两个集和的笛卡尔积 $C\times D$ 的一个子集 $r$ , 该子集满足这样的条件：$C$ 的元素表示后续组成坐标的第一个数值。如果我们这样表示 $C\times D$ 的子集 
$$[(c,d)\in r\ 并且 (c,d')\in r]\Longrightarrow [d=d']$$
我们就认为 $r$ 是指派的方式—— $c$ 对应 $C$ 中的元素 , $d$ 对应 $D$ 中的元素 —— 他们满足 $(c,d)\in r$ 

> 这样定义真的很不常见(至少我是第一次见)

对于一个指派法则，我们有 **定义域** (domain) 表示由 $r$ 所定义的坐标的第一个坐标元素组成 $C$ 的子集； **像集** (image set) 表示 $r$ 所定义的坐标的第二个坐标元素组成 $D$ 的子集。 
$$\text{diomain } r=\{ c\mid \text{there exists }d\in D \text{ such that } (c,d)\in r \}$$
$$\text{image set } r=\{ d\mid \text{there exists }c\in C \text{ such that } (c,d)\in r \}$$
如果我们给定了一个指派法则，其定义域和值域是完全确定的

用此，我们来定义函数

**Def.** **函数** (function) $f$ 指一个指派法则 $r$ , 连同包含 $r$ 的像集的集和 $B$ . 法则 $r$ 的定义域 $A$ 就是 $f$ 的**定义域**；$r$ 的像集就称为 $f$ 的**像集** .集和 $B$ 称为 $f$ 的 **值域** (range) , 我们可以这样表示 
$$f:A\to B$$
我们称为 $f$ 是 $A$ 到 $B$ 的函数 ( 或者称 $f$ 是 $A$ 到 $B$ 的一个 **映射** (map) ) 

曾经我们遇到的函数形式是 $f(x)=\text{****}$ . 我们可以理解对于 $A$ 中的元素 $a$ 对应的 $f(a)\in B$ 是唯一的 , 我们称 $f(a)$ 是 $f$ 在 $a$ 的**值** (value).但是仅仅这样的一个方法不足以准确的描述一个函数，我们定义对 $f$ 的限制 

**Def.** 设 $f:A\to B$ , $A_{0}$ 是 $A$ 的一个子集，$f$ 在 $A_{0}$ 上的限制表示由子集 $A_{0}$ 映射到 $B$ 的函数 
$$\{ (a,f(a)) \mid a\in A_{0} \}$$
![[1773885386250_edit_410380566493811.png]]

### 复合映射

设 $f : A \to B$、$g : B \to C$ 是两个函数。我们可以先作用 $f$，再作用 $g$，得到从 $A$ 到 $C$ 的函数，称为 $f$ 与 $g$ 的**复合**

**Def.** 设 $f : A \to B$，$g : B \to C$。定义 **复合映射** $g \circ f : A \to C$ 为
$$(g \circ f)(a) := g(f(a)), \quad a \in A.$$
复合运算满足结合律：$(h \circ g) \circ f = h \circ (g \circ f)$，但一般不可交换（$g \circ f \neq f \circ g$）。

### 单射、满射与双射

一个函数可以按它“如何填满”值域与如何“识别”定义域中的元素来分类。

**Def.** 设 $f : A \to B$ 是一个函数。

1. 若对任意 $a_1, a_2 \in A$，$f(a_1) = f(a_2)$ 蕴含 $a_1 = a_2$，则称 $f$ 是**单射**（injective，也叫一一映射）。
2. 若对于任意 $b \in B$，都存在 $a \in A$ 使得 $f(a) = b$，即 $f$ 的像集等于 $B$，则称 $f$ 是**满射**（surjective，也叫到上映射）。
3. 若 $f$ 既是单射又是满射，则称 $f$ 是**双射**（bijective，也叫一一对应）。

### 逆映射

**Def.** 设 $f : A \to B$ 是双射。定义 $f$ 的**逆映射** $f^{-1} : B \to A$ 为
$$f^{-1}(b) := \text{ 唯一的 } a \in A \text{ 使得 } f(a) = b.$$
于是 $f^{-1} \circ f = \operatorname{Id}_A$，$f \circ f^{-1} = \operatorname{Id}_B$。一个函数有逆映射当且仅当它是双射。

### 集合的像与原像

**Def.** 设 $f : A \to B$，$A_0 \subseteq A$，$B_0 \subseteq B$。
- 定义 $A_0$ 的**像集**（image）为 $f(A_0) := \{f(a) \mid a \in A_0\}$。
- 定义 $B_0$ 的**原像** / **逆像**（preimage）为 $f^{-1}(B_0) := \{a \in A \mid f(a) \in B_0\}$。

注意原像 $f^{-1}(B_0)$ 总是一个集合（即使 $f$ 不可逆），它是“把 $B_0$ 的每个点都往回拉”得到的东西。并且 $f^{-1}$ 保并集与交集：
$$f^{-1}\left(\bigcup_\alpha B_\alpha\right) = \bigcup_\alpha f^{-1}(B_\alpha), \qquad f^{-1}\left(\bigcap_\alpha B_\alpha\right) = \bigcap_\alpha f^{-1}(B_\alpha).$$
这一点在拓扑学里极为重要：映射的连续性正是用“开集的原像是开集”来刻画的。

### 下标族（indexed family）

我们这里的“族”（collection）可以更系统地用**下标集**来组织。

**Def.** 设 $A$ 是一个集合，$\Lambda$ 称为**下标集**。若对每个 $\lambda \in \Lambda$ 都指定了一个 $A$ 中的元素 $a_\lambda$，我们就得到一个**下标族** $\{a_\lambda\}_{\lambda \in \Lambda}$，简记为 $(a_\lambda)_{\lambda \in \Lambda}$。当 $\Lambda = \mathbb{N}$ 时它就是一个**序列**。

类似地可以对下标族取**任意并**与**任意交**：
$$\bigcup_{\lambda \in \Lambda} A_\lambda, \qquad \bigcap_{\lambda \in \Lambda} A_\lambda.$$
这恰是前面“集族的并和交”用下标书写的版本。
