---
tags:
  - Algebra
  - Groups
---
如果我们面对一个群或者一个集合，我们会很自然的想到如何对集和进行划分。我们希望有一个便捷的方式，对一个集合进行一个简介有理的划分

> [!ABSTRACT] Definition4.1
> 集合的一个划分表示讲一个集合划为几个非空不交的几个集和，并且这些集合完全覆盖原来的集合
$$S=\text{Union of disjoint nonempty subset}$$

我们可以参考 [[Chapter.1.1 Set Theory and Logic.Set]] 中的集族概念，对于集合划分的简单的理解我们可以想 “奇数” 和 "偶数" 完成的对整数集的一个划分。对对称群 $S_{3}$ 可以划分为 $\{ 1 \},\{ y,xy,x^{2}y \},\{ x,x^{2} \}$ 他们满足划分的定义

> [!ABSTRACT] Definition4.2
> 等价关系意味着集合 $S$ 中元素之间的关系，如果他们满足 :
>- Transitive : 如果 $a$ 与 $b$ 等价，$b$ 与 $c$ 等价，故 $a$ 与 $c$ 等价
>- Symmetric : 如果 $a$ 与 $b$ 等价，$b$ 与 $a$ 也等价
>- reflexive : 对于所有的 $a$ , 都有 $a$ 与自身等价
>我们常常用符号 $a \sim b$ 来表示两个元素之间的 **等价** （Equivalence Relation）。集和元素的共轭是一类比较重要的等价

> [!TIP] Proposition4.1
> 一个等价关系在集合 $S$ 中构成了集和的一个划分, 反之亦然


对于这个证明我们主要是证明由等价关系推到集和的划分，我们首先要引入对等价类的定义 

> [!ABSTRACT] Definition.4.3
> $S$ 的一个子集包含了等价于 $a$ 的所有元素 $b$ , 我们记为 
>$$C_{a}=\{ b\in S \mid a \sim b \}$$
>这就称为 **等价类** （equivalence class）以下引理将完成对上述命题的证明

> [!Success] Lemma.4.3.1
> 给出集合 $S$ 中的等价关系，其等价类构成的集合 $S$ 的子集构成集和的划分
>我们这里要验证的是这些子集是非交且满射非空的：
  > 1. **非空** : 由于 $a$ 在 $C_{a}$ 中，显然我们的子集是非空的
  > 2. **满射** : 由于在去等价类时 $a$ 是在 $S$ 中任意的，满射也是显然的
   >3. 我们主要要验证的是 **非交**
   
**Proof.** 我们利用反证法：假使 $d\in C_{a}\cap C_{{b}}$ , 如果 $x$ 在 $C_{b}$ 中，那么有 $b \sim x$ ; 我们又有 $a \sim d$ , $b \sim d$ . 利用对称性，我们有 $d \sim b$ . 于是我们连续使用两次传递性，得到 $a\sim x$ . 于是我们有 $x$ 在 $C_{a}$ 中，由于这里 $x$ 在 $C_b$ 中任意——我们得到 $C_{b} \subset C_{a}$ . 反之，我们可以得到 $C_{a} \subset C_{b}$ .因此，如果两个等价类有交集，这两个等价类相等（为同一个等价类），因此，我们得到等价类是非交的 $\square$ 

比如，我们如果要划分一个整数集，我们可以将其分为奇集和偶集。或者我们可以用后续的模算术来划分它。在完成划分之后，我们其实已经得到了一个新的集和 $\overline{S}$ , 它的元素为我们划分好的子集：入上述例子就能表示为 
$$\overline{S}=\{ \overline{Odd},\overline{Even} \}$$
更方便的，我们可以选取集合中的代表元素来作为这个集和的表示，如 
$$\overline{S}=\{ \overline{0},\overline{1} \}$$
对于任何一个等价关系，我们有映射 
$$\pi:S\to \overline{S}$$
有 
$$\pi(a)=\overline{a}$$
## 纤维

这个映射关系让我们认识到 $\pi^{-1}(x)\quad x\in{\overline{a}}$ 并不是一个映射。在数学中，我们形象的用**纤维** (fibre) 来表示。
![[1775011188043_edit_327242115639952.png]]
就像植物的纤维一样非常形象（对）
 如果 $G$ 是一个有限群，我们可以定义一个映射 $f\colon G\to \mathbb{N}$ 到自然数集合 $\{1,2,3,\ldots \}$，令 $f(a)$ 为 $G$ 中元素 $a$ 的阶。这个映射的纤维是具有相同阶的元素的集合
回到群同态 $\phi :G\to G^{\prime}$。由 $\phi$ 定义的 $G$ 上的等价关系通常用 $\equiv$ 而不是 $\sim$ 表示，并称为**同余**：
$$a\equiv b\text{ 如果 }\phi (a) = \phi (b).$$
> [!TIP] Proposition.4.4
> 我们令映射到 $1$ 的集和为 **核** ，映射到其他元素的映射，我们就能称为 $K$ 的陪集 $aK$ ，这些陪集是映射 $\varphi$ 的纤维，他们构成了集和的划分。

既然我们已经有了陪集，不如就介绍陪集吧

# 陪集

## 左陪集

> [!ABSTRACT] Definition.4.4
> 若 $H$ 是群 $G$ 的子群，并且 $a$ 是群 $G$ 中的一个元素，有子集 
>$$aH=\{ ah \mid h \text{ in } H \}$$
>这我们称为 **左陪集** （Left cosets）, $H$ 也是一个左陪集 $H=1H$

群 $G$ 中 $H$ 的陪集构成了 $G$ 的一个同余关系等价类 
$$a \equiv b,\text{ if }b=ah\text{ for some }h \text{ in }H$$
这个证明是简单的，我们来验证同余是一个等价类

- Transitivity : 假设 $a\equiv b$ 和 $b\equiv c$ . 我们有 $b=ah$ 和 $c=bh'$ 其中 $h$ 和 $h'$ 为 $H$ 的元素，有 $c=ahh'$ . 由于 $H$ 是子群，故有 $c\equiv a$ .
- Symmetry : 设 $a\equiv b$ , 因此 $b=ah$ . 固有 $a=bh^{-1}$ 由于 $h\in H$ 故 $b\equiv a$ .
- Reflexitity : $a=a 1$ 显然 $a\equiv a$ .

> [!Danger]   Corollary.4.1   群 $G$ 子群 $H$ 的左陪集构成群 $G$ 的一个子群 
> **Proof.**  $aH$ 定义了 $G$ 的一个特定子集。设 $H$ 是群 $G$ 的一个子群，$a$ 和 $b$ 是 $G$ 中的元素。以下条件等价：
> 1. $b = ah$ 对于某个$h$ 在 $H$ 中 , 或 $a^{-1}b$ 是 $H$  中的一个元素
 >2. $b$ 是左陪集的 $aH$ 元素
 >3. 陪集 $aH$ 和 $bH$ 是等价的

一个子群的左陪集个数称为该子群在 $G$ 中的 **指数** ( index )。记为 
$$[G:H]$$
因此 $S_{3}$ 中子群 $\langle y \rangle$ 的指数是 3。当 $G$ 是无限群时，指数也**可能**是无限的。( 注意：中文译本中这这个**可能**漏译 )

> [!Success] Lemma.4.0.1
> 所有 $G$ 子群 $H$ 左陪集 $aH$ 有着相同的阶

证明不难，主要是定义 $H\to aH$ 是双射的

于是，我们得到了计数法则 
$$|G|=|H|[G:H]$$
 其中 $|G|$ 和 $|H|$ 为 群 $G$ 和子群 $H$ 的阶，从计数公式可以得出，右边的项整除左边。于是我们得到 **拉格朗日定理** . 

> [!NOTE] Lagrange's Theorem
> 令 $H$ 为有限群 $G$ 的子群，子群 $H$ 的阶整除群 $G$ 的阶

> [!Danger] Corollary.4.2
> 有限群中一个元素的阶整除该群的阶。

**Proof.** 群 $G$ 中一个元素 $a$ 的阶等于由 $a$ 生成的循环子群 $\langle a \rangle$ 的阶, 再依据拉格朗日定理。

> [!Danger] Corollary.4.3
> 假设一个群 $G$ 有素数阶 $p$。设 $a$ 是 $G$ 中除单位元外的任何元素。那么 $G$ 是由 $a$ 生成的循环群 $\langle a \rangle$。

**Proof.** 一个元素 $a \neq 1$ 的阶大于 1，并且它整除 $G$ 的阶，而 $G$ 的阶是素数 $p$。所以 $a$ 的阶等于 $p$。这也是由 $a$ 生成的循环子群 $\langle a \rangle$ 的阶。由于 $G$ 的阶为 $p$，$\langle a \rangle = G$。

这个引理分类了素数阶 $p$ 的群，它们形成了一个同构类。计数公式也可以应用于给定的同态 $\phi : G \to G'$ 的情况。正如我们所看到的 ，核 $\ker \phi$ 的左陪集是映射 $\phi$ 的非空纤维。它们与像中的元素一一对应。 
$$[G:\ker \varphi]=|\mathrm{Im} \varphi|$$


> [!danger]  Corollary 4.4
> 令 $\varphi:G\to G'$ 是有限群的一个同态 . 我们有 
> - $|G|=|\ker \varphi||\mathrm{Im}\ \varphi|$
> - $|\ker \varphi|$ 整除 $|G|$,与此同时
> - $|\mathrm{Im}\ \varphi |$ 同时整除 $|G|$ 与 $|G'|$

**Proof.** 这里的证明则是利用此前的结论，最后我们用拉格朗日定理求出 $|\mathrm{Im}\ \varphi|$ 也整除 $|G'|$


> [!important] Propsition.4.5   Multiplicative Property of the Index
> 如果 $G\supset H\supset K$ 为群 $G$ 的子群 . 有 $[G:K]=[G:H][H:K]$

**Proof.** 我们将假设右边的两个指数是有限的，比如 $[G:H] = m$ 和 $[H:K] = n$。当一个或另一个无限时推理类似。我们列出 $H$ 在 $G$ 中的 $m$ 个陪集，为每个陪集选择代表元素，比如 $g_{1}H,\ldots ,g_{m}H$。那么 $g_{1}H\cup \dots \cup g_{m}H$ 是 $G$ 的一个划分。类似地，我们为 $K$ 在 $H$ 中的每个陪集选择代表元素，得到划分 $H = h_{1}K\cup \dots \cup h_{n}K$。由于乘以 $g_{i}$ 是一个可逆操作，$g_{i}H = g_{i}h_{1}K\cup \dots \cup g_{i}h_{n}K$ 将是陪集 $g_{i}H$ 的一个划分。将这些划分放在一起，$G$ 被划分为 $mn$ 个陪集 $g_{i}h_{j}K$。

## 右陪集

YYSY，右陪集与左陪集几乎是等价的，我们主要有以下有趣的命题 


> [!important] Proposition.4.6
> 令 $H$ 为群 $G$ 的子群，下列情况等价：
> 1. $H$ 为正规子群 ：对于所有的 $H$ 有 $G$ 中所有元素 $g$ , 有 $ghg^{-1}$ 在 $H$ 中
> 2. 对于所有 $G$ 中的 $g$ , 有 $gHg^{-1}=H$
> 3. 对于所有 $G$ 中的 $g$ , 有左陪集 $gH$ 等价于右陪集 $Hg$
> 4. 任意群 $G$ 的左陪集都有右陪集 

**Proof.**  我们令 $H$ 为正规子群，根据 $1.$ 我们就有 $ghg^{-1}$ 在 $H$ 中， $ghg^{-1}\subset H$  、随后自然的有 $g^{-1}Hg \subset H$ 我们将两边再次乘以 $g$ 或者 $g^{-1}$ 就有 $gHg^{-1} \supset H$ ，于是 $2.$ 成立；
若 $2.$ 成立，那么有 $gHg^{-1}=H$ 我们右乘一个 $g$ 就有 $gH=Hg$ , 于是 $3.$ 成立
$3.$ 蕴含 $4.$ 是显然的，我们只要验证 $4. \Rightarrow 3.$ 我们记得右陪集划分群 $G$，并且注意到左陪集 $g H$ 和右陪集 $H g$ 有一个公共元素，即 $g = g \cdot 1 = 1 \cdot g$。所以如果左陪集 $g H$ 等于某个右陪集，那个陪集必须是 $H g$。


> [!important] Proposition.4.7
> - 若 $H$ 是群 $G$ 的子群，且 $g$ 是群 $G$ 的一个元素，群 $gHg^{-1}$ 依旧是一个子群
> - 如果群 $G$ 只有一个阶为 $r$ 的子群 $H$ ,那么这个子群是正规的（normal）

**Proof.** 由 $g$ 的共轭是 $G$ 的一个自同构， $g H g^{- 1}$ 是 $H$ 的像 . 参考上一个命题我们可以知道 $gHg^{-1}$ 的阶即为 $r$

>Note: If $H$ is a subgroup of a finite group $G$ , the counting formulas using right cosets or left cosets are the same, so the number of left cosets is equal to the number of right cosets. This is also true when $G$ is infinite, though the proof can't be made by counting (see Exercise M.8).

# Modular Arithmetic

> 模运算非常有趣，我记得我公众号的很古早的文章就有过用模运算来解行列式问题 , 这里我们主要讲模运算在群中的应用，或者说。抛弃了其计算外衣，我们这样在群里作用是什么呢？

> 答：在群里当然是水群喽。

此前我们提及对集和的划分，我们采用了 **模运算** 。

模 $n$ 的同余类集合可以用符号 $\mathbb{Z} / \mathbb{Z}n$、$\mathbb{Z} / n\mathbb{Z}$ 或 $\mathbb{Z} / (n)$ 中的任何一个表示。通过使用整数并在除以 $n$ 后取余数，可以在 $\mathbb{Z} / \mathbb{Z}n$ 中明确地进行加、减和乘运算。它们告诉我们，将整数 $a$ 映射到其同余类 $\overline{a}$ 的映射
$$\mathbb{Z}\to \mathbb{Z} / \mathbb{Z}n$$
与加法和乘法兼容。因此可以在整数中进行计算，然后在最后将结果传递到 $\mathbb{Z} / \mathbb{Z}n$。如果保持数字较小，计算会更简单。这可以通过在计算的某个部分之后计算余数来实现。

数字上的横线变得麻烦。它们经常被省略。当省略横线时，只需记住这个规则：
$$\text{在 }\mathbb{Z} / \mathbb{Z}n\text{ 中写 }a = b\text{ 意味着 }a\equiv b\text{ 模 }n. $$
模一个素整数的同余具有特殊性质，这里埋个坑

===EXERCISES===
---
