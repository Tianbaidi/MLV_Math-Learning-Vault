---
tags:
  - Algebra
  - Groups
---
===== Page 37 =====

### 2.1 LAWS OF COMPOSITION

### 2.1 合成律

II est peu de notions en mathematiques qui soient plus primitives que celle de loi de composition.

—Nicolas Bourbaki

A law of composition on a set $S$ is any rule for combining pairs $a,b$ of elements of $S$ to get another element, say $p$ , of $S$ . Some models for this concept are addition and multiplication of real numbers. Matrix multiplication on the set of $n\times n$ matrices is another example.

集合 $S$ 上的一个**合成律**是将 $S$ 中的元素对 $a,b$ 组合起来得到 $S$ 中另一个元素（比如 $p$）的任何规则。这个概念的一些模型是实数的加法和乘法。$n\times n$ 矩阵集上的矩阵乘法是另一个例子。

Formally, a law of composition is a function of two variables, or a map
$$S\times S\to S.$$

形式上，合成律是一个二元函数，或者说是一个映射
$$S\times S\to S.$$

Here $S\times S$ denotes, as always, the product set, whose elements are pairs $a,b$ of elements of $S$ .

这里 $S\times S$ 一如既往地表示乘积集，其元素是 $S$ 的元素对 $a,b$。

The element obtained by applying the law to a pair $a,b$ is usually written using a notation resembling one used for multiplication or addition:
$$p = ab,a\times b,a\circ b,a + b,$$
or whatever, a choice being made for the particular law in question. The element $p$ may be called the product or the sum of $a$ and $b$ , depending on the notation chosen.

通过将合成律应用于一对 $a,b$ 得到的元素通常用类似于乘法或加法的记号表示：
$$p = ab,a\times b,a\circ b,a + b,$$
或者任何其他记号，根据所讨论的特定规则进行选择。元素 $p$ 可以称为 $a$ 和 $b$ 的积或和，取决于所选的记号。

We will use the product notation $ab$ most of the time. Anything done with product notation can be rewritten using another notation such as addition, and it will continue to be valid. The rewriting is just a change of notation.

大部分时间我们将使用乘法记号 $ab$。任何用乘法记号完成的事情都可以用另一种记号（如加法）重写，并且它仍然有效。重写仅仅是记号的改变。

It is important to note right away that $ab$ stands for a certain element of $S$ , namely for the element obtained by applying the given law to the elements denoted by $a$ and $b$ . Thus if the law is matrix multiplication and if $a = \begin{bmatrix} 1 & 3 \\ 0 & 2 \end{bmatrix}$ and $b = \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix}$ , then $ab$ denotes the matrix $\begin{bmatrix} 7 & 3 \\ 4 & 2 \end{bmatrix}$ . Once the product $ab$ has been evaluated, the elements $a$ and $b$ cannot be recovered from it.

必须立刻注意到 $ab$ 代表 $S$ 中的一个特定元素，即通过将给定规则应用于用 $a$ 和 $b$ 表示的元素所得到的元素。因此，如果规则是矩阵乘法，且 $a = \begin{bmatrix} 1 & 3 \\ 0 & 2 \end{bmatrix}$，$b = \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix}$，那么 $ab$ 表示矩阵 $\begin{bmatrix} 7 & 3 \\ 4 & 2 \end{bmatrix}$。一旦乘积 $ab$ 被计算出来，元素 $a$ 和 $b$ 就不能从中恢复出来。

With multiplicative notation, a law of composition is associative if the rule
$$(ab)c = a(bc)\quad (\mathrm{associative~law}) \quad (2.1.1)$$

使用乘法记号，如果规则
$$(ab)c = a(bc)\quad (\text{结合律}) \quad (2.1.1)$$

===== Page 38 =====

holds for all $a,b,c$ in $S,$ where $(a b)c$ means first multiply (apply the law to) $a$ and $b$ ,then multiply the result $a b$ by $c.$ A law of composition is commutative if
$$a b = b a\quad (c o m m u t a t i v e l a w)$$
holds for all $a$ and $b$ in $S.$ Matrix multiplication is associative, but not commutative.

对所有 $S$ 中的 $a,b,c$ 成立，其中 $(a b)c$ 表示先将 $a$ 和 $b$ 相乘（应用合成律于它们），然后将结果 $a b$ 乘以 $c$。如果
$$a b = b a\quad (\text{交换律})$$
对所有 $S$ 中的 $a$ 和 $b$ 成立，则称合成律是**交换的**。矩阵乘法是结合的，但不是交换的。

It is customary to reserve additive notation $a + b$ for commutative laws - laws such that $a + b = b + a$ for all $a$ and $b.$ Multiplicative notation carries no implication either way concerning commutativity.

习惯上将加法记号 $a + b$ 保留给交换律——即对所有 $a$ 和 $b$ 有 $a + b = b + a$ 的律。乘法记号对交换性没有任何暗示。

The associative law is more fundamental than the commutative law, and one reason for this is that composition of functions is associative. Let $T$ be a set, and let $g$ and $f$ be maps (or functions) from $T$ to $T.$ Let $g\circ f$ denote the composed map $t\hookrightarrow g(f(t))$ : first apply $f$ then $g.$ The rule
$$g,f\hookrightarrow g\circ f$$
is a law of composition on the set of maps $T\rightarrow T.$ This law is associative. If $f,g,$ and $h$ are three maps from $T$ to $T,$ then $(h\circ g)\circ f = h\circ (g\circ f)$

结合律比交换律更基本，原因之一在于函数的复合是结合的。设 $T$ 是一个集合，$g$ 和 $f$ 是从 $T$ 到 $T$ 的映射（或函数）。令 $g\circ f$ 表示复合映射 $t\mapsto g(f(t))$：先应用 $f$，然后 $g$。规则
$$g,f\mapsto g\circ f$$
是映射集合 $T\rightarrow T$ 上的一个合成律。这个律是结合的。如果 $f,g$ 和 $h$ 是从 $T$ 到 $T$ 的三个映射，那么 $(h\circ g)\circ f = h\circ (g\circ f)$

$$T\underbrace{f\underbrace{\longrightarrow}_{g\circ f}T\underbrace{\longrightarrow}_{h\circ g}T\underbrace{\longrightarrow}_{h}T$$

Both of the composed maps send an element $t$ to $h(g(f(t)))$

两个复合映射都将元素 $t$ 送到 $h(g(f(t)))$。

When $T$ contains two elements, say $T = \{a,b\}$ , there are four maps $T\rightarrow T$

当 $T$ 包含两个元素时，比如 $T = \{a,b\}$，有四个映射 $T\rightarrow T$：

$i$ : the identity map, defined by $i(a) = a$ $i(b) = b$
$\tau$ : the transposition, defined by $\tau (a) = b$ $\tau (b) = a$
$\alpha$ : the constant function $\alpha (a) = \alpha (b) = a$
$\beta$ : the constant function $\beta (a) = \beta (b) = b$

$i$：恒等映射，定义为 $i(a) = a$，$i(b) = b$
$\tau$：对换，定义为 $\tau (a) = b$，$\tau (b) = a$
$\alpha$：常值函数 $\alpha (a) = \alpha (b) = a$
$\beta$：常值函数 $\beta (a) = \beta (b) = b$

The law of composition on the set $\{i,\tau ,\alpha ,\beta \}$ of maps $T\rightarrow T$ can be exhibited in a multiplication table:

映射集合 $\{i,\tau ,\alpha ,\beta \}$ 上的合成律可以用乘法表表示：

\[\begin{array}{c|cccc}
\circ & i & \tau & \alpha & \beta \\ \hline
i & i & \tau & \alpha & \beta \\
\tau & \tau & i & \beta & \alpha \\
\alpha & \alpha & \alpha & \alpha & \alpha \\
\beta & \beta & \beta & \beta & \beta
\end{array}\]

which is to be read in this way:
$$\tau \circ \alpha = \beta ,\quad \text{while}\quad \alpha \circ \tau = \alpha .$$

其解读方式如下：
$$\tau \circ \alpha = \beta ,\quad \text{而}\quad \alpha \circ \tau = \alpha .$$

Composition of functions is not a commutative law.

函数的复合不是交换律。

===== Page 39 =====

Going back to a general law of composition, suppose we want to define the product of a string of $n$ elements of a set: $a_{1}a_{2}\dots a_{n} = ?$ There are various ways to do this using the given law, which tells us how to multiply two elements. For instance, we could first use the law to find the product $a_{1}a_{2}$ , then multiply this element by $a_{3}$ , and so on:
$$((a_{1}a_{2})a_{3})a_{4}\dots .$$

回到一般的合成律，假设我们想定义一个集合中 $n$ 个元素串的乘积：$a_{1}a_{2}\dots a_{n} = ?$ 有各种方法可以使用给定的合成律（该律告诉我们如何将两个元素相乘）来完成。例如，我们可以先用该律求出乘积 $a_{1}a_{2}$，然后将这个元素乘以 $a_{3}$，依此类推：
$$((a_{1}a_{2})a_{3})a_{4}\dots .$$

There are several other ways to form a product with the elements in the given order, but if the law is associative, then all of them yield the same element of $S$ . This allows us to speak of the product of an arbitrary string of elements.

还有几种其他方法可以按给定顺序用这些元素形成乘积，但如果该律是结合的，那么所有这些方法都产生 $S$ 中的同一个元素。这使我们能够谈论任意元素串的乘积。

Proposition 2.1.4 Let an associative law of composition be given on a set $S$ . There is a unique way to define, for every integer $n$ , a product of $n$ elements $a_{1},\ldots ,a_{n}$ of $S$ , denoted temporarily by $[a_{1}\dots a_{n}]$ , with the following properties:

命题 2.1.4 设在一个集合 $S$ 上给定了一个结合的合成律。存在唯一的方法，对每个整数 $n$ 定义 $S$ 中 $n$ 个元素 $a_{1},\ldots ,a_{n}$ 的乘积，暂时记为 $[a_{1}\dots a_{n}]$，具有以下性质：

(i) The product $[a_{1}]$ of one element is the element itself.
(ii) The product $[a_{1}a_{2}]$ of two elements is given by the law of composition.
(iii) For any integer $i$ in the range $1\leq i< n$ , $[a_{1}\dots a_{n}] = [a_{1}\dots a_{i}][a_{i + 1}\dots a_{n}]$ .

(i) 一个元素的乘积 $[a_{1}]$ 就是该元素本身。
(ii) 两个元素的乘积 $[a_{1}a_{2}]$ 由合成律给出。
(iii) 对于 $1\leq i< n$ 范围内的任意整数 $i$，$[a_{1}\dots a_{n}] = [a_{1}\dots a_{i}][a_{i + 1}\dots a_{n}]$。

The right side of equation (iii) means that the two products $[a_{1}\dots a_{i}]$ and $[a_{i + 1}\dots a_{n}]$ are formed first, and the results are then multiplied using the law of composition.

等式 (iii) 的右边意味着先形成两个乘积 $[a_{1}\dots a_{i}]$ 和 $[a_{i + 1}\dots a_{n}]$，然后使用合成律将结果相乘。

Proof. We use induction on $n$ . The product is defined by (i) and (ii) for $n\leq 2$ , and it does satisfy (iii) when $n = 2$ . Suppose that we have defined the product of $r$ elements when $r\leq n - 1$ , and that it is the unique product satisfying (iii). We then define the product of $n$ elements by the rule
$$[a_{1}\dots a_{n}] = [a_{1}\dots a_{n - 1}][a_{n}],$$
where the terms on the right side are those already defined. If a product satisfying (iii) exists, then this formula gives the product because it is (iii) when $i = n - 1$ . So if the product of $n$ elements exists, it is unique. We must now check (iii) for $i< n - 1$ :

证明：我们对 $n$ 使用归纳法。乘积由 (i) 和 (ii) 对 $n\leq 2$ 定义，并且当 $n = 2$ 时它确实满足 (iii)。假设我们已经定义了当 $r\leq n - 1$ 时 $r$ 个元素的乘积，并且它是满足 (iii) 的唯一乘积。然后我们通过规则定义 $n$ 个元素的乘积
$$[a_{1}\dots a_{n}] = [a_{1}\dots a_{n - 1}][a_{n}],$$
其中右边的项是已经定义的。如果存在满足 (iii) 的乘积，那么这个公式就给出了该乘积，因为它是当 $i = n - 1$ 时的 (iii)。所以如果 $n$ 个元素的乘积存在，它是唯一的。我们现在必须检查当 $i< n - 1$ 时的 (iii)：

$$[a_{1}\dots a_{n}] = [a_{1}\dots a_{n-1}][a_{n}] \quad\text{(definition)}$$
$$= ([a_{1}\dots a_{i}][a_{i+1}\dots a_{n-1}])[a_{n}] \quad\text{(induction hypothesis)}$$
$$= [a_{1}\dots a_{i}]([a_{i+1}\dots a_{n-1}][a_{n}]) \quad\text{(associative law)}$$
$$= [a_{1}\dots a_{i}][a_{i+1}\dots a_{n}] \quad\text{(induction hypothesis)}$$

This completes the proof. We will drop the brackets from now on and denote the product by $a_{1}\dots a_{n}$ .

这就完成了证明。从现在起我们将去掉括号，将乘积记为 $a_{1}\dots a_{n}$。

An identity for a law of composition is an element $e$ of $S$ such that
$$e a = a \quad\text{and}\quad a e = a, \quad\text{for all } a \text{ in } S. \quad (2.1.5)$$

一个合成律的**单位元**是 $S$ 中的一个元素 $e$，使得
$$e a = a \quad\text{且}\quad a e = a, \quad\text{对所有 } S \text{ 中的 } a \text{ 成立}. \quad (2.1.5)$$

There can be at most one identity, for if $e$ and $e^{\prime}$ are two such elements, then since $e$ is an identity, $e e^{\prime} = e^{\prime}$ , and since $e^{\prime}$ is an identity, $e = e e^{\prime}$ . Thus $e = e e^{\prime} = e^{\prime}$ .

最多只能有一个单位元，因为如果 $e$ 和 $e^{\prime}$ 是两个这样的元素，那么由于 $e$ 是单位元，$e e^{\prime} = e^{\prime}$，并且由于 $e^{\prime}$ 是单位元，$e = e e^{\prime}$。因此 $e = e e^{\prime} = e^{\prime}$。

Both matrix multiplication and composition of functions have an identity. For $n\times n$ matrices it is the identity matrix $I$ , and for the set of maps $T\to T$ it is the identity map - the map that carries each element of $T$ to itself.

矩阵乘法和函数的复合都有一个单位元。对于 $n\times n$ 矩阵，它是单位矩阵 $I$；对于映射集合 $T\to T$，它是恒等映射——将 $T$ 的每个元素映射到自身的映射。

===== Page 40 =====

The identity element will often be denoted by 1 if the law of composition is written multiplicatively, and by 0 if the law is written additively. These elements do not need to be related to the numbers 1 and 0, but they share the property of being identity elements for their laws of composition.

如果合成律写成乘法形式，单位元通常记为 1；如果写成加法形式，则记为 0。这些元素不需要与数字 1 和 0 有关，但它们具有作为其合成律的单位元的共同性质。

Suppose that a law of composition on a set $S$ , written multiplicatively, is associative and has an identity 1. An element $a$ of $S$ is invertible if there is another element $b$ such that
$$a b = 1\mathrm{~and~}b a = 1,$$
and if so, then $b$ is called the inverse of $a$ . The inverse of an element is usually denoted by $a^{- 1}$ , or when additive notation is being used, by $- a$ .

假设一个集合 $S$ 上的合成律，写成乘法形式，是结合的并且有一个单位元 1。如果存在另一个元素 $b$ 使得
$$a b = 1 \quad\text{和}\quad b a = 1,$$
则称 $S$ 中的元素 $a$ 是**可逆的**，如果是这样，那么 $b$ 被称为 $a$ 的**逆元**。一个元素的逆元通常记为 $a^{- 1}$，或者当使用加法记号时，记为 $- a$。

We list without proof some elementary properties of inverses. All but the last have already been discussed for matrices. For an example that illustrates the last statement, see Exercise 1.3.

我们不加证明地列出逆元的一些基本性质。除了最后一条，其余都已经讨论过矩阵的情况。对于说明最后一条的示例，请参见练习 1.3。

If an element $a$ has both a left inverse $\ell$ and a right inverse $r$ , i.e., if $\ell a = 1$ and $a r = 1$ , then $\ell = r$ , $a$ is invertible, and $r$ is its inverse. If $a$ is invertible, its inverse is unique. Inverses multiply in the opposite order: If $a$ and $b$ are invertible, so is the product $a b$ , and $(a b)^{- 1} = b^{- 1}a^{- 1}$ . An element $a$ may have a left inverse or a right inverse, though it is not invertible.

如果一个元素 $a$ 既有左逆元 $\ell$ 又有右逆元 $r$，即如果 $\ell a = 1$ 且 $a r = 1$，那么 $\ell = r$，$a$ 是可逆的，并且 $r$ 是其逆元。如果 $a$ 是可逆的，它的逆元是唯一的。逆元以相反的顺序相乘：如果 $a$ 和 $b$ 是可逆的，那么乘积 $a b$ 也是可逆的，并且 $(a b)^{- 1} = b^{- 1}a^{- 1}$。一个元素 $a$ 可能有左逆元或右逆元，尽管它不是可逆的。

Power notation may be used for an associative law: With $n > 0$ , $a^{n} = a\dots a$ ( $n$ factors), $a^{- n} = a^{- 1}\dots a^{- 1}$ , and $a^{0} = 1$ . The usual rules for manipulation of powers hold: $a^{r}a^{s} = a^{r + s}$ and $(a^{r})^{s} = a^{r s}$ . When additive notation is used for the law of composition, the power notation $a^{n}$ is replaced by the notation $n a = a + \dots +a$ .

对于一个结合的律，可以使用幂记号：当 $n > 0$ 时，$a^{n} = a\dots a$（$n$ 个因子），$a^{- n} = a^{- 1}\dots a^{- 1}$，并且 $a^{0} = 1$。幂的常规操作规则成立：$a^{r}a^{s} = a^{r + s}$ 和 $(a^{r})^{s} = a^{r s}$。当对合成律使用加法记号时，幂记号 $a^{n}$ 被替换为记号 $n a = a + \dots +a$。

Fraction notation $\frac{b}{a}$ is not advisable unless the law of composition is commutative, because it isn't clear from the notation whether the fraction stands for $b a^{- 1}$ or for $a^{- 1}b$ , and these two elements may be different.

除非合成律是交换的，否则不建议使用分数记号 $\frac{b}{a}$，因为从记号中不清楚分数代表 $b a^{- 1}$ 还是 $a^{- 1}b$，而这两个元素可能是不同的。

### 2.2 GROUPS AND SUBGROUPS

### 2.2 群和子群

A group is a set $G$ together with a law of composition that has the following properties:

一个**群**是一个集合 $G$ 连同满足以下性质的合成律：

The law of composition is associative: $(a b)c = a(b c)$ for all $a,b,c$ in $G$ .
$G$ contains an identity element 1, such that $1a = a$ and $a1 = a$ for all $a$ in $G$ .
Every element $a$ of $G$ has an inverse, an element $b$ such that $a b = 1$ and $b a = 1$ .

合成律是结合的：对于 $G$ 中所有 $a,b,c$，$(a b)c = a(b c)$。
$G$ 包含一个单位元 1，使得对于 $G$ 中所有 $a$，有 $1a = a$ 和 $a1 = a$。
$G$ 中每个元素 $a$ 都有一个逆元，即一个元素 $b$，使得 $a b = 1$ 且 $b a = 1$。

An abelian group is a group whose law of composition is commutative.

一个**阿贝尔群**是其合成律是交换的群。

For example, the set of nonzero real numbers forms an abelian group under multiplication, and the set of all real numbers forms an abelian group under addition. The set of invertible $n\times n$ matrices, the general linear group, is a very important group in which the law of composition is matrix multiplication. It is not abelian unless $n = 1$ .

例如，非零实数集在乘法下构成一个阿贝尔群，而所有实数集在加法下构成一个阿贝尔群。可逆 $n\times n$ 矩阵的集合，即一般线性群，是一个非常重要的群，其合成律是矩阵乘法。除非 $n = 1$，否则它不是阿贝尔群。

When the law of composition is evident, it is customary to denote a group and the set of its elements by the same symbol.

当合成律显而易见时，习惯上用同一个符号表示一个群及其元素的集合。

The order of a group $G$ is the number of elements that it contains. We will often denote the order by $|G|$ :
$$|G| = \mathrm{number~of~elements,~the~order,~of~}G. \quad (2.2.1)$$

一个群 $G$ 的**阶**是它所包含的元素个数。我们经常用 $|G|$ 表示阶：
$$|G| = \text{元素个数，即 }G\text{ 的阶}. \quad (2.2.1)$$

===== Page 41 =====

If the order is finite, $G$ is said to be a finite group. If not, $G$ is an infinite group. The same terminology is used for any set. The order $|S|$ of a set $S$ is the number of its elements.

如果阶是有限的，则称 $G$ 是**有限群**。如果不是，则 $G$ 是**无限群**。同样的术语用于任何集合。一个集合 $S$ 的阶 $|S|$ 是其元素的个数。

Here is our notation for some familiar infinite abelian groups:

以下是我们对一些熟悉的无限阿贝尔群的记号：

$$\begin{array}{r l}
\mathbb{Z}^{+}: & \text{整数集，加法为其合成律}\\
\mathbb{R}^{+}: & \text{实数集，加法为其合成律}\\
\mathbb{R}^{\times}: & \text{非零实数集，乘法为其合成律}\\
\mathbb{C}^{+},\mathbb{C}^{\times}: & \text{类似的群，其中复数集 }\mathbb{C}\text{ 取代了实数集 }\mathbb{R}
\end{array} \quad (2.2.2)$$

Warning: Others might use the symbol $\mathbb{R}^{+}$ to denote the set of positive real numbers. To be unambiguous, it might be better to denote the additive group of reals by $(\mathbb{R}, + )$ , thus displaying its law of composition explicitly. However, our notation is more compact. Also, the symbol $\mathbb{R}^{\times}$ denotes the multiplicative group of nonzero real numbers. The set of all real numbers is not a group under multiplication because 0 isn't invertible. $\square$

警告：其他人可能使用符号 $\mathbb{R}^{+}$ 来表示正实数集。为了明确起见，最好将实数的加法群记为 $(\mathbb{R}, +)$，从而明确显示其合成律。然而，我们的记号更紧凑。此外，符号 $\mathbb{R}^{\times}$ 表示非零实数的乘法群。所有实数的集合在乘法下不是群，因为 0 不可逆。$\square$

Proposition 2.2.3 Cancellation Law. Let $a,b,c$ be elements of a group $G$ whose law of composition is written multiplicatively. If $ab = ac$ or if $ba = ca$ , then $b = c$ . If $ab = a$ or if $ba = a$ , then $b = 1$ .

命题 2.2.3 消去律。设 $a,b,c$ 是群 $G$ 中的元素，其合成律写成乘法形式。如果 $ab = ac$ 或 $ba = ca$，那么 $b = c$。如果 $ab = a$ 或 $ba = a$，那么 $b = 1$。

Proof. Multiply both sides of $ab = ac$ on the left by $a^{- 1}$ to obtain $b = c$ . The other proofs are analogous. $\square$

证明：在 $ab = ac$ 的两边左乘 $a^{- 1}$ 得到 $b = c$。其他证明类似。$\square$

Multiplication by $a^{- 1}$ is essential for this proof. The Cancellation Law needn't hold when the element $a$ is not invertible. For instance,

乘上 $a^{- 1}$ 对于这个证明是必不可少的。当元素 $a$ 不可逆时，消去律不一定成立。例如，
$$\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \begin{bmatrix} 1 \\ 2 \end{bmatrix} = \begin{bmatrix} 5 \\ 11 \end{bmatrix},\quad \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \begin{bmatrix} 1 \\ 2 \end{bmatrix} = \begin{bmatrix} 5 \\ 11 \end{bmatrix}$$
这里原文的例子可能有笔误，但意思清楚。

Two basic examples of groups are obtained from laws of composition that we have considered - multiplication of matrices and composition of functions - by leaving out the elements that are not invertible.

两个基本的群例子来自于我们考虑过的合成律——矩阵乘法和函数的复合——通过去掉那些不可逆的元素得到。

The $n\times n$ general linear group is the group of all invertible $n\times n$ matrices. It is denoted by
$$G L_{n} = \{n\times n\mathrm{~invertible~matrices~}A\} .$$

$n\times n$ **一般线性群**是所有可逆 $n\times n$ 矩阵的群。记为
$$G L_{n} = \{n\times n\text{ 可逆矩阵 } A\}.$$

If we want to indicate that we are working with real or with complex matrices, we write $G L_{n}(\mathbb{R})$ or $G L_{n}(\mathbb{C})$ , according to the case.

如果我们想指出是在实数或复数矩阵上工作，我们分别写成 $G L_{n}(\mathbb{R})$ 或 $G L_{n}(\mathbb{C})$。

Let $M$ be the set of maps from a set $T$ to itself. A map $f:T\to T$ has an inverse function if and only if it is bijective, in which case we say $f$ is a permutation of $T$ . The permutations of $T$ form a group, the law being composition of maps. As in section 1.5, we use multiplicative notation for the composition of permutations, writing $q p$ for $q\circ p$ .

设 $M$ 是从一个集合 $T$ 到自身的映射的集合。一个映射 $f:T\to T$ 有逆函数当且仅当它是双射的，在这种情况下我们称 $f$ 是 $T$ 的一个**置换**。$T$ 的置换构成一个群，其合成律是映射的复合。如同 1.5 节，我们为置换的复合使用乘法记号，将 $q\circ p$ 写成 $q p$。

The group of permutations of the set of indices $\{1,2,\ldots ,\mathbf{n}\}$ is called the symmetric group, and is denoted by $S_{n}$ :
$$S_{n}\mathrm{~is~the~group~of~permutations~of~the~indices~}\mathbf{1},2,\ldots ,\mathbf{n}. \quad (2.2.5)$$

指标集 $\{1,2,\ldots ,\mathbf{n}\}$ 的置换群称为**对称群**，记为 $S_{n}$：
$$S_{n}\text{ 是指标 } \mathbf{1},2,\ldots ,\mathbf{n}\text{ 的置换群}. \quad (2.2.5)$$

===== Page 42 =====

There are $n!$ ( $n$ factorial) $= 1\cdot 2\cdot 3\dots n$ ) permutations of a set of $n$ elements, so the symmetric group $S_{n}$ is a finite group of order $n!$

有 $n!$（$n$ 阶乘 $= 1\cdot 2\cdot 3\dots n$）个 $n$ 个元素的集合的置换，所以对称群 $S_{n}$ 是一个阶为 $n!$ 的有限群。

The permutations of a set $\{a,b\}$ of two elements are the identity $i$ and the transposition $\tau$ (see 2.1.3). They form a group of order two. If we replace $a$ by 1 and $b$ by 2, we see that this is the same group as the symmetric group $S_{2}$ . There is essentially only one group $G$ of order two. To see this, we note that one of its elements must be the identity 1; let the other element be $g$ . The multiplication table for the group contains the four products 11, 1g, $g1$ and $g g$ . All except $g g$ are determined by the fact that 1 is the identity element. Moreover, the Cancellation Law shows that $g g\neq g$ . The only possibility is $g g = 1$ . So the multiplication table is completely determined. There is just one group law.

两个元素的集合 $\{a,b\}$ 的置换是恒等置换 $i$ 和对换 $\tau$（见 2.1.3）。它们构成一个二阶群。如果我们将 $a$ 替换为 1，$b$ 替换为 2，我们看到这与对称群 $S_{2}$ 是同一个群。本质上只有一个二阶群 $G$。要看到这一点，我们注意到它的一个元素必须是单位元 1；设另一个元素为 $g$。该群的乘法表包含四个乘积 11, 1g, $g1$ 和 $g g$。除了 $g g$ 之外，所有乘积都由 1 是单位元这一事实确定。此外，消去律表明 $g g\neq g$。唯一的可能性是 $g g = 1$。所以乘法表被完全确定。只有一个群律。

We describe the symmetric group $S_{3}$ next. This group, which has order six, serves as a convenient example because it is the smallest group whose law of composition isn't commutative. We will refer to it often. To describe it, we pick two particular permutations in terms of which we can write all others. We take the cyclic permutation (123), and the transposition (12), and label them as $x$ and $y$ , respectively. The rules
$$x^{3} = 1, y^{2} = 1, yx = x^{2}y \quad (2.2.6)$$
are easy to verify. Using the cancellation law, one sees that the six elements $1, x$ , $x^{2}$ , $y$ , $xy$ , $x^{2}y$ are distinct. So they are the six elements of the group:
$$S_{3} = \{1,x,x^{2};y,xy,x^{2}y\} . \quad (2.2.7)$$

接下来我们描述对称群 $S_{3}$。这个群有六阶，作为一个方便的例子，因为它是最小的合成律不交换的群。我们将经常提到它。为了描述它，我们选取两个特定的置换，通过它们我们可以写出所有其他置换。我们取循环置换 (123)，以及对换 (12)，并将它们分别标记为 $x$ 和 $y$。规则
$$x^{3} = 1, y^{2} = 1, yx = x^{2}y \qquad (2.2.6)$$
很容易验证。使用消去律，可以看到六个元素 $1, x, x^{2}, y, xy, x^{2}y$ 是互不相同的。所以它们是群的六个元素：
$$S_{3} = \{1,x,x^{2};y,xy,x^{2}y\} . \qquad (2.2.7)$$

In the future, we will refer to (2.2.6) and (2.2.7) as our "usual presentation" of the symmetric group $S_{3}$ . Note that $S_{3}$ is not a commutative group, because $yx\neq xy$ .

将来，我们将把 (2.2.6) 和 (2.2.7) 称为对称群 $S_{3}$ 的“通常表示”。注意 $S_{3}$ 不是交换群，因为 $yx\neq xy$。

The rules (2.2.6) suffice for computation. Any product of the elements $x$ and $y$ and of their inverses can be shown to be equal to one of the products (2.2.7) by applying the rules repeatedly. To do so, we move all occurrences of $y$ to the right side using the last rule, and we use the first two rules to keep the exponents small. For instance,
$$x^{-1}y^{3}x^{2}y = x^{2}yx^{2}y = x^{2}(yx)xy = x^{2}(x^{2}y)xy = xyxy = x(x^{2}y)y = 1. \quad (2.2.8)$$

规则 (2.2.6) 足以进行计算。$x$ 和 $y$ 及其逆元的任何乘积都可以通过重复应用这些规则证明等于 (2.2.7) 中的一个乘积。为此，我们使用最后一个规则将所有出现的 $y$ 移到右边，并使用前两个规则保持指数较小。例如，
$$x^{-1}y^{3}x^{2}y = x^{2}yx^{2}y = x^{2}(yx)xy = x^{2}(x^{2}y)xy = xyxy = x(x^{2}y)y = 1. \qquad (2.2.8)$$

One can write out a multiplication table for $S_{3}$ with the aid of the rules (2.2.6), and because of this, those rules are called defining relations for the group. We study defining relations in Chapter 7.

借助规则 (2.2.6) 可以写出 $S_{3}$ 的乘法表，因此这些规则被称为群的**定义关系**。我们在第七章研究定义关系。

We stop here. The structure of $S_{n}$ becomes complicated very rapidly as $n$ increases.

我们在这里停下来。随着 $n$ 的增加，$S_{n}$ 的结构变得非常复杂。

One reason that the general linear groups and the symmetric groups are important is that many other groups are contained in them as subgroups. A subset $H$ of a group $G$ is a subgroup if it has the following properties:

一般线性群和对称群重要的一个原因是许多其他群作为子群包含在其中。群 $G$ 的一个子集 $H$ 是一个**子群**，如果它具有以下性质：

(2.2.9) Closure: If $a$ and $b$ are in $H$ , then $ab$ is in $H$
Identity: 1 is in $H$
Inverses: If $a$ is in $H$ , then $a^{- 1}$ is in $H$ .

(2.2.9) **封闭性**：如果 $a$ 和 $b$ 在 $H$ 中，那么 $ab$ 在 $H$ 中。
**单位元**：1 在 $H$ 中。
**逆元**：如果 $a$ 在 $H$ 中，那么 $a^{- 1}$ 在 $H$ 中。

These conditions are explained as follows: The first one tells us that the law of composition on the group $G$ defines a law of composition on $H$ , called the induced law. The second and third conditions say that $H$ is a group with respect to this induced law. Notice that (2.2.9)

这些条件解释如下：第一个条件告诉我们群 $G$ 上的合成律在 $H$ 上定义了一个合成律，称为**诱导律**。第二和第三个条件说明 $H$ 关于这个诱导律是一个群。注意 (2.2.9)

===== Page 43 =====

ments all parts of the definition of a group except for the associative law. We don't need to mention associativity. It carries over automatically from $G$ to the subset $H$ .

涵盖了群的定义的所有部分，除了结合律。我们不需要提到结合律。它自动从 $G$ 传递到子集 $H$。

Notes: (i) In mathematics, it is essential to learn the definition of each term. An intuitive feeling will not suffice. For example, the set $T$ of invertible real (upper) triangular $2 \times 2$ matrices is a subgroup of the general linear group $GL_2$ , and there is only one way to verify this, namely to go back to the definition. It is true that $T$ is a subset of $GL_2$ . One must verify that the product of invertible triangular matrices is triangular, that the identity is triangular, and that the inverse of an invertible triangular matrix is triangular. Of course these points are very easy to check.

注：(i) 在数学中，学习每个术语的定义是必不可少的。直观的感觉是不够的。例如，可逆实（上）三角 $2 \times 2$ 矩阵的集合 $T$ 是一般线性群 $GL_2$ 的一个子群，验证这一点只有一种方法，即回到定义。确实，$T$ 是 $GL_2$ 的子集。必须验证可逆三角矩阵的乘积是三角的，单位元是三角的，以及可逆三角矩阵的逆是三角的。当然这些点很容易验证。

(ii) Closure is sometimes mentioned as one of the axioms for a group, to indicate that the product $ab$ of elements of $G$ is again an element of $G$ . We include closure as a part of what is meant by a law of composition. Then it doesn't need to be mentioned separately in the definition of a group.

(ii) 封闭性有时被列为群的公理之一，以表明 $G$ 中元素的乘积 $ab$ 再次是 $G$ 的元素。我们将封闭性作为合成律含义的一部分。那么它不需要在群的定义中单独提及。

## Examples 2.2.10

## 例子 2.2.10

(a) The set of complex numbers of absolute value 1, the set of points on the unit circle in the complex plane, is a subgroup of the multiplicative group $\mathbb{C}^{\times}$ called the circle group.
(b) The group of real $n \times n$ matrices with determinant 1 is a subgroup of the general linear group $GL_n$ , called the special linear group. It is denoted by $SL_n$ :
$$SL_{n}(\mathbb{R})\mathrm{~is~the~set~of~real~}n\times n\mathrm{~matrices~}A\mathrm{~with~determinant~equal~to~}1.$$

(a) 绝对值为 1 的复数集合，即复平面上的单位圆上的点集，是乘法群 $\mathbb{C}^{\times}$ 的一个子群，称为**圆群**。
(b) 行列式为 1 的实 $n\times n$ 矩阵群是一般线性群 $GL_n$ 的一个子群，称为**特殊线性群**。记为 $SL_n$：
$$SL_{n}(\mathbb{R})\text{ 是行列式等于 }1\text{ 的实 } n\times n\text{ 矩阵 } A\text{ 的集合}.$$

The defining properties (2.2.9) are often very easy to verify for a particular subgroup, and we may not carry the verification out.

对于特定的子群，定义性质 (2.2.9) 通常很容易验证，我们可能不会执行验证。

Every group $G$ has two obvious subgroups: the group $G$ itself, and the trivial subgroup that consists of the identity element alone. A subgroup is a proper subgroup if it is not one of those two.

每个群 $G$ 都有两个明显的子群：群 $G$ 本身，以及仅由单位元组成的**平凡子群**。如果子群不是这两个之一，则称为**真子群**。

### 2.3 SUBGROUPS OF THE ADDITIVE GROUP OF INTEGERS

### 2.3 整数加法群的子群

We review some elementary number theory here, in terms of subgroups of the additive group $\mathbb{Z}^{+}$ of integers. To begin, we list the axioms for a subgroup when additive notation is used in the group: A subset $S$ of a group $G$ with law of composition written additively is a subgroup if it has these properties:

我们在这里回顾一些初等数论，用整数加法群 $\mathbb{Z}^{+}$ 的子群来表述。首先，当群中使用加法记号时，列出子群的公理：群 $G$ 的一个子集 $S$，其合成律写成加法形式，如果它具有以下性质，则是一个子群：

(2.3.1)

Closure: If $a$ and $b$ are in $S$ , then $a + b$ is in $S$ .
Identity: 0 is in $S$ .
Inverses: If $a$ is in $S$ then $- a$ is in $S$ .

(2.3.1)

**封闭性**：如果 $a$ 和 $b$ 在 $S$ 中，那么 $a + b$ 在 $S$ 中。
**单位元**：0 在 $S$ 中。
**逆元**：如果 $a$ 在 $S$ 中，那么 $- a$ 也在 $S$ 中。

Let $a$ be an integer different from 0. We denote the subset of $\mathbb{Z}$ that consists of all multiples of $a$ by $\mathbb{Z}a$ :
$$\mathbb{Z}a = \{n\in \mathbb{Z}\mid n = ka\mathrm{~for~some~}k\mathrm{~in~}\mathbb{Z}\} .$$

设 $a$ 是一个非零整数。我们用 $\mathbb{Z}a$ 表示由 $a$ 的所有倍数组成的 $\mathbb{Z}$ 的子集：
$$\mathbb{Z}a = \{n\in \mathbb{Z}\mid n = ka\text{ 对于某个 }k\text{ 在 }\mathbb{Z}\text{ 中}\}.$$

===== Page 44 =====

This is a subgroup of $\mathbb{Z}^{+}$ . Its elements can also be described as the integers divisible by $a$ .

这是 $\mathbb{Z}^{+}$ 的一个子群。它的元素也可以描述为能被 $a$ 整除的整数。

Theorem 2.3.3 Let $S$ be a subgroup of the additive group $\mathbb{Z}^{+}$ . Either $S$ is the trivial subgroup $\{0\}$ , or else it has the form $\mathbb{Z}a$ , where $a$ is the smallest positive integer in $S$ .

定理 2.3.3 设 $S$ 是加法群 $\mathbb{Z}^{+}$ 的一个子群。要么 $S$ 是平凡子群 $\{0\}$，要么它具有 $\mathbb{Z}a$ 的形式，其中 $a$ 是 $S$ 中最小的正整数。

Proof. Let $S$ be a subgroup of $\mathbb{Z}^{+}$ . Then 0 is in $S$ , and if 0 is the only element of $S$ then $S$ is the trivial subgroup. So that case is settled. Otherwise, $S$ contains an integer $n$ different from 0, and either $n$ or $- n$ is positive. The third property of a subgroup tells us that $- n$ is in $S$ , so in either case, $S$ contains a positive integer. We must show that $S$ is equal to $\mathbb{Z}a$ , when $a$ is the smallest positive integer in $S$ .

证明：设 $S$ 是 $\mathbb{Z}^{+}$ 的一个子群。那么 0 在 $S$ 中，如果 0 是 $S$ 的唯一元素，那么 $S$ 是平凡子群。所以这种情况已经解决。否则，$S$ 包含一个非零整数 $n$，而 $n$ 或 $- n$ 是正数。子群的第三个性质告诉我们 $- n$ 也在 $S$ 中，所以无论哪种情况，$S$ 都包含一个正整数。我们必须证明，当 $a$ 是 $S$ 中最小的正整数时，$S$ 等于 $\mathbb{Z}a$。

We first show that $\mathbb{Z}a$ is a subset of $S$ , in other words, that $k a$ is in $S$ for every integer $k$ . If $k$ is a positive integer, then $k a = a + a + \dots +a$ ( $k$ terms). Since $a$ is in $S$ , closure and induction show that $k a$ is in $S$ . Since inverses are in $S$ , $- k a$ is in $S$ . Finally, $0 = 0a$ is in $S$ .

我们首先证明 $\mathbb{Z}a$ 是 $S$ 的子集，换句话说，对于每个整数 $k$，$k a$ 在 $S$ 中。如果 $k$ 是正整数，那么 $k a = a + a + \dots +a$（$k$ 项）。由于 $a$ 在 $S$ 中，封闭性和归纳法表明 $k a$ 在 $S$ 中。由于逆元在 $S$ 中，$- k a$ 也在 $S$ 中。最后，$0 = 0a$ 在 $S$ 中。

Next we show that $S$ is a subset of $\mathbb{Z}a$ , that is, every element $n$ of $S$ is an integer multiple of $a$ . We use division with remainder to write $n = q a + r$ , where $q$ and $r$ are integers and where the remainder $r$ is in the range $0 \leq r < a$ . Since $\mathbb{Z}a$ is contained in $S$ , $q a$ is in $S$ , and of course $n$ is in $S$ . Since $S$ is a subgroup, $r = n - q a$ is in $S$ too. Now by our choice, $a$ is the smallest positive integer in $S$ , while the remainder $r$ is in the range $0 \leq r < a$ . The only remainder that can be in $S$ is 0. So $r = 0$ and $n$ is the integer multiple $q a$ of $a$ . $\square$

接下来我们证明 $S$ 是 $\mathbb{Z}a$ 的子集，也就是说，$S$ 中的每个元素 $n$ 都是 $a$ 的整数倍。我们使用带余除法将 $n$ 写成 $n = q a + r$，其中 $q$ 和 $r$ 是整数，并且余数 $r$ 在 $0 \leq r < a$ 范围内。由于 $\mathbb{Z}a$ 包含在 $S$ 中，$q a$ 在 $S$ 中，当然 $n$ 在 $S$ 中。由于 $S$ 是一个子群，$r = n - q a$ 也在 $S$ 中。现在根据我们的选择，$a$ 是 $S$ 中最小的正整数，而余数 $r$ 在 $0 \leq r < a$ 范围内。可能在 $S$ 中的唯一余数是 0。所以 $r = 0$，并且 $n$ 是 $a$ 的整数倍 $q a$。$\square$

There is a striking application of Theorem 2.3.3 to subgroups that contain two integers $a$ and $b$ . The set of all integer combinations $r a + s b$ of $a$ and $b$ ,
$$S = \mathbb{Z}a + \mathbb{Z}b = \{n\in \mathbb{Z}\mid n = r a + s b\mathrm{~for~some~integers~}r,s\}$$
is a subgroup of $\mathbb{Z}^{+}$ . It is called the subgroup generated by $a$ and $b$ because it is the smallest subgroup that contains both $a$ and $b$ . Let's assume that $a$ and $b$ aren't both zero, so that $S$ is not the trivial subgroup $\{0\}$ . Theorem 2.3.3 tells us that this subgroup $S$ has the form $\mathbb{Z}d$ for some positive integer $d$ ; it is the set of integers divisible by $d$ . The generator $d$ is called the greatest common divisor of $a$ and $b$ , for reasons that are explained in parts (a) and (b) of the next proposition. The greatest common divisor of $a$ and $b$ is sometimes denoted by $\gcd (a,b)$ .

定理 2.3.3 有一个惊人的应用，用于包含两个整数 $a$ 和 $b$ 的子群。$a$ 和 $b$ 的所有整数组合 $r a + s b$ 的集合，
$$S = \mathbb{Z}a + \mathbb{Z}b = \{n\in \mathbb{Z}\mid n = r a + s b\text{ 对于某些整数 }r,s\}$$
是 $\mathbb{Z}^{+}$ 的一个子群。它被称为由 $a$ 和 $b$ 生成的子群，因为它是包含 $a$ 和 $b$ 两者的最小子群。我们假设 $a$ 和 $b$ 不全为零，这样 $S$ 就不是平凡子群 $\{0\}$。定理 2.3.3 告诉我们这个子群 $S$ 具有 $\mathbb{Z}d$ 的形式，其中 $d$ 是某个正整数；它是能被 $d$ 整除的整数的集合。生成元 $d$ 被称为 $a$ 和 $b$ 的**最大公因数**，原因由下一个命题的 (a) 和 (b) 部分解释。$a$ 和 $b$ 的最大公因数有时记为 $\gcd (a,b)$。

Proposition 2.3.5 Let $a$ and $b$ be integers, not both zero, and let $d$ be their greatest common divisor, the positive integer that generates the subgroup $S = \mathbb{Z}a + \mathbb{Z}b$ . So $\mathbb{Z}d = \mathbb{Z}a + \mathbb{Z}b$ . Then
(a) $d$ divides $a$ and $b$ .
(b) If an integer $e$ divides both $a$ and $b$ , it also divides $d$ .
(c) There are integers $r$ and $s$ such that $d = r a + s b$ .

命题 2.3.5 设 $a$ 和 $b$ 是不全为零的整数，并设 $d$ 是它们的最大公因数，即生成子群 $S = \mathbb{Z}a + \mathbb{Z}b$ 的正整数。所以 $\mathbb{Z}d = \mathbb{Z}a + \mathbb{Z}b$。那么
(a) $d$ 整除 $a$ 和 $b$。
(b) 如果整数 $e$ 整除 $a$ 和 $b$，那么它也整除 $d$。
(c) 存在整数 $r$ 和 $s$ 使得 $d = r a + s b$。

Proof. Part (c) restates the fact that $d$ is an element of $S$ . Next, $a$ and $b$ are elements of $S$ and $S = \mathbb{Z}d$ , so $d$ divides $a$ and $b$ . Finally, if an integer $e$ divides both $a$ and $b$ , then $e$ divides the integer combination $r a + s b = d$ . $\square$

证明：(c) 部分重述了 $d$ 是 $S$ 的元素这一事实。接下来，$a$ 和 $b$ 是 $S$ 的元素，并且 $S = \mathbb{Z}d$，所以 $d$ 整除 $a$ 和 $b$。最后，如果整数 $e$ 整除 $a$ 和 $b$，那么 $e$ 整除整数组合 $r a + s b = d$。$\square$

Note: If $e$ divides $a$ and $b$ , then $e$ divides any integer of the form $m a + n b$ . So (c) implies (b). But (b) does not imply (c). As we shall see, property (c) is a powerful tool. $\square$

注：如果 $e$ 整除 $a$ 和 $b$，那么 $e$ 整除任何形如 $m a + n b$ 的整数。所以 (c) 蕴含 (b)。但 (b) 并不蕴含 (c)。正如我们将看到的，性质 (c) 是一个强大的工具。$\square$

One can compute a greatest common divisor easily by repeated division with remainder: For example, if $a = 314$ and $b = 136$ , then
$$314 = 2\cdot 136 + 42,136 = 3\cdot 42 + 10,42 = 4\cdot 10 + 2.$$

可以通过重复带余除法轻松计算最大公因数：例如，如果 $a = 314$ 和 $b = 136$，那么
$$314 = 2\cdot 136 + 42,\quad 136 = 3\cdot 42 + 10,\quad 42 = 4\cdot 10 + 2.$$

===== Page 45 =====

Using the first of these equations, one can show that any integer combination of 314 and 136 can also be written as an integer combination of 136 and the remainder 42, and vice versa. So $\mathbb{Z}(314) + \mathbb{Z}(136) = \mathbb{Z}(136) + \mathbb{Z}(42)$ , and therefore $\gcd (314,136) = \gcd (136,42)$ . Similarly, $\gcd (136,42) = \gcd (42,10) = \gcd (10,2) = 2$ . So the greatest common divisor of 314 and 136 is 2. This iterative method of finding the greatest common divisor of two integers is called the Euclidean Algorithm.

使用这些方程中的第一个，可以证明 314 和 136 的任何整数组合也可以写成 136 和余数 42 的整数组合，反之亦然。所以 $\mathbb{Z}(314) + \mathbb{Z}(136) = \mathbb{Z}(136) + \mathbb{Z}(42)$，因此 $\gcd (314,136) = \gcd (136,42)$。类似地，$\gcd (136,42) = \gcd (42,10) = \gcd (10,2) = 2$。所以 314 和 136 的最大公因数是 2。这种求两个整数最大公因数的迭代方法称为**欧几里得算法**。

If integers $a$ and $b$ are given, a second way to find their greatest common divisor is to factor each of them into prime integers and then to collect the common prime factors. Properties (a) and (b) of Proposition 2.3.5 are easy to verify using this method. But without Theorem 2.3.3, property (c), that the integer determined by this method is an integer combination of $a$ and $b$ wouldn't be clear at all. Let's not discuss this point further here. We come back to it in Chapter 12.

如果给定整数 $a$ 和 $b$，求其最大公因数的第二种方法是将每个数分解为素整数，然后收集共同的素因子。使用这种方法，命题 2.3.5 的性质 (a) 和 (b) 很容易验证。但如果没有定理 2.3.3，通过这种方法确定的整数是 $a$ 和 $b$ 的整数组合这一性质 (c) 就完全不清楚了。我们现在不进一步讨论这一点。我们将在第十二章回到这个问题。

Two nonzero integers $a$ and $b$ are said to be relatively prime if the only positive integer that divides both of them is 1. Then their greatest common divisor is 1: $\mathbb{Z}a + \mathbb{Z}b = \mathbb{Z}$ .

如果两个非零整数 $a$ 和 $b$ 同时整除它们的唯一正整数是 1，则称它们是**互素的**。那么它们的最大公因数是 1：$\mathbb{Z}a + \mathbb{Z}b = \mathbb{Z}$。

Corollary 2.3.6 A pair $a,b$ of integers is relatively prime if and only if there are integers $r$ and $s$ such that $ra + sb = 1$ .

推论 2.3.6 一对整数 $a,b$ 互素当且仅当存在整数 $r$ 和 $s$ 使得 $ra + sb = 1$。

Corollary 2.3.7 Let $p$ be a prime integer. If $p$ divides a product $ab$ of integers, then $p$ divides $a$ or $p$ divides $b$ .

推论 2.3.7 设 $p$ 是一个素整数。如果 $p$ 整除整数乘积 $ab$，那么 $p$ 整除 $a$ 或 $p$ 整除 $b$。

Proof. Suppose that the prime $p$ divides $ab$ but does not divide $a$ . The only positive divisors of $p$ are 1 and $p$ . Since $p$ does not divide $a$ , $\gcd (a,p) = 1$ . Therefore there are integers $r$ and $s$ such that $ra + sp = 1$ . We multiply by $b$ : $rab + spb = b$ , and we note that $p$ divides both $rab$ and $spb$ . So $p$ divides $b$ .

证明：假设素数 $p$ 整除 $ab$ 但不整除 $a$。$p$ 的正因数只有 1 和 $p$。由于 $p$ 不整除 $a$，$\gcd (a,p) = 1$。因此存在整数 $r$ 和 $s$ 使得 $ra + sp = 1$。我们乘以 $b$：$rab + spb = b$，并注意到 $p$ 整除 $rab$ 和 $spb$。所以 $p$ 整除 $b$。$\square$

There is another subgroup of $\mathbb{Z}^{+}$ associated to a pair $a,b$ of integers, namely the intersection $\mathbb{Z}a\cap \mathbb{Z}b$ , the set of integers contained both in $\mathbb{Z}a$ and in $\mathbb{Z}b$ . We assume now that neither $a$ nor $b$ is zero. Then $\mathbb{Z}a\cap \mathbb{Z}b$ is a subgroup. It is not the trivial subgroup $\{0\}$ because it contains the product $ab$ , which isn't zero. So $\mathbb{Z}a\cap \mathbb{Z}b$ has the form $\mathbb{Z}m$ for some positive integer $m$ . This integer $m$ is called the least common multiple of $a$ and $b$ , sometimes denoted by $\operatorname{lcm}(a,b)$ , for reasons that are explained in the next proposition.

与一对整数 $a,b$ 相关的还有 $\mathbb{Z}^{+}$ 的另一个子群，即交集 $\mathbb{Z}a\cap \mathbb{Z}b$，即同时包含在 $\mathbb{Z}a$ 和 $\mathbb{Z}b$ 中的整数的集合。我们现在假设 $a$ 和 $b$ 都不为零。那么 $\mathbb{Z}a\cap \mathbb{Z}b$ 是一个子群。它不是平凡子群 $\{0\}$，因为它包含乘积 $ab$，而 $ab$ 不为零。所以 $\mathbb{Z}a\cap \mathbb{Z}b$ 具有 $\mathbb{Z}m$ 的形式，其中 $m$ 是某个正整数。这个整数 $m$ 被称为 $a$ 和 $b$ 的**最小公倍数**，有时记为 $\operatorname{lcm}(a,b)$，原因由下一个命题解释。

Proposition 2.3.8 Let $a$ and $b$ be integers different from zero, and let $m$ be their least common multiple - the positive integer that generates the subgroup $S = \mathbb{Z}a\cap \mathbb{Z}b$ . So $\mathbb{Z}m = \mathbb{Z}a\cap \mathbb{Z}b$ . Then
(a) $m$ is divisible by both $a$ and $b$ .
(b) If an integer $n$ is divisible by $a$ and by $b$ , then it is divisible by $m$ .

命题 2.3.8 设 $a$ 和 $b$ 是不为零的整数，并设 $m$ 是它们的最小公倍数——生成子群 $S = \mathbb{Z}a\cap \mathbb{Z}b$ 的正整数。所以 $\mathbb{Z}m = \mathbb{Z}a\cap \mathbb{Z}b$。那么
(a) $m$ 能被 $a$ 和 $b$ 整除。
(b) 如果整数 $n$ 能被 $a$ 和 $b$ 整除，那么它能被 $m$ 整除。

Proof. Both statements follow from the fact that an integer is divisible by $a$ and by $b$ if and only if it is contained in $\mathbb{Z}m = \mathbb{Z}a\cap \mathbb{Z}b$ . $\square$

证明：两个陈述都源于这样一个事实：一个整数能被 $a$ 和 $b$ 整除当且仅当它包含在 $\mathbb{Z}m = \mathbb{Z}a\cap \mathbb{Z}b$ 中。$\square$

Corollary 2.3.9 Let $d = \gcd (a,b)$ and $m = \operatorname{lcm}(a,b)$ be the greatest common divisor and least common multiple of a pair $a,b$ of positive integers, respectively. Then $ab = dm$ .

推论 2.3.9 设 $d = \gcd (a,b)$ 和 $m = \operatorname{lcm}(a,b)$ 分别是一对正整数 $a,b$ 的最大公因数和最小公倍数。那么 $ab = dm$。

Proof. Since $b / d$ is an integer, $a$ divides $ab / d$ . Similarly, $b$ divides $ab / d$ . So $m$ divides $ab / d$ , and $dm$ divides $ab$ . Next, we write $d = ra + sb$ . Then $dm = ram + sbm$ . Both terms

证明：由于 $b / d$ 是整数，$a$ 整除 $ab / d$。类似地，$b$ 整除 $ab / d$。所以 $m$ 整除 $ab / d$，并且 $dm$ 整除 $ab$。接下来，我们写成 $d = ra + sb$。那么 $dm = ram + sbm$。右边两项

===== Page 46 =====

on the right are divisible by $ab$ , so $ab$ divides $dm$ . Since $ab$ and $dm$ are positive and each one divides the other, $ab = dm$ . $\square$

都能被 $ab$ 整除，所以 $ab$ 整除 $dm$。由于 $ab$ 和 $dm$ 都是正数且彼此整除，所以 $ab = dm$。$\square$

### 2.4 CYCLIC GROUPS

### 2.4 循环群

We come now to an important abstract example of a subgroup, the cyclic subgroup generated by an arbitrary element $x$ of a group $G$ . We use multiplicative notation. The cyclic subgroup $H$ generated by $x$ is the set of all elements that are powers of $x$ :
$$H = \{\ldots ,x^{-2},x^{-1},1,x,x^{2},\ldots \} . \quad (2.4.1)$$

现在我们来看一个重要的抽象子群例子，即由群 $G$ 中任意元素 $x$ 生成的循环子群。我们使用乘法记号。由 $x$ 生成的循环子群 $H$ 是 $x$ 的所有幂的集合：
$$H = \{\ldots ,x^{-2},x^{-1},1,x,x^{2},\ldots \} . \qquad (2.4.1)$$

This is the smallest subgroup of $G$ that contains $x$ , and it is often denoted by $\langle x\rangle$ . But to interpret (2.4.1) correctly, we must remember that the notation $x^{n}$ represents an element of the group that is obtained in a particular way. Different powers may represent the same element. For example, if $G$ is the multiplicative group $\mathbb{R}^{\times}$ and $x = - 1$ , then all elements in the list are equal to 1 or to $- 1$ , and $H$ is the set $\{1, - 1\}$ .

这是 $G$ 中包含 $x$ 的最小子群，通常记为 $\langle x\rangle$。但要正确解释 (2.4.1)，我们必须记住记号 $x^{n}$ 代表以特定方式获得的群中的一个元素。不同的幂可能代表相同的元素。例如，如果 $G$ 是乘法群 $\mathbb{R}^{\times}$ 且 $x = - 1$，那么列表中的所有元素都等于 1 或 $- 1$，并且 $H$ 是集合 $\{1, - 1\}$。

There are two possibilities: Either the powers $x^{n}$ represent distinct elements, or they do not. We analyze the case that the powers of $x$ are not distinct.

有两种可能性：要么幂 $x^{n}$ 表示不同的元素，要么不。我们分析 $x$ 的幂不互异的情况。

Proposition 2.4.2 Let $\langle x\rangle$ be the cyclic subgroup of a group $G$ generated by an element $x$ and let $S$ denote the set of integers $k$ such that $x^{k} = 1$ .
(a) The set $S$ is a subgroup of the additive group $\mathbb{Z}^{+}$ .
(b) Two powers $x^{r} = x^{s}$ , with $r \geq s$ , are equal if and only if $x^{r - s} = 1$ , i.e., if and only if $r - s$ is in $S$ .
(c) Suppose that $S$ is not the trivial subgroup. Then $S = \mathbb{Z}n$ for some positive integer $n$ . The powers $1, x, x^{2}, \ldots , x^{n - 1}$ are the distinct elements of the subgroup $\langle x \rangle$ , and the order of $\langle x \rangle$ is $n$ .

命题 2.4.2 设 $\langle x\rangle$ 是由群 $G$ 中一个元素 $x$ 生成的循环子群，并设 $S$ 表示满足 $x^{k} = 1$ 的整数 $k$ 的集合。
(a) 集合 $S$ 是加法群 $\mathbb{Z}^{+}$ 的一个子群。
(b) 两个幂 $x^{r} = x^{s}$，其中 $r \geq s$，相等当且仅当 $x^{r - s} = 1$，即当且仅当 $r - s$ 在 $S$ 中。
(c) 假设 $S$ 不是平凡子群。那么 $S = \mathbb{Z}n$ 对于某个正整数 $n$。幂 $1, x, x^{2}, \ldots , x^{n - 1}$ 是子群 $\langle x \rangle$ 中互不相同的元素，并且 $\langle x \rangle$ 的阶为 $n$。

Proof. (a) If $x^{k} = 1$ and $x^{\ell} = 1$ , then $x^{k + \ell} = x^{k}x^{\ell} = 1$ . This shows that if $k$ and $\ell$ are in $S$ , then $k + \ell$ is in $S$ . So the first property (2.3.1) for a subgroup is verified. Also, $x^{0} = 1$ , so 0 is in $S$ . Finally, if $k$ is in $S$ , i.e., $x^{k} = 1$ , then $x^{- k} = (x^{k})^{- 1} = 1$ too, so $- k$ is in $S$ .
(b) This follows from the Cancellation Law 2.2.3.
(c) Suppose that $S \neq \{0\}$ . Theorem 2.3.3 shows that $S = \mathbb{Z}n$ , where $n$ is the smallest positive integer in $S$ . If $x^{k}$ is an arbitrary power, we divide $k$ by $n$ , writing $k = qn + r$ with $r$ in the range $0 \leq r < n$ . Then $x^{qn} = 1^{q} = 1$ , and $x^{k} = x^{qn}x^{r} = x^{r}$ . Therefore $x^{k}$ is equal to one of the powers $1, x, \ldots , x^{n - 1}$ . It follows from (b) that these powers are distinct, because $x^{n}$ is the smallest positive power equal to 1. $\square$

证明：(a) 如果 $x^{k} = 1$ 且 $x^{\ell} = 1$，那么 $x^{k + \ell} = x^{k}x^{\ell} = 1$。这表明如果 $k$ 和 $\ell$ 在 $S$ 中，那么 $k + \ell$ 也在 $S$ 中。所以子群的第一个性质 (2.3.1) 得到验证。此外，$x^{0} = 1$，所以 0 在 $S$ 中。最后，如果 $k$ 在 $S$ 中，即 $x^{k} = 1$，那么 $x^{- k} = (x^{k})^{- 1} = 1$ 也一样，所以 $- k$ 在 $S$ 中。
(b) 这由消去律 2.2.3 得出。
(c) 假设 $S \neq \{0\}$。定理 2.3.3 表明 $S = \mathbb{Z}n$，其中 $n$ 是 $S$ 中最小的正整数。如果 $x^{k}$ 是任意幂，我们将 $k$ 除以 $n$，写成 $k = qn + r$，其中 $r$ 在 $0 \leq r < n$ 范围内。那么 $x^{qn} = 1^{q} = 1$，且 $x^{k} = x^{qn}x^{r} = x^{r}$。因此 $x^{k}$ 等于 $1, x, \ldots , x^{n - 1}$ 之一。由 (b) 可知这些幂是互异的，因为 $x^{n}$ 是等于 1 的最小正幂。$\square$

The group $\langle x \rangle = \{1, x, \ldots , x^{n - 1} \}$ described by part (c) of this proposition is called a cyclic group of order $n$ . It is called cyclic because repeated multiplication by $x$ cycles through the $n$ elements.

由这个命题的 (c) 部分描述的群 $\langle x \rangle = \{1, x, \ldots , x^{n - 1} \}$ 称为**阶为 $n$ 的循环群**。它被称为循环是因为反复乘以 $x$ 循环遍历这 $n$ 个元素。

An element $x$ of a group has order $n$ if $n$ is the smallest positive integer with the property $x^{n} = 1$ , which is the same thing as saying that the cyclic subgroup $\langle x \rangle$ generated by $x$ has order $n$ .

群中一个元素 $x$ 的**阶**为 $n$，如果 $n$ 是满足 $x^{n} = 1$ 的最小正整数，这与说由 $x$ 生成的循环子群 $\langle x \rangle$ 的阶为 $n$ 是一回事。

With the usual presentation of the symmetric group $S_{3}$ , the element $x$ has order 3, and $y$ has order 2. In any group, the identity element is the only element of order 1.

在对称群 $S_{3}$ 的通常表示中，元素 $x$ 的阶为 3，$y$ 的阶为 2。在任何群中，单位元是唯一的阶为 1 的元素。

===== Page 47 =====

If $x^{n} \neq 1$ for all $n > 0$, one says that $x$ has infinite order. The matrix $\begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$ has infinite order in $GL_2(\mathbb{R})$, while $\begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix}$ has order 6.

如果对于所有 $n > 0$ 都有 $x^{n} \neq 1$，则称 $x$ 有**无限阶**。矩阵 $\begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$ 在 $GL_2(\mathbb{R})$ 中有无限阶，而 $\begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix}$ 的阶为 6。

When $x$ has infinite order, the group $\langle x \rangle$ is said to be infinite cyclic. We won't have much to say about that case.

当 $x$ 有无限阶时，群 $\langle x \rangle$ 称为**无限循环群**。我们对此情况不会有太多讨论。

Proposition 2.4.3 Let $x$ be an element of finite order $n$ in a group, and let $k$ be an integer that is written as $k = nq + r$ where $q$ and $r$ are integers and $r$ is in the range $0 \leq r < n$.
* $x^{k} = x^{r}$.
* $x^{k} = 1$ if and only if $r = 0$.
* Let $d$ be the greatest common divisor of $k$ and $n$. The order of $x^{k}$ is equal to $n/d$.

命题 2.4.3 设 $x$ 是群中一个阶为 $n$ 的有限阶元素，并将整数 $k$ 写成 $k = nq + r$，其中 $q$ 和 $r$ 是整数，且 $r$ 在 $0 \leq r < n$ 范围内。
* $x^{k} = x^{r}$。
* $x^{k} = 1$ 当且仅当 $r = 0$。
* 设 $d$ 是 $k$ 和 $n$ 的最大公因数。$x^{k}$ 的阶等于 $n/d$。

One may also speak of the subgroup of a group $G$ generated by a subset $U$. This is the smallest subgroup of $G$ that contains $U$, and it consists of all elements of $G$ that can be expressed as a product of a string of elements of $U$ and of their inverses. A subset $U$ of $G$ is said to generate $G$ if every element of $G$ is such a product. For example, we saw in (2.2.7) that the set $U = \{x,y\}$ generates the symmetric group $S_3$. The elementary matrices generate $GL_n$ (1.2.16). In both of these examples, inverses aren't needed. That isn't always true. An infinite cyclic group $\langle x \rangle$ is generated by the element $x$, but negative powers are needed to fill out the group.

我们也可以谈论由群 $G$ 的子集 $U$ 生成的子群。这是 $G$ 中包含 $U$ 的最小子群，由 $G$ 中所有可以表示为 $U$ 中元素及其逆元的元素串乘积的元素组成。如果 $G$ 的每个元素都是这样的乘积，则称 $U$ **生成** $G$。例如，我们在 (2.2.7) 中看到集合 $U = \{x,y\}$ 生成对称群 $S_3$。初等矩阵生成 $GL_n$ (1.2.16)。在这两个例子中，不需要逆元。这并非总是如此。无限循环群 $\langle x \rangle$ 由元素 $x$ 生成，但需要负幂来填充整个群。

The Klein four group $V$, the group consisting of the four matrices
$$\left\{ \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}, \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}, \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}, \begin{bmatrix} -1 & 0 \\ 0 & -1 \end{bmatrix} \right\}, \qquad (2.4.4)$$
is the simplest group that is not cyclic. Any two of its elements different from the identity generate $V$. The quaternion group $H$ is another example of a small group. It consists of the eight matrices
$$H = \{\pm 1, \pm i, \pm j, \pm k\}, \qquad (2.4.5)$$
where
$$1 = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix},\quad i = \begin{bmatrix} i & 0 \\ 0 & -i \end{bmatrix},\quad j = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix},\quad k = \begin{bmatrix} 0 & i \\ i & 0 \end{bmatrix}.$$

**克莱因四元群** $V$，由四个矩阵组成的群
$$\left\{ \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}, \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}, \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}, \begin{bmatrix} -1 & 0 \\ 0 & -1 \end{bmatrix} \right\}, \qquad (2.4.4)$$
是**不是**循环群的最简单群。除单位元外的任何两个元素生成 $V$。**四元数群** $H$ 是另一个小群的例子。它由八个矩阵组成：
$$H = \{\pm 1, \pm i, \pm j, \pm k\}, \qquad (2.4.5)$$
其中
$$1 = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix},\quad i = \begin{bmatrix} i & 0 \\ 0 & -i \end{bmatrix},\quad j = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix},\quad k = \begin{bmatrix} 0 & i \\ i & 0 \end{bmatrix}.$$

These matrices can be obtained from the Pauli matrices of physics by multiplying by $i$. The two elements $i$ and $j$ generate $H$. Computation leads to the formulas
$$i^{2} = j^{2} = k^{2} = -1 ,\quad ij = -ji = k ,\quad jk = -kj = i ,\quad ki = -ik = j. \qquad (2.4.6)$$

这些矩阵可以通过乘以 $i$ 从物理学的泡利矩阵得到。两个元素 $i$ 和 $j$ 生成 $H$。计算得到公式
$$i^{2} = j^{2} = k^{2} = -1 ,\quad ij = -ji = k ,\quad jk = -kj = i ,\quad ki = -ik = j. \qquad (2.4.6)$$

### 2.5 HOMOMORPHISMS

### 2.5 同态

Let $G$ and $G^{\prime}$ be groups, written with multiplicative notation. A homomorphism $\phi:G \rightarrow G^{\prime}$ is a map from $G$ to $G^{\prime}$ such that for all $a$ and $b$ in $G$,
$$\phi(ab) = \phi(a)\phi(b). \qquad (2.5.1)$$

设 $G$ 和 $G^{\prime}$ 是群，写成乘法记号。一个**同态** $\phi:G \to G^{\prime}$ 是从 $G$ 到 $G^{\prime}$ 的一个映射，使得对于 $G$ 中所有的 $a$ 和 $b$，
$$\phi(ab) = \phi(a)\phi(b). \qquad (2.5.1)$$

===== Page 48 =====

The left side of this equation means
first multiply $a$ and $b$ in $G$ , then send the product to $G^{\prime}$ using the map $\phi$
while the right side means
first send $a$ and $b$ individually to $G^{\prime}$ using the map $\phi$ , then multiply their images in $G^{\prime}$ .

这个等式的左边意思是
先在 $G$ 中相乘 $a$ 和 $b$，然后通过映射 $\phi$ 将乘积送到 $G^{\prime}$，
而右边意思是
先用映射 $\phi$ 将 $a$ 和 $b$ 分别送到 $G^{\prime}$，然后在 $G^{\prime}$ 中乘它们的像。

Intuitively, a homomorphism is a map that is compatible with the laws of composition in the two groups, and it provides a way to relate different groups.

直观上，同态是一个与两个群中的合成律兼容的映射，它提供了一种关联不同群的方法。

Examples 2.5.2 The following maps are homomorphisms:

例子 2.5.2 以下映射是同态：

(a) the determinant function $\operatorname{det}:G L_{n}(\mathbb{R})\to \mathbb{R}^{\times}$ (1.4.10)
(b) the sign homomorphism $\sigma :S_{n}\to \{\pm 1\}$ that sends a permutation to its sign (1.5.11),
(c) the exponential map $\exp :\mathbb{R}^{+}\to \mathbb{R}^{\times}$ defined by $x\mapsto e^{x}$
(d) the map $\phi :\mathbb{Z}^{+}\to G$ defined by $\phi (n) = a^{n}$ , where $a$ is a given element of $G$
(e) the absolute value map $|\cdot|:\mathbb{C}^{\times}\to \mathbb{R}^{\times}$

(a) 行列式函数 $\det:G L_{n}(\mathbb{R})\to \mathbb{R}^{\times}$ (1.4.10)
(b) 符号同态 $\sigma :S_{n}\to \{\pm 1\}$，它将一个置换映射到它的符号 (1.5.11)，
(c) 指数映射 $\exp :\mathbb{R}^{+}\to \mathbb{R}^{\times}$，定义为 $x\mapsto e^{x}$
(d) 映射 $\phi :\mathbb{Z}^{+}\to G$，定义为 $\phi (n) = a^{n}$，其中 $a$ 是 $G$ 中给定的元素
(e) 绝对值映射 $|\cdot|:\mathbb{C}^{\times}\to \mathbb{R}^{\times}$

In examples (c) and (d), the law of composition is written additively in the domain and multiplicatively in the range. The condition (2.5.1) for a homomorphism must be rewritten to take this into account. It becomes
$$\phi (a + b) = \phi (a)\phi (b).$$

在例子 (c) 和 (d) 中，合成律在定义域中写成加法形式，在值域中写成乘法形式。同态的条件 (2.5.1) 必须重写以考虑这一点。它变为
$$\phi (a + b) = \phi (a)\phi (b).$$

The formula showing that the exponential map is a homomorphism is $e^{a + b} = e^{a}e^{b}$ .

显示指数映射是一个同态的公式是 $e^{a + b} = e^{a}e^{b}$。

The following homomorphisms need to be mentioned, though they are less interesting. The trivial homomorphism $\phi :G\to G^{\prime}$ between any two groups maps every element of $G$ to the identity in $G^{\prime}$ . If $H$ is a subgroup of $G$ , the inclusion map $i:H\to G$ defined by $i(x) = x$ for $x$ in $H$ is a homomorphism.

虽然不太有趣，但以下同态也需要提及。**平凡同态** $\phi :G\to G^{\prime}$ 将 $G$ 的每个元素映射到 $G^{\prime}$ 中的单位元。如果 $H$ 是 $G$ 的一个子群，包含映射 $i:H\to G$ 定义为 $i(x) = x$ 对于 $x$ 在 $H$ 中，是一个同态。

Proposition 2.5.3 Let $\phi :G\to G^{\prime}$ be a group homomorphism.
(a) If $a_{1},\ldots ,a_{k}$ are elements of $G$ , then $\phi (a_{1}\cdots a_{k}) = \phi (a_{1})\cdots \phi (a_{k})$
(b) $\phi$ maps the identity to the identity: $\phi (1_{G}) = 1_{G^{\prime}}$
(c) $\phi$ maps inverses to inverses: $\phi (a^{-1}) = \phi (a)^{-1}$

命题 2.5.3 设 $\phi :G\to G^{\prime}$ 是一个群同态。
(a) 如果 $a_{1},\ldots ,a_{k}$ 是 $G$ 中的元素，那么 $\phi (a_{1}\cdots a_{k}) = \phi (a_{1})\cdots \phi (a_{k})$。
(b) $\phi$ 将单位元映射到单位元：$\phi (1_{G}) = 1_{G^{\prime}}$。
(c) $\phi$ 将逆元映射到逆元：$\phi (a^{-1}) = \phi (a)^{-1}$。

Proof. The first assertion follows by induction from the definition. Next, since $1\cdot 1 = 1$ and since $\phi$ is a homomorphism, $\phi (1)\phi (1) = \phi (1\cdot 1) = \phi (1)$ . We cancel $\phi (1)$ from both sides (2.2.3) to obtain $\phi (1) = 1$ . Finally, $\phi (a^{- 1})\phi (a) = \phi (a^{- 1}a) = \phi (1) = 1$ . Hence $\phi (a^{- 1})$ is the inverse of $\phi (a)$ . $\square$

证明：第一个断言通过归纳法直接从定义得出。其次，由于 $1\cdot 1 = 1$ 且 $\phi$ 是一个同态，$\phi (1)\phi (1) = \phi (1\cdot 1) = \phi (1)$。我们从两边消去 $\phi (1)$ (2.2.3) 得到 $\phi (1) = 1$。最后，$\phi (a^{- 1})\phi (a) = \phi (a^{- 1}a) = \phi (1) = 1$。因此 $\phi (a^{- 1})$ 是 $\phi (a)$ 的逆元。$\square$

A group homomorphism determines two important subgroups: its image and its kernel.

一个群同态确定两个重要的子群：它的像和它的核。

The image of a homomorphism $\phi :G\to G^{\prime}$ , often denoted by $\operatorname{im}\phi$ , is simply the image of $\phi$ as a map of sets:
$$\operatorname{im}\phi = \left\{x\in G^{\prime}\mid x = \phi (a)\mathrm{~for~some~}a\mathrm{~in~}G\right\} , \quad (2.5.4)$$

同态 $\phi :G\to G^{\prime}$ 的**像**，通常记为 $\operatorname{im}\phi$，就是 $\phi$ 作为集合映射的像：
$$\operatorname{im}\phi = \left\{x\in G^{\prime}\mid x = \phi (a)\text{ 对于某个 }a\text{ 在 }G\text{ 中}\right\} , \qquad (2.5.4)$$

Another notation for the image would be $\phi (G)$ .

像的另一种记号是 $\phi (G)$。

===== Page 49 =====

The image of the map $\mathbb{Z}^{+} \to G$ that sends $n \to a^{n}$ is the cyclic subgroup $\langle a \rangle$ generated by $a$ .

映射 $\mathbb{Z}^{+} \to G$ 将 $n$ 送到 $a^{n}$ 的像是 $a$ 生成的循环子群 $\langle a \rangle$。

The image of a homomorphism is a subgroup of the range. We will verify closure and omit the other verifications. Let $x$ and $y$ be elements of the image. This means that there are elements $a$ and $b$ in $G$ such that $x = \phi (a)$ and $y = \phi (b)$ . Since $\phi$ is a homomorphism, $xy = \phi (a)\phi (b) = \phi (ab)$ . So $xy$ is equal to $\phi$ (something). It is in the image too.

同态的像是一个子群。我们将验证封闭性，并省略其他验证。设 $x$ 和 $y$ 是像中的元素。这意味着存在 $G$ 中的元素 $a$ 和 $b$ 使得 $x = \phi (a)$ 和 $y = \phi (b)$。由于 $\phi$ 是一个同态，$xy = \phi (a)\phi (b) = \phi (ab)$。所以 $xy$ 等于 $\phi$（某个东西）。它也在像中。

The kernel of a homomorphism is more subtle and also more important. The kernel of $\phi$ often denoted by $\ker \phi$ , is the set of elements of $G$ that are mapped to the identity in $G^{\prime}$ :
$$\ker \phi = \{a\in G\mid \phi (a) = 1\} . \quad (2.5.5)$$

同态的**核**更微妙，也更重要。$\phi$ 的核，通常记为 $\ker \phi$，是 $G$ 中被映射到 $G^{\prime}$ 中单位元的元素集合：
$$\ker \phi = \{a\in G\mid \phi (a) = 1\} . \qquad (2.5.5)$$

The kernel is a subgroup of $G$ because, if $a$ and $b$ are in the kernel, then $\phi (ab) = \phi (a)\phi (b) = 1 \cdot 1 = 1$ , so $ab$ is in the kernel, and so on.

核是 $G$ 的一个子群，因为如果 $a$ 和 $b$ 在核中，那么 $\phi (ab) = \phi (a)\phi (b) = 1 \cdot 1 = 1$，所以 $ab$ 在核中，等等。

The kernel of the determinant homomorphism $G L_{n}(\mathbb{R}) \to \mathbb{R}^{\times}$ is the special linear group $S L_{n}(\mathbb{R})$ (2.2.11). The kernel of the sign homomorphism $S_{n} \to \{\pm 1\}$ is called the alternating group. It consists of the even permutations, and is denoted by $A_{n}$ :

行列式同态 $G L_{n}(\mathbb{R}) \to \mathbb{R}^{\times}$ 的核是特殊线性群 $S L_{n}(\mathbb{R})$ (2.2.11)。符号同态 $S_{n} \to \{\pm 1\}$ 的核称为**交错群**。它由偶置换组成，记为 $A_{n}$：

(2.5.6) The alternating group $A_{n}$ is the group of even permutations.

(2.5.6) **交错群** $A_{n}$ 是偶置换的群。

The kernel is important because it controls the entire homomorphism. It tells us not only which elements of $G$ are mapped to the identity in $G^{\prime}$ , but also which pairs of elements have the same image in $G^{\prime}$ .

核之所以重要，是因为它控制着整个同态。它不仅告诉我们 $G$ 中哪些元素被映射到 $G^{\prime}$ 中的单位元，还告诉我们哪些元素对在 $G^{\prime}$ 中有相同的像。

If $H$ is a subgroup of a group $G$ and $a$ is an element of $G$ , the notation $aH$ will stand for the set of all products $ah$ with $h$ in $H$ :
$$a H = \{g\in G|g = a h\mathrm{~for~some~}h\mathrm{~in~}H\} . \quad (2.5.7)$$

如果 $H$ 是群 $G$ 的一个子群，$a$ 是 $G$ 中的一个元素，记号 $aH$ 将表示所有乘积 $ah$ 的集合，其中 $h$ 在 $H$ 中：
$$a H = \{g\in G\mid g = a h\text{ 对于某个 }h\text{ 在 }H\text{ 中}\} . \qquad (2.5.7)$$

This set is called a left coset of $H$ in $G$ , the word "left" referring to the fact that the element $a$ appears on the left.

这个集合称为 $H$ 在 $G$ 中的**左陪集**，这里的“左”指的是元素 $a$ 出现在左边。

Proposition 2.5.8 Let $\phi :G \to G^{\prime}$ be a homomorphism of groups, and let $a$ and $b$ be elements of $G$ . Let $K$ be the kernel of $\phi$ . The following conditions are equivalent:
$\phi (a) = \phi (b)$
$a^{- 1}b$ is in $K$
$b$ is in the coset $aK$
the cosets $bK$ and $aK$ are equal.

命题 2.5.8 设 $\phi :G \to G^{\prime}$ 是一个群同态，并设 $a$ 和 $b$ 是 $G$ 中的元素。设 $K$ 是 $\phi$ 的核。以下条件等价：
$\phi (a) = \phi (b)$
$a^{- 1}b$ 在 $K$ 中
$b$ 在陪集 $aK$ 中
陪集 $bK$ 和 $aK$ 相等。

Proof. Suppose that $\phi (a) = \phi (b)$ . Then $\phi (a^{- 1}b) = \phi (a^{- 1})\phi (b) = \phi (a)^{- 1}\phi (b) = 1$ . Therefore $a^{- 1}b$ is in the kernel $K$ . To prove the converse, we turn this argument around. If $a^{- 1}b$ is in $K$ , then $1 = \phi (a^{- 1}b) = \phi (a)^{- 1}\phi (b)$ , so $\phi (a) = \phi (b)$ . This shows that the first two bullets are equivalent. Their equivalence with the other bullets follows. $\square$

证明：假设 $\phi (a) = \phi (b)$。那么 $\phi (a^{- 1}b) = \phi (a^{- 1})\phi (b) = \phi (a)^{- 1}\phi (b) = 1$。因此 $a^{- 1}b$ 在核 $K$ 中。为了证明逆命题，我们把这个论证反过来。如果 $a^{- 1}b$ 在 $K$ 中，那么 $1 = \phi (a^{- 1}b) = \phi (a)^{- 1}\phi (b)$，所以 $\phi (a) = \phi (b)$。这表明前两个条件是等价的。它们与后两个条件的等价性也随之得出。$\square$

Corollary 2.5.9 A homomorphism $\phi : G \to G^{\prime}$ is injective if and only if its kernel $K$ is the trivial subgroup $\{1\}$ of $G$ .

推论 2.5.9 一个同态 $\phi : G \to G^{\prime}$ 是单射当且仅当它的核 $K$ 是 $G$ 的平凡子群 $\{1\}$。

===== Page 50 =====

Proof. If $K = \{1\}$ , Proposition 2.5.8 shows that $\phi (a) = \phi (b)$ only when $a^{- 1}b = 1$ , i.e., $a = b$ . Conversely, if $\phi$ is injective, then the identity is the only element of $G$ such that $\phi (a) = 1$ , so $K = \{1\}$ . $\square$

证明：如果 $K = \{1\}$，命题 2.5.8 表明只有当 $a^{- 1}b = 1$，即 $a = b$ 时，才有 $\phi (a) = \phi (b)$。反之，如果 $\phi$ 是单射，那么 $G$ 中唯一满足 $\phi (a) = 1$ 的元素是单位元，所以 $K = \{1\}$。$\square$

The kernel of a homomorphism has another important property that is explained in the next proposition. If $a$ and $g$ are elements of a group $G$ , the element $gag^{- 1}$ is called the conjugate of $a$ by $g$ .

同态的核还有另一个重要性质，在下一个命题中解释。如果 $a$ 和 $g$ 是群 $G$ 中的元素，则元素 $gag^{- 1}$ 称为 $a$ 被 $g$ 的**共轭**。

Definition 2.5.10 A subgroup $N$ of a group $G$ is a normal subgroup if for every $a$ in $N$ and every $g$ in $G$ , the conjugate $gag^{- 1}$ is in $N$ .

定义 2.5.10 群 $G$ 的一个子群 $N$ 是**正规子群**，如果对于 $N$ 中的每个 $a$ 和 $G$ 中的每个 $g$，共轭 $gag^{- 1}$ 都在 $N$ 中。

Proposition 2.5.11 The kernel of a homomorphism is a normal subgroup.

命题 2.5.11 同态的核是一个正规子群。

Proof. If $a$ is in the kernel of a homomorphism $\phi :G\to G^{\prime}$ and if $g$ is any element of $G$ then $\phi (gag^{- 1}) = \phi (g)\phi (a)\phi (g^{- 1}) = \phi (g)1\phi (g)^{- 1} = 1$ . Therefore $gag^{- 1}$ is in the kernel too. $\square$

证明：如果 $a$ 在同态 $\phi :G\to G^{\prime}$ 的核中，并且如果 $g$ 是 $G$ 的任何元素，那么 $\phi (gag^{- 1}) = \phi (g)\phi (a)\phi (g^{- 1}) = \phi (g)1\phi (g)^{- 1} = 1$。因此 $gag^{- 1}$ 也在核中。$\square$

Thus the special linear group $SL_{n}(\mathbb{R})$ is a normal subgroup of the general linear group $GL_{n}(\mathbb{R})$ , and the alternating group $A_{n}$ is a normal subgroup of the symmetric group $S_{n}$ . Every subgroup of an abelian group is normal, because if $G$ is abelian, then $gag^{- 1} = a$ for all $a$ and all $g$ in the group. But subgroups of nonabelian groups needn't be normal. For example, in the symmetric group $S_{3}$ , with its usual presentation (2.2.7), the cyclic subgroup $\langle y\rangle$ of order two is not normal, because $y$ is in $G$ , but $xyx^{- 1} = x^{2}y$ isn't in $\langle y\rangle$ .

因此，特殊线性群 $SL_{n}(\mathbb{R})$ 是一般线性群 $GL_{n}(\mathbb{R})$ 的正规子群，交错群 $A_{n}$ 是对称群 $S_{n}$ 的正规子群。阿贝尔群的每个子群都是正规的，因为如果 $G$ 是阿贝尔的，那么对于所有 $a$ 和群中的所有 $g$，有 $gag^{- 1} = a$。但非阿贝尔群的子群不一定是正规的。例如，在对称群 $S_{3}$ 中，用其通常表示 (2.2.7)，阶为 2 的循环子群 $\langle y\rangle$ 不是正规的，因为 $y$ 在 $G$ 中，但 $xyx^{- 1} = x^{2}y$ 不在 $\langle y\rangle$ 中。

The center of a group $G$ , which is often denoted by $Z$ , is the set of elements that commute with every element of $G$ :
$$Z = \{z\in G\mid zx = xz\mathrm{~for~all~}x\in G\} . \quad (2.5.12)$$

群 $G$ 的**中心**，通常记为 $Z$，是与 $G$ 中每个元素都交换的元素的集合：
$$Z = \{z\in G\mid zx = xz\text{ 对于所有 }x\in G\} . \qquad (2.5.12)$$

It is always a normal subgroup of $G$ . The center of the special linear group $SL_{2}(\mathbb{R})$ consists of the two matrices $I, - I$ . The center of the symmetric group $S_{n}$ is trivial if $n \geq 3$ .

它总是 $G$ 的一个正规子群。特殊线性群 $SL_{2}(\mathbb{R})$ 的中心由两个矩阵 $I, - I$ 组成。对称群 $S_{n}$ 的中心当 $n \geq 3$ 时是平凡的。

Example 2.5.13 A homomorphism $\phi :S_{4}\to S_{3}$ between symmetric groups.

例 2.5.13 对称群 $S_{4}$ 到 $S_{3}$ 的一个同态 $\phi$。

There are three ways to partition the set of four indices $\{1,2,3,4\}$ into pairs of subsets of order two, namely
$$\Pi_{1}:\{1,2\} \cup \{3,4\} ,\quad \Pi_{2}:\{1,3\} \cup \{2,4\} ,\quad \Pi_{3}:\{1,4\} \cup \{2,3\} . \quad (2.5.14)$$

有三种方式将四个指标 $\{1,2,3,4\}$ 的集合划分成两个二阶子集的配对，即
$$\Pi_{1}:\{1,2\} \cup \{3,4\} ,\quad \Pi_{2}:\{1,3\} \cup \{2,4\} ,\quad \Pi_{3}:\{1,4\} \cup \{2,3\} . \qquad (2.5.14)$$

An element of the symmetric group $S_{4}$ permutes the four indices, and by doing so it also permutes these three partitions. This defines the map $\phi$ from $S_{4}$ to the group of permutations of the set $\{\Pi_{1}, \Pi_{2}, \Pi_{3}\}$ , which is the symmetric group $S_{3}$ . For example, the 4- cycle $p = (1234)$ acts on subsets of order two as follows:
$$\{1,2\} \mapsto \{2,3\},\; \{1,3\} \mapsto \{2,4\},\; \{1,4\} \mapsto \{1,2\},\; \{2,3\} \mapsto \{3,4\},\; \{2,4\} \mapsto \{1,3\},\; \{3,4\} \mapsto \{1,4\}.$$

对称群 $S_{4}$ 中的一个元素置换这四个指标，并且这样做时也置换这三个划分。这定义了从 $S_{4}$ 到集合 $\{\Pi_{1}, \Pi_{2}, \Pi_{3}\}$ 的置换群的映射 $\phi$，后者就是对称群 $S_{3}$。例如，4-循环 $p = (1234)$ 对二阶子集的作用如下：
$$\{1,2\} \mapsto \{2,3\},\; \{1,3\} \mapsto \{2,4\},\; \{1,4\} \mapsto \{1,2\},\; \{2,3\} \mapsto \{3,4\},\; \{2,4\} \mapsto \{1,3\},\; \{3,4\} \mapsto \{1,4\}.$$

Looking at this action, one sees that $p$ acts on the set $\{\Pi_{1}, \Pi_{2}, \Pi_{3}\}$ of partitions as the transposition $(\Pi_{1} \Pi_{3})$ that fixes $\Pi_{2}$ and interchanges $\Pi_{1}$ and $\Pi_{3}$ .

观察这个作用，可以看到 $p$ 在划分的集合 $\{\Pi_{1}, \Pi_{2}, \Pi_{3}\}$ 上的作用是对换 $(\Pi_{1} \Pi_{3})$，它固定 $\Pi_{2}$ 并交换 $\Pi_{1}$ 和 $\Pi_{3}$。

===== Page 51 =====

If $p$ and $q$ are elements of $S_{4}$ , the product $pq$ is the composed permutation $p\circ q$ and the action of $pq$ on the set $\{\Pi_{1},\Pi_{2},\Pi_{3}\}$ is the composition of the actions of $q$ and $p$ . Therefore $\phi (pq) = \phi (p)\phi (q)$ , and $\phi$ is a homomorphism.

如果 $p$ 和 $q$ 是 $S_{4}$ 中的元素，乘积 $pq$ 是复合置换 $p\circ q$，而 $pq$ 在集合 $\{\Pi_{1},\Pi_{2},\Pi_{3}\}$ 上的作用是 $q$ 和 $p$ 的作用的复合。因此 $\phi (pq) = \phi (p)\phi (q)$，并且 $\phi$ 是一个同态。

The map is surjective, so its image is the whole group $S_{3}$ . Its kernel can be computed. It is the subgroup of $S_{4}$ consisting of the identity and the three products of disjoint transpositions:
$$K = \{1, (12)(34), (13)(24), (14)(23)\} . \quad (2.15.5)$$

这个映射是满射的，所以它的像是整个群 $S_{3}$。可以计算出它的核。它是 $S_{4}$ 中由单位元和三个不相交对换的乘积组成的子群：
$$K = \{1, (12)(34), (13)(24), (14)(23)\} . \qquad (2.15.5)$$

### 2.6 ISOMORPHISMS

### 2.6 同构

An isomorphism $\phi :G\to G^{\prime}$ from a group $G$ to a group $G^{\prime}$ is a bijective group homomorphism - a bijective map such that $\phi (ab) = \phi (a)\phi (b)$ for all $a$ and $b$ in $G$ .

从一个群 $G$ 到另一个群 $G^{\prime}$ 的一个**同构** $\phi :G\to G^{\prime}$ 是一个双射的群同态——一个双射映射，使得对于 $G$ 中所有的 $a$ 和 $b$，有 $\phi (ab) = \phi (a)\phi (b)$。

## Examples 2.6.1

- The exponential map $e^{x}$ is an isomorphism, when it is viewed as a map from the additive group $\mathbb{R}^{+}$ to its image, the multiplicative group of positive real numbers.
- If $a$ is an element of infinite order in a group $G$ , the map sending $n\mapsto a^{n}$ is an isomorphism from the additive group $\mathbb{Z}^{+}$ to the infinite cyclic subgroup $\langle a\rangle$ of $G$ .
- The set $\mathcal{P}$ of $n\times n$ permutation matrices is a subgroup of $GL_{n}$ , and the map $S_{n}\to \mathcal{P}$ that sends a permutation to its associated matrix (1.5.7) is an isomorphism.

## 例子 2.6.1

- 指数映射 $e^{x}$ 是一个同构，当它被视为从加法群 $\mathbb{R}^{+}$ 到其像（正实数的乘法群）的映射时。
- 如果 $a$ 是群 $G$ 中一个无限阶的元素，则映射 $n\mapsto a^{n}$ 是从加法群 $\mathbb{Z}^{+}$ 到 $G$ 的无限循环子群 $\langle a\rangle$ 的一个同构。
- $n\times n$ 置换矩阵的集合 $\mathcal{P}$ 是 $GL_{n}$ 的一个子群，将置换映射到其关联矩阵 (1.5.7) 的映射 $S_{n}\to \mathcal{P}$ 是一个同构。

Corollary 2.5.9 gives us a way to verify that a homomorphism $\phi :G\to G^{\prime}$ is an isomorphism. To do so, we check that $\ker \phi = \{1\}$ , which implies that $\phi$ is injective, and also that $\operatorname{im}\phi = G^{\prime}$ , that is, $\phi$ is surjective.

推论 2.5.9 为我们提供了一种验证同态 $\phi :G\to G^{\prime}$ 是否为同构的方法。为此，我们检查 $\ker \phi = \{1\}$，这蕴含 $\phi$ 是单射，同时检查 $\operatorname{im}\phi = G^{\prime}$，即 $\phi$ 是满射。

Lemma 2.6.2 If $\phi :G\to G^{\prime}$ is an isomorphism, the inverse map $\phi^{- 1}:G^{\prime}\to G$ is also an isomorphism.

引理 2.6.2 如果 $\phi :G\to G^{\prime}$ 是一个同构，则逆映射 $\phi^{- 1}:G^{\prime}\to G$ 也是一个同构。

Proof. The inverse of a bijective map is bijective. We must show that for all $x$ and $y$ in $G^{\prime}$ $\phi^{- 1}(x)\phi^{- 1}(y) = \phi^{- 1}(xy)$ . We set $a = \phi^{- 1}(x)$ $b = \phi^{- 1}(y)$ , and $c = \phi^{- 1}(xy)$ . What has to be shown is that $ab = c$ , and since $\phi$ is bijective, it suffices to show that $\phi (ab) = \phi (c)$ . Since $\phi$ is a homomorphism,
$$\phi (ab) = \phi (a)\phi (b) = xy = \phi (c). \quad \square$$

证明：双射映射的逆也是双射的。我们必须证明对于 $G^{\prime}$ 中所有的 $x$ 和 $y$，有 $\phi^{- 1}(x)\phi^{- 1}(y) = \phi^{- 1}(xy)$。设 $a = \phi^{- 1}(x)$，$b = \phi^{- 1}(y)$，$c = \phi^{- 1}(xy)$。需要证明的是 $ab = c$，由于 $\phi$ 是双射，只需证明 $\phi (ab) = \phi (c)$。由于 $\phi$ 是一个同态，
$$\phi (ab) = \phi (a)\phi (b) = xy = \phi (c). \quad \square$$

This lemma shows that when $\phi :G\to G^{\prime}$ is an isomorphism, we can make a computation in either group, then use $\phi$ or $\phi^{- 1}$ to carry it over to the other. So, for computation with the group law, the two groups have identical properties. To picture this conclusion intuitively, suppose that the elements of one of the groups are put into unlabeled boxes, and that we have an oracle that tells us, when presented with two boxes, which box contains their product. We will have no way to decide whether the elements in the boxes are from $G$ or from $G^{\prime}$ .

这个引理表明，当 $\phi :G\to G^{\prime}$ 是一个同构时，我们可以任选一个群进行计算，然后使用 $\phi$ 或 $\phi^{- 1}$ 将其传递到另一个群。因此，就群律的计算而言，这两个群具有相同的性质。为了直观地理解这个结论，假设一个群的元素被放入未标记的盒子中，并且我们有一个神谕，当我们呈现两个盒子时，它会告诉我们哪个盒子包含它们的乘积。我们将无法判断盒子中的元素是来自 $G$ 还是来自 $G^{\prime}$。

Two groups $G$ and $G^{\prime}$ are said to be isomorphic if there exists an isomorphism $\phi$ from $G$ to $G^{\prime}$ . We sometimes indicate that two groups are isomorphic by the symbol $\approx$
$$G\approx G^{\prime}\mathrm{~means~that~}G\mathrm{~is~isomorphic~to~}G^{\prime}.$$

两个群 $G$ 和 $G^{\prime}$ 被称为**同构**，如果存在一个从 $G$ 到 $G^{\prime}$ 的同构 $\phi$。我们有时用符号 $\approx$ 表示两个群同构
$$G\approx G^{\prime}\text{ 意味着 }G\text{ 同构于 }G^{\prime}.$$

===== Page 52 =====

Since isomorphic groups have identical properties, it is often convenient to identify them with each other when speaking informally. For instance, we often blur the distinction between the symmetric group $S_{n}$ and the isomorphic group $\mathcal{P}$ of permutation matrices.

由于同构的群具有相同的性质，在非正式讨论中通常可以将它们等同起来。例如，我们经常模糊对称群 $S_{n}$ 与置换矩阵的同构群 $\mathcal{P}$ 之间的区别。

The groups isomorphic to a given group $G$ form what is called the isomorphism class of $G$ .

同构于给定群 $G$ 的群组成所谓 $G$ 的**同构类**。

Any two groups in an isomorphism class are isomorphic. When one speaks of classifying groups, what is meant is to describe these isomorphism classes. This is too hard to do for all groups, but we will see that every group of prime order $p$ is cyclic. So all groups of order $p$ are isomorphic. There are two isomorphism classes of groups of order 4 (2.11.5) and five isomorphism classes of groups of order 12 (7.8.1).

同构类中的任意两个群都是同构的。当谈到对群进行分类时，意思就是描述这些同构类。对所有群做这件事太难了，但我们将看到每个素数阶群 $p$ 都是循环的。所以所有 $p$ 阶群都是同构的。有 4 阶群的两个同构类 (2.11.5) 和 12 阶群的五个同构类 (7.8.1)。

An interesting and sometimes confusing point about isomorphisms is that there exist isomorphisms $\phi :G\to G$ from a group $G$ to itself. Such an isomorphism is called an automorphism. The identity map is an automorphism, of course, but there are nearly always others. The most important type of automorphism is conjugation: Let $g$ be a fixed element of a group $G$ . Conjugation by $g$ is the map $\phi$ from $G$ to itself defined by
$$\phi (x) = gxg^{-1}. \quad (2.6.4)$$

关于同构有一个有趣且有时令人困惑的点：存在从群 $G$ 到自身的同构 $\phi :G\to G$。这样的同构称为**自同构**。当然恒等映射是一个自同构，但几乎总是存在其他自同构。最重要的自同构类型是**共轭**：设 $g$ 是群 $G$ 中一个固定元素。由 $g$ 的共轭是从 $G$ 到自身的映射 $\phi$，定义为
$$\phi (x) = gxg^{-1}. \qquad (2.6.4)$$

This is an automorphism because, first of all, it is a homomorphism:
$$\phi (xy) = gxyg^{-1} = gxg^{-1}gyg^{-1} = \phi (x)\phi (y),$$
and second, it is bijective because it has an inverse function - conjugation by $g^{- 1}$ .

这是一个自同构，因为首先，它是一个同态：
$$\phi (xy) = gxyg^{-1} = gxg^{-1}gyg^{-1} = \phi (x)\phi (y),$$
其次，它是双射的，因为它有一个逆函数——由 $g^{- 1}$ 的共轭。

If the group is abelian, conjugation by any element $g$ is the identity map: $gxg^{- 1} = x$ . But any noncommutative group has nontrivial conjugations, and so it has automorphisms different from the identity. For instance, in the symmetric group $S_{3}$ , presented as usual, conjugation by $y$ interchanges $x$ and $x^{2}$ .

如果群是阿贝尔的，任何元素 $g$ 的共轭就是恒等映射：$gxg^{- 1} = x$。但任何非交换群都有非平凡的共轭，因此它有不同于恒等映射的自同构。例如，在对称群 $S_{3}$ 中，如通常表示的那样，由 $y$ 的共轭交换 $x$ 和 $x^{2}$。

As was said before, the element $gxg^{- 1}$ is the conjugate of $x$ by $g$ , and two elements $x$ and $x^{\prime}$ of a group $G$ are conjugate if $x^{\prime} = gxg^{- 1}$ for some $g$ in $G$ . The conjugate $gxg^{- 1}$ behaves in much the same way as the element $x$ itself; for example, it has the same order in the group. This follows from the fact that it is the image of $x$ by an automorphism. (See the discussion following Lemma 2.6.2. )

如前所述，元素 $gxg^{- 1}$ 是 $x$ 被 $g$ 的共轭，并且群 $G$ 的两个元素 $x$ 和 $x^{\prime}$ 是**共轭的**，如果对于某个 $g$ 在 $G$ 中，$x^{\prime} = gxg^{- 1}$。共轭 $gxg^{- 1}$ 的行为与元素 $x$ 本身非常相似；例如，它在群中具有相同的阶。这是因为它是由自同构得到的像。（参见引理 2.6.2 后的讨论。）

Note: One may sometimes wish to determine whether or not two elements $x$ and $y$ of a group $G$ are conjugate, i.e., whether or not there is an element $g$ in $G$ such that $y = gxg^{- 1}$ . It is almost always simpler to rewrite the equation to be solved for $g$ as $yg = gx$ .

注：有时人们可能希望确定群 $G$ 的两个元素 $x$ 和 $y$ 是否共轭，即是否存在 $G$ 中的一个元素 $g$ 使得 $y = gxg^{- 1}$。几乎总是将待解的关于 $g$ 的方程重写为 $yg = gx$ 会更简单。

The next lemma follows by moving things from one side of an equation to the other.

下一个引理通过将项从方程的一边移到另一边得到。

Lemma 2.6.5 Two elements $a$ and $b$ of a group commute, $ab = ba$ , if and only if $aba^{- 1} = b$ , and this is true if and only if $aba^{- 1}b^{- 1} = 1$ .

引理 2.6.5 群中的两个元素 $a$ 和 $b$ 交换，$ab = ba$，当且仅当 $aba^{- 1} = b$，并且这成立当且仅当 $aba^{- 1}b^{- 1} = 1$。

### 2.7 EQUIVALENCE RELATIONS AND PARTITIONS

### 2.7 等价关系和划分

A fundamental mathematical construction starts with a set $S$ and forms a new set by equating certain elements of $S$ . For instance, we may divide the set of integers into two classes, the

一个基本的数学构造从一个集合 $S$ 开始，通过将 $S$ 的某些元素等同起来形成一个新的集合。例如，我们可以将整数集划分为两类，

===== Page 53 =====

even integers and the odd integers. The new set we obtain consists of two elements that could be called Even and Odd. Or, it is common to view congruent triangles in the plane as equivalent geometric objects. This very general procedure arises in several ways that we discuss here.

偶整数和奇整数。我们得到的新集合由两个元素组成，可以称为偶和奇。或者，通常将平面中的全等三角形视为等价的几何对象。这个非常普遍的过程在我们这里讨论的几种方式中出现。

A partition $\Pi$ of a set $S$ is a subdivision of $S$ into nonoverlapping, nonempty subsets:
$$S = \mathrm{union~of~disjoint~nonempty~subsets.}$$

一个集合 $S$ 的**划分** $\Pi$ 是将 $S$ 细分为不重叠的非空子集：
$$S = \text{不相交非空子集的并集}.$$

The two sets Even and Odd partition the set of integers. With the usual notation, the sets
$$\{1\} ,\{y,x y,x^{2}y\} ,\{x,x^{2}\} \quad (2.7.2)$$
form a partition of the symmetric group $S_{3}$

偶数和奇数这两个集合划分了整数集。用通常的记号，集合
$$\{1\} ,\{y,x y,x^{2}y\} ,\{x,x^{2}\} \qquad (2.7.2)$$
构成了对称群 $S_{3}$ 的一个划分。

An equivalence relation on a set $S$ is a relation that holds between certain pairs of elements of $S$ . We may write it as $a\sim b$ and speak of it as equivalence of $a$ and $b$ . An equivalence relation is required to be:

一个集合 $S$ 上的**等价关系**是一种在 $S$ 的某些元素对之间成立的关系。我们可以将其写为 $a\sim b$ 并将其称为 $a$ 和 $b$ 的等价。一个等价关系需要满足：

$$\{2.7.3\} \quad (2.7.3)$$
transitive: If $a\sim b$ and $b\sim c$ ,then $a\sim c$
symmetric:If $a\sim b$ ,then $b\sim a$
reflexive:For all $a$ $a\sim a$

**传递性**：如果 $a\sim b$ 且 $b\sim c$，那么 $a\sim c$。
**对称性**：如果 $a\sim b$，那么 $b\sim a$。
**自反性**：对于所有 $a$，$a\sim a$。

Congruence of triangles is an example of an equivalence relation on the set of triangles in the plane. If $A,B$ and $C$ are triangles, and if $A$ is congruent to $B$ and $B$ is congruent to $C$ ,then $A$ is congruent to $C$ ,etc.

三角形的全等是平面中三角形集合上的一个等价关系例子。如果 $A,B$ 和 $C$ 是三角形，并且 $A$ 全等于 $B$，$B$ 全等于 $C$，那么 $A$ 全等于 $C$，等等。

Conjugacy is an equivalence relation on a group. Two group elements are conjugate, $a\sim b$ ,if $b = g a g^{- 1}$ for some group element $g$ .We check transitivity: Suppose that $a\sim b$ and $b\sim c$ . This means that $b = g_{1}a g_{1}^{- 1}$ and $c = g_{2}b g_{2}^{- 1}$ for some group elements $g_{1}$ and $g_{2}$ Then $c = g_{2}(g_{1}a g_{1}^{- 1})g_{2}^{- 1} = (g_{2}g_{1})a(g_{2}g_{1})^{- 1}$ , so $a\sim c$

共轭是群上的一个等价关系。两个群元素共轭，$a\sim b$，如果对于某个群元素 $g$，$b = g a g^{- 1}$。我们检查传递性：假设 $a\sim b$ 且 $b\sim c$。这意味着对于某些群元素 $g_{1}$ 和 $g_{2}$，$b = g_{1}a g_{1}^{- 1}$ 且 $c = g_{2}b g_{2}^{- 1}$。那么 $c = g_{2}(g_{1}a g_{1}^{- 1})g_{2}^{- 1} = (g_{2}g_{1})a(g_{2}g_{1})^{- 1}$，所以 $a\sim c$。

The concepts of a partition of $S$ and an equivalence relation on $S$ are logically equivalent, though in practice one may be presented with just one of the two.

$S$ 的划分和 $S$ 上的等价关系这两个概念在逻辑上是等价的，尽管在实践中可能只给出其中一个。

Proposition 2.7.4 An equivalence relation on a set $S$ determines a partition of $S$ ,and conversely.

命题 2.7.4 一个集合 $S$ 上的等价关系决定了 $S$ 的一个划分，反之亦然。

Proof. Given a partition of $S$ , the corresponding equivalence relation is defined by the rule that $a\sim b$ if $a$ and $b$ lie in the same subset of the partition. The axioms for an equivalence relation are obviously satisfied. Conversely, given an equivalence relation, one defines a partition this way: The subset that contains $a$ is the set of all elements $b$ such that $a\sim b$ . This subset is called the equivalence class of $a$ . We'll denote it by $C_{a}$ here:
$$C_{a} = \{b\in S\mid a\sim b\} . \quad (2.7.5)$$

证明：给定 $S$ 的一个划分，相应的等价关系由规则 $a\sim b$ 定义，如果 $a$ 和 $b$ 位于该划分的同一个子集中。等价关系的公理显然满足。反之，给定一个等价关系，按以下方式定义一个划分：包含 $a$ 的子集是满足 $a\sim b$ 的所有元素 $b$ 的集合。这个子集称为 $a$ 的**等价类**。我们在这里将其记为 $C_{a}$：
$$C_{a} = \{b\in S\mid a\sim b\} . \qquad (2.7.5)$$

The next lemma completes the proof of the proposition.

下一个引理完成了命题的证明。

===== Page 54 =====

Lemma 2.7.6 Given an equivalence relation on a set $S$ , the subsets of $S$ that are equivalence classes partition $S$ .

引理 2.7.6 给定集合 $S$ 上的一个等价关系，作为等价类的 $S$ 的子集构成了 $S$ 的一个划分。

Proof. This is an important point, so we will check it carefully. We must remember that the notation $C_{a}$ stands for a subset defined in a certain way. The partition consists of the subsets, and several notations may describe the same subset.

证明：这是一个重要点，所以我们将仔细检查。我们必须记住记号 $C_{a}$ 表示以某种方式定义的子集。划分由这些子集组成，并且几个记号可能描述同一个子集。

The reflexive axiom tells us that $a$ is in its equivalence class. Therefore the class $C_{a}$ is nonempty, and since $a$ can be any element, the union of the equivalence classes is the whole set $S$ . The remaining property of a partition that must be verified is that equivalence classes are disjoint. To show this, we show:
$$\mathrm{If} C_{a} \mathrm{and} C_{b} \mathrm{have an element in common, then} C_{a} = C_{b}. \quad (2.7.7)$$

自反公理告诉我们 $a$ 在其等价类中。因此类 $C_{a}$ 非空，并且由于 $a$ 可以是任意元素，所有等价类的并集是整个集合 $S$。必须验证的划分的剩余性质是等价类是不相交的。为此，我们证明：
$$\text{如果 }C_{a} \text{ 和 } C_{b} \text{ 有一个公共元素，那么 } C_{a} = C_{b}. \qquad (2.7.7)$$

Since we can interchange the roles of $a$ and $b$ , it will suffice to show that if $C_{a}$ and $C_{b}$ have an element, say $d$ , in common, then $C_{b} \subset C_{a}$ , i.e., any element $x$ of $C_{b}$ is also in $C_{a}$ . If $x$ is in $C_{b}$ , then $b \sim x$ . Since $d$ is in both sets, $a \sim d$ and $b \sim d$ , and the symmetry property tells us that $d \sim b$ . So we have $a \sim d$ , $d \sim b$ , and $b \sim x$ . Two applications of transitivity show that $a \sim x$ , and therefore that $x$ is in $C_{a}$ . $\square$

由于我们可以互换 $a$ 和 $b$ 的角色，只需证明如果 $C_{a}$ 和 $C_{b}$ 有一个公共元素，记为 $d$，那么 $C_{b} \subset C_{a}$，即 $C_{b}$ 中的任何元素 $x$ 也在 $C_{a}$ 中。如果 $x$ 在 $C_{b}$ 中，那么 $b \sim x$。由于 $d$ 在两个集合中，$a \sim d$ 且 $b \sim d$，对称性质告诉我们 $d \sim b$。所以我们有 $a \sim d$，$d \sim b$ 和 $b \sim x$。两次应用传递性表明 $a \sim x$，因此 $x$ 在 $C_{a}$ 中。$\square$

For example, the relation on a group defined by $a \sim b$ if $a$ and $b$ are elements of the same order is an equivalence relation. The corresponding partition is exhibited in (2.7.2) for the symmetric group $S_{3}$ .

例如，群上由 $a \sim b$ 定义的关系，如果 $a$ 和 $b$ 具有相同的阶，则是一个等价关系。对应的划分在 (2.7.2) 中为对称群 $S_{3}$ 展示出来。

If a partition of a set $S$ is given, we may construct a new set $\overline{S}$ whose elements are the subsets. We imagine putting the subsets into separate piles, and we regard the piles as the elements of our new set $\overline{S}$ . It seems advisable to have a notation to distinguish a subset from the element of the set $\overline{S}$ (the pile) that it represents. If $U$ is a subset, we will denote by $[U]$ the corresponding element of $\overline{S}$ . Thus if $S$ is the set of integers and if Even and Odd denote the subsets of even and odd integers, respectively, then $\overline{S}$ contains the two elements [Even] and [Odd].

如果给定集合 $S$ 的一个划分，我们可以构造一个新的集合 $\overline{S}$，其元素是这些子集。我们想象将这些子集放入不同的堆中，并将这些堆视为新集合 $\overline{S}$ 的元素。似乎有必要有一个记号来区分一个子集和它在 $\overline{S}$ 中代表的元素（堆）。如果 $U$ 是一个子集，我们将用 $[U]$ 表示 $\overline{S}$ 中对应的元素。因此，如果 $S$ 是整数集，并且 Even 和 Odd 分别表示偶数和奇数整数的子集，那么 $\overline{S}$ 包含两个元素 [Even] 和 [Odd]。

We will use this notation more generally. When we want to regard a subset $U$ of $S$ as an element of a set of subsets of $S$ , we denote it by $[U]$ .

我们将更一般地使用这个记号。当我们要将 $S$ 的一个子集 $U$ 视为 $S$ 的子集集合中的一个元素时，我们将其记为 $[U]$。

When an equivalence relation on $S$ is given, the equivalence classes form a partition, and we obtain a new set $\overline{S}$ whose elements are the equivalence classes $[C_{a}]$ . We can think of the elements of this new set in another way, as the set obtained by changing what we mean by equality among elements. If $a$ and $b$ are in $S$ , we interpret $a \sim b$ to mean that $a$ and $b$ become equal in $\overline{S}$ , because $C_{a} = C_{b}$ . With this way of looking at it, the difference between the two sets $S$ and $\overline{S}$ is that in $\overline{S}$ more elements have been declared "equal," i.e., equivalent. It seems to me that we often treat congruent triangles this way in school.

当给定 $S$ 上的一个等价关系时，等价类形成一个划分，我们得到一个新的集合 $\overline{S}$，其元素是等价类 $[C_{a}]$。我们可以用另一种方式思考这个新集合的元素，即作为通过改变我们对元素之间相等的理解而得到的集合。如果 $a$ 和 $b$ 在 $S$ 中，我们将 $a \sim b$ 解释为 $a$ 和 $b$ 在 $\overline{S}$ 中变成相等，因为 $C_{a} = C_{b}$。按照这种看法，两个集合 $S$ 和 $\overline{S}$ 之间的区别在于，在 $\overline{S}$ 中，更多的元素被宣布为“相等”，即等价。在我看来，我们在学校经常这样处理全等三角形。

For any equivalence relation, there is a natural surjective map
$$\pi :S\to \overline{S} \quad (2.7.8)$$
that maps an element $a$ of $S$ to its equivalence class: $\pi (a) = [C_{a}]$ . When we want to regard $\overline{S}$ as the set obtained from $S$ by changing the notion of equality, it will be convenient to denote the element $[C_{a}]$ of $\overline{S}$ by the symbol $\overline{a}$ . Then the map $\pi$ becomes
$$\pi (a) = \overline{a}.$$

对于任何等价关系，存在一个自然的满射映射
$$\pi :S\to \overline{S} \qquad (2.7.8)$$
将 $S$ 中的一个元素 $a$ 映射到它的等价类：$\pi (a) = [C_{a}]$。当我们想把 $\overline{S}$ 视为通过改变相等概念从 $S$ 得到的集合时，用符号 $\overline{a}$ 表示 $\overline{S}$ 中的元素 $[C_{a}]$ 会很方便。那么映射 $\pi$ 变为
$$\pi (a) = \overline{a}.$$

===== Page 55 =====

We can work in $\overline{S}$ with the symbols used for elements of $S$ , but with bars over them to remind us of the new rule:
$$\mathrm{If~}a\mathrm{~and~}b\mathrm{~are~in~}S,\mathrm{~then~}\overline{a} = \overline{b}\mathrm{~means~}a\sim b. \quad (2.7.9)$$

我们可以在 $\overline{S}$ 中使用用于 $S$ 中元素的符号，但上面有横线提醒我们新规则：
$$\text{如果 }a\text{ 和 }b\text{ 在 }S\text{ 中，那么 }\overline{a} = \overline{b}\text{ 意味着 }a\sim b. \qquad (2.7.9)$$

A disadvantage of this bar notation is that many symbols represent the same element of $\overline{S}$ . Sometimes this disadvantage can be overcome by choosing a particular element, a representative element, in each equivalence class. For example, the even and the odd integers are often represented by $\overline{0}$ and $\overline{1}$ :
$$\{[Even],[Odd]\} = \{\overline{0},\overline{1}\} . \quad (2.7.10)$$

这种横线记法的一个缺点是许多符号代表 $\overline{S}$ 中的同一个元素。有时可以通过在每个等价类中选择一个特定的元素，即一个**代表元素**来克服这个缺点。例如，偶数和奇数整数通常用 $\overline{0}$ 和 $\overline{1}$ 表示：
$$\{[Even],[Odd]\} = \{\overline{0},\overline{1}\} . \qquad (2.7.10)$$

Though the pile picture may be easier to grasp at first, the second way of viewing $\overline{S}$ is often better because the bar notation is easier to manipulate algebraically.

尽管堆的图景可能更容易理解，但看待 $\overline{S}$ 的第二种方式通常更好，因为横线记法更容易进行代数操作。

## The Equivalence Relation Defined by a Map

## 由映射定义的等价关系

Any map of sets $f\colon S\to T$ gives us an equivalence relation on its domain $S$ . It is defined by the rule $a\sim b$ if $f(a) = f(b)$ .

任何集合映射 $f\colon S\to T$ 都在其定义域 $S$ 上给出一个等价关系。它由规则 $a\sim b$ 定义，如果 $f(a) = f(b)$。

The inverse image of an element $t$ of $T$ is the subset of $S$ consisting of all elements $s$ such that $f(s) = t$ . It is denoted symbolically as
$$f^{-1}(t) = \{s\in S\mid f(s) = t\} . \quad (2.7.11)$$

$T$ 中一个元素 $t$ 的**原像**是 $S$ 中所有满足 $f(s) = t$ 的元素 $s$ 组成的子集。它用符号表示为
$$f^{-1}(t) = \{s\in S\mid f(s) = t\} . \qquad (2.7.11)$$

This is symbolic notation. Please remember that unless $f$ is bijective, $f^{- 1}$ will not be a map. The inverse images are also called the fibres of the map $f$ , and the fibres that are not empty are the equivalence classes for the relation defined above.

这是符号记法。请记住，除非 $f$ 是双射，否则 $f^{- 1}$ 不会是一个映射。原像也称为映射 $f$ 的**纤维**，非空纤维就是上述关系定义的等价类。

Here the set $\overline{S}$ of equivalence classes has another incarnation, as the image of the map. The elements of the image correspond bijectively to the nonempty fibres, which are the equivalence classes.

这里，等价类的集合 $\overline{S}$ 有另一种表现形式，即映射的像。像中的元素与非空纤维（即等价类）一一对应。

![image](2.7.12) Some Fibres of the Absolute Value Map $\mathbb{C}^{\times}\to \mathbb{R}^{\times}$

![image](2.7.12) 绝对值映射 $\mathbb{C}^{\times}\to \mathbb{R}^{\times}$ 的一些纤维

Example 2.7.13 If $G$ is a finite group, we can define a map $f\colon G\to \mathbb{N}$ to the set $\{1,2,3,\ldots \}$ of natural numbers, letting $f(a)$ be the order of the element $a$ of $G$ . The fibres of this map are the sets of elements with the same order (see (2.7.2), for example). $\square$

例 2.7.13 如果 $G$ 是一个有限群，我们可以定义一个映射 $f\colon G\to \mathbb{N}$ 到自然数集合 $\{1,2,3,\ldots \}$，令 $f(a)$ 为 $G$ 中元素 $a$ 的阶。这个映射的纤维是具有相同阶的元素的集合（例如见 (2.7.2)）。$\square$

===== Page 56 =====

We go back to a group homomorphism $\phi :G\to G^{\prime}$ . The equivalence relation on $G$ defined by $\phi$ is usually denoted by $\equiv$ , rather than by $\sim$ , and is referred to as congruence:
$$a\equiv b\mathrm{~if~}\phi (a) = \phi (b). \quad (2.7.14)$$

我们回到群同态 $\phi :G\to G^{\prime}$。由 $\phi$ 定义的 $G$ 上的等价关系通常用 $\equiv$ 而不是 $\sim$ 表示，并称为**同余**：
$$a\equiv b\text{ 如果 }\phi (a) = \phi (b). \qquad (2.7.14)$$

We have seen that elements $a$ and $b$ of $G$ are congruent, i.e., $\phi (a) = \phi (b)$ , if and only if $b$ is in the coset $aK$ of the kernel $K$ (2.5.8).

我们已经看到，$G$ 中的元素 $a$ 和 $b$ 是同余的，即 $\phi (a) = \phi (b)$，当且仅当 $b$ 在核 $K$ 的陪集 $aK$ 中 (2.5.8)。

Proposition 2.7.15 Let $K$ be the kernel of a homomorphism $\phi :G\to G^{\prime}$ . The fibre of $\phi$ that contains an element $a$ of $G$ is the coset $aK$ of $K$ . These cosets partition the group $G$ , and they correspond to elements of the image of $\phi$ . $\square$

命题 2.7.15 设 $K$ 是同态 $\phi :G\to G^{\prime}$ 的核。包含 $G$ 中元素 $a$ 的 $\phi$ 的纤维是 $K$ 的陪集 $aK$。这些陪集划分了群 $G$，并且它们对应于 $\phi$ 的像中的元素。$\square$

![image](2.7.16) A Schematic Diagram of a Group Homomorphism.

![image](2.7.16) 一个群同态的示意图。

### 2.8 COSETS

### 2.8 陪集

As before, if $H$ is a subgroup of $G$ and if $a$ is an element of $G$ , the subset
$$aH = \{ah\mid h\mathrm{~in~}H\} . \quad (2.8.1)$$
is called a left coset. The subgroup $H$ is a particular left coset because $H = 1H$ . The cosets of $H$ in $G$ are equivalence classes for the congruence relation
$$a\equiv b\mathrm{~if~}b = ah\mathrm{~for~some~}h\mathrm{~in~}H. \quad (2.8.2)$$

如前所述，如果 $H$ 是 $G$ 的一个子群，并且如果 $a$ 是 $G$ 中的一个元素，那么子集
$$aH = \{ah\mid h\text{ 在 }H\text{ 中}\} . \qquad (2.8.1)$$
称为一个**左陪集**。子群 $H$ 是一个特定的左陪集，因为 $H = 1H$。$H$ 在 $G$ 中的陪集是同余关系
$$a\equiv b\text{ 如果 }b = ah\text{ 对于某个 }h\text{ 在 }H\text{ 中}. \qquad (2.8.2)$$
的等价类。

This is very simple, but let's verify that congruence is an equivalence relation.

这非常简单，但让我们验证同余是一个等价关系。

Transitivity: Suppose that $a\equiv b$ and $b\equiv c$ . This means that $b = ah$ and $c = bh^{\prime}$ for some elements $h$ and $h^{\prime}$ of $H$ . Therefore $c = a h h^{\prime}$ . Since $H$ is a subgroup, $h h^{\prime}$ is in $H$ , and thus $a\equiv c$ .

传递性：假设 $a\equiv b$ 且 $b\equiv c$。这意味着对于 $H$ 中的某些元素 $h$ 和 $h^{\prime}$，有 $b = ah$ 和 $c = bh^{\prime}$。因此 $c = a h h^{\prime}$。由于 $H$ 是一个子群，$h h^{\prime}$ 在 $H$ 中，因此 $a\equiv c$。

Symmetry: Suppose $a\equiv b$ , so that $b = ah$ . Then $a = bh^{- 1}$ and $h^{- 1}$ is in $H$ , so $b\equiv a$ .
Reflexivity: $a = a1$ and 1 is in $H$ , so $a\equiv a$ .

对称性：假设 $a\equiv b$，使得 $b = ah$。那么 $a = bh^{- 1}$ 并且 $h^{- 1}$ 在 $H$ 中，所以 $b\equiv a$。
自反性：$a = a1$ 且 1 在 $H$ 中，所以 $a\equiv a$。

Notice that we have made use of all the defining properties of a subgroup here: closure, inverses, and identity.

注意，我们在这里使用了子群的所有定义性质：封闭性、逆元和单位元。

===== Page 57 =====

2.8.3 The left cosets of a subgroup $H$ of a group $G$ partition the group.

2.8.3 子群 $H$ 在群 $G$ 中的左陪集划分了该群。

Proof. The left cosets are the equivalence classes for the congruence relation (2.8.2). $\square$

证明：左陪集是同余关系 (2.8.2) 的等价类。$\square$

Keep in mind that the notation $aH$ defines a certain subset of $G$ . As with any equivalence relation, several notations may define the same subset. For example, in the symmetric group $S_{3}$ , with the usual presentation (2.2.6), the element $y$ generates a cyclic subgroup $H = \langle y \rangle$ of order 2. There are three left cosets of $H$ in $G$ :
$$H = \{1,y\} = yH,\quad xH = \{x,xy\} = xyH,\quad x^{2}H = \{x^{2},x^{2}y\} = x^{2}yH. \quad (2.8.4)$$

请记住，记号 $aH$ 定义了 $G$ 的一个特定子集。与任何等价关系一样，几个记号可能定义同一个子集。例如，在对称群 $S_{3}$ 中，用通常的表示 (2.2.6)，元素 $y$ 生成一个阶为 2 的循环子群 $H = \langle y \rangle$。$H$ 在 $G$ 中有三个左陪集：
$$H = \{1,y\} = yH,\quad xH = \{x,xy\} = xyH,\quad x^{2}H = \{x^{2},x^{2}y\} = x^{2}yH. \qquad (2.8.4)$$

These sets do partition the group.

这些集合确实划分了群。

Recapitulating, let $H$ be a subgroup of a group $G$ and let $a$ and $b$ be elements of $G$ . The following are equivalent:
$$b = ah\mathrm{for~some~}h\mathrm{~in~}H,\mathrm{or,~}a^{-1}b\mathrm{~is~an~element~of~}H,$$
$$b\mathrm{~is~an~element~of~the~left~coset~}aH,$$
$$\mathrm{~the~left~cosets~}aH\mathrm{~and~}bH\mathrm{~are~equal.}$$

概括一下，设 $H$ 是群 $G$ 的一个子群，$a$ 和 $b$ 是 $G$ 中的元素。以下条件等价：
$$b = ah\text{ 对于某个 }h\text{ 在 }H\text{ 中},\quad \text{或,}\quad a^{-1}b\text{ 是 }H\text{ 中的一个元素},$$
$$b\text{ 是左陪集 }aH\text{ 的一个元素},$$
$$\text{左陪集 }aH\text{ 和 }bH\text{ 相等}.$$

The number of left cosets of a subgroup is called the index of $H$ in $G$ . The index is denoted by
$$[G:H]. \quad (2.8.6)$$

一个子群的左陪集个数称为该子群在 $G$ 中的**指数**。指数记为
$$[G:H]. \qquad (2.8.6)$$

Thus the index of the subgroup $\langle y \rangle$ of $S_{3}$ is 3. When $G$ is infinite, the index may be infinite too.

因此 $S_{3}$ 中子群 $\langle y \rangle$ 的指数是 3。当 $G$ 是无限群时，指数也可能是无限的。

Lemma 2.8.7 All left cosets $aH$ of a subgroup $H$ of a group $G$ have the same order.

引理 2.8.7 群 $G$ 中一个子群 $H$ 的所有左陪集 $aH$ 具有相同的阶。

Proof. Multiplication by $a$ defines a map $H \to aH$ that sends $h \mapsto ah$ . This map is bijective because its inverse is multiplication by $a^{- 1}$ . $\square$

证明：乘以 $a$ 定义了一个映射 $H \to aH$，该映射将 $h \mapsto ah$。这个映射是双射，因为它的逆是乘以 $a^{- 1}$。$\square$

Since the cosets all have the same order, and since they partition the group, we obtain the important Counting Formula
$$\begin{array}{c}{|G| = |H| |G:H|}\\ {(\text{order of }G) = (\text{order of }H)(\text{number of cosets})}, \end{array} \quad (2.8.8)$$

由于所有陪集都具有相同的阶，并且它们划分了群，我们得到了重要的**计数公式**
$$\begin{array}{c}{|G| = |H| \cdot |G:H|}\\ {(\text{群 }G\text{ 的阶}) = (\text{子群 }H\text{ 的阶})(\text{陪集个数})}, \end{array} \qquad (2.8.8)$$

where, as always, $|G|$ denotes the order of the group. The equality has the obvious meaning if some terms are infinite. For the subgroup $\langle y \rangle$ of $S_{3}$ , the formula reads $6 = 2 \cdot 3$ .

和往常一样，$|G|$ 表示群的阶。如果某些项是无限的，等式具有明显的含义。对于 $S_{3}$ 的子群 $\langle y \rangle$，公式为 $6 = 2 \cdot 3$。

It follows from the counting formula that the terms on the right side of (2.8.8) divide the left side. One of these facts is called Lagrange's Theorem:

从计数公式可以得出，(2.8.8) 右边的项整除左边。其中一个事实称为**拉格朗日定理**：

Theorem 2.8.9 Lagrange's Theorem. Let $H$ be a subgroup of a finite group $G$ . The order of $H$ divides the order of $G$ .

定理 2.8.9 拉格朗日定理。设 $H$ 是有限群 $G$ 的一个子群。$H$ 的阶整除 $G$ 的阶。

Corollary 2.8.10 The order of an element of a finite group divides the order of the group.

推论 2.8.10 有限群中一个元素的阶整除该群的阶。

===== Page 58 =====

Proof. The order of an element $a$ of a group $G$ is equal to the order of the cyclic subgroup $\langle a \rangle$ generated by $a$ (Proposition 2.4.2). $\square$

证明：群 $G$ 中一个元素 $a$ 的阶等于由 $a$ 生成的循环子群 $\langle a \rangle$ 的阶（命题 2.4.2）。$\square$

Corollary 2.8.11 Suppose that a group $G$ has prime order $p$ . Let $a$ be any element of $G$ other than the identity. Then $G$ is the cyclic group $\langle a \rangle$ generated by $a$ .

推论 2.8.11 假设一个群 $G$ 有素数阶 $p$。设 $a$ 是 $G$ 中除单位元外的任何元素。那么 $G$ 是由 $a$ 生成的循环群 $\langle a \rangle$。

Proof. The order of an element $a \neq 1$ is greater than 1 and it divides the order of $G$ , which is the prime integer $p$ . So the order of $a$ is equal to $p$ . This is also the order of the cyclic subgroup $\langle a \rangle$ generated by $a$ . Since $G$ has order $p, \langle a \rangle = G$ . $\square$

证明：一个元素 $a \neq 1$ 的阶大于 1，并且它整除 $G$ 的阶，而 $G$ 的阶是素数 $p$。所以 $a$ 的阶等于 $p$。这也是由 $a$ 生成的循环子群 $\langle a \rangle$ 的阶。由于 $G$ 的阶为 $p$，$\langle a \rangle = G$。$\square$

This corollary classifies groups of prime order $p$ . They form one isomorphism class, the class of the cyclic groups of order $p$ .

这个推论分类了素数阶 $p$ 的群。它们形成一个同构类，即 $p$ 阶循环群的类。

The counting formula can also be applied when a homomorphism $\phi : G \to G'$ is given. As we have seen (2.7.15), the left cosets of the kernel $\ker \phi$ are the nonempty fibres of the map $\phi$ . They are in bijective correspondence with the elements of the image.
$$[G:\ker \phi ] = |\operatorname{im}\phi |. \quad (2.8.12)$$

计数公式也可以应用于给定同态 $\phi : G \to G'$ 的情况。正如我们所看到的 (2.7.15)，核 $\ker \phi$ 的左陪集是映射 $\phi$ 的非空纤维。它们与像中的元素一一对应。
$$[G:\ker \phi ] = |\operatorname{im}\phi |. \qquad (2.8.12)$$

Corollary 2.8.13 Let $\phi : G \to G'$ be a homomorphism of finite groups. Then
$|G| = |\ker \phi | \cdot |\mathrm{im}\phi |$ ,
$|\ker \phi |$ divides $|G|$ and $|\mathrm{im}\phi |$ divides both $|G|$ and $|G'|$

推论 2.8.13 设 $\phi : G \to G'$ 是有限群的一个同态。那么
$|G| = |\ker \phi | \cdot |\mathrm{im}\phi |$，
$|\ker \phi |$ 整除 $|G|$，并且 $|\mathrm{im}\phi |$ 同时整除 $|G|$ 和 $|G'|$。

Proof. The first formula is obtained by combining (2.8.8) and (2.8.12), and it implies that $|\ker \phi |$ and $|\mathrm{im}\phi |$ divide $|G|$ . Since the image is a subgroup of $G'$ , Lagrange's theorem tells us that its order divides $|G'|$ too. $\square$

证明：第一个公式是通过结合 (2.8.8) 和 (2.8.12) 得到的，它蕴含 $|\ker \phi |$ 和 $|\mathrm{im}\phi |$ 整除 $|G|$。由于像 $G'$ 的一个子群，拉格朗日定理告诉我们它的阶也整除 $|G'|$。$\square$

For example, the sign homomorphism $\sigma : S_{n} \to \{\pm 1\}$ (2.5.2)(b) is surjective, so its image has order 2. Its kernel, the alternating group $A_{n}$ , has order $\frac{1}{2} n!$ . Half of the elements of $S_{n}$ are even permutations, and half are odd permutations.

例如，符号同态 $\sigma : S_{n} \to \{\pm 1\}$ (2.5.2)(b) 是满射的，所以它的像的阶为 2。它的核，交错群 $A_{n}$，的阶是 $\frac{1}{2} n!$。$S_{n}$ 中一半的元素是偶置换，一半是奇置换。

The counting formula 2.8.8 has an analogue when a chain of subgroups is given.

计数公式 2.8.8 在给出一串子群时有一个类比。

Proposition 2.8.14 Multiplicative Property of the Index. Let $G \supset H \supset K$ be subgroups of a group $G$ . Then $[G:K] = [G:H][H:K]$ .

命题 2.8.14 指数的乘法性质。设 $G \supset H \supset K$ 是群 $G$ 的子群。那么 $[G:K] = [G:H][H:K]$。

Proof. We will assume that the two indices on the right are finite, say $[G:H] = m$ and $[H:K] = n$ . The reasoning when one or the other is infinite is similar. We list the $m$ cosets of $H$ in $G$ , choosing representative elements for each coset, say as $g_{1}H,\ldots ,g_{m}H$ . Then $g_{1}H\cup \dots \cup g_{m}H$ is a partition of $G$ . Similarly, we choose representative elements for each coset of $K$ in $H$ , obtaining a partition $H = h_{1}K\cup \dots \cup h_{n}K$ . Since multiplication by $g_{i}$ is an invertible operation, $g_{i}H = g_{i}h_{1}K\cup \dots \cup g_{i}h_{n}K$ will be a partition of the coset $g_{i}H$ . Putting these partitions together, $G$ is partitioned into the $mn$ cosets $g_{i}h_{j}K$ . $\square$

证明：我们将假设右边的两个指数是有限的，比如 $[G:H] = m$ 和 $[H:K] = n$。当一个或另一个无限时推理类似。我们列出 $H$ 在 $G$ 中的 $m$ 个陪集，为每个陪集选择代表元素，比如 $g_{1}H,\ldots ,g_{m}H$。那么 $g_{1}H\cup \dots \cup g_{m}H$ 是 $G$ 的一个划分。类似地，我们为 $K$ 在 $H$ 中的每个陪集选择代表元素，得到划分 $H = h_{1}K\cup \dots \cup h_{n}K$。由于乘以 $g_{i}$ 是一个可逆操作，$g_{i}H = g_{i}h_{1}K\cup \dots \cup g_{i}h_{n}K$ 将是陪集 $g_{i}H$ 的一个划分。将这些划分放在一起，$G$ 被划分为 $mn$ 个陪集 $g_{i}h_{j}K$。$\square$

## Right Cosets

## 右陪集

Let us go back to the definition of cosets. We made the decision to work with left cosets $aH$ . One can also define right cosets of a subgroup $H$ and repeat the above discussion for them.

让我们回到陪集的定义。我们决定使用左陪集 $aH$ 工作。也可以定义一个子群 $H$ 的右陪集，并为它们重复上述讨论。

===== Page 59 =====

The right cosets of a subgroup $H$ of a group $G$ are the sets
$$H a = \{h a\mid h\in H\} . \quad (2.8.15)$$

群 $G$ 中一个子群 $H$ 的**右陪集**是集合
$$H a = \{h a\mid h\in H\} . \qquad (2.8.15)$$

They are equivalence classes for the relation (right congruence)
$$a = b \text{ if } b = ha, \text{ for some } h \text{ in } H.$$

它们是关系（右同余）
$$a \equiv b \text{ 如果 } b = ha, \text{ 对于某个 } h \text{ 在 } H \text{ 中}$$
的等价类。

Right cosets also partition the group $G$ , but they aren't always the same as left cosets. For instance, the right cosets of the subgroup $\langle y \rangle$ of $S_{3}$ are
$$H = \{1,y\} = H y,\quad H x = \{x,x^{2}y\} = H x^{2}y,\quad H x^{2} = \{x^{2},x y\} = H x y. \quad (2.8.16)$$

右陪集也划分群 $G$，但它们并不总是与左陪集相同。例如，$S_{3}$ 中子群 $\langle y \rangle$ 的右陪集是
$$H = \{1,y\} = H y,\quad H x = \{x,x^{2}y\} = H x^{2}y,\quad H x^{2} = \{x^{2},x y\} = H x y. \qquad (2.8.16)$$

This isn't the same as the partition (2.8.4) into left cosets. However, if a subgroup is normal, its right and left cosets are equal.

这与左陪集划分 (2.8.4) 不同。然而，如果一个子群是正规的，它的左右陪集是相等的。

Proposition 2.8.17 Let $H$ be a subgroup of a group $G$ . The following conditions are equivalent:
(i) $H$ is a normal subgroup: For all $h$ in $H$ and all $g$ in $G$ , $g h g^{-1}$ is in $H$ .
(ii) For all $g$ in $G$ , $g H g^{-1} = H$ .
(iii) For all $g$ in $G$ , the left coset $g H$ is equal to the right coset $H g$ .
(iv) Every left coset of $H$ in $G$ is a right coset.

命题 2.8.17 设 $H$ 是群 $G$ 的一个子群。以下条件等价：
(i) $H$ 是一个正规子群：对于 $H$ 中所有 $h$ 和 $G$ 中所有 $g$，$g h g^{-1}$ 在 $H$ 中。
(ii) 对于 $G$ 中所有 $g$，$g H g^{-1} = H$。
(iii) 对于 $G$ 中所有 $g$，左陪集 $g H$ 等于右陪集 $H g$。
(iv) $H$ 在 $G$ 中的每个左陪集都是右陪集。

Proof. The notation $g H g^{- 1}$ stands for the set of all elements $g h g^{- 1}$ , with $h$ in $H$ .

证明：记号 $g H g^{- 1}$ 表示所有元素 $g h g^{- 1}$ 的集合，其中 $h$ 在 $H$ 中。

Suppose that $H$ is normal. So (i) holds, and it implies that $g H g^{- 1} \subset H$ for all $g$ in $G$ . Substituting $g^{- 1}$ for $g$ shows that $g^{- 1} H g \subset H$ as well. We multiply this inclusion on the left by $g$ and on the right by $g^{- 1}$ to conclude that $H \subset g H g^{- 1}$ . Therefore $g H g^{- 1} = H$ . This shows that (i) implies (ii). It is clear that (ii) implies (i). Next, if $g H g^{- 1} = H$ , we multiply this equation on the right by $g$ to conclude that $g H = H g$ . This shows that (ii) implies (iii). One sees similarly that (iii) implies (ii). Since (iii) implies (iv) is obvious, it remains only to check that (iv) implies (iii).

假设 $H$ 是正规的。所以 (i) 成立，它蕴含对于 $G$ 中所有 $g$，$g H g^{- 1} \subset H$。将 $g^{- 1}$ 代入 $g$ 表明 $g^{- 1} H g \subset H$ 也成立。我们在左边乘以 $g$，在右边乘以 $g^{- 1}$，得出 $H \subset g H g^{- 1}$。因此 $g H g^{- 1} = H$。这表明 (i) 蕴含 (ii)。显然 (ii) 蕴含 (i)。接下来，如果 $g H g^{- 1} = H$，我们在等式右边乘以 $g$，得出 $g H = H g$。这表明 (ii) 蕴含 (iii)。类似地可以看到 (iii) 蕴含 (ii)。由于 (iii) 蕴含 (iv) 是显然的，只需检查 (iv) 蕴含 (iii)。

We ask: Under what circumstances can a left coset be equal to a right coset? We recall that the right cosets partition the group $G$ , and we note that the left coset $g H$ and the right coset $H g$ have an element in common, namely $g = g \cdot 1 = 1 \cdot g$ . So if the left coset $g H$ is equal to any right coset, that coset must be $H g$ . $\square$

我们问：在什么情况下一个左陪集可以等于一个右陪集？我们记得右陪集划分群 $G$，并且注意到左陪集 $g H$ 和右陪集 $H g$ 有一个公共元素，即 $g = g \cdot 1 = 1 \cdot g$。所以如果左陪集 $g H$ 等于某个右陪集，那个陪集必须是 $H g$。$\square$

## Proposition 2.8.18

## 命题 2.8.18

(a) If $H$ is a subgroup of a group $G$ and $g$ is an element of $G$ , the set $g H g^{-1}$ is also a subgroup.
(b) If a group $G$ has just one subgroup $H$ of order $r$ , then that subgroup is normal.

(a) 如果 $H$ 是群 $G$ 的一个子群，$g$ 是 $G$ 中的一个元素，那么集合 $g H g^{-1}$ 也是一个子群。
(b) 如果一个群 $G$ 只有一个阶为 $r$ 的子群 $H$，那么这个子群是正规的。

Proof. (a) Conjugation by $g$ is an automorphism of $G$ (see (2.6.4)), and $g H g^{- 1}$ is the image of $H$ . (b) See (2.8.17): $g H g^{- 1}$ is a subgroup of order $r$ . $\square$

证明：(a) 由 $g$ 的共轭是 $G$ 的一个自同构（见 (2.6.4)），而 $g H g^{- 1}$ 是 $H$ 的像。(b) 见 (2.8.17)：$g H g^{- 1}$ 是一个阶为 $r$ 的子群。$\square$

Note: If $H$ is a subgroup of a finite group $G$ , the counting formulas using right cosets or left cosets are the same, so the number of left cosets is equal to the number of right cosets. This is also true when $G$ is infinite, though the proof can't be made by counting (see Exercise M.8). $\square$

注：如果 $H$ 是有限群 $G$ 的一个子群，使用右陪集或左陪集的计数公式是相同的，所以左陪集的个数等于右陪集的个数。当 $G$ 是无限群时，这也是成立的，尽管不能通过计数来证明（见练习 M.8）。$\square$

===== Page 60 =====

### 2.9 MODULAR ARITHMETIC

### 2.9 模算术

This section contains a brief discussion of one of the most important concepts in number theory, congruence of integers. If you have not run across this concept before, you will want to read more about it. See, for instance, [Stark]. We work with a fixed positive integer $n$ throughout the section.

本节简要讨论数论中最重要的概念之一：整数的同余。如果你以前没有遇到过这个概念，你可能想多读一些相关内容。例如，见 [Stark]。整个部分我们固定一个正整数 $n$。

Two integers $a$ and $b$ are said to be congruent modulo $n$
$$a\equiv b\mathrm{~modulo~}n, \quad (2.9.1)$$
if $n$ divides $b - a$ or if $b = a + nk$ for some integer $k$ . For instance, $2\equiv 17$ modulo 5.

两个整数 $a$ 和 $b$ 称为**模 $n$ 同余**
$$a\equiv b\ \text{模 }n, \qquad (2.9.1)$$
如果 $n$ 整除 $b - a$，或者对于某个整数 $k$，$b = a + nk$。例如，$2\equiv 17$ 模 5。

It is easy to check that congruence is an equivalence relation, so we may consider the equivalence classes, called congruence classes, that it defines. We use bar notation, and denote the congruence class of an integer $a$ modulo $n$ by the symbol $\overline{a}$ . This congruence class is the set of integers
$$\overline{a} = \{\ldots ,a - n,a,a + n,a + 2n,\ldots \} . \quad (2.9.2)$$

很容易检查同余是一个等价关系，因此我们可以考虑它所定义的等价类，称为**同余类**。我们使用横线记号，并用符号 $\overline{a}$ 表示一个整数 $a$ 模 $n$ 的同余类。这个同余类是整数集
$$\overline{a} = \{\ldots ,a - n,a,a + n,a + 2n,\ldots \} . \qquad (2.9.2)$$

If $a$ and $b$ are integers, the equation $\overline{a} = \overline{b}$ means that $a\equiv b$ modulo $n$ , or that $n$ divides $b - a$ . The congruence class $\overline{0}$ is the subgroup
$$\overline{0} = \mathbb{Z}n = \{\ldots , - n,0,n,2n,\ldots \} = \{kn\mid k\in \mathbb{Z}\}$$
of the additive group $\mathbb{Z}^{+}$ . The other congruence classes are the cosets of this subgroup. Please note that $\mathbb{Z}n$ is not a right coset - it is a subgroup of $\mathbb{Z}^{+}$ . The notation for a coset of a subgroup $H$ analogous to $aH$ , but using additive notation for the law of composition, is $a + H = \{a + h\mid h\in H\}$ . To simplify notation, we denote the subgroup $\mathbb{Z}n$ by $H$ . Then the cosets of $H$ , the congruence classes, are the sets
$$a + H = \{a + kn\mid k\in \mathbb{Z}\} . \quad (2.9.3)$$

如果 $a$ 和 $b$ 是整数，等式 $\overline{a} = \overline{b}$ 意味着 $a\equiv b$ 模 $n$，或者 $n$ 整除 $b - a$。同余类 $\overline{0}$ 是加法群 $\mathbb{Z}^{+}$ 的子群
$$\overline{0} = \mathbb{Z}n = \{\ldots , - n,0,n,2n,\ldots \} = \{kn\mid k\in \mathbb{Z}\}$$
的陪集。其他同余类是这个子群的陪集。请注意，$\mathbb{Z}n$ 不是右陪集——它是 $\mathbb{Z}^{+}$ 的一个子群。子群 $H$ 的陪集记号类似于 $aH$，但对合成律使用加法记号，则为 $a + H = \{a + h\mid h\in H\}$。为简化记号，我们将子群 $\mathbb{Z}n$ 记为 $H$。那么 $H$ 的陪集，即同余类，是集合
$$a + H = \{a + kn\mid k\in \mathbb{Z}\} . \qquad (2.9.3)$$

The $n$ integers 0, 1, ..., $n - 1$ are representative elements for the $n$ congruence classes.

$n$ 个整数 0, 1, ..., $n - 1$ 是 $n$ 个同余类的代表元素。

Proposition 2.9.4 There are $n$ congruence classes modulo $n$ , namely $\overline{0},\overline{1},\ldots ,\overline{n - 1}$ . The index $[\mathbb{Z}:\mathbb{Z}n]$ of the subgroup $\mathbb{Z}n$ in $\mathbb{Z}$ is $n$ . $\square$

命题 2.9.4 有 $n$ 个模 $n$ 的同余类，即 $\overline{0},\overline{1},\ldots ,\overline{n - 1}$。子群 $\mathbb{Z}n$ 在 $\mathbb{Z}$ 中的指数 $[\mathbb{Z}:\mathbb{Z}n]$ 是 $n$。$\square$

Let $\overline{a}$ and $\overline{b}$ be congruence classes represented by integers $a$ and $b$ . Their sum is defined to be the congruence class of $a + b$ , and their product is the class of $ab$ . In other words, by definition,
$$\overline{a} +\overline{b} = \overline{a + b}\quad \mathrm{and}\quad \overline{a}\overline{b} = \overline{ab}. \quad (2.9.5)$$

设 $\overline{a}$ 和 $\overline{b}$ 是由整数 $a$ 和 $b$ 代表的同余类。它们的和定义为 $a + b$ 的同余类，它们的积定义为 $ab$ 的类。换句话说，根据定义，
$$\overline{a} +\overline{b} = \overline{a + b}\quad \text{和}\quad \overline{a}\overline{b} = \overline{ab}. \qquad (2.9.5)$$

This definition needs some justification, because the same congruence class can be represented by many different integers. Any integer $a^{\prime}$ congruent to $a$ modulo $n$ represents the same class as $a$ does. So it had better be true that if $a^{\prime}\equiv a$ and $b^{\prime}\equiv b$ , then $a^{\prime} + b^{\prime}\equiv a + b$ and $a^{\prime}b^{\prime}\equiv ab$ . Fortunately, this is so.

这个定义需要一些理由，因为同一个同余类可以由许多不同的整数代表。任何与 $a$ 模 $n$ 同余的整数 $a^{\prime}$ 代表与 $a$ 相同的类。所以最好要确保如果 $a^{\prime}\equiv a$ 且 $b^{\prime}\equiv b$，那么 $a^{\prime} + b^{\prime}\equiv a + b$ 且 $a^{\prime}b^{\prime}\equiv ab$。幸运的是，确实如此。

Lemma 2.9.6 If $a^{\prime}\equiv a$ and $b^{\prime}\equiv b$ modulo $n$ , then $a^{\prime} + b^{\prime}\equiv a + b$ and $a^{\prime}b^{\prime}\equiv ab$ modulo $n$ .

引理 2.9.6 如果 $a^{\prime}\equiv a$ 且 $b^{\prime}\equiv b$ 模 $n$，那么 $a^{\prime} + b^{\prime}\equiv a + b$ 且 $a^{\prime}b^{\prime}\equiv ab$ 模 $n$。

===== Page 61 =====

Proof. Assume that $a^{\prime} \equiv a$ and $b^{\prime} \equiv b$ , so that $a^{\prime} = a + rn$ and $b^{\prime} = b + sn$ for some integers $r$ and $s$ . Then $a^{\prime} + b^{\prime} = a + b + (r + s)n$ . This shows that $a^{\prime} + b^{\prime} \equiv a + b$ . Similarly, $a^{\prime} b^{\prime} = (a + rn)(b + sn) = ab + (as + rb + rns)n$ , so $a^{\prime} b^{\prime} \equiv ab$ . $\square$

证明：假设 $a^{\prime} \equiv a$ 且 $b^{\prime} \equiv b$，所以对于某些整数 $r$ 和 $s$，$a^{\prime} = a + rn$ 且 $b^{\prime} = b + sn$。那么 $a^{\prime} + b^{\prime} = a + b + (r + s)n$。这表明 $a^{\prime} + b^{\prime} \equiv a + b$。类似地，$a^{\prime} b^{\prime} = (a + rn)(b + sn) = ab + (as + rb + rns)n$，所以 $a^{\prime} b^{\prime} \equiv ab$。$\square$

The associative, commutative, and distributive laws hold for addition and multiplication of congruence classes because they hold for addition and multiplication of integers. For example, the distributive law is verified as follows:
$$\overline{a(b + c)} = \overline{a(b + c)} = \overline{a(b + c)} (\text{definition of }+ \text{and }\times \text{for congruence classes})$$
$$\qquad = \overline{a b + a c} (\text{distributive law in the integers})$$
$$\qquad = \overline{a b} +\overline{a c} = \overline{a b} +\overline{a c} (\text{definition of }+ \text{and }\times \text{for congruence classes}).$$

加法、乘法的结合律、交换律和分配律对于同余类成立，因为它们对于整数的加法和乘法成立。例如，分配律验证如下：
$$\overline{a(b + c)} = \overline{a(b + c)} = \overline{a(b + c)} \ (\text{+ 和 }\times \text{ 对于同余类的定义})$$
$$\qquad = \overline{a b + a c} \ (\text{整数中的分配律})$$
$$\qquad = \overline{a b} +\overline{a c} = \overline{a b} +\overline{a c} \ (\text{+ 和 }\times \text{ 对于同余类的定义}).$$

The verifications of other laws are similar, and we omit them.

其他律的验证类似，我们省略。

The set of congruence classes modulo $n$ may be denoted by any one of the symbols $\mathbb{Z} / \mathbb{Z}n$ $\mathbb{Z} / n\mathbb{Z}$ or $\mathbb{Z} / (n)$ . Addition, subtraction, and multiplication in $\mathbb{Z} / \mathbb{Z}n$ can be made explicit by working with integers and taking remainders after division by $n$ . That is what the formulas (2.9.5) mean. They tell us that the map
$$\mathbb{Z}\to \mathbb{Z} / \mathbb{Z}n \quad (2.9.7)$$
that sends an integer $a$ to its congruence class $\overline{a}$ is compatible with addition and multiplication. Therefore computations can be made in the integers and then carried over to $\mathbb{Z} / \mathbb{Z}n$ at the end. However, computations are simpler if the numbers are kept small. This can be done by computing the remainder after some part of a computation has been made.

模 $n$ 的同余类集合可以用符号 $\mathbb{Z} / \mathbb{Z}n$、$\mathbb{Z} / n\mathbb{Z}$ 或 $\mathbb{Z} / (n)$ 中的任何一个表示。通过使用整数并在除以 $n$ 后取余数，可以在 $\mathbb{Z} / \mathbb{Z}n$ 中明确地进行加、减和乘运算。这就是公式 (2.9.5) 的含义。它们告诉我们，将整数 $a$ 映射到其同余类 $\overline{a}$ 的映射
$$\mathbb{Z}\to \mathbb{Z} / \mathbb{Z}n \qquad (2.9.7)$$
与加法和乘法兼容。因此可以在整数中进行计算，然后在最后将结果传递到 $\mathbb{Z} / \mathbb{Z}n$。然而，如果保持数字较小，计算会更简单。这可以通过在计算的某个部分之后计算余数来实现。

Thus if $n = 29$ , so that $\mathbb{Z} / \mathbb{Z}n = \{\overline{0}, \overline{1}, \overline{2}, \ldots , \overline{28}\}$ , then $(35)(17 + \overline{7})$ can be computed as $\overline{35} \cdot \overline{24} = \overline{6} \cdot (- \overline{5}) = - \overline{30} = - \overline{1}$ .

因此，如果 $n = 29$，那么 $\mathbb{Z} / \mathbb{Z}n = \{\overline{0}, \overline{1}, \overline{2}, \ldots , \overline{28}\}$，那么 $(35)(17 + \overline{7})$ 可以计算为 $\overline{35} \cdot \overline{24} = \overline{6} \cdot (- \overline{5}) = - \overline{30} = - \overline{1}$。

In the long run, the bars over the numbers become a nuisance. They are often left off. When omitting bars, one just has to remember this rule:
$$\mathrm{To~say~}a = b\mathrm{~in~}\mathbb{Z} / \mathbb{Z}n\mathrm{~means~that~}a\equiv b\mathrm{~modulo~}n. \quad (2.9.8)$$

从长远来看，数字上的横线变得麻烦。它们经常被省略。当省略横线时，只需记住这个规则：
$$\text{在 }\mathbb{Z} / \mathbb{Z}n\text{ 中写 }a = b\text{ 意味着 }a\equiv b\text{ 模 }n. \qquad (2.9.8)$$

Congruences modulo a prime integer have special properties, which we discuss at the beginning of the next chapter.

模一个素整数的同余具有特殊性质，我们在下一章开头讨论这些性质。

### 2.10 THE CORRESPONDENCE THEOREM

### 2.10 对应定理

Let $\phi :G\to G$ be a group homomorphism, and let $H$ be a subgroup of $G$ .We may restrict $\phi$ to $H$ ,obtaining a homomorphism
$$\phi |_{H}:H\to G. \quad (2.10.1)$$

设 $\phi :G\to G$ 是一个群同态，并设 $H$ 是 $G$ 的一个子群。我们可以将 $\phi$ 限制到 $H$ 上，得到一个同态
$$\phi |_{H}:H\to G. \qquad (2.10.1)$$

This means that we take the same map $\phi$ but restrict its domain: So by definition, if $h$ is in $H$ , then $[\phi |_{H}](h) = \phi (h)$ . (We've added brackets around the symbol $\phi |_{H}$ for clarity.) The restriction is a homomorphism because $\phi$ is one, and the kernel of $\phi |_{H}$ is the intersection of the kernel of $\phi$ with $H$ :
$$\ker (\phi |_{H}) = (\ker \phi)\cap H. \quad (2.10.2)$$

这意味着我们采用同一个映射 $\phi$ 但限制其定义域：根据定义，如果 $h$ 在 $H$ 中，那么 $[\phi |_{H}](h) = \phi (h)$。（为了清晰起见，我们在符号 $\phi |_{H}$ 周围加了括号。）这个限制是一个同态，因为 $\phi$ 是一个同态，并且 $\phi |_{H}$ 的核是 $\phi$ 的核与 $H$ 的交集：
$$\ker (\phi |_{H}) = (\ker \phi)\cap H. \qquad (2.10.2)$$

===== Page 62 =====

This is clear from the definition of the kernel. The image of $\phi |_{H}$ is the same as the image $\phi (H)$ of $H$ under the map $\phi$ .

从核的定义可以清楚地看出这一点。$\phi |_{H}$ 的像与 $H$ 在映射 $\phi$ 下的像 $\phi (H)$ 相同。

The Counting Formula may help to describe the restriction. According to Corollary (2.8.13), the order of the image divides both $|H|$ and $|G'|$ . If $|H|$ and $|G'|$ have no common factor, $\phi (H) = \{1\}$ , so $H$ is contained in the kernel.

计数公式可能有助于描述这个限制。根据推论 (2.8.13)，像的阶同时整除 $|H|$ 和 $|G'|$。如果 $|H|$ 和 $|G'|$ 没有公因子，那么 $\phi (H) = \{1\}$，因此 $H$ 包含在核中。

Example 2.10.3 The image of the sign homomorphism $\sigma :S_{n}\to \{\pm 1\}$ has order 2. If a subgroup $H$ of the symmetric group $S_{n}$ has odd order, it will be contained in the kernel of $\sigma$ , the alternating group $A_{n}$ of even permutations. This will be so when $H$ is the cyclic subgroup generated by a permutation $q$ that is an element of odd order in the group. Every permutation whose order in the group is odd, such as an $n$ - cycle with $n$ odd, is an even permutation. A permutation that has even order in the group may be odd or even. $\square$

例 2.10.3 符号同态 $\sigma :S_{n}\to \{\pm 1\}$ 的像的阶为 2。如果对称群 $S_{n}$ 的一个子群 $H$ 有奇数阶，它将包含在 $\sigma$ 的核中，即偶置换群 $A_{n}$。当 $H$ 是由一个置换 $q$ 生成的循环子群，而 $q$ 在群中是奇阶元素时，就会发生这种情况。每个在群中具有奇数阶的置换，例如 $n$ 为奇数时的 $n$-循环，都是偶置换。在群中具有偶数阶的置换可能是奇的或偶的。$\square$

Proposition 2.10.4 Let $\phi :G\to G'$ be a homomorphism with kernel $K$ and let $H'$ be a subgroup of $G'$ . Denote the inverse image $\phi^{- 1}(H')$ by $H$ . Then $H$ is a subgroup of $G$ that contains $K$ . If $H'$ is a normal subgroup of $G'$ , then $H$ is a normal subgroup of $G$ . If $\phi$ is surjective and if $H$ is a normal subgroup of $G$ , then $H'$ is a normal subgroup of $G'$ .

命题 2.10.4 设 $\phi :G\to G'$ 是一个同态，其核为 $K$，并设 $H'$ 是 $G'$ 的一个子群。将原像 $\phi^{- 1}(H')$ 记为 $H$。那么 $H$ 是 $G$ 的一个包含 $K$ 的子群。如果 $H'$ 是 $G'$ 的正规子群，那么 $H$ 是 $G$ 的正规子群。如果 $\phi$ 是满射并且 $H$ 是 $G$ 的正规子群，那么 $H'$ 是 $G'$ 的正规子群。

For example, let $\phi$ denote the determinant homomorphism $G L_{n}(\mathbb{R})\to \mathbb{R}^{\times}$ . The set of positive real numbers is a subgroup of $\mathbb{R}^{\times}$ ; it is normal because $\mathbb{R}^{\times}$ is abelian. Its inverse image, the set of invertible matrices with positive determinant, is a normal subgroup of $G L_{n}(\mathbb{R})$ .

例如，令 $\phi$ 表示行列式同态 $G L_{n}(\mathbb{R})\to \mathbb{R}^{\times}$。正实数集是 $\mathbb{R}^{\times}$ 的一个子群；它是正规的，因为 $\mathbb{R}^{\times}$ 是阿贝尔的。它的原像，即具有正行列式的可逆矩阵的集合，是 $G L_{n}(\mathbb{R})$ 的一个正规子群。

Proof. This proof is simple, but we must keep in mind that $\phi^{- 1}$ is not a map. By definition, $\phi^{- 1}(H') = H$ is the set of elements $x$ of $G$ such that $\phi (x)$ is in $H'$ . First, if $x$ is in the kernel $K$ , then $\phi (x) = 1$ . Since 1 is in $H'$ , $x$ is in $H$ . Thus $H$ contains $K$ . We verify the conditions for a subgroup.

证明：这个证明很简单，但我们必须记住 $\phi^{- 1}$ 不是一个映射。根据定义，$\phi^{- 1}(H') = H$ 是 $G$ 中满足 $\phi (x)$ 在 $H'$ 中的元素 $x$ 的集合。首先，如果 $x$ 在核 $K$ 中，那么 $\phi (x) = 1$。由于 1 在 $H'$ 中，$x$ 在 $H$ 中。因此 $H$ 包含 $K$。我们验证子群的条件。

Closure: Suppose that $x$ and $y$ are in $H$ . Then $\phi (x)$ and $\phi (y)$ are in $H'$ . Since $H'$ is a subgroup, $\phi (x)\phi (y)$ is in $H'$ . Since $\phi$ is a homomorphism, $\phi (x)\phi (y) = \phi (xy)$ . So $\phi (xy)$ is in $H'$ , and $xy$ is in $H$ .

封闭性：假设 $x$ 和 $y$ 在 $H$ 中。那么 $\phi (x)$ 和 $\phi (y)$ 在 $H'$ 中。由于 $H'$ 是一个子群，$\phi (x)\phi (y)$ 在 $H'$ 中。由于 $\phi$ 是一个同态，$\phi (x)\phi (y) = \phi (xy)$。所以 $\phi (xy)$ 在 $H'$ 中，因此 $xy$ 在 $H$ 中。

Identity: 1 is in $H$ because $\phi (1) = 1$ is in $H'$ .
Inverses: Let $x$ be an element of $H$ . Then $\phi (x)$ is in $H'$ , and since $H'$ is a subgroup, $\phi (x)^{- 1}$ is also in $H'$ . Since $\phi$ is a homomorphism, $\phi (x)^{- 1} = \phi (x^{- 1})$ , so $\phi (x^{- 1})$ is in $H'$ , and $x^{- 1}$ is in $H$ .

单位元：1 在 $H$ 中，因为 $\phi (1) = 1$ 在 $H'$ 中。
逆元：设 $x$ 是 $H$ 中的一个元素。那么 $\phi (x)$ 在 $H'$ 中，并且由于 $H'$ 是一个子群，$\phi (x)^{- 1}$ 也在 $H'$ 中。由于 $\phi$ 是一个同态，$\phi (x)^{- 1} = \phi (x^{- 1})$，所以 $\phi (x^{- 1})$ 在 $H'$ 中，因此 $x^{- 1}$ 在 $H$ 中。

Suppose that $H'$ is a normal subgroup. Let $x$ and $g$ be elements of $H$ and $G$ , respectively. Then $\phi (gxg^{- 1}) = \phi (g)\phi (x)\phi (g)^{- 1}$ is a conjugate of $\phi (x)$ , and $\phi (x)$ is in $H'$ . Because $H'$ is normal, $\phi (gxg^{- 1})$ is in $H'$ , and therefore $gxg^{- 1}$ is in $H$ .

假设 $H'$ 是一个正规子群。设 $x$ 和 $g$ 分别是 $H$ 和 $G$ 中的元素。那么 $\phi (gxg^{- 1}) = \phi (g)\phi (x)\phi (g)^{- 1}$ 是 $\phi (x)$ 的一个共轭，并且 $\phi (x)$ 在 $H'$ 中。因为 $H'$ 是正规的，$\phi (gxg^{- 1})$ 在 $H'$ 中，因此 $gxg^{- 1}$ 在 $H$ 中。

Suppose that $\phi$ is surjective, and that $H$ is a normal subgroup of $G$ . Let $a$ be in $H'$ , and let $b$ be in $G'$ . There are elements $x$ of $H$ and $y$ of $G$ such that $\phi (x) = a$ and $\phi (y) = b$ . Since $H$ is normal, $yxy^{- 1}$ is in $H$ , and therefore $\phi (yxy^{- 1}) = bab^{- 1}$ is in $H'$ . $\square$

假设 $\phi$ 是满射，并且 $H$ 是 $G$ 的一个正规子群。设 $a$ 在 $H'$ 中，$b$ 在 $G'$ 中。存在 $H$ 中的元素 $x$ 和 $G$ 中的元素 $y$ 使得 $\phi (x) = a$ 和 $\phi (y) = b$。由于 $H$ 是正规的，$yxy^{- 1}$ 在 $H$ 中，因此 $\phi (yxy^{- 1}) = bab^{- 1}$ 在 $H'$ 中。$\square$

Theorem 2.10.5 Correspondence Theorem. Let $\phi :G\to G'$ be a surjective group homomorphism with kernel $K$ . There is a bijective correspondence between subgroups of $G'$ and subgroups of $G$ that contain $K$ :
$$\{\mathrm{subgroups~of~}G\mathrm{~that~contain~}K\} \longleftrightarrow \{\mathrm{subgroups~of~}G'\} .$$

定理 2.10.5 对应定理。设 $\phi :G\to G'$ 是一个满射群同态，其核为 $K$。在 $G'$ 的子群和 $G$ 中包含 $K$ 的子群之间存在一个双射对应：
$$\{\text{包含 }K\text{ 的 }G\text{ 的子群}\} \longleftrightarrow \{G' \text{ 的子群}\}.$$

===== Page 63 =====

This correspondence is defined as follows:
a subgroup $H$ of $G$ that contains $K \rightsquigarrow$ its image $\phi (H)$ in $G'$ ,
a subgroup $H'$ of $G' \rightsquigarrow$ its inverse image $\phi^{- 1}(H')$ in $G$ .

这个对应定义如下：
一个包含 $K$ 的 $G$ 的子群 $H$ $\rightsquigarrow$ 它在 $G'$ 中的像 $\phi (H)$，
一个 $G'$ 的子群 $H'$ $\rightsquigarrow$ 它在 $G$ 中的原像 $\phi^{- 1}(H')$。

If $H$ and $H'$ are corresponding subgroups, then $H$ is normal in $G$ if and only if $H'$ is normal in $G'$ .

如果 $H$ 和 $H'$ 是相互对应的子群，那么 $H$ 在 $G$ 中是正规的当且仅当 $H'$ 在 $G'$ 中是正规的。

If $H$ and $H'$ are corresponding subgroups, then $|H| = |H'||K|$ .

如果 $H$ 和 $H'$ 是相互对应的子群，那么 $|H| = |H'||K|$。

Example 2.10.6 We go back to the homomorphism $\phi : S_4 \to S_3$ that was defined in Example 2.5.13, and its kernel $K$ (2.5.15).

例 2.10.6 我们回到例 2.5.13 中定义的同态 $\phi : S_4 \to S_3$ 及其核 $K$ (2.5.15)。

The group $S_{3}$ has six subgroups, four of them proper. With the usual presentation, there is one proper subgroup of order 3, the cyclic group $\langle x \rangle$ , and there are three subgroups of order 2, including $\langle y \rangle$ . The Correspondence Theorem tells us that there are four proper subgroups of $S_{4}$ that contain $K$ . Since $|K| = 4$ , there is one subgroup of order 12 and there are three of order 8.

群 $S_{3}$ 有六个子群，其中四个是真子群。用通常的表示，有一个阶为 3 的真子群，即循环群 $\langle x \rangle$，还有三个阶为 2 的子群，包括 $\langle y \rangle$。对应定理告诉我们，$S_{4}$ 中有四个包含 $K$ 的真子群。由于 $|K| = 4$，有一个阶为 12 的子群，三个阶为 8 的子群。

We know a subgroup of order 12, namely the alternating group $A_{4}$ . That is the subgroup that corresponds to the cyclic group $\langle x \rangle$ of $S_{3}$ .

我们知道一个阶为 12 的子群，即交错群 $A_{4}$。这是对应于 $S_{3}$ 的循环群 $\langle x \rangle$ 的子群。

The subgroups of order 8 can be explained in terms of symmetries of a square. With vertices of the square labeled as in the figure below, a counterclockwise rotation through the angle $\pi /2$ corresponds to the 4- cycle (1234). Reflection about the diagonal through the vertex 1 corresponds to the transposition (24). These two permutations generate a subgroup of order 8. The other subgroups of order 8 can be obtained by labeling the vertices in other ways.

阶为 8 的子群可以用正方形的对称性来解释。将正方形的顶点按图中所示标记，逆时针旋转 $\pi /2$ 对应于 4-循环 (1234)。关于通过顶点 1 的对角线的反射对应于对换 (24)。这两个置换生成一个阶为 8 的子群。其他阶为 8 的子群可以通过其他方式标记顶点得到。

![image](2.10.6)

There are also some subgroups of $S_{4}$ that do not contain $K$ . The Correspondence Theorem has nothing to say about those subgroups.

$S_{4}$ 还有一些不包含 $K$ 的子群。对应定理对这些子群没有说明。

Proof of the Correspondence Theorem. Let $H$ be a subgroup of $G$ that contains $K$ , and let $H'$ be a subgroup of $G'$ . We must check the following points:
$\phi (H)$ is a subgroup of $G'$ .
$\phi^{- 1}(H')$ is a subgroup of $G$ , and it contains $K$ .
$H'$ is a normal subgroup of $G'$ if and only if $\phi^{- 1}(H')$ is a normal subgroup of $G$ .
(bijectivity of the correspondence) $\phi (\phi^{- 1}(H')) = H'$ and $\phi^{- 1}(\phi (H)) = H$ .
$|\phi^{- 1}(H')| = |H'||K|$ .

对应定理的证明。设 $H$ 是 $G$ 的一个包含 $K$ 的子群，并设 $H'$ 是 $G'$ 的一个子群。我们必须检查以下几点：
* $\phi (H)$ 是 $G'$ 的一个子群。
* $\phi^{- 1}(H')$ 是 $G$ 的一个子群，并且它包含 $K$。
* $H'$ 是 $G'$ 的正规子群当且仅当 $\phi^{- 1}(H')$ 是 $G$ 的正规子群。
* （对应的双射性）$\phi (\phi^{- 1}(H')) = H'$ 和 $\phi^{- 1}(\phi (H)) = H$。
* $|\phi^{- 1}(H')| = |H'||K|$。

Since $\phi (H)$ is the image of the homomorphism $\phi |_{H}$ , it is a subgroup of $G'$ . The second and third bullets form Proposition 2.10.4.

由于 $\phi (H)$ 是同态 $\phi |_{H}$ 的像，它是 $G'$ 的一个子群。第二和第三点构成命题 2.10.4。

Concerning the fourth bullet, the equality $\phi (\phi^{- 1}(H')) = H'$ is true for any surjective map of sets $\phi : S \to S'$ and any subset $H'$ of $S'$ . Also, $H \subset \phi^{- 1}(\phi (H))$ is true for any map

关于第四点，等式 $\phi (\phi^{- 1}(H')) = H'$ 对于任何满射集合映射 $\phi : S \to S'$ 和 $S'$ 的任何子集 $H'$ 都成立。此外，对于任何集合映射 $\phi : S \to S'$ 和 $S$ 的任何子集 $H$，有 $H \subset \phi^{- 1}(\phi (H))$。

===== Page 64 =====

$\phi$ of sets and any subset $H$ of $S$ .We omit the verification of these facts. Then the only thing remaining to be verified is that $H\supset \phi^{- 1}(\phi (H))$ . Let $x$ be an element of $\phi^{- 1}(\phi (H))$ We must show that $x$ is in $H$ .By definition of the inverse image, $\phi (x)$ is in $\phi (H)$ ,say $\phi (x) = \phi (a)$ ,with $a$ in $H$ .Then $a^{- 1}x$ is in the kernel $K$ (2.5.8),and since $H$ contains $K$ $a^{- 1}x$ is in $H$ . Since both $a$ and $a^{- 1}x$ are in $H,x$ is in $H$ too.

我们省略这些事实的验证。那么唯一需要验证的是 $H\supset \phi^{- 1}(\phi (H))$。设 $x$ 是 $\phi^{- 1}(\phi (H))$ 中的一个元素。我们必须证明 $x$ 在 $H$ 中。根据原像的定义，$\phi (x)$ 在 $\phi (H)$ 中，比如说 $\phi (x) = \phi (a)$，其中 $a$ 在 $H$ 中。那么 $a^{- 1}x$ 在核 $K$ 中 (2.5.8)，并且由于 $H$ 包含 $K$，$a^{- 1}x$ 在 $H$ 中。由于 $a$ 和 $a^{- 1}x$ 都在 $H$ 中，$x$ 也在 $H$ 中。

We leave the proof of the last bullet as an exercise. $\square$

我们留下最后一个要点的证明作为练习。$\square$

### 2.11 PRODUCT GROUPS

### 2.11 乘积群

Let $G,G^{\prime}$ be two groups. The product set $G\times G^{\prime}$ , the set of pairs of elements $(a,a^{\prime})$ with $a$ in $G$ and $a^{\prime}$ in $G^{\prime}$ , can be made into a group by component- wise multiplication - that is, multiplication of pairs is defined by the rule
$$(a,a^{\prime})\cdot (b,b^{\prime}) = (ab,a^{\prime}b^{\prime}). \quad (2.11.1)$$

设 $G,G^{\prime}$ 是两个群。乘积集 $G\times G^{\prime}$，即元素对 $(a,a^{\prime})$ 的集合，其中 $a$ 在 $G$ 中，$a^{\prime}$ 在 $G^{\prime}$ 中，可以通过分量乘法构成一个群——也就是说，对对的乘法定义为规则
$$(a,a^{\prime})\cdot (b,b^{\prime}) = (ab,a^{\prime}b^{\prime}). \qquad (2.11.1)$$

The pair $(1,1)$ is the identity, and the inverse of $(a,a^{\prime})$ is $(a^{- 1},a^{\prime - 1})$ . The associative law in $G\times G^{\prime}$ follows from the fact that it holds in $G$ and in $G^{\prime}$ .

对 $(1,1)$ 是单位元，$(a,a^{\prime})$ 的逆是 $(a^{- 1},a^{\prime - 1})$。$G\times G^{\prime}$ 中的结合律由它在 $G$ 和 $G^{\prime}$ 中成立推出。

The group obtained in this way is called the product of $G$ and $G^{\prime}$ and is denoted by $G\times G^{\prime}$ . It is related to the two factors $G$ and $G^{\prime}$ in a simple way that we can sum up in terms of some homomorphisms

这样得到的群称为 $G$ 和 $G^{\prime}$ 的**乘积**，记为 $G\times G^{\prime}$。它通过一些同态以简单的方式与两个因子 $G$ 和 $G^{\prime}$ 相关联。

![image](2.11.2)

They are defined by $i(x) = (x,1)$ , $i^{\prime}(x^{\prime}) = (1,x^{\prime})$ , $p(x,x^{\prime}) = x$ , $p^{\prime}(x,x^{\prime}) = x^{\prime}$ . The injective homomorphisms $i$ and $i^{\prime}$ may be used to identify $G$ and $G^{\prime}$ with their images, the subgroups $G\times 1$ and $1\times G^{\prime}$ of $G\times G^{\prime}$ . The maps $p$ and $p^{\prime}$ are surjective, the kernel of $p$ is $1\times G^{\prime}$ , and the kernel of $p^{\prime}$ is $G\times 1$ . These are the projections.

它们由 $i(x) = (x,1)$，$i^{\prime}(x^{\prime}) = (1,x^{\prime})$，$p(x,x^{\prime}) = x$，$p^{\prime}(x,x^{\prime}) = x^{\prime}$ 定义。单射同态 $i$ 和 $i^{\prime}$ 可用于将 $G$ 和 $G^{\prime}$ 等同于它们的像，即 $G\times G^{\prime}$ 的子群 $G\times 1$ 和 $1\times G^{\prime}$。映射 $p$ 和 $p^{\prime}$ 是满射的，$p$ 的核是 $1\times G^{\prime}$，$p^{\prime}$ 的核是 $G\times 1$。这些是**投影**。

It is obviously desirable to decompose a given group $G$ as a product, that is, to find groups $H$ and $H^{\prime}$ such that $G$ is isomorphic to the product $H\times H^{\prime}$ . The groups $H$ and $H^{\prime}$ will be simpler, and the relation between $H\times H^{\prime}$ and its factors is easily understood. It is rare that a group is a product, but it does happen occasionally.

显然，将给定的群 $G$ 分解为乘积是可取的，即找到群 $H$ 和 $H^{\prime}$，使得 $G$ 同构于乘积 $H\times H^{\prime}$。群 $H$ 和 $H^{\prime}$ 会更简单，并且 $H\times H^{\prime}$ 与其因子的关系很容易理解。一个群是乘积的情况很少，但偶尔会发生。

For example, it is rather surprising that a cyclic group of order 6 can be decomposed: A cyclic group $C_{6}$ of order 6 is isomorphic to the product $C_{2}\times C_{3}$ of cyclic groups of orders 2 and 3. To see this, say that $C_{2} = \langle y\rangle$ and $C_{3} = \langle z\rangle$ , with $y^{2} = 1$ and $z^{3} = 1$ , and let $x$ denote the element $(y,z)$ of the product group $C_{2}\times C_{3}$ . The smallest positive integer $k$ such that $x^{k} = (y^{k},z^{k})$ is the identity $(1,1)$ is $k = 6$ . So $x$ has order 6. Since $C_{2}\times C_{3}$ also has order 6, it is equal to the cyclic group $\langle x\rangle$ . The powers of $x$ , in order, are
$$(1,1),(y,z),(1,z^{2}),(y,1),(1,z),(y,z^{2}).$$

例如，一个 6 阶循环群可以分解，这相当令人惊讶：一个 6 阶循环群 $C_{6}$ 同构于 2 阶和 3 阶循环群的乘积 $C_{2}\times C_{3}$。为了看到这一点，设 $C_{2} = \langle y\rangle$ 且 $C_{3} = \langle z\rangle$，其中 $y^{2} = 1$，$z^{3} = 1$，并令 $x$ 表示乘积群 $C_{2}\times C_{3}$ 中的元素 $(y,z)$。使得 $x^{k} = (y^{k},z^{k})$ 为单位元 $(1,1)$ 的最小正整数 $k$ 是 $k = 6$。所以 $x$ 的阶为 6。由于 $C_{2}\times C_{3}$ 的阶也是 6，它等于由 $x$ 生成的循环群 $\langle x\rangle$。$x$ 的幂依次为
$$(1,1),(y,z),(1,z^{2}),(y,1),(1,z),(y,z^{2}).$$

There is an analogous statement for a cyclic group of order $r s$ , whenever the two integers $r$ and $s$ have no common factor.

对于阶为 $r s$ 的循环群，只要两个整数 $r$ 和 $s$ 没有公因子，也有类似的结论。

Proposition 2.11.3 Let $r$ and $s$ be relatively prime integers. A cyclic group of order $r s$ is isomorphic to the product of a cyclic group of order $r$ and a cyclic group of order $s$ . $\square$

命题 2.11.3 设 $r$ 和 $s$ 是互素的整数。一个 $r s$ 阶循环群同构于一个 $r$ 阶循环群和一个 $s$ 阶循环群的乘积。$\square$

===== Page 65 =====

On the other hand, a cyclic group of order 4 is not isomorphic to a product of two cyclic groups of order 2. Every element of $C_2 \times C_2$ has order 1 or 2, whereas a cyclic group of order 4 contains two elements of order 4.

另一方面，一个 4 阶循环群不同构于两个 2 阶循环群的乘积。$C_2 \times C_2$ 中的每个元素的阶都是 1 或 2，而一个 4 阶循环群包含两个 4 阶元素。

The next proposition describes product groups.

下一个命题描述了乘积群。

Proposition 2.11.4 Let $H$ and $K$ be subgroups of a group $G$ , and let $f\colon H\times K\to G$ be the multiplication map, defined by $f(h,k) = hk$ . Its image is the set $H K = \{h k\mid h\in H,k\in K\}$
(a) $f$ is injective if and only if $H\cap K = \{1\}$
(b) $f$ is a homomorphism from the product group $H\times K$ to $G$ if and only if elements of $K$ commute with elements of $H\colon hk = kh$
(c) If $H$ is a normal subgroup of $G$ , then $HK$ is a subgroup of $G$
(d) $f$ is an isomorphism from the product group $H\times K$ to $G$ if and only if $H\cap K = \{1\}$ $HK = G$ , and also $H$ and $K$ are normal subgroups of $G$

命题 2.11.4 设 $H$ 和 $K$ 是群 $G$ 的子群，并设 $f\colon H\times K\to G$ 是乘法映射，定义为 $f(h,k) = hk$。它的像是集合 $H K = \{h k\mid h\in H,k\in K\}$。
(a) $f$ 是单射当且仅当 $H\cap K = \{1\}$。
(b) $f$ 是从乘积群 $H\times K$ 到 $G$ 的同态当且仅当 $K$ 中的元素与 $H$ 中的元素交换：$hk = kh$。
(c) 如果 $H$ 是 $G$ 的一个正规子群，那么 $HK$ 是 $G$ 的一个子群。
(d) $f$ 是从乘积群 $H\times K$ 到 $G$ 的同构当且仅当 $H\cap K = \{1\}$，$HK = G$，并且 $H$ 和 $K$ 是 $G$ 的正规子群。

It is important to note that the multiplication map may be bijective though it isn't a group homomorphism. This happens, for instance, when $G = S_{3}$ , and with the usual notation, $H = \langle x\rangle$ and $K = \langle y\rangle$ .

重要的是要注意，乘法映射可能是双射的，尽管它不是群同态。例如，当 $G = S_{3}$ 时，用通常的记号，$H = \langle x\rangle$ 和 $K = \langle y\rangle$，就会发生这种情况。

Proof. (a) If $H\cap K$ contains an element $x\neq 1$ , then $x^{- 1}$ is in $H$ , and $f(x^{- 1},x) = 1 = f(1,1)$ so $f$ is not injective. Suppose that $H\cap K = \{1\}$ . Let $(h_{1},k_{1})$ and $(h_{2},k_{2})$ be elements of $H\times K$ such that $h_{1}k_{1} = h_{2}k_{2}$ . We multiply both sides of this equation on the left by $h_{1}^{- 1}$ and on the right by $k_{2}^{- 1}$ , obtaining $k_{1}k_{2}^{- 1} = h_{1}^{- 1}h_{2}$ . The left side is an element of $K$ and the right side is an element of $H$ . Since $H\cap K = \{1\}$ , $k_{1}k_{2}^{- 1} = h_{1}^{- 1}h_{2} = 1$ . Then $k_{1} = k_{2}$ , $h_{1} = h_{2}$ , and $(h_{1},k_{1}) = (h_{2},k_{2})$ .
(b) Let $(h_{1},k_{1})$ and $(h_{2},k_{2})$ be elements of the product group $H\times K$ . The product of these elements in the product group $H\times K$ is $(h_{1}h_{2},k_{1}k_{2})$ , and $f(h_{1}h_{2},k_{1}k_{2}) = h_{1}h_{2}k_{1}k_{2}$ , while $f(h_{1},k_{1})f(h_{2},k_{2}) = h_{1}k_{1}h_{2}k_{2}$ . These elements are equal if and only if $h_{2}k_{1} = k_{1}h_{2}$ .
(c) Suppose that $H$ is a normal subgroup. We note that $KH$ is a union of the left cosets $kH$ with $k$ in $K$ , and that $HK$ is a union of the right cosets $Hk$ . Since $H$ is normal, $kH = Hk$ , and therefore $HK = KH$ . Closure of $HK$ under multiplication follows, because $HKHK = HHKK = HK$ . Also, $(hk)^{- 1} = k^{- 1}h^{- 1}$ is in $KH = HK$ . This proves closure of $HK$ under inverses.
(d) Suppose that $H$ and $K$ satisfy the conditions given. Then $f$ is both injective and surjective, so it is bijective. According to (b), it is an isomorphism if and only if $hk = kh$ for all $h$ in $H$ and $k$ in $K$ . Consider the commutator $(hkh^{-1})k^{-1} = h(kh^{-1}k^{-1})$ . Since $K$ is normal, the left side is in $K$ , and since $H$ is normal, the right side is in $H$ . Since $H\cap K = \{1\}$ , $hkh^{-1}k^{-1} = 1$ , and $hk = kh$ . Conversely, if $f$ is an isomorphism, one may verify the conditions listed in the isomorphic group $H\times K$ instead of in $G$ . $\square$

证明：(a) 如果 $H\cap K$ 包含一个元素 $x\neq 1$，那么 $x^{- 1}$ 在 $H$ 中，并且 $f(x^{- 1},x) = 1 = f(1,1)$，所以 $f$ 不是单射。假设 $H\cap K = \{1\}$。设 $(h_{1},k_{1})$ 和 $(h_{2},k_{2})$ 是 $H\times K$ 中的元素，使得 $h_{1}k_{1} = h_{2}k_{2}$。我们在该等式左边乘以 $h_{1}^{- 1}$，右边乘以 $k_{2}^{- 1}$，得到 $k_{1}k_{2}^{- 1} = h_{1}^{- 1}h_{2}$。左边是 $K$ 的元素，右边是 $H$ 的元素。由于 $H\cap K = \{1\}$，$k_{1}k_{2}^{- 1} = h_{1}^{- 1}h_{2} = 1$。那么 $k_{1} = k_{2}$，$h_{1} = h_{2}$，且 $(h_{1},k_{1}) = (h_{2},k_{2})$。
(b) 设 $(h_{1},k_{1})$ 和 $(h_{2},k_{2})$ 是乘积群 $H\times K$ 中的元素。这些元素在乘积群 $H\times K$ 中的乘积是 $(h_{1}h_{2},k_{1}k_{2})$，而 $f(h_{1}h_{2},k_{1}k_{2}) = h_{1}h_{2}k_{1}k_{2}$，同时 $f(h_{1},k_{1})f(h_{2},k_{2}) = h_{1}k_{1}h_{2}k_{2}$。这两个元素相等当且仅当 $h_{2}k_{1} = k_{1}h_{2}$。
(c) 假设 $H$ 是一个正规子群。我们注意到 $KH$ 是左陪集 $kH$ 的并集，其中 $k$ 在 $K$ 中，而 $HK$ 是右陪集 $Hk$ 的并集。由于 $H$ 是正规的，$kH = Hk$，因此 $HK = KH$。$HK$ 在乘法下的封闭性随之而来，因为 $HKHK = HHKK = HK$。此外，$(hk)^{- 1} = k^{- 1}h^{- 1}$ 在 $KH = HK$ 中。这证明了 $HK$ 对逆元的封闭性。
(d) 假设 $H$ 和 $K$ 满足给定的条件。那么 $f$ 既是单射又是满射，所以它是双射。根据 (b)，它是一个同构当且仅当对于所有 $h$ 在 $H$ 中，$k$ 在 $K$ 中，有 $hk = kh$。考虑换位子 $(hkh^{-1})k^{-1} = h(kh^{-1}k^{-1})$。由于 $K$ 是正规的，左边在 $K$ 中，由于 $H$ 是正规的，右边在 $H$ 中。由于 $H\cap K = \{1\}$，$hkh^{-1}k^{-1} = 1$，且 $hk = kh$。反之，如果 $f$ 是一个同构，可以在同构的群 $H\times K$ 中验证列出的条件，而不是在 $G$ 中验证。$\square$

We use this proposition to classify groups of order 4:

我们使用这个命题来分类 4 阶群：

Proposition 2.11.5 There are two isomorphism classes of groups of order 4, the class of the cyclic group $C_4$ of order 4 and the class of the Klein Four Group, which is isomorphic to the product $C_2 \times C_2$ of two groups of order 2.

命题 2.11.5 有两个 4 阶群的同构类，即 4 阶循环群 $C_4$ 的类和克莱因四元群的类，后者同构于两个 2 阶群的乘积 $C_2 \times C_2$。

===== Page 66 =====

Proof. Let $G$ be a group of order 4. The order of any element $x$ of $G$ divides 4, so there are two cases to consider:

证明：设 $G$ 是一个 4 阶群。$G$ 中任何元素 $x$ 的阶整除 4，所以需要考虑两种情况：

Case 1: $G$ contains an element of order 4. Then $G$ is a cyclic group of order 4.
Case 2: Every element of $G$ except the identity has order 2.

情况 1：$G$ 包含一个 4 阶元素。那么 $G$ 是一个 4 阶循环群。
情况 2：除单位元外，$G$ 的每个元素都是 2 阶。

In this case, $x = x^{- 1}$ for every element $x$ of $G$ . Let $x$ and $y$ be two elements of $G$ . Then $xy$ has order 2, so $xyx^{- 1}y^{- 1} = (xy)(xy) = 1$ . This shows that $x$ and $y$ commute (2.6.5), and since these are arbitrary elements, $G$ is abelian. So every subgroup is normal. We choose distinct elements $x$ and $y$ in $G$ , and we let $H$ and $K$ be the cyclic groups of order 2 that they generate. Proposition 2.11.4(d) shows that $G$ is isomorphic to the product group $H \times K$ . $\square$

在这种情况下，对于 $G$ 的每个元素 $x$，有 $x = x^{- 1}$。设 $x$ 和 $y$ 是 $G$ 的两个元素。那么 $xy$ 的阶为 2，所以 $xyx^{- 1}y^{- 1} = (xy)(xy) = 1$。这表明 $x$ 和 $y$ 交换 (2.6.5)，并且由于这些是任意元素，$G$ 是阿贝尔的。所以每个子群都是正规的。我们在 $G$ 中选择两个不同的元素 $x$ 和 $y$，并让 $H$ 和 $K$ 分别是由它们生成的 2 阶循环群。命题 2.11.4(d) 表明 $G$ 同构于乘积群 $H \times K$。$\square$

### 2.12 QUOTIENT GROUPS

### 2.12 商群

In this section we show that a law of composition can be defined on the set of cosets of a normal subgroup $N$ of any group $G$ . This law makes the set of cosets of a normal subgroup into a group, called a quotient group.

在本节中，我们证明可以在任何群 $G$ 的正规子群 $N$ 的陪集集合上定义一个合成律。这个合成律将正规子群的陪集集合构成一个群，称为**商群**。

Addition of congruence classes of integers modulo $n$ is an example of the quotient construction. Another familiar example is addition of angles. Every real number represents an angle, and two real numbers represent the same angle if they differ by an integer multiple of $2\pi$ . The group $N$ of integer multiples of $2\pi$ is a subgroup of the additive group $\mathbb{R}^{+}$ of real numbers, and angles correspond naturally to (additive) cosets $\theta +N$ of $N$ in $G$ . The group of angles is the quotient group whose elements are the cosets.

整数模 $n$ 的同余类的加法是商构造的一个例子。另一个熟悉的例子是角度的加法。每个实数代表一个角度，如果两个实数相差 $2\pi$ 的整数倍，则它们代表同一个角度。整数倍 $2\pi$ 的群 $N$ 是实数加法群 $\mathbb{R}^{+}$ 的一个子群，角度自然地对应于 $N$ 在 $G$ 中的（加法）陪集 $\theta +N$。角度的群是商群，其元素是这些陪集。

The set of cosets of a normal subgroup $N$ of a group $G$ is often denoted by $G / N$ .
$$G / N\mathrm{~is~the~set~of~cosets~of~}N\mathrm{~in~}G. \quad (2.12.1)$$

群 $G$ 的正规子群 $N$ 的陪集集合通常记为 $G / N$。
$$G / N\text{ 是 }N\text{ 在 }G\text{ 中的陪集的集合}. \qquad (2.12.1)$$

When we regard a coset $C$ as an element of the set of cosets, the bracket notation $[C]$ may be used. If $C = aN$ , we may also use the bar notation to denote the element $[C]$ by $\overline{a}$ and then we would denote the set of cosets by $\overline{G}$ :
$$\overline{G} = G / N.$$

当我们把一个陪集 $C$ 视为陪集集合中的一个元素时，可以使用括号记号 $[C]$。如果 $C = aN$，我们也可以使用横线记号将元素 $[C]$ 记为 $\overline{a}$，那么我们将陪集集合记为 $\overline{G}$：
$$\overline{G} = G / N.$$

Theorem 2.12.2 Let $N$ be a normal subgroup of a group $G$ , and let $\overline{G}$ denote the set of cosets of $N$ in $G$ . There is a law of composition on $\overline{G}$ that makes this set into a group, such that the map $\pi :G \to \overline{G}$ defined by $\pi (a) = \overline{a}$ is a surjective homomorphism whose kernel is $N$ .

定理 2.12.2 设 $N$ 是群 $G$ 的一个正规子群，并设 $\overline{G}$ 表示 $N$ 在 $G$ 中的陪集的集合。在 $\overline{G}$ 上存在一个合成律，使该集合成为一个群，并且由 $\pi (a) = \overline{a}$ 定义的映射 $\pi :G \to \overline{G}$ 是一个满射同态，其核为 $N$。

The map $\pi$ is often referred to as the canonical map from $G$ to $\overline{G}$ . The word "canonical" indicates that this is the only map that we might reasonably be talking about.

映射 $\pi$ 通常称为从 $G$ 到 $\overline{G}$ 的**典范映射**。“典范”一词表明这是我们可能合理讨论的唯一映射。

The next corollary is very simple, but it is important enough to single out:

下一个推论非常简单，但非常重要，值得单独指出：

Corollary 2.12.3 Let $N$ be a normal subgroup of a group $G$ , and let $\overline{G}$ denote the set of cosets of $N$ in $G$ . Let $\pi :G \to \overline{G}$ be the canonical homomorphism. Let $a_{1}, \ldots , a_{k}$ be elements of $G$ such that the product $a_{1} \cdots a_{k}$ is in $N$ . Then $\overline{a_{1}} \cdots \overline{a_{k}} = \overline{1}$ .

推论 2.12.3 设 $N$ 是群 $G$ 的一个正规子群，并设 $\overline{G}$ 表示 $N$ 在 $G$ 中的陪集的集合。设 $\pi :G \to \overline{G}$ 是典范同态。设 $a_{1}, \ldots , a_{k}$ 是 $G$ 中的元素，使得乘积 $a_{1} \cdots a_{k}$ 在 $N$ 中。那么 $\overline{a_{1}} \cdots \overline{a_{k}} = \overline{1}$。

Proof. Let $p = a_{1} \cdots a_{k}$ . Then $p$ is in $N$ , so $\pi (p) = \overline{p} = \overline{1}$ . Since $\pi$ is a homomorphism, $\overline{a_{1}} \cdots \overline{a_{k}} = \overline{p}$ . $\square$

证明：设 $p = a_{1} \cdots a_{k}$。那么 $p$ 在 $N$ 中，所以 $\pi (p) = \overline{p} = \overline{1}$。由于 $\pi$ 是一个同态，$\overline{a_{1}} \cdots \overline{a_{k}} = \overline{p}$。$\square$

===== Page 67 =====

Proof of Theorem 2.12.2. There are several things to be done. We must
- define a law of composition on $\overline{G}$ ,
- prove that the law makes $\overline{G}$ into a group,
- prove that $\pi$ is a surjective homomorphism, and
- prove that the kernel of $\pi$ is $N$ .

定理 2.12.2 的证明。需要做几件事。我们必须
- 在 $\overline{G}$ 上定义一个合成律，
- 证明该律使 $\overline{G}$ 成为一个群，
- 证明 $\pi$ 是一个满射同态，以及
- 证明 $\pi$ 的核是 $N$。

We use the following notation: If $A$ and $B$ are subsets of a group $G$ , then $AB$ denotes the set of products $ab$ :
$$AB = \{x\in G\mid x = ab\mathrm{for~some~}a\in A\mathrm{~and~}b\in B\} .$$

我们使用以下记号：如果 $A$ 和 $B$ 是群 $G$ 的子集，那么 $AB$ 表示乘积 $ab$ 的集合：
$$AB = \{x\in G\mid x = ab\text{ 对于某个 }a\in A\text{ 和 }b\in B\} .$$

We will call this a product set, though in some other contexts the phrase "product set" refers to the set $A\times B$ of pairs of elements.

我们称其为乘积集，尽管在其他一些上下文中，“乘积集”一词指的是元素对的集合 $A\times B$。

Lemma 2.12.5 Let $N$ be a normal subgroup of a group $G$ , and let $aN$ and $bN$ be cosets of $N$ . The product set $(aN)(bN)$ is also a coset. It is equal to the coset $abN$ .

引理 2.12.5 设 $N$ 是群 $G$ 的一个正规子群，并设 $aN$ 和 $bN$ 是 $N$ 的陪集。乘积集 $(aN)(bN)$ 也是一个陪集。它等于陪集 $abN$。

We note that the set $(aN)(bN)$ consists of all elements of $G$ that can be written in the form $anbn'$ , with $n$ and $n'$ in $N$ .

我们注意到集合 $(aN)(bN)$ 由 $G$ 中所有可以写成 $anbn'$ 形式的元素组成，其中 $n$ 和 $n'$ 在 $N$ 中。

Proof. Since $N$ is a subgroup, $NN = N$ . Since $N$ is normal, left and right cosets are equal: $Nb = bN$ (2.8.17). The lemma is proved by the following formal manipulation:
$$(aN)(bN) = a(Nb)N = a(bN)N = abNN = abN. \quad \square$$

证明：由于 $N$ 是一个子群，$NN = N$。由于 $N$ 是正规的，左陪集和右陪集相等：$Nb = bN$ (2.8.17)。该引理通过以下形式推导得到证明：
$$(aN)(bN) = a(Nb)N = a(bN)N = abNN = abN. \quad \square$$

This lemma allows us to define multiplication on the set $\overline{G} = G / N$ . Using the bracket notation (2.7.8), the definition is this: If $C_1$ and $C_2$ are cosets, then $[C_1][C_2] = [C_1C_2]$ . Where $C_1C_2$ is the product set. The lemma shows that this product set is another coset. To compute the product $[C_1][C_2]$ , take any elements $a$ in $C_1$ and $b$ in $C_2$ . Then $C_1 = aN$ , $C_2 = bN$ , and $C_1C_2$ is the coset $abN$ that contains $ab$ . So we have the very natural formula
$$[aN][bN] = [abN]\quad \mathrm{or}\quad \overline{ab} = \overline{ab}. \quad (2.12.6)$$

这个引理允许我们在集合 $\overline{G} = G / N$ 上定义乘法。使用括号记号 (2.7.8)，定义如下：如果 $C_1$ 和 $C_2$ 是陪集，那么 $[C_1][C_2] = [C_1C_2]$。其中 $C_1C_2$ 是乘积集。引理表明这个乘积集是另一个陪集。为了计算乘积 $[C_1][C_2]$，取 $C_1$ 中的任意元素 $a$ 和 $C_2$ 中的任意元素 $b$。那么 $C_1 = aN$，$C_2 = bN$，并且 $C_1C_2$ 是包含 $ab$ 的陪集 $abN$。所以我们得到了非常自然的公式
$$[aN][bN] = [abN]\quad \text{或}\quad \overline{ab} = \overline{ab}. \qquad (2.12.6)$$

Then by definition of the map $\pi$ in (2.12.2),
$$\pi (a)\pi (b) = \overline{ab} = \overline{ab} = \pi (ab). \quad (2.12.7)$$

然后根据 (2.12.2) 中映射 $\pi$ 的定义，
$$\pi (a)\pi (b) = \overline{ab} = \overline{ab} = \pi (ab). \qquad (2.12.7)$$

The fact that $\pi$ is a homomorphism will follow from (2.12.7), once we show that $\overline{G}$ is a group. Since the canonical map $\pi$ is surjective (2.7.8), the next lemma proves this.

一旦我们证明了 $\overline{G}$ 是一个群，$\pi$ 是一个同态这一事实将紧随 (2.12.7) 得出。由于典范映射 $\pi$ 是满射的 (2.7.8)，下一个引理证明了这一点。

Lemma 2.12.8 Let $G$ be a group, and let $Y$ be a set with a law of composition, both laws written with multiplicative notation. Let $\phi :G\to Y$ be a surjective map with the homomorphism property, that $\phi (ab) = \phi (a)\phi (b)$ for all $a$ and $b$ in $G$ . Then $Y$ is a group and $\phi$ is a homomorphism.

引理 2.12.8 设 $G$ 是一个群，$Y$ 是一个具有合成律的集合，两个律都用乘法记号书写。设 $\phi :G\to Y$ 是一个具有同态性质的满射映射，即对于 $G$ 中所有 $a$ 和 $b$，有 $\phi (ab) = \phi (a)\phi (b)$。那么 $Y$ 是一个群，且 $\phi$ 是一个同态。

===== Page 68 =====

Proof. The group axioms that are true in $G$ are carried over to $Y$ by the surjective map $\phi$ Here is the proof of the associative law: Let $y_{1},y_{2},y_{3}$ be elements of $Y.$ Since $\phi$ is surjective, $y_{i} = \phi (x_{i})$ for some $x_{i}$ in $G$ .Then
$$(y_{1}y_{2})y_{3} = (\phi (x_{1})\phi (x_{2}))\phi (x_{3}) = \phi (x_{1}x_{2})\phi (x_{3}) = \phi ((x_{1}x_{2})x_{3})$$
$$\qquad = \phi (x_{1}(x_{2}x_{3})) = \phi (x_{1})\phi (x_{2}x_{3}) = \phi (x_{1})(\phi (x_{2})\phi (x_{3})) = y_{1}(y_{2}y_{3}).$$

证明：在 $G$ 中成立的群公理通过满射映射 $\phi$ 传递到 $Y$。以下是结合律的证明：设 $y_{1},y_{2},y_{3}$ 是 $Y$ 中的元素。由于 $\phi$ 是满射，对于 $G$ 中的某些 $x_{i}$，有 $y_{i} = \phi (x_{i})$。那么
$$(y_{1}y_{2})y_{3} = (\phi (x_{1})\phi (x_{2}))\phi (x_{3}) = \phi (x_{1}x_{2})\phi (x_{3}) = \phi ((x_{1}x_{2})x_{3})$$
$$\qquad = \phi (x_{1}(x_{2}x_{3})) = \phi (x_{1})\phi (x_{2}x_{3}) = \phi (x_{1})(\phi (x_{2})\phi (x_{3})) = y_{1}(y_{2}y_{3}).$$

The equality marked with an asterisk is the associative law in $G$ . The other equalities follow from the homomorphism property of $\phi$ . The verifications of the other group axioms are similar. $\square$

标有星号的等式是 $G$ 中的结合律。其他等式由 $\phi$ 的同态性质推出。其他群公理的验证类似。$\square$

The only thing remaining to be verified is that the kernel of the homomorphism $\pi$ is the subgroup $N$ . Well, $\pi (a) = \pi (1)$ if and only if $\overline{a} = \overline{1}$ , or $[aN] = [1N]$ , and this is true if and only if $a$ is an element of $N$ . $\square$

唯一需要验证的是同态 $\pi$ 的核是子群 $N$。好吧，$\pi (a) = \pi (1)$ 当且仅当 $\overline{a} = \overline{1}$，或 $[aN] = [1N]$，而这成立当且仅当 $a$ 是 $N$ 的一个元素。$\square$

![image](2.12.9) A Schematic Diagram of Coset Multiplication.

![image](2.12.9) 陪集乘法的示意图。

Note: Our assumption that $N$ be a normal subgroup of $G$ is crucial to Lemma 2.12.5. If $H$ is not normal, there will be left cosets $C_{1}$ and $C_{2}$ of $H$ in $G$ such that the product set $C_{1}C_{2}$ does not lie in a single left coset. Going back once more to the subgroup $H = \langle y\rangle$ of $S_{3}$ the product set $(1H)(xH)$ contains four elements: $\{1,y\} \{x,xy\} = \{x,xy,x^{2}y,x^{2}\}$ . It is not a coset. The subgroup $H$ is not normal. $\square$

注：我们假设 $N$ 是 $G$ 的正规子群对引理 2.12.5 至关重要。如果 $H$ 不是正规的，则存在 $H$ 在 $G$ 中的左陪集 $C_{1}$ 和 $C_{2}$，使得乘积集 $C_{1}C_{2}$ 不包含在单个左陪集中。再次回到 $S_{3}$ 的子群 $H = \langle y\rangle$，乘积集 $(1H)(xH)$ 包含四个元素：$\{1,y\} \{x,xy\} = \{x,xy,x^{2}y,x^{2}\}$。它不是一个陪集。子群 $H$ 不是正规的。$\square$

The next theorem relates the quotient group construction to a general group homomorphism, and it provides a fundamental method of identifying quotient groups.

下一个定理将商群构造与一般的群同态联系起来，并提供了一种识别商群的基本方法。

Theorem 2.12.10 First Isomorphism Theorem. Let $\phi :G\to G^{\prime}$ be a surjective group homomorphism with kernel $N$ . The quotient group $\overline{G} = G / N$ is isomorphic to the image $G^{\prime}$ . To be precise, let $\pi :G\to \overline{G}$ be the canonical map. There is a unique isomorphism $\overline{\phi} :\overline{G}\to G^{\prime}$ such that $\phi = \overline{\phi}\circ \pi$ .

定理 2.12.10 第一同构定理。设 $\phi :G\to G^{\prime}$ 是一个满射群同态，其核为 $N$。商群 $\overline{G} = G / N$ 同构于像 $G^{\prime}$。准确地说，设 $\pi :G\to \overline{G}$ 是典范映射。存在唯一的同构 $\overline{\phi} :\overline{G}\to G^{\prime}$，使得 $\phi = \overline{\phi}\circ \pi$。

===== Page 69 =====

Proof. The elements of $\overline{G}$ are the cosets of $N$ , and they are also the fibres of the map $\phi$ (2.7.15). The map $\overline{\phi}$ referred to in the theorem is the one that sends a nonempty fibre to its image: $\overline{\phi} (\overline{x}) = \phi (x)$ . For any surjective map of sets $\phi :G \to G'$ , one can form the set $\overline{G}$ of fibres, and then one obtains a diagram as above, in which $\overline{\phi}$ is the bijective map that sends a fibre to its image. When $\phi$ is a group homomorphism, $\overline{\phi}$ is an isomorphism because $\overline{\phi} (ab) = \phi (ab) = \phi (a)\phi (b) = \overline{\phi} (\overline{a})\overline{\phi} (\overline{b})$ . $\square$

证明：$\overline{G}$ 的元素是 $N$ 的陪集，它们也是映射 $\phi$ 的纤维 (2.7.15)。定理中提到的映射 $\overline{\phi}$ 是将非空纤维送到其像的映射：$\overline{\phi} (\overline{x}) = \phi (x)$。对于任何满射集合映射 $\phi :G \to G'$，我们可以构造纤维的集合 $\overline{G}$，然后得到如上图，其中 $\overline{\phi}$ 是将纤维送到其像的双射映射。当 $\phi$ 是一个群同态时，$\overline{\phi}$ 是一个同构，因为 $\overline{\phi} (ab) = \phi (ab) = \phi (a)\phi (b) = \overline{\phi} (\overline{a})\overline{\phi} (\overline{b})$。$\square$

Corollary 2.12.11 Let $\phi :G \to G'$ be a group homomorphism with kernel $N$ and image $H'$ . The quotient group $\overline{G} = G / N$ is isomorphic to the image $H'$ . $\square$

推论 2.12.11 设 $\phi :G \to G'$ 是一个群同态，其核为 $N$，像为 $H'$。商群 $\overline{G} = G / N$ 同构于像 $H'$。$\square$

Two quick examples: The image of the absolute value map $\mathbb{C}^{\times} \to \mathbb{R}^{\times}$ is the group of positive real numbers, and its kernel is the unit circle $U$ . The theorem asserts that the quotient group $\mathbb{C}^{\times} / U$ is isomorphic to the multiplicative group of positive real numbers. The determinant is a surjective homomorphism $G L_{n}(\mathbb{R}) \to \mathbb{R}^{\times}$ , whose kernel is the special linear group $S L_{n}(\mathbb{R})$ . So the quotient $G L_{n}(\mathbb{R}) / S L_{n}(\mathbb{R})$ is isomorphic to $\mathbb{R}^{\times}$ .

两个快速例子：绝对值映射 $\mathbb{C}^{\times} \to \mathbb{R}^{\times}$ 的像是正实数群，其核是单位圆 $U$。该定理断言商群 $\mathbb{C}^{\times} / U$ 同构于正实数的乘法群。行列式是一个满射同态 $G L_{n}(\mathbb{R}) \to \mathbb{R}^{\times}$，其核是特殊线性群 $S L_{n}(\mathbb{R})$。所以商群 $G L_{n}(\mathbb{R}) / S L_{n}(\mathbb{R})$ 同构于 $\mathbb{R}^{\times}$。

There are also theorems called the Second and the Third Isomorphism Theorems, though they are less important.

还有称为第二同构定理和第三同构定理的定理，尽管它们不那么重要。

---

## EXERCISES

## 练习

## Section 1 Laws of Composition

## 第1节 合成律

1.1. Let $S$ be a set. Prove that the law of composition defined by $ab = a$ for all $a$ and $b$ in $S$ is associative. For which sets does this law have an identity?

1.1. 设 $S$ 是一个集合。证明由 $ab = a$ 对 $S$ 中所有 $a$ 和 $b$ 定义的合成律是结合的。对于哪些集合，这个律有单位元？

1.2. Prove the properties of inverses that are listed near the end of the section.

1.2. 证明本节末尾列出的逆元的性质。

1.3. Let $\mathbb{N}$ denote the set $\{1,2,3,\ldots ,\}$ of natural numbers, and let $s:\mathbb{N}\to \mathbb{N}$ be the shift map, defined by $s(n) = n + 1$ . Prove that $s$ has no right inverse, but that it has infinitely many left inverses.

1.3. 设 $\mathbb{N}$ 表示自然数的集合 $\{1,2,3,\ldots ,\}$，并设 $s:\mathbb{N}\to \mathbb{N}$ 是移位映射，定义为 $s(n) = n + 1$。证明 $s$ 没有右逆元，但有无限多个左逆元。

## Section 2 Groups and Subgroups

## 第2节 群和子群

2.1. Make a multiplication table for the symmetric group $S_{3}$ .

2.1. 制作对称群 $S_{3}$ 的乘法表。

2.2. Let $S$ be a set with an associative law of composition and with an identity element. Prove that the subset consisting of the invertible elements in $S$ is a group.

2.2. 设 $S$ 是一个具有结合合成律和单位元的集合。证明由 $S$ 中可逆元素组成的子集是一个群。

2.3. Let $x,y,z$ ,and $w$ be elements of a group $G$
(a) Solve for $y$ , given that $x y z^{-1}w = 1$
(b) Suppose that $x y z = 1$ . Does it follow that $y z x = 1$ ? Does it follow that $y x z = 1$ ?

2.3. 设 $x,y,z$ 和 $w$ 是群 $G$ 中的元素。
(a) 已知 $x y z^{-1}w = 1$，求解 $y$。
(b) 假设 $x y z = 1$。能否推出 $y z x = 1$？能否推出 $y x z = 1$？

===== Page 70 =====

2.4. In which of the following cases is $H$ a subgroup of $G$ ?
(a) $G = G L_{n}(\mathbb{C})$ and $H = G L_{n}(\mathbb{R})$
(b) $G = \mathbb{R}^{\times}$ and $H = \{1, - 1\}$
(c) $G = \mathbb{Z}^{+}$ and $H$ is the set of positive integers.
(d) $G = \mathbb{R}^{\times}$ and $H$ is the set of positive reals.
(e) $G = G L_{2}(\mathbb{R})$ and $H$ is the set of matrices $\left[ \begin{array}{ll}a & 0\\ 0 & 0 \end{array} \right]$ , with $a\neq 0$

2.4. 在以下哪些情况下 $H$ 是 $G$ 的子群？
(a) $G = G L_{n}(\mathbb{C})$，$H = G L_{n}(\mathbb{R})$
(b) $G = \mathbb{R}^{\times}$，$H = \{1, - 1\}$
(c) $G = \mathbb{Z}^{+}$，$H$ 是正整数集合。
(d) $G = \mathbb{R}^{\times}$，$H$ 是正实数集合。
(e) $G = G L_{2}(\mathbb{R})$，$H$ 是矩阵 $\left[ \begin{array}{ll}a & 0\\ 0 & 0 \end{array} \right]$ 的集合，其中 $a\neq 0$

2.5. In the definition of a subgroup, the identity element in $H$ is required to be the identity of $G$ . One might require only that $H$ have an identity element, not that it need be the same as the identity in $G$ . Show that if $H$ has an identity at all, then it is the identity in $G$ . Show that the analogous statement is true for inverses.

2.5. 在子群的定义中，要求 $H$ 中的单位元是 $G$ 的单位元。人们可能只要求 $H$ 有一个单位元，而不要求它与 $G$ 中的单位元相同。证明如果 $H$ 确实有一个单位元，那么它就是 $G$ 中的单位元。证明关于逆元的类似陈述也是正确的。

2.6. Let $G$ be a group. Define an opposite group $G^{\circ}$ with law of composition $a*b$ as follows: The underlying set is the same as $G$ , but the law of composition is $a*b = ba$ . Prove that $G^{\circ}$ is a group.

2.6. 设 $G$ 是一个群。定义其**相反群** $G^{\circ}$，其合成律 $a*b$ 如下：基础集合与 $G$ 相同，但合成律为 $a*b = ba$。证明 $G^{\circ}$ 是一个群。

## Section 3 Subgroups of the Additive Group of Integers

## 第3节 整数加法群的子群

3.1. Let $a = 123$ and $b = 321$ . Compute $d = \gcd (a,b)$ , and express $d$ as an integer combination $ra + sb$ .

3.1. 设 $a = 123$，$b = 321$。计算 $d = \gcd (a,b)$，并将 $d$ 表示为整数组合 $ra + sb$。

3.2. Prove that if $a$ and $b$ are positive integers whose sum is a prime $p$ , their greatest common divisor is 1.

3.2. 证明如果 $a$ 和 $b$ 是正整数，且其和是素数 $p$，则它们的最大公因数为 1。

3.3. (a) Define the greatest common divisor of a set $\{a_{1},\ldots ,a_{n}\}$ of $n$ integers. Prove that it exists, and that it is an integer combination of $a_{1},\ldots ,a_{n}$ . (b) Prove that if the greatest common divisor of $\{a_{1},\ldots ,a_{n}\}$ is $d$ , then the greatest common divisor of $\{a_{1} / d,\ldots ,a_{n} / d\}$ is 1.

3.3. (a) 定义 $n$ 个整数的集合 $\{a_{1},\ldots ,a_{n}\}$ 的最大公因数。证明它存在，并且它是 $a_{1},\ldots ,a_{n}$ 的整数组合。(b) 证明如果 $\{a_{1},\ldots ,a_{n}\}$ 的最大公因数是 $d$，那么 $\{a_{1} / d,\ldots ,a_{n} / d\}$ 的最大公因数是 1。

## Section 4 Cyclic Groups

## 第4节 循环群

4.1. Let $a$ and $b$ be elements of a group $G$ . Assume that $a$ has order 7 and that $a^{3}b = ba^{3}$ . Prove that $ab = ba$ .

4.1. 设 $a$ 和 $b$ 是群 $G$ 中的元素。假设 $a$ 的阶为 7，且 $a^{3}b = ba^{3}$。证明 $ab = ba$。

4.2. An $n$ th root of unity is a complex number $z$ such that $z^{n} = 1$ .
(a) Prove that the $n$ th roots of unity form a cyclic subgroup of $\mathbb{C}^{\times}$ of order $n$ .
(b) Determine the product of all the $n$ th roots of unity.

4.2. $n$ 次单位根是满足 $z^{n} = 1$ 的复数 $z$。
(a) 证明 $n$ 次单位根构成 $\mathbb{C}^{\times}$ 的一个 $n$ 阶循环子群。
(b) 求所有 $n$ 次单位根的乘积。

4.3. Let $a$ and $b$ be elements of a group $G$ . Prove that $ab$ and $ba$ have the same order.

4.3. 设 $a$ 和 $b$ 是群 $G$ 中的元素。证明 $ab$ 和 $ba$ 具有相同的阶。

4.4. Describe all groups $G$ that contain no proper subgroup.

4.4. 描述所有不包含真子群的群 $G$。

4.5. Prove that every subgroup of a cyclic group is cyclic. Do this by working with exponents, and use the description of the subgroups of $\mathbb{Z}^{+}$ .

4.5. 证明循环群的每个子群都是循环的。通过处理指数来证明，并使用 $\mathbb{Z}^{+}$ 的子群的描述。

4.6. (a) Let $G$ be a cyclic group of order 6. How many of its elements generate $G$ ? Answer the same question for cyclic groups of orders 5 and 8. (b) Describe the number of elements that generate a cyclic group of arbitrary order $n$ .

4.6. (a) 设 $G$ 是一个 6 阶循环群。它的多少个元素生成 $G$？对 5 阶和 8 阶循环群回答相同的问题。(b) 描述生成任意 $n$ 阶循环群的元素的个数。

4.7. Let $x$ and $y$ be elements of a group $G$ . Assume that each of the elements $x$ , $y$ , and $xy$ has order 2. Prove that the set $H = \{1, x, y, xy\}$ is a subgroup of $G$ , and that it has order 4.

4.7. 设 $x$ 和 $y$ 是群 $G$ 中的元素。假设元素 $x$、$y$ 和 $xy$ 的阶都是 2。证明集合 $H = \{1, x, y, xy\}$ 是 $G$ 的一个子群，且其阶为 4。

===== Page 71 =====

4.8. (a) Prove that the elementary matrices of the first and third types (1.2.4) generate $GL_{n}(\mathbb{R})$ . (b) Prove that the elementary matrices of the first type generate $SL_{n}(\mathbb{R})$ . Do the $2 \times 2$ case first.

4.8. (a) 证明第一类和第三类初等矩阵 (1.2.4) 生成 $GL_{n}(\mathbb{R})$。(b) 证明第一类初等矩阵生成 $SL_{n}(\mathbb{R})$。先处理 $2 \times 2$ 的情况。

4.9. How many elements of order 2 does the symmetric group $S_{4}$ contain?

4.9. 对称群 $S_{4}$ 包含多少个 2 阶元素？

4.10. Show by example that the product of elements of finite order in a group need not have finite order. What if the group is abelian?

4.10. 举例说明群中有限阶元素的乘积不一定有有限阶。如果群是阿贝尔群呢？

4.11. (a) Adapt the method of row reduction to prove that the transpositions generate the symmetric group $S_{n}$ . (b) Prove that, for $n \geq 3$ , the three-cycles generate the alternating group $A_{n}$ .

4.11. (a) 改编行简化方法以证明对换生成对称群 $S_{n}$。(b) 证明对于 $n \geq 3$，3-循环生成交错群 $A_{n}$。

## Section 5 Homomorphisms

## 第5节 同态

5.1. Let $\phi :G\to G^{\prime}$ be a surjective homomorphism. Prove that if $G$ is cyclic, then $G^{\prime}$ is cyclic, and if $G$ is abelian, then $G^{\prime}$ is abelian.

5.1. 设 $\phi :G\to G^{\prime}$ 是一个满射同态。证明如果 $G$ 是循环的，那么 $G^{\prime}$ 是循环的；如果 $G$ 是阿贝尔的，那么 $G^{\prime}$ 是阿贝尔的。

5.2. Prove that the intersection $K\cap H$ of subgroups of a group $G$ is a subgroup of $H$ and that if $K$ is a normal subgroup of $G$ , then $K\cap H$ is a normal subgroup of $H$ .

5.2. 证明群 $G$ 的子群 $K$ 和 $H$ 的交集 $K\cap H$ 是 $H$ 的子群，并且如果 $K$ 是 $G$ 的正规子群，那么 $K\cap H$ 是 $H$ 的正规子群。

5.3. Let $U$ denote the group of invertible upper triangular $2\times 2$ matrices $A = \left[ \begin{array}{cc}a & b\\ 0 & d \end{array} \right]$ , and let $\phi :U\to \mathbb{R}^{\times}$ be the map that sends $A\mapsto a^{2}$ . Prove that $\phi$ is a homomorphism, and determine its kernel and image.

5.3. 设 $U$ 表示可逆上三角 $2\times 2$ 矩阵 $A = \left[ \begin{array}{cc}a & b\\ 0 & d \end{array} \right]$ 的群，并设 $\phi :U\to \mathbb{R}^{\times}$ 是将 $A$ 映射到 $a^{2}$ 的映射。证明 $\phi$ 是一个同态，并确定其核和像。

5.4. Let $f:\mathbb{R}^{+}\to \mathbb{C}^{\times}$ be the map $f(x) = e^{i x}$ . Prove that $f$ is a homomorphism, and determine its kernel and image.

5.4. 设 $f:\mathbb{R}^{+}\to \mathbb{C}^{\times}$ 是映射 $f(x) = e^{i x}$。证明 $f$ 是一个同态，并确定其核和像。

5.5. Prove that the $n\times n$ matrices that have the block form $M = \left[ \begin{array}{cc}A & B\\ 0 & D \end{array} \right]$ , with $A$ in $GL_{r}(\mathbb{R})$ and $D$ in $GL_{n - r}(\mathbb{R})$ , form a subgroup $H$ of $GL_{n}(\mathbb{R})$ , and that the map $H\to GL_{r}(\mathbb{R})$ that sends $M\mapsto A$ is a homomorphism. What is its kernel?

5.5. 证明具有块形式 $M = \left[ \begin{array}{cc}A & B\\ 0 & D \end{array} \right]$ 的 $n\times n$ 矩阵，其中 $A$ 在 $GL_{r}(\mathbb{R})$ 中，$D$ 在 $GL_{n - r}(\mathbb{R})$ 中，构成 $GL_{n}(\mathbb{R})$ 的一个子群 $H$，并且将 $M$ 映射到 $A$ 的映射 $H\to GL_{r}(\mathbb{R})$ 是一个同态。它的核是什么？

5.6. Determine the center of $GL_{n}(\mathbb{R})$ .
Hint: You are asked to determine the invertible matrices $A$ that commute with every invertible matrix $B$ . Do not test with a general matrix $B$ . Test with elementary matrices.

5.6. 确定 $GL_{n}(\mathbb{R})$ 的中心。
提示：要求确定与每个可逆矩阵 $B$ 交换的可逆矩阵 $A$。不要用一般的矩阵 $B$ 来测试。用初等矩阵来测试。

## Section 6 Isomorphisms

## 第6节 同构

6.1. Let $G^{\prime}$ be the group of real matrices of the form $\left[ \begin{array}{cc}1 & x\\ 1 & 1 \end{array} \right]$ . Is the map $\mathbb{R}^{+}\to G^{\prime}$ that sends $x$ to this matrix an isomorphism?

6.1. 设 $G^{\prime}$ 是形如 $\left[ \begin{array}{cc}1 & x\\ 1 & 1 \end{array} \right]$ 的实矩阵的群。将 $x$ 映射到这个矩阵的映射 $\mathbb{R}^{+}\to G^{\prime}$ 是一个同构吗？

6.2. Describe all homomorphisms $\phi :\mathbb{Z}^{+}\to \mathbb{Z}^{+}$ . Determine which are injective, which are surjective, and which are isomorphisms.

6.2. 描述所有同态 $\phi :\mathbb{Z}^{+}\to \mathbb{Z}^{+}$。确定哪些是单射，哪些是满射，哪些是同构。

6.3. Show that the functions $f = 1 / x$ , $g = (x - 1) / x$ generate a group of functions, the law of composition being composition of functions, that is isomorphic to the symmetric group $S_{3}$ .

6.3. 证明函数 $f = 1 / x$，$g = (x - 1) / x$ 生成一个函数群，其合成律是函数的复合，该群同构于对称群 $S_{3}$。

6.4. Prove that in a group, the products $ab$ and $ba$ are conjugate elements.

6.4. 证明在一个群中，乘积 $ab$ 和 $ba$ 是共轭元素。

6.5. Decide whether or not the two matrices $A = \left[ \begin{array}{cc}3 & 2\\ 2 & 2 \end{array} \right]$ and $B = \left[ \begin{array}{cc}1 & 1\\ - 2 & 4 \end{array} \right]$ are conjugate elements of the general linear group $GL_{2}(\mathbb{R})$ .

6.5. 判断两个矩阵 $A = \left[ \begin{array}{cc}3 & 2\\ 2 & 2 \end{array} \right]$ 和 $B = \left[ \begin{array}{cc}1 & 1\\ - 2 & 4 \end{array} \right]$ 是否是一般线性群 $GL_{2}(\mathbb{R})$ 中的共轭元素。

===== Page 72 =====

6.6. Are the matrices $\left[ \begin{array}{cc}1 & 1\\ 1 & 1 \end{array} \right], \left[ \begin{array}{cc}1 & 1\\ 1 & 1 \right]$ conjugate elements of the group $GL_2(\mathbb{R})$ ? Are they conjugate elements of $SL_2(\mathbb{R})$ ?

6.6. 矩阵 $\begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}$ 和 $\begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}$ 是群 $GL_2(\mathbb{R})$ 中的共轭元素吗？它们是 $SL_2(\mathbb{R})$ 中的共轭元素吗？(注：原文此处第二个矩阵似乎有误)

6.7. Let $H$ be a subgroup of $G$ and let $g$ be a fixed element of $G$ . The conjugate subgroup $gHg^{-1}$ is defined to be the set of all conjugates $ghg^{-1}$ , with $h$ in $H$ . Prove that $gHg^{-1}$ is a subgroup of $G$ .

6.7. 设 $H$ 是 $G$ 的一个子群，$g$ 是 $G$ 中一个固定元素。共轭子群 $gHg^{-1}$ 定义为所有共轭 $ghg^{-1}$ 的集合，其中 $h$ 在 $H$ 中。证明 $gHg^{-1}$ 是 $G$ 的一个子群。

6.8. Prove that the map $A \mapsto (A^t)^{-1}$ is an automorphism of $GL_n(\mathbb{R})$ .

6.8. 证明映射 $A \mapsto (A^t)^{-1}$ 是 $GL_n(\mathbb{R})$ 的一个自同构。

6.9. Prove that a group $G$ and its opposite group $G^{\circ}$ (Exercise 2.6) are isomorphic.

6.9. 证明群 $G$ 和它的相反群 $G^{\circ}$（练习 2.6）是同构的。

6.10. Find all automorphisms of
(a) a cyclic group of order 10,
(b) the symmetric group $S_3$ .

6.10. 找出以下所有自同构：
(a) 一个 10 阶循环群，
(b) 对称群 $S_3$。

6.11. Let $a$ be an element of a group $G$ . Prove that if the set $\{1, a\}$ is a normal subgroup of $G$ , then $a$ is in the center of $G$ .

6.11. 设 $a$ 是群 $G$ 中的一个元素。证明如果集合 $\{1, a\}$ 是 $G$ 的一个正规子群，那么 $a$ 在 $G$ 的中心中。

## Section 7 Equivalence Relations and Partitions

## 第7节 等价关系和划分

7.1. Let $G$ be a group. Prove that the relation $a \sim b$ if $b = gag^{-1}$ for some $g$ in $G$ is an equivalence relation on $G$ .

7.1. 设 $G$ 是一个群。证明如果对于某个 $g$ 在 $G$ 中，$b = gag^{-1}$，则关系 $a \sim b$ 是 $G$ 上的一个等价关系。

7.2. An equivalence relation on $S$ is determined by the subset $R$ of the set $S \times S$ consisting of those pairs $(a, b)$ such that $a \sim b$ . Write the axioms for an equivalence relation in terms of the subset $R$ .

7.2. $S$ 上的一个等价关系由集合 $S \times S$ 的子集 $R$ 决定，该子集由满足 $a \sim b$ 的那些对 $(a, b)$ 组成。用子集 $R$ 来写出等价关系的公理。

7.3. With the notation of Exercise 7.2, is the intersection $R \cap R'$ of two equivalence relations $R$ and $R'$ an equivalence relation? Is the union?

7.3. 使用练习 7.2 的记号，两个等价关系 $R$ 和 $R'$ 的交集 $R \cap R'$ 是一个等价关系吗？并集呢？

7.4. A relation $R$ on the set of real numbers can be thought of as a subset of the $(x, y)$ -plane. With the notation of Exercise 7.2, explain the geometric meaning of the reflexive and symmetric properties.

7.4. 实数集上的关系 $R$ 可以被视为 $(x, y)$-平面的一个子集。使用练习 7.2 的记号，解释自反性和对称性的几何意义。

7.5. With the notation of Exercise 7.2, each of the following subsets $R$ of the $(x, y)$ -plane defines a relation on the set $\mathbb{R}$ of real numbers. Determine which of the axioms (2.7.3) are satisfied: (a) the set $\{(s, s) \mid s \in \mathbb{R}\}$ , (b) the empty set, (c) the locus $\{xy + 1 = 0\}$ , (d) the locus $\{x^2 y - xy^2 - x + y = 0\}$ .

7.5. 使用练习 7.2 的记号，$(x, y)$-平面的以下每个子集 $R$ 定义了实数集 $\mathbb{R}$ 上的一个关系。确定满足 (2.7.3) 中的哪些公理：(a) 集合 $\{(s, s) \mid s \in \mathbb{R}\}$，(b) 空集，(c) 轨迹 $\{xy + 1 = 0\}$，(d) 轨迹 $\{x^2 y - xy^2 - x + y = 0\}$。

7.6. How many different equivalence relations can be defined on a set of five elements?

7.6. 在五个元素的集合上可以定义多少种不同的等价关系？

## Section 8 Cosets

## 第8节 陪集

8.1. Let $H$ be the cyclic subgroup of the alternating group $A_4$ generated by the permutation (123). Exhibit the left and the right cosets of $H$ explicitly.

8.1. 设 $H$ 是由置换 (123) 生成的交错群 $A_4$ 的循环子群。明确写出 $H$ 的左陪集和右陪集。

8.2. In the additive group $\mathbb{R}^m$ of vectors, let $W$ be the set of solutions of a system of homogeneous linear equations $AX = 0$ . Show that the set of solutions of an inhomogeneous system $AX = B$ is either empty, or else it is an (additive) coset of $W$ .

8.2. 在向量的加法群 $\mathbb{R}^m$ 中，设 $W$ 是齐次线性方程组 $AX = 0$ 的解集。证明非齐次方程组 $AX = B$ 的解集要么为空，要么是 $W$ 的一个（加法）陪集。

8.3. Does every group whose order is a power of a prime $p$ contain an element of order $p$ ?

8.3. 每个阶是素数 $p$ 的幂的群都包含一个 $p$ 阶元素吗？

8.4. Does a group of order 35 contain an element of order 5? of order 7?

8.4. 一个 35 阶的群包含一个 5 阶元素吗？包含一个 7 阶元素吗？

8.5. A finite group contains an element $x$ of order 10 and also an element $y$ of order 6. What can be said about the order of $G$ ?

8.5. 一个有限群包含一个 10 阶元素 $x$ 和一个 6 阶元素 $y$。关于 $G$ 的阶可以说什么？

8.6. Let $\phi : G \to G'$ be a group homomorphism. Suppose that $|G| = 18$ , $|G'| = 15$ , and that $\phi$ is not the trivial homomorphism. What is the order of the kernel?

8.6. 设 $\phi : G \to G'$ 是一个群同态。假设 $|G| = 18$，$|G'| = 15$，且 $\phi$ 不是平凡同态。核的阶是多少？

===== Page 73 =====

8.7. A group $G$ of order 22 contains elements $x$ and $y$ , where $x \neq 1$ and $y$ is not a power of $x$ . Prove that the subgroup generated by these elements is the whole group $G$ .

8.7. 一个 22 阶的群 $G$ 包含元素 $x$ 和 $y$，其中 $x \neq 1$，且 $y$ 不是 $x$ 的幂。证明由这些元素生成的子群是整个群 $G$。

8.8. Let $G$ be a group of order 25. Prove that $G$ has at least one subgroup of order 5, and that if it contains only one subgroup of order 5, then it is a cyclic group.

8.8. 设 $G$ 是一个 25 阶的群。证明 $G$ 至少有一个 5 阶子群，并且如果它只包含一个 5 阶子群，那么它是一个循环群。

8.9. Let $G$ be a finite group. Under what circumstances is the map $\phi :G\to G$ defined by $\phi (x) = x^{2}$ an automorphism of $G?$

8.9. 设 $G$ 是一个有限群。在什么情况下由 $\phi (x) = x^{2}$ 定义的映射 $\phi :G\to G$ 是 $G$ 的一个自同构？

8.10. Prove that every subgroup of index 2 is a normal subgroup, and show by example that a subgroup of index 3 need not be normal.

8.10. 证明每个指数为 2 的子群都是正规子群，并举例说明指数为 3 的子群不一定是正规的。

8.11. Let $G$ and $H$ be the following subgroups of $G L_{2}(\mathbb{R})$ :

8.11. 设 $G$ 和 $H$ 是 $G L_{2}(\mathbb{R})$ 的以下子群：
$$G = \left\{ \begin{bmatrix} x & y \\ 0 & 1 \end{bmatrix} \right\}, \quad H = \left\{ \begin{bmatrix} 1 & n \\ 0 & 1 \end{bmatrix} \right\}$$
with $x$ and $y$ real and $x > 0$ . An element of $G$ can be represented by a point in the right half plane. Make sketches showing the partitions of the half plane into left cosets and into right cosets of $H$ .

其中 $x$ 和 $y$ 是实数且 $x > 0$。$G$ 的一个元素可以用右半平面中的一个点表示。画出草图，展示半平面被划分为 $H$ 的左陪集和右陪集的情况。

8.12. Let $S$ be a subset of a group $G$ that contains the identity element 1, and such that the left cosets $aS$ , with $a$ in $G$ , partition $G$ . Prove that $S$ is a subgroup of $G$ .

8.12. 设 $S$ 是群 $G$ 的一个子集，它包含单位元 1，并且使得左陪集 $aS$（其中 $a$ 在 $G$ 中）划分了 $G$。证明 $S$ 是 $G$ 的一个子群。

8.13. Let $S$ be a set with a law of composition. A partition $\Pi_{1} \cup \Pi_{2} \cup \dots$ of $S$ is compatible with the law of composition if for all $i$ and $j$ , the product set
$$\Pi_{i}\Pi_{j} = \{x y\mid x\in \Pi_{i},y\in \Pi_{j}\}$$
is contained in a single subset $\Pi_{k}$ of the partition.
(a) The set $\mathbb{Z}$ of integers can be partitioned into the three sets [Pos], [Neg], [(0)]. Discuss the extent to which the laws of composition $+$ and $\times$ are compatible with this partition.
(b) Describe all partitions of the integers that are compatible with the operation $+$ .

8.13. 设 $S$ 是一个具有合成律的集合。如果对于所有 $i$ 和 $j$，乘积集
$$\Pi_{i}\Pi_{j} = \{x y\mid x\in \Pi_{i},y\in \Pi_{j}\}$$
包含在划分的单个子集 $\Pi_{k}$ 中，则称 $S$ 的划分 $\Pi_{1} \cup \Pi_{2} \cup \dots$ 与合成律**兼容**。
(a) 整数集 $\mathbb{Z}$ 可以划分为三个集合 [正]、[负]、[0]。讨论合成律 $+$ 和 $\times$ 与这个划分的兼容程度。
(b) 描述所有与运算 $+$ 兼容的整数划分。

## Section 9 Modular Arithmetic

## 第9节 模算术

9.1. For which integers $n$ does 2 have a multiplicative inverse in $\mathbb{Z} / \mathbb{Z} n$ ?

9.1. 对于哪些整数 $n$，2 在 $\mathbb{Z} / \mathbb{Z} n$ 中有乘法逆元？

9.2. What are the possible values of $a^{2}$ modulo 4? modulo 8?

9.2. $a^{2}$ 模 4 的可能值是什么？模 8 呢？

9.3. Prove that every integer $a$ is congruent to the sum of its decimal digits modulo 9.

9.3. 证明每个整数 $a$ 模 9 同余于其十进制数字之和。

9.4. Solve the congruence $2x \equiv 5$ modulo 9 and modulo 6.

9.4. 解同余式 $2x \equiv 5$ 模 9 和模 6。

9.5. Determine the integers $n$ for which the pair of congruences $2x - y \equiv 1$ and $4x + 3y \equiv 2$ modulo $n$ has a solution.

9.5. 确定整数 $n$，使得同余式组 $2x - y \equiv 1$ 和 $4x + 3y \equiv 2$ 模 $n$ 有解。

9.6. Prove the Chinese Remainder Theorem: Let $a, b, u, v$ be integers, and assume that the greatest common divisor of $a$ and $b$ is 1. Then there is an integer $x$ such that $x \equiv u$ modulo $a$ and $x \equiv v$ modulo $b$ .
Hint: Do the case $u = 0$ and $v = 1$ first.

9.6. 证明中国剩余定理：设 $a, b, u, v$ 是整数，并假设 $a$ 和 $b$ 的最大公因数为 1。那么存在整数 $x$ 使得 $x \equiv u$ 模 $a$ 且 $x \equiv v$ 模 $b$。
提示：先处理 $u = 0$ 和 $v = 1$ 的情况。

9.7. Determine the order of each of the matrices $A = \left[ \begin{array}{cc}1 & 1 \\ 0 & 1 \end{array} \right]$ and $B = \left[ \begin{array}{cc}1 & 1 \\ 1 & 0 \end{array} \right]$ when the matrix entries are interpreted modulo 3.

9.7. 当矩阵元素解释为模 3 时，确定矩阵 $A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$ 和 $B = \begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix}$ 的阶。

===== Page 74 =====

## Section 10 The Correspondence Theorem

## 第10节 对应定理

10.1. Describe how to tell from the cycle decomposition whether a permutation is odd or even.

10.1. 描述如何从循环分解判断一个置换是奇置换还是偶置换。

10.2. Let $H$ and $K$ be subgroups of a group $G$
(a) Prove that the intersection $xH\cap yK$ of two cosets of $H$ and $K$ is either empty or else is a coset of the subgroup $H\cap K$ .
(b) Prove that if $H$ and $K$ have finite index in $G$ then $H\cap K$ also has finite index in $G$ .

10.2. 设 $H$ 和 $K$ 是群 $G$ 的子群。
(a) 证明 $H$ 和 $K$ 的两个陪集 $xH\cap yK$ 的交要么为空，要么是子群 $H\cap K$ 的一个陪集。
(b) 证明如果 $H$ 和 $K$ 在 $G$ 中有有限指数，那么 $H\cap K$ 在 $G$ 中也有有限指数。

10.3. Let $G$ and $G^{\prime}$ be cyclic groups of orders 12 and 6, generated by elements $x$ and $y$ respectively, and let $\phi :G\to G^{\prime}$ be the map defined by $\phi (x^{i}) = y^{i}$ . Exhibit the correspondence referred to in the Correspondence Theorem explicitly.

10.3. 设 $G$ 和 $G^{\prime}$ 分别是 12 阶和 6 阶循环群，分别由元素 $x$ 和 $y$ 生成，并设 $\phi :G\to G^{\prime}$ 是由 $\phi (x^{i}) = y^{i}$ 定义的映射。明确展示对应定理中提到的对应关系。

10.4. With the notation of the Correspondence Theorem, let $H$ and $H^{\prime}$ be corresponding subgroups. Prove that $[G:H] = [G^{\prime}:H^{\prime}]$ .

10.4. 使用对应定理的记号，设 $H$ 和 $H^{\prime}$ 是相互对应的子群。证明 $[G:H] = [G^{\prime}:H^{\prime}]$。

10.5. With reference to the homomorphism $S_{4}\to S_{3}$ described in Example 2.5.13, determine the six subgroups of $S_{4}$ that contain $K$ .

10.5. 参考例 2.5.13 中描述的同态 $S_{4}\to S_{3}$，确定 $S_{4}$ 中包含 $K$ 的六个子群。

## Section 11 Product Groups

## 第11节 乘积群

11.1. Let $x$ be an element of order $r$ of a group $G$ and let $y$ be an element of $G^{\prime}$ of order $s$ . What is the order of $(x,y)$ in the product group $G\times G^{\prime}$ ?

11.1. 设 $x$ 是群 $G$ 中一个阶为 $r$ 的元素，$y$ 是 $G^{\prime}$ 中一个阶为 $s$ 的元素。$(x,y)$ 在乘积群 $G\times G^{\prime}$ 中的阶是多少？

11.2. What does Proposition 2.11.4 tell us when, with the usual notation for the symmetric group $S_{3}$ , $K$ and $H$ are the subgroups $\langle y\rangle$ and $\langle x\rangle$ ?

11.2. 当使用对称群 $S_{3}$ 的通常记号，$K$ 和 $H$ 是子群 $\langle y\rangle$ 和 $\langle x\rangle$ 时，命题 2.11.4 告诉我们什么？

11.3. Prove that the product of two infinite cyclic groups is not infinite cyclic.

11.3. 证明两个无限循环群的乘积不是无限循环的。

11.4. In each of the following cases, determine whether or not $G$ is isomorphic to the product group $H\times K$ .
(a) $G = \mathbb{R}^{\times},H = \{\pm 1\} ,K =$ positive real numbers).
(b) $G =$ (invertible upper triangular $2\times 2$ matrices), $H =$ invertible diagonal matrices), $K =$ (upper triangular matrices with diagonal entries 1).
(c) $G = \mathbb{C}^{\times},H =$ unit circle), $K =$ positive real numbers).

11.4. 在以下每种情况下，判断 $G$ 是否同构于乘积群 $H\times K$。
(a) $G = \mathbb{R}^{\times}$，$H = \{\pm 1\}$，$K =$ 正实数。
(b) $G =$ 可逆上三角 $2\times 2$ 矩阵，$H =$ 可逆对角矩阵，$K =$ 对角元为 1 的上三角矩阵。
(c) $G = \mathbb{C}^{\times}$，$H =$ 单位圆，$K =$ 正实数。

11.5. Let $G_{1}$ and $G_{2}$ be groups, and let $Z_{i}$ be the center of $G_{i}$ . Prove that the center of the product group $G_{1}\times G_{2}$ is $Z_{1}\times Z_{2}$ .

11.5. 设 $G_{1}$ 和 $G_{2}$ 是群，$Z_{i}$ 是 $G_{i}$ 的中心。证明乘积群 $G_{1}\times G_{2}$ 的中心是 $Z_{1}\times Z_{2}$。

11.6. Let $G$ be a group that contains normal subgroups of orders 3 and 5, respectively. Prove that $G$ contains an element of order 15.

11.6. 设 $G$ 是一个群，它分别包含阶为 3 和 5 的正规子群。证明 $G$ 包含一个 15 阶元素。

11.7. Let $H$ be a subgroup of a group $G$ , let $\phi :G\to H$ be a homomorphism whose restriction to $H$ is the identity map, and let $N$ be its kernel. What can one say about the product map $H\times N\to G$ ?

11.7. 设 $H$ 是群 $G$ 的一个子群，$\phi :G\to H$ 是一个限制到 $H$ 上是恒等映射的同态，$N$ 是其核。关于乘积映射 $H\times N\to G$ 能说什么？

11.8. Let $G,G^{\prime}$ and $H$ be groups. Establish a bijective correspondence between homomorphisms $\Phi :H\to G\times G^{\prime}$ from $H$ to the product group and pairs $(\phi ,\phi^{\prime})$ consisting of a homomorphism $\phi :H\to G$ and a homomorphism $\phi^{\prime}:H\to G^{\prime}$ .

11.8. 设 $G,G^{\prime}$ 和 $H$ 是群。建立从 $H$ 到乘积群 $G\times G^{\prime}$ 的同态 $\Phi :H\to G\times G^{\prime}$ 与由一个同态 $\phi :H\to G$ 和一个同态 $\phi^{\prime}:H\to G^{\prime}$ 组成的对 $(\phi ,\phi^{\prime})$ 之间的双射对应。

11.9. Let $H$ and $K$ be subgroups of a group $G$ . Prove that the product set $HK$ is a subgroup of $G$ if and only if $HK = KH$ .

11.9. 设 $H$ 和 $K$ 是群 $G$ 的子群。证明乘积集 $HK$ 是 $G$ 的一个子群当且仅当 $HK = KH$。

## Section 12 Quotient Groups

## 第12节 商群

12.1. Show that if a subgroup $H$ of a group $G$ is not normal, there are left cosets $aH$ and $bH$ whose product is not a coset.

12.1. 证明如果群 $G$ 的一个子群 $H$ 不是正规的，则存在左陪集 $aH$ 和 $bH$，它们的乘积不是一个陪集。

===== Page 75 =====

12.2. In the general linear group $GL_3(\mathbb{R})$ , consider the subsets
$$H = \left\{ \begin{bmatrix} 1 & * & * \\ 0 & 1 & * \\ 0 & 0 & 1 \end{bmatrix} \right\}, \quad K = \left\{ \begin{bmatrix} 1 & 0 & * \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \right\}$$
where $*$ represents an arbitrary real number. Show that $H$ is a subgroup of $GL_3$ ,that $K$ is a normal subgroup of $H$ ,and identify the quotient group $H / K$ Determine the center of $H$

12.2. 在一般线性群 $GL_3(\mathbb{R})$ 中，考虑子集
$$H = \left\{ \begin{bmatrix} 1 & * & * \\ 0 & 1 & * \\ 0 & 0 & 1 \end{bmatrix} \right\}, \quad K = \left\{ \begin{bmatrix} 1 & 0 & * \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \right\}$$
其中 $*$ 代表任意实数。证明 $H$ 是 $GL_3$ 的一个子群，$K$ 是 $H$ 的一个正规子群，并识别商群 $H / K$。确定 $H$ 的中心。

12.3. Let $P$ be a partition of a group $G$ with the property that for any pair of elements $A$ $B$ of the partition, the product set $A B$ is contained entirely within another element $C$ of the partition. Let $N$ be the element of $P$ that contains 1. Prove that $N$ is a normal subgroup of $G$ and that $P$ is the set of its cosets.

12.3. 设 $P$ 是群 $G$ 的一个划分，其性质是：对于划分的任意一对元素 $A$ 和 $B$，乘积集 $A B$ 完全包含在划分的另一个元素 $C$ 中。设 $N$ 是 $P$ 中包含 1 的元素。证明 $N$ 是 $G$ 的一个正规子群，并且 $P$ 是其陪集的集合。

12.4. Let $H = \{\pm 1,\pm i\}$ be the subgroup of $G = \mathbb{C}^{\times}$ of fourth roots of unity. Describe the cosets of $H$ in $G$ explicitly. Is $G / H$ isomorphic to $G$ ?

12.4. 设 $H = \{\pm 1,\pm i\}$ 是 $G = \mathbb{C}^{\times}$ 的 4 次单位根子群。明确描述 $H$ 在 $G$ 中的陪集。$G / H$ 同构于 $G$ 吗？

12.5. Let $G$ be the group of upper triangular real matrices $\left[ \begin{array}{cc}a & b\\ 0 & d \end{array} \right]$ , with $a$ and $d$ different from zero. For each of the following subsets, determine whether or not $S$ is a subgroup, and whether or not $S$ is a normal subgroup. If $S$ is a normal subgroup, identify the quotient group $G / S$ .
(i) $S$ is the subset defined by $b = 0$
(ii) $S$ is the subset defined by $d = 1$
(iii) $S$ is the subset defined by $a = d$ .

12.5. 设 $G$ 是上三角实矩阵 $\begin{bmatrix} a & b \\ 0 & d \end{bmatrix}$ 的群，其中 $a$ 和 $d$ 不为零。对于以下每个子集，判断 $S$ 是否是一个子群，以及 $S$ 是否是一个正规子群。如果 $S$ 是一个正规子群，识别商群 $G / S$。
(i) $S$ 是由 $b = 0$ 定义的子集
(ii) $S$ 是由 $d = 1$ 定义的子集
(iii) $S$ 是由 $a = d$ 定义的子集

## Miscellaneous Problems

## 杂题

M.1. Describe the column vectors $(a,c)^{t}$ that occur as the first column of an integer matrix $A$ whose inverse is also an integer matrix.

M.1. 描述作为整数矩阵 $A$ 的第一列出现的列向量 $(a,c)^{t}$，其中 $A$ 的逆矩阵也是整数矩阵。

M.2. (a) Prove that every group of even order contains an element of order 2. (b) Prove that every group of order 21 contains an element of order 3.

M.2. (a) 证明每个偶数阶群包含一个 2 阶元素。(b) 证明每个 21 阶群包含一个 3 阶元素。

M.3. Classify groups of order 6 by analyzing the following three cases:
(i) $G$ contains an element of order 6.
(ii) $G$ contains an element of order 3 but none of order 6.
(iii) All elements of $G$ have order 1 or 2.

M.3. 通过分析以下三种情况来分类 6 阶群：
(i) $G$ 包含一个 6 阶元素。
(ii) $G$ 包含一个 3 阶元素但不包含 6 阶元素。
(iii) $G$ 的所有元素阶为 1 或 2。

M.4. A semigroup $S$ is a set with an associative law of composition and with an identity. Elements are not required to have inverses, and the Cancellation Law need not hold. A semigroup $S$ is said to be generated by an element $s$ if the set $\{1,s,s^{2},\ldots \}$ of nonnegative powers of $s$ is equal to $S$ . Classify semigroups that are generated by one element.

M.4. 一个**半群** $S$ 是一个具有结合合成律和单位元的集合。不要求元素有逆元，消去律不一定成立。如果 $s$ 的非负幂集 $\{1,s,s^{2},\ldots \}$ 等于 $S$，则称半群 $S$ 由元素 $s$ 生成。分类由一个元素生成的半群。

M.5. Let $S$ be a finite semigroup (see Exercise M.4) in which the Cancellation Law 2.2.3 holds. Prove that $S$ is a group.

M.5. 设 $S$ 是一个有限半群（见练习 M.4），其中消去律 2.2.3 成立。证明 $S$ 是一个群。

\*M.6. Let $a = (a_1,\ldots ,a_k)$ and $b = (b_1,\ldots ,b_k)$ be points in $k$ - dimensional space $\mathbb{R}^k$ . A path from $a$ to $b$ is a continuous function on the unit interval $[0,1]$ with values in $\mathbb{R}^k$ , a function $X:[0,1]\to \mathbb{R}^k$ , sending $t\mapsto X(t) = (x_1(t),\ldots ,x_k(t))$ , such that $X(0) = a$ and $X(1) = b$ . If $S$ is a subset of $\mathbb{R}^k$ and if $a$ and $b$ are in $S$ , define $a\sim b$ if $a$ and $b$ can be joined by a path lying entirely in $S$ .

\*M.6. 设 $a = (a_1,\ldots ,a_k)$ 和 $b = (b_1,\ldots ,b_k)$ 是 $k$ 维空间 $\mathbb{R}^k$ 中的点。从 $a$ 到 $b$ 的一条**道路**是单位区间 $[0,1]$ 上的连续函数，取值在 $\mathbb{R}^k$ 中，即函数 $X:[0,1]\to \mathbb{R}^k$，将 $t$ 映射到 $X(t) = (x_1(t),\ldots ,x_k(t))$，使得 $X(0) = a$，$X(1) = b$。如果 $S$ 是 $\mathbb{R}^k$ 的一个子集，且 $a$ 和 $b$ 在 $S$ 中，如果 $a$ 和 $b$ 可以通过一条完全位于 $S$ 内的道路连接，则定义 $a\sim b$。

===== Page 76 =====

1) Show that $\sim$ is an equivalence relation on $S$ . Be careful to check that any paths you construct stay within the set $S$ .
(b) A subset $S$ is path connected if $a\sim b$ for any two points $a$ and $b$ in $S$ . Show that every subset $S$ is partitioned into path-connected subsets with the property that two points in different subsets cannot be connected by a path in $S$ .
(c) Which of the following loci in $\mathbb{R}^{2}$ are path-connected: $\{x^{2} + y^{2} = 1\}$ $\{x y = 0\}$ $\{x y = 1\}$ ?

(a) 证明 $\sim$ 是 $S$ 上的一个等价关系。小心检查你构造的任何道路都保持在集合 $S$ 内。
(b) 如果对于 $S$ 中任意两点 $a$ 和 $b$，有 $a\sim b$，则称子集 $S$ 是**道路连通的**。证明每个子集 $S$ 被划分为道路连通子集，其性质是不同子集中的两点不能由 $S$ 中的道路连接。
(c) $\mathbb{R}^{2}$ 中的以下轨迹哪些是道路连通的：$\{x^{2} + y^{2} = 1\}$，$\{x y = 0\}$，$\{x y = 1\}$？

\*M.7. The set of $n\times n$ matrices can be identified with the space $\mathbb{R}^{n\times n}$ . Let $G$ be a subgroup of $G L_{n}(\mathbb{R})$ . With the notation of Exercise M.6, prove:
(a) If $A,B,C,D$ are in $G$ , and if there are paths in $G$ from $A$ to $B$ and from $C$ to $D$ , then there is a path in $G$ from $A C$ to $B D$ .
(b) The set of matrices that can be joined to the identity $I$ forms a normal subgroup of $G$ . (It is called the connected component of $G$ .)

\*M.7. $n\times n$ 矩阵的集合可以与空间 $\mathbb{R}^{n\times n}$ 等同。设 $G$ 是 $G L_{n}(\mathbb{R})$ 的一个子群。使用练习 M.6 的记号，证明：
(a) 如果 $A,B,C,D$ 在 $G$ 中，并且 $G$ 中存在从 $A$ 到 $B$ 和从 $C$ 到 $D$ 的道路，那么 $G$ 中存在从 $A C$ 到 $B D$ 的道路。
(b) 可以连接到单位元 $I$ 的矩阵的集合构成 $G$ 的一个正规子群。（它被称为 $G$ 的**连通分支**。）

\*M.8. (a) The group $S L_{n}(\mathbb{R})$ is generated by elementary matrices of the first type (see Exercise 4.8). Use this fact to prove that $S L_{n}(\mathbb{R})$ is path- connected.
(b) Show that $G L_{n}(\mathbb{R})$ is a union of two path-connected subsets, and describe them.

\*M.8. (a) 群 $S L_{n}(\mathbb{R})$ 由第一类初等矩阵生成（见练习 4.8）。利用这一事实证明 $S L_{n}(\mathbb{R})$ 是道路连通的。
(b) 证明 $G L_{n}(\mathbb{R})$ 是两个道路连通子集的并集，并描述它们。

M.9. (double cosets) Let $H$ and $K$ be subgroups of a group $G$ , and let $g$ be an element of $G$ . The set $H g K = \{x\in G\mid x = h g k$ for some $h\in H,k\in K\}$ is called a double coset. Do the double cosets partition $G$ ?

M.9. （双陪集）设 $H$ 和 $K$ 是群 $G$ 的子群，$g$ 是 $G$ 中的一个元素。集合 $H g K = \{x\in G\mid x = h g k$ 对于某个 $h\in H,k\in K\}$ 称为一个**双陪集**。双陪集划分 $G$ 吗？

M.10. Let $H$ be a subgroup of a group $G$ . Show that the double cosets (see Exercise M.9)
$$H g H = \{h_{1}g h_{2}|h_{1},h_{2}\in H\}$$
are the left cosets $g H$ if and only if $H$ is normal.

M.10. 设 $H$ 是群 $G$ 的一个子群。证明双陪集（见练习 M.9）
$$H g H = \{h_{1}g h_{2} \mid h_{1},h_{2}\in H\}$$
是左陪集 $g H$ 当且仅当 $H$ 是正规的。

\*M.11. Most invertible matrices can be written as a product $A = L U$ of a lower triangular matrix $L$ and an upper triangular matrix $U$ , where in addition all diagonal entries of $U$ are 1.
(a) Explain how to compute $L$ and $U$ when the matrix $A$ is given.
(b) Prove uniqueness, that there is at most one way to write $A$ as such a product.
(c) Show that every invertible matrix can be written as a product $L P U$ , where $L$ , $U$ are as above and $P$ is a permutation matrix.
(d) Describe the double cosets $L g U$ (see Exercise M.9).

\*M.11. 大多数可逆矩阵可以写成一个下三角矩阵 $L$ 和一个上三角矩阵 $U$ 的乘积 $A = L U$，此外 $U$ 的所有对角元都是 1。
(a) 解释当给定矩阵 $A$ 时，如何计算 $L$ 和 $U$。
(b) 证明唯一性，即将 $A$ 写成这种乘积的方式至多有一种。
(c) 证明每个可逆矩阵都可以写成一个乘积 $L P U$，其中 $L$、$U$ 如上所述，$P$ 是一个置换矩阵。
(d) 描述双陪集 $L g U$（见练习 M.9）。

M.12. (postage stamp problem) Let $a$ and $b$ be positive, relatively prime integers.
(a) Prove that every sufficiently large positive integer $n$ can be obtained as $r a + s b$ where $r$ and $s$ are positive integers.
(b) Determine the largest integer that is not of this form.

M.12. （邮票问题）设 $a$ 和 $b$ 是正互素整数。
(a) 证明每个足够大的正整数 $n$ 都可以表示为 $r a + s b$，其中 $r$ 和 $s$ 是正整数。
(b) 确定不能表示为这种形式的最大整数。

M.13. (a game) The starting position is the point $(1,1)$ , and a permissible "move" replaces a point $(a,b)$ by one of the points $(a + b,b)$ or $(a,a + b)$ . So the position after the first move will be either $(2,1)$ or $(1,2)$ . Determine the points that can be reached.

M.13. （一个游戏）起始位置是点 $(1,1)$，一个允许的“移动”将点 $(a,b)$ 替换为点 $(a + b,b)$ 或 $(a,a + b)$ 之一。所以第一次移动后的位置将是 $(2,1)$ 或 $(1,2)$。确定可以到达的点。

M.14. (generating $S L_{2}(\mathbb{Z})$ ) Prove that the two matrices
$$E = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}, \quad E' = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$$

M.14. （生成 $S L_{2}(\mathbb{Z})$）证明两个矩阵
$$E = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}, \quad E' = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$$

===== Page 77 =====

generate the group $SL_2(\mathbb{Z})$ of all integer matrices with determinant 1. Remember that the subgroup they generate consists of all elements that can be expressed as products using the four elements $E, E', E^{- 1}, E^{- 1}$ .
Hint: Do not try to write a matrix directly as a product of the generators. Use row reduction.

生成所有行列式为 1 的整数矩阵的群 $SL_2(\mathbb{Z})$。记住它们生成的子群由所有可以用四个元素 $E, E', E^{-1}, E'^{-1}$ 的乘积表示的元素组成。
提示：不要试图直接将一个矩阵写成生成元的乘积。使用行简化。

M.15. (the semigroup generated by elementary matrices) Determine the semigroup $S$ (see Exercise M.4) of matrices $A$ that can be written as a product, of arbitrary length, each of whose terms is one of the two matrices
$$E = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}, \quad E' = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$$
Show that every element of $S$ can be expressed as such a product in exactly one way.

M.15. （由初等矩阵生成的半群）确定矩阵 $A$ 的半群 $S$（见练习 M.4），这些矩阵可以写成任意长度的乘积，其中每一项是两个矩阵之一
$$E = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}, \quad E' = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$$
证明 $S$ 的每个元素恰好可以以一种方式表示为这样的乘积。

M.16. (the homophonic group: a mathematical diversion) By definition, English words have the same pronunciation if their phonetic spellings in the dictionary are the same. The homophonic group $\mathcal{H}$ is generated by the letters of the alphabet, subject to the following relations: English words with the same pronunciation represent equal elements of the group. Thus $be = bee$ , and since $\mathcal{H}$ is a group, we can cancel $be$ to conclude that $e = 1$ . Try to determine the group $\mathcal{H}$ .

M.16. （同音群：一个数学消遣）根据定义，如果英语单词在字典中的音标拼写相同，则它们具有相同的发音。同音群 $\mathcal{H}$ 由字母表的字母生成，受以下关系约束：具有相同发音的英语单词代表群中的相等元素。因此 $be = bee$，并且由于 $\mathcal{H}$ 是一个群，我们可以消去 $be$ 得出 $e = 1$。尝试确定群 $\mathcal{H}$。

---