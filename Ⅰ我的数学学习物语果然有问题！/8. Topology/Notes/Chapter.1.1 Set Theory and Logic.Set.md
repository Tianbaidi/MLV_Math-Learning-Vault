---
tags:
  - Topology
  - Set_Theory
---
> 这一部分的集合论将会作为本库中最为全面的集合论，如有教材以后要参考集合论或者逻辑用语的可以直接跳转到此处。

> 拓扑学教材参考 Munkers ，由于使用方便，这里采用中译版（时不时参考原版教材）

# 集合论基础

## Notations

我们用 $A,B\dots$ 大写字母来表示**集合** (set) ; $a,b\dots$ 小写字母则表示为集和中的 $Object$ 或者 $Element$ (有时也会被简称为 $Point$ , 对于中文表示，集和可以称为集，**元素**可以称为**元**或者**点**)

如果元素 $a$ 在集和 $A$ 中，那么就称 $a$ 属于 $A$ , 记为 
$$a \in A$$
否则就为 
$$a \not \in A$$

我们所提及的 "$=$ " 指的是逻辑上的 **同一** (Identitity) . 如元素 $a=b$ 就表示同一个符号，例如 $\frac{1}{2}=\frac{2}{4}$ ; 集和 $A=B$ 则表示两个集和中的元素完全相同, 否则就记为  $A \neq B$ 

我们可以有以下表示集和的方式 

**列举**
即将集和中的元素全都列举出来，记为 
$$A=\{ a,b,c \}$$
**描述**
我们描述集和元素的一些性质，从而确定这个集和，如 $\{ \mid \}$ 其中左半部分为元素的符号，$\mid$ 可以理解为“使得” ，如 
$$B=\{ x\mid \text{x is an even integer}\}$$

### 集和间的关系 

#### 子集

如果集和 $A$ 中的元素全都能在 $B$ 中找到，我们就称 $A$ 是 $B$ 的**子集** (subset), 记为 
$$A \subset B$$
若 $A\neq B$ 那么我们的定义更加严格，称为 **真子集** (Proper subset) 我们用记号 
$$A \subsetneq B$$
来表示，这两个记号也被称为 **包含** (Inclusion)与 **真包含** (Proper inclusion) 

#### 集和运算

##### 并集

> 高中的时候，并集往往取 “并” 这个字的脑袋部分来记忆，可见当时的理解是多么粗浅

如果我们将两个集和的元素同一为一个集和，用自然语言是这样描述的：“元素 $x$ 在 $A$ 中或者 $B$ 中”，用集和的方式就记为 
$$A \cup B=\{ x \mid x \in A\ or\ x\in B \}$$
<img src="c1,Topology p1.png" style="float:right; margin:0 0 1em 1em;" width="150">
##### 交集

> 高中的时候，交集往往取 "交" 中间这一部分 “八” 来记忆，看来非常巧合，交即是交中间（误导向）

如果我们去两个集和间相同的元素组成一个新的集和，用自然语言是这样描述的：“元素 $x$ 在 $A$ 且在 $B$ 中”，我们这样表示 
$$A \cap B=\{x \mid x \in A \text{ and } x\in B \}$$
<img src="c1,Topology p2.png" style="float:right; margin:0 0 1em 1em;" width="150">
如果两个集合之间没有相同的元素，我们就定义空集 $\varnothing$ , 记为 
$$A \cap B=\varnothing$$
> 对于空集 $\varnothing$ , 这是一个完全由定义产生的符号，我们不难对这个定义进行如下推广 
>$$A\cup\varnothing=A\qquad A\cap \varnothing=\varnothing$$

##### 差
集合间还有运算称为集合的 **差** ( difference ),我们用常用的符号 $-$ 来表示，记为 
$$A-B=\{ x \mid x\in A \text{ and } x\not\in B \}$$
有时我们也称为 $B$ 相对于 $A$ 的补集，简称 **补** ( complement ) 
<img src="c1,Topology p3.png" style="float:right; margin:0 0 1em 1em;" width="150">
自此，我们可以对上述运算进行组合，最终可以逐渐得到集合论的法则。里面很多公式可以由我们画图得到一个直观的结果

##### 运算法则

**第一分配律** 对于任意集合 $A,B,C$ ; 我们有以下公式 
$$A\cap(B\cup C)=(A \cap B)\cup(A\cap C)$$
**proof.** 对于集合等式的证明，我们往往采用相互包含的方式来证明,即 
证明：a. $A\cap(B\cup C)\subset(A \cap B)\cup(A\cap C)$   b. $(A \cap B)\cup(A\cap C)\subset A\cap(B\cup C)$ 
我们首先看第一个证明
令 $x\in A$ 同时 $x\in B\cup C$ ，我们对后者进行分类讨论
1. $x\in B$ 时，我们有 $x\in A$ 且 $x\in B$ 于是我们得到 $x\in (A \cap B)$ . 
2. $x\in C$ 时，我们有 $x\in A$ 且 $x\in C$ 于是我们得到 $x\in (A \cap C)$ .
这两个条件是同时成立的，于是 $x\in(A \cap B)\cup(A\cap C)$ , a. 成立 

现在我们看第二个证明
令 $y\in(A \cap B)$ 或者 $y\in (A \cap C)$ , 我们同样可以分类讨论 
1. $y\in (A \cap B)$ 我们可以得到 $y\in A$ 且 $y\in B$ 。根据并集 $B\cup C$ 我们可以知道 $y\in A\cap (B \cup C)$
2. $y\in (A \cap C)$ 我们可以得到 $y\in A$ 且 $y\in C$ 。根据并集 $B\cup C$ 我们可以知道 $y\in A\cap (B \cup C)$
于是我们得证 b. $\square$ 

**第二分配率** 对于任意集和 $A,B,C$ ；我们有以下公式 
$$A\cup(B\cap C)=(A\cup B)\cap(A \cup C)$$
**De Margan 定律** 对于任意集和 $A,B,C$ ; 我们有以下公式 
$$A-(B \cup C)=(A-B)\cap(A-C)$$ $$A-(B \cap C)=(A-B)\cup (A-C)$$
对于这个定律，我们可以这样记忆 :**并的补等于补的交，交的补等于补的并**
这两个请读者自证
![[c1 ,Topology p3.png]]

#### 集和的族

既然我们已经有了关于集和的运算，可否试想过将集和作为集和的元素？我们将一个以集和为元素的集称为 **族** (Collection) , 或者称为 **集族** (Collection of sets) ,常用英文花体大写 $\mathcal{A},\mathcal{B}$ 等来表示。我们可以套娃式的运用此前的想法，既然集和间有交并计算，集族间有没有呢？那当然是有的。但是这个并不是很有意思，我们可以考虑集族内部的交和并

##### 任意并和任意交

给定一个集族 $\mathcal{A}$ ,$\mathcal{A}$ 中元素的 **并** (union) 我们定义为 
$$\bigcup_{A\in\mathcal{A}}A=\{ x \mid \text{for at least one }A\in \mathcal{A} \}$$
**交** (intersection) 我们定义为 
$$\bigcap_{A\in \mathcal{A}}A=\{ x \mid \text{for every }A\in\mathcal{A} \}$$
对于我们的空族的并相对直观 
$$\bigcup_{A\in\mathcal{A}}A=\varnothing$$
但对于空族的交就显得不是很显然，Munkres 表示不在定义空族的交。

对 De Margan 公式进行推广，我们有
$$\left(\bigcup_{j=1}^{\infty} E_j\right)^c = \bigcap_{j=1}^{\infty} E_j^c$$

#### 笛卡尔积 （Cartesian product）

这个概念并非困难，若我们将两个集和看成两个垂直的数轴，元素作为其中的一维坐标，笛卡尔积就表示这两个数轴包围的面积中的点的集和。
我们定义集和 $A$ $B$ ,其 **笛卡尔积** $A\times B$ (有时我们也直接称为 **积** （product）) 表示 
$$A\times B=\{ (a,b) \mid a\in A \text{ and } b\in B \}$$
$(a,b)$ 我们表示为有序偶对 (Order pairs)

对于一个有序偶对，我们为了防止与此前学过的开区间相混淆，我们统一描述为 
$$a\times b$$
笛卡尔积在此后我们也会遇到，很难想想等到那是的笛卡尔积会不会仍然是现在模样（大致是不会的吧）

