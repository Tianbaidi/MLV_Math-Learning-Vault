---
tags:
  - Topology
  - Set_Theory
---
> In the previous note, we learned that continuity can be described without referring to a **metric**. By axiomatizing neighborhoods, interior, and open sets, we arrived at the structure underlying a general topological space. What remains is to define that structure directly.

Let us first recall how open sets arise from a neighborhood structure.

> [!ABSTRACT] Definition 1 (Open Sets)
> In a topological space defined via a neighborhood structure, a set $U$ is called **open** if
> $$U\in\mathcal{N}(x)\quad\text{for every }x\in U.$$

By the equivalence of neighborhood structures and interior structures, we immediately obtain the following equivalent characterization:

> [!TIP] Proposition 1 (Open Sets and Interior)
> A subset $U\subset X$ is open if and only if $\operatorname{Int}(U)=U$.

Given $(X, \mathcal{N})$, if we denote by
$$\mathcal{T} = \{U \subset X \mid U \text{ is an open set}\}$$
the family of all open sets in $(X,\mathcal{N})$, then the following properties hold:

(O1) $\emptyset \in \mathcal{T}$ and $X \in \mathcal{T}$.
(O2) If $U_1, U_2 \in \mathcal{T}$, then $U_1 \cap U_2 \in \mathcal{T}$.
(O3) If $\{U_\alpha : \alpha \in \Lambda\} \subset \mathcal{T}$, then $\bigcup_{\alpha \in \Lambda} U_\alpha \in \mathcal{T}$.

The open-set axioms are more concise than the neighborhood or interior axioms, so we may use them to define topology directly.

# The Definition of a Topology

> [!ABSTRACT] Definition 2 (Topology and Topological Space)
> Let $X$ be a set. A family $\mathcal{T}\subset\mathcal{P}(X)$ satisfying (O1), (O2), and (O3) is called a **topology** on $X$. The pair $(X,\mathcal{T})$ is called a **topological space**, and the members of $\mathcal{T}$ are called its **open sets**.

Since we have derived the open set axioms from the neighborhood axioms (NEBH), we can naturally define neighborhoods in a topological space.

> [!ABSTRACT] Definition 3 (Neighborhoods in a Topological Space)
> Let $(X,\mathcal{T})$ be a topological space, $x\in X$, and $N\subset X$. If there exists an open set $U\in\mathcal{T}$ such that
> $$x\in U\subset N,$$
> then $N$ is called a **neighborhood** of $x$.

Thus, given a topology $\mathcal{T}$, the neighborhood system of a point $x$ is
$$\mathcal{N}_{\mathcal{T}}(x)
=\{N\subset X\mid \exists U\in\mathcal{T}\text{ such that }x\in U\subset N\}.$$
This leads us to the following proposition.

> [!TIP] Proposition 2 (Topologies and Neighborhood Structures)
> Let $X$ be a set. The assignments
> $$\mathcal{T}\longmapsto\mathcal{N}_{\mathcal{T}}
> \qquad\text{and}\qquad
> \mathcal{N}\longmapsto
> \mathcal{T}_{\mathcal{N}}
> :=\{U\subset X\mid U\in\mathcal{N}(x)\text{ for every }x\in U\}$$
> establish a bijective correspondence between topologies on $X$ and neighborhood structures on $X$.

Proof.
**$\mathcal{N}_{\mathcal{T}}$ satisfies axioms $(\text{N}1)\text{--}(\text{N}4)$.**
- **$(\text{N}1)$**: If $N \in \mathcal{N}_{\mathcal{T}}(x)$, then $x \in U \subset N$ for some $U \in \mathcal{T}$, so $x \in N$.

- **$(\text{N}2)$**: If $M \supset N$ and $N \in \mathcal{N}_{\mathcal{T}}(x)$, then $x \in U \subset N \subset M$ for some $U \in \mathcal{T}$, so $M \in \mathcal{N}_{\mathcal{T}}(x)$.

- **$(\text{N}3)$**: If $N_1, N_2 \in \mathcal{N}_{\mathcal{T}}(x)$, there exist $U_1, U_2 \in \mathcal{T}$ such that $x \in U_1 \subset N_1$ and $x \in U_2 \subset N_2$. By $(\text{O}2)$, $U_1 \cap U_2 \in \mathcal{T}$, and $x \in U_1 \cap U_2 \subset N_1 \cap N_2$, so $N_1 \cap N_2 \in \mathcal{N}_{\mathcal{T}}(x)$.

- **$(\text{N}4)$**: If $N \in \mathcal{N}_{\mathcal{T}}(x)$, there exists $U \in \mathcal{T}$ with $x \in U \subset N$. Set $M = U$. Then $M \in \mathcal{N}_{\mathcal{T}}(x)$ and $M \subset N$. Moreover, for any $y \in M = U$, since $y \in U \subset N$ and $U \in \mathcal{T}$, we have $N \in \mathcal{N}_{\mathcal{T}}(y)$.

**$\mathcal{T}_{\mathcal{N}}$ satisfies axioms $(\text{O}1)\text{--}(\text{O}3)$.**
- **$(\text{O}1)$**: Vacuously, $\emptyset \in \mathcal{T}_{\mathcal{N}}$. For each $x\in X$, the family $\mathcal{N}(x)$ is nonempty; choose $N\in\mathcal{N}(x)$. Since $N\subset X$, axiom $(\mathrm{N}2)$ gives $X\in\mathcal{N}(x)$. Hence $X\in\mathcal{T}_{\mathcal{N}}$.

- **$(\text{O}2)$**: If $U_1, U_2 \in \mathcal{T}_{\mathcal{N}}$, then for any $x \in U_1 \cap U_2$, we have $U_1 \in \mathcal{N}(x)$ and $U_2 \in \mathcal{N}(x)$. By $(\text{N}3)$, $U_1 \cap U_2 \in \mathcal{N}(x)$, so $U_1 \cap U_2 \in \mathcal{T}_{\mathcal{N}}$.

- **$(\text{O}3)$**: Let $\{U_\alpha\}_{\alpha \in \Lambda} \subset \mathcal{T}_{\mathcal{N}}$ and $x \in \bigcup U_\alpha$. Then $x \in U_{\alpha_0}$ for some $\alpha_0$. Since $U_{\alpha_0} \in \mathcal{T}_{\mathcal{N}}$, $U_{\alpha_0} \in \mathcal{N}(x)$. By $(\text{N}2)$, since $\bigcup U_\alpha \supset U_{\alpha_0}$, we have $\bigcup U_\alpha \in \mathcal{N}(x)$. Thus $\bigcup U_\alpha \in \mathcal{T}_{\mathcal{N}}$.

**Bijective Correspondence.**
- **$\mathcal{T}_{\mathcal{N}_{\mathcal{T}}} = \mathcal{T}$**: If $U\in\mathcal{T}$, then $U\in\mathcal{N}_{\mathcal{T}}(x)$ for every $x\in U$, so $U\in\mathcal{T}_{\mathcal{N}_{\mathcal{T}}}$. Conversely, if $U\in\mathcal{T}_{\mathcal{N}_{\mathcal{T}}}$, then for every $x\in U$ there exists $V_x\in\mathcal{T}$ with $x\in V_x\subset U$. Hence
  $$U=\bigcup_{x\in U}V_x\in\mathcal{T}.$$

- **$\mathcal{N}_{\mathcal{T}_{\mathcal{N}}} = \mathcal{N}$**: If $N\in\mathcal{N}_{\mathcal{T}_{\mathcal{N}}}(x)$, then some $U\in\mathcal{T}_{\mathcal{N}}$ satisfies $x\in U\subset N$. Thus $U\in\mathcal{N}(x)$, and $(\mathrm{N}2)$ gives $N\in\mathcal{N}(x)$. Conversely, suppose $N\in\mathcal{N}(x)$ and set
  $$U:=\{y\in X\mid N\in\mathcal{N}(y)\}.$$
  Axiom $(\mathrm{N}4)$ gives $x\in U$, while another application of $(\mathrm{N}4)$ shows that $U\in\mathcal{N}(y)$ for every $y\in U$. Hence $U\in\mathcal{T}_{\mathcal{N}}$ and $x\in U\subset N$, so $N\in\mathcal{N}_{\mathcal{T}_{\mathcal{N}}}(x)$. $\square$

Now that open sets can be defined via a topology, can closed sets be defined analogously?

> [!ABSTRACT] Definition 4 (Closed Sets)
> A subset $F$ of a topological space $(X,\mathcal{T})$ is called **closed** if its complement
> $$F^c=X\setminus F$$
> is open.

By De Morgan's laws and the open-set axioms, closed sets satisfy:

(C1) $\emptyset$ and $X$ are both closed sets.
(C2) If $F_1, F_2$ are closed sets, then $F_1 \cup F_2$ is also a closed set.
(C3) If $F_\alpha$ is a closed set for every $\alpha \in \Lambda$, then $\bigcap_{\alpha \in \Lambda} F_\alpha$ is also a closed set.

In some arguments, this closed-set formulation is more convenient than the open-set formulation.

## Some Examples of Topologies

> [!Example] Example 1 (A Finite Topology and a Non-Example)
> Let $X=\{a,b,c\}$. Then
> $$\mathcal{T}=\{\varnothing,\{a\},\{a,b\},X\}$$
> is a topology on $X$. In contrast,
> $$\mathcal{S}=\{\varnothing,\{a\},\{b\},X\}$$
> is not a topology, because $\{a\}\cup\{b\}=\{a,b\}\notin\mathcal{S}$.

- **(Metric Topology)** Let $(X, d)$ be any metric space. Set
$$\mathcal{T}_{\text{metric}} = \{U \subset X \mid \forall x \in U, \, \exists r > 0 \text{ such that } B(x, r) \subset U\}.$$
Then $\mathcal{T}_{\text{metric}}$ is a topology on $X$, called the **metric topology**.
- **(Discrete Topology)** Let $X$ be any set. Set
$$\mathcal{T}_{\text{discrete}} = \mathcal{P}(X) = \{A \mid A \subset X\}.$$
This is a topology on $X$, and it is precisely the metric topology induced by the discrete metric.
- **(Trivial Topology)** Let $X$ be any set. Set
$$\mathcal{T}_{\text{trivial}} = \{\emptyset, X\}.$$
It is easy to see that this is a topology on $X$. However, as long as $X$ contains more than one element, it is not a metric topology. It is also known as the **indiscrete topology**.
- **(Cofinite Topology)** Let $X$ be any set. Set
$$\mathcal{T}_{\text{cofinite}} = \{A \subset X \mid A = \varnothing \text{ or } X \setminus A \text{ is finite}\}.$$
	This is a topology on $X$, verified as follows:
	-  $\emptyset \in \mathcal{T}$; $X \in \mathcal{T}$ because $X^c = \emptyset$, which is finite.

	- If $A, B \in \mathcal{T}$ with $A, B \neq \emptyset$, then $A^c$ and $B^c$ are finite, so $(A \cap B)^c = A^c \cup B^c$ is finite.

	- If $A_\alpha \in \mathcal{T}$ and at least one $A_{\alpha_1} \neq \emptyset$, then $(\bigcup_\alpha A_\alpha)^c = \bigcap_\alpha A_\alpha^c \subset A_{\alpha_1}^c$, which is finite.

- **(Cocountable Topology)** Let $X$ be any set. Set
$$\mathcal{T}_{\text{cocountable}} = \{A \subset X \mid A = \varnothing \text{ or } X\setminus A \text{ is at most countable}\}.$$
This is a topology on $X$; its verification is included in Question 1.
- **(Zariski Topology)** Let $X = \mathbb{C}^n$ and $R = \mathbb{C}[z_1, \dots, z_n]$, i.e., the polynomial ring in $n$ variables over the complex numbers. Define

For any family $S\subset R$, write
$$V(S)=\{x\in\mathbb{C}^n\mid f(x)=0\text{ for every }f\in S\}.$$
The **Zariski topology** is defined by declaring the sets $V(S)$ to be closed; equivalently,
$$\mathcal{T}_{\text{Zariski}}
=\{\mathbb{C}^n\setminus V(S)\mid S\subset R\}.$$

Because $R$ is Noetherian, every set $V(S)$ is already the common zero locus of finitely many polynomials. More generally, the Zariski topology is defined on the spectrum of any commutative ring and is fundamental in algebraic geometry.
- **(Sorgenfrey Topology)** Let $X = \mathbb{R}$, and define

$$\mathcal{T}_{\text{Sorgenfrey}} = \{U \subset \mathbb{R} \mid \forall x \in U, \, \exists \varepsilon > 0 \text{ such that } [x, x + \varepsilon) \subset U\}.$$

It can be verified that this is a topology. This topology will serve as an important counterexample for understanding the relationships among various topological properties.

> [!Question] Question 1 (Verifying Topology Axioms)
> Show that the cocountable, Zariski, and Sorgenfrey topologies defined above satisfy (O1)–(O3).


## Comparison of Different Topologies

When comparing two topologies on the same set, we often compare their relative **coarseness** or **fineness**.

> [!ABSTRACT] Definition 5 (Comparison of Topologies)
> Let $\mathcal{T}_1$ and $\mathcal{T}_2$ be two topologies on $X$. We say that $\mathcal{T}_1$ is **coarser than** $\mathcal{T}_2$, or equivalently, that $\mathcal{T}_2$ is **finer than** $\mathcal{T}_1$, if
> $$\mathcal{T}_1 \subset \mathcal{T}_2.$$

> [!Warning] Remark 1 (Extremal and Incomparable Topologies)
> On any set $X$, $\mathcal{T}_{\text{trivial}}$ is the coarsest topology, while $\mathcal{T}_{\text{discrete}}$ is the finest. Two topologies need not be comparable. For example, on $X=\{a,b,c\}$,
> $$\mathcal{T}_1=\{\varnothing,\{a\},X\},
> \qquad
> \mathcal{T}_2=\{\varnothing,\{b\},X\}$$
> are topologies, but neither contains the other.

In general, two different topologies on the same set need not be comparable. Nevertheless, we have the following result:

> [!TIP] Proposition 3 (Intersection of Topologies)
> Given any family of topologies $\{\mathcal{T}_\alpha\}_{\alpha \in \Lambda}$ on $X$, the intersection
> $$\bigcap_{\alpha \in \Lambda} \mathcal{T}_\alpha$$
> is also a topology on $X$.

Proof.

- Since $\emptyset, X \in \mathcal{T}_\alpha$ for all $\alpha$, we have $\emptyset, X \in \bigcap_\alpha \mathcal{T}_\alpha$.
- If $U_1, U_2 \in \bigcap_\alpha \mathcal{T}_\alpha$, then $U_1, U_2 \in \mathcal{T}_\alpha$ for all $\alpha$. Thus $U_1 \cap U_2 \in \mathcal{T}_\alpha$ for all $\alpha$, which implies $U_1 \cap U_2 \in \bigcap_\alpha \mathcal{T}_\alpha$.
- If $U_\beta \in \bigcap_\alpha \mathcal{T}_\alpha$ for all $\beta$, then $U_\beta \in \mathcal{T}_\alpha$ for all $\beta$ and all $\alpha$. Thus $\bigcup_\beta U_\beta \in \mathcal{T}_\alpha$ for all $\alpha$, which implies $\bigcup_\beta U_\beta \in \bigcap_\alpha \mathcal{T}_\alpha$.           $\square$

## Constructing New Spaces from Existing Topological Spaces
The most common constructions are the subspace topology, obtained by inheriting the topology of the ambient space on a subset, and the product topology, defined on the product space through an appropriate method.

> [!TIP] Proposition 4 (Subspace Topology)
> Let $(X, \mathcal{T})$ be a topological space and let $Y \subset X$ be a subset. Then the family of sets
> $$\mathcal{T}_Y := \{U \cap Y \mid U \in \mathcal{T}\}$$
> is a topology on $Y$, called the **subspace topology**.

For example, if $Y=[0,1]\subset\mathbb{R}$ has the subspace topology, then $[0,\tfrac12)$ is open in $Y$ because
$$[0,\tfrac12)=(-1,\tfrac12)\cap Y,$$
even though it is not open in $\mathbb{R}$.

> [!TIP] Proposition 5 (Product Topology)
> Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces. Then
> $$\mathcal{T}_{X \times Y} := \{W \subset X \times Y \mid \forall (x, y) \in W, \, \exists U \in \mathcal{T}_X \text{ and } V \in \mathcal{T}_Y \text{ such that } (x, y) \in U \times V \subset W\}$$
> is a topology on $X \times Y$, called the **product topology**.

> [!Question] Question 2 (The Product Topology)
> Verify that the product topology as defined above satisfies the open set axioms (O1)–(O3).

# Properties of Topology
As in many courses, once the definitions are established, we turn to studying properties. The main topics we investigate are the properties of convergence and continuity. Moreover, we will introduce open mappings, closed mappings, and homeomorphisms.
## Convergence in Topological Spaces
It is natural to define the convergence of sequences of points in a topological space.
### Convergence of Point Sequences

The notation $x_n\to x_0$ means that the sequence eventually enters, and thereafter remains in, every neighborhood of $x_0$.

> [!ABSTRACT] Definition 6 (Convergence of a Sequence)
> Let $(x_n)$ be a sequence in a topological space $(X,\mathcal{T})$ and let $x_0\in X$. We say that $(x_n)$ **converges to** $x_0$, and write $x_n\to x_0$, if for every neighborhood $A$ of $x_0$ there exists $k\in\mathbb{N}$ such that
> $$n\ge k\quad\Longrightarrow\quad x_n\in A.$$

Here are some examples:

> [!Example] Example 2 (Convergence in a Metric Topology)
> Consider a metric space $(X, d)$. We have defined two notions of sequence convergence: convergence with respect to the metric, and convergence with respect to the metric topology. It is easy to verify that these two notions coincide; that is, $x_n$ converges to $x_0$ in the metric topology if and only if
> $$\forall \varepsilon > 0, \, \exists k > 0 \text{ such that } d(x_n, x_0) < \varepsilon \text{ for all } n > k.$$

> [!Example] Example 3 (Convergence in the Discrete Topology)
> Consider the discrete topological space $(X, \mathcal{T}_{\text{discrete}})$. Since $\{x_0\}$ is an open neighborhood of $x_0$, we have $x_n \to x_0$ if and only if
> $$\exists k > 0 \text{ such that } x_n = x_0 \text{ for all } n > k.$$
> In other words, in a discrete topological space, only "eventually constant" sequences converge.

> [!Example] Example 4 (Convergence in the Indiscrete Topology)
> Consider the indiscrete topological space $(X, \mathcal{T}_{\text{trivial}})$. Since the only nonempty open set is $X$, every sequence in $X$ converges to every point of $X$. In particular, limits need not be unique.

> [!Warning] Remark 2 (Uniqueness of Limits)
> The nonuniqueness above is not a defect in the definition: it records how little the indiscrete topology can distinguish points. Later, the Hausdorff separation axiom will guarantee that a convergent sequence has at most one limit.

> [!Example] Example 5 (Convergence in the Cofinite Topology)
> In a cofinite topological space,
> $$x_n\to x_0
> \quad\Longleftrightarrow\quad
> \{n\in\mathbb{N}\mid x_n=x\}\text{ is finite for every }x\ne x_0.$$
> Indeed, a neighborhood of $x_0$ may exclude only finitely many points, so the sequence must eventually avoid any prescribed finite subset of $X\setminus\{x_0\}$. Consequently:
> - If the $x_n$ are all distinct, then the sequence $x_1, x_2, \dots$ converges to every point $x_0 \in X$.
>
> - A sequence of the form $x_0, x_1, x_0, x_2, x_0, \dots$ (where $x_1, x_2, \dots$ are distinct points different from $x_0$) has $x_0$ as its unique limit.
>
> - A sequence of the form $x_1, x_2, x_1, x_2, \dots$ (with $x_1 \neq x_2$) does not converge to any point.

> [!Example] Example 6 (Convergence in the Cocountable Topology)
> Let $X$ be uncountable and give it the cocountable topology. Then $x_n \to x_0$ if and only if
> $$\exists k > 0 \text{ such that } x_n = x_0 \text{ for all } n > k.$$
> To see the nontrivial direction, suppose that $(x_n)$ is not eventually equal to $x_0$. The set
> $$C=\{x_n\mid x_n\ne x_0\}$$
> is at most countable, so $X\setminus C$ is an open neighborhood of $x_0$ that the sequence fails to enter permanently.

### Pointwise Convergence Topology
Consider the set of all real-valued functions on $[0,1]$:
$$X=\mathbb{R}^{[0,1]}.$$
Pointwise convergence means
$$f_n\to f
\quad\Longleftrightarrow\quad
f_n(x)\to f(x)\text{ for every }x\in[0,1].$$

> [!ABSTRACT] Definition 7 (Topology of Pointwise Convergence)
> For $f\in X$, points $x_1,\dots,x_m\in[0,1]$, and $\varepsilon>0$, define
> $$\omega(f;x_1,\dots,x_m;\varepsilon)
> :=\{g\in X\mid |g(x_i)-f(x_i)|<\varepsilon
> \text{ for }1\le i\le m\}.$$
> A set $U\subset X$ is declared open if, for every $f\in U$, there exist finitely many points $x_1,\dots,x_m$ and some $\varepsilon>0$ such that
> $$f\in\omega(f;x_1,\dots,x_m;\varepsilon)\subset U.$$
> The resulting family of open sets is denoted by $\mathcal{T}_{\mathrm{p.c.}}$ and is called the **topology of pointwise convergence**.

The neighborhood $\omega(f;x_1,\dots,x_m;\varepsilon)$ controls a function at only finitely many points. It does not require the function to remain uniformly close to $f$ between those points.

```tikz
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}

\begin{document}
  \begin{tikzpicture}[scale=1.2]
    % 1. 顶部标题
    \node at (3.0, 3.8) {\large $\omega(f_0; x_1, x_2, x_3; \varepsilon)$};

    % 2. 坐标轴
    \draw[thick] (-0.3, 0) -- (6.3, 0);
    \draw[->, thick] (0, -0.2) -- (0, 4.0);

    % 3. 刻度与标记
    \draw[thick] (0, -0.08) -- (0, 0.08) node[below left] {$0$};
    \draw[thick] (1.5, -0.08) -- (1.5, 0.08) node[below=2pt] {$x_1$};
    \draw[thick] (3.0, -0.08) -- (3.0, 0.08) node[below=2pt] {$x_2$};
    \draw[thick] (4.5, -0.08) -- (4.5, 0.08) node[below=2pt] {$x_3$};
    \draw[thick] (6.0, -0.08) -- (6.0, 0.08) node[below=2pt] {$1$};

    % 4. 左侧 epsilon 标注
    \draw[<->, thick] (-0.3, 0.5) -- (-0.3, 1.0) node[midway, left] {$\varepsilon$};
    \draw[<->, thick] (-0.3, 1.0) -- (-0.3, 1.5) node[midway, left] {$\varepsilon$};

    % 5. 上下虚线包络线 (f_0 + eps 和 f_0 - eps)
    \draw[dashed, thick] plot [smooth] coordinates {
      (0, 1.5) (1.5, 2.2) (2.8, 2.6) (4.5, 2.1) (6.0, 3.5)
    };
    \draw[dashed, thick] plot [smooth] coordinates {
      (0, 0.5) (1.5, 1.2) (2.8, 1.6) (4.5, 1.1) (6.0, 2.5)
    };

    % 6. 基准函数 f_0（黑色粗线）
    \draw[ultra thick, black] plot [smooth] coordinates {
      (0, 1.0) (1.5, 1.7) (2.8, 2.1) (4.5, 1.6) (6.0, 3.0)
    };

    % 7. 红色函数（穿出虚线带，但在 x1, x2, x3 处掉入带内）
    \draw[thick, red] plot [smooth] coordinates {
      (0, 1.4) (0.7, 2.0) (1.5, 1.8) (2.3, 2.8) (3.0, 2.0) (3.8, 0.8) (4.5, 1.5) (5.3, 1.2) (6.0, 3.2)
    };

    % 8. 蓝色函数
    \draw[thick, blue] plot [smooth] coordinates {
      (0, 0.8) (1.5, 1.75) (3.0, 1.95) (4.5, 1.55) (6.0, 2.9)
    };

    % 9. 绿色函数
    \draw[thick, green!80!black] plot [smooth] coordinates {
      (0, 1.2) (1.5, 1.65) (3.0, 2.25) (4.5, 1.4) (6.0, 3.1)
    };

    % 10. f_0 标签指示箭头
    \draw[->, thick] (3.8, 1.5) node[left] {$f_0$} -- (3.4, 1.95);

  \end{tikzpicture}
\end{document}
```
The black curve represents $f_0$. The blue and green curves remain inside the entire $\varepsilon$-tube, so they certainly satisfy the three pointwise constraints. The red curve leaves the tube between the marked points, but it still satisfies $|g(x_i)-f_0(x_i)|<\varepsilon$ for $i=1,2,3$. Hence it also belongs to $\omega(f_0;x_1,x_2,x_3;\varepsilon)$. This is exactly the distinction between controlling finitely many values and controlling a function uniformly on its whole domain.

> [!TIP] Proposition 6 (Pointwise and Topological Convergence)
> The family $\mathcal{T}_{\mathrm{p.c.}}$ is a topology on $X=\mathbb{R}^{[0,1]}$. A sequence $(f_n)$ converges to $f$ in this topology if and only if $f_n(x)\to f(x)$ for every $x\in[0,1]$.

Proof. We first verify the topology axioms:
- Clearly, $\emptyset, X \in \mathcal{T}_{\text{p.c.}}$.

- If $U_1, U_2 \in \mathcal{T}_{\text{p.c.}}$, then for any $f_0 \in U_1 \cap U_2$, there exist points $x_1, \dots, x_m, y_1, \dots, y_n \in [0, 1]$ and $\varepsilon_1, \varepsilon_2 > 0$ such that
$$U_1 \supset \omega(f_0; x_1, \dots, x_m; \varepsilon_1) \quad \text{and} \quad U_2 \supset \omega(f_0; y_1, \dots, y_n; \varepsilon_2).$$
Hence, we have
$$U_1 \cap U_2 \supset \omega(f_0; x_1, \dots, x_m, y_1, \dots, y_n; \min(\varepsilon_1, \varepsilon_2)),$$

which implies $U_1 \cap U_2 \in \mathcal{T}_{\text{p.c.}}$.

- If $U_\alpha \in \mathcal{T}_{\text{p.c.}}$ for all $\alpha$ and $f_0 \in \bigcup_\alpha U_\alpha$, then there exists some $\alpha_0$ such that $f_0 \in U_{\alpha_0}$. By definition, there exist $x_1, \dots, x_m \in [0, 1]$ and $\varepsilon > 0$ such that
$$\omega(f_0; x_1, \dots, x_m; \varepsilon) \subset U_{\alpha_0}.$$
This clearly implies that
$$\omega(f_0; x_1, \dots, x_m; \varepsilon) \subset \bigcup_\alpha U_\alpha,$$
and thus $\bigcup_\alpha U_\alpha \in \mathcal{T}_{\text{p.c.}}$.

Next, we prove that the pointwise convergence of a sequence of functions is equivalent to convergence under the topology $\mathcal{T}_{\text{p.c.}}$:
Suppose $(f_n)$ converges pointwise to $f$. Let $U \subset X$ be an open set in $\mathcal{T}_{\text{p.c.}}$ with $f \in U$. Then there exist $x_1, \dots, x_m \in [0, 1]$ and $\varepsilon > 0$ such that
$$\omega(f; x_1, \dots, x_m; \varepsilon) \subset U.$$
By the definition of pointwise convergence, $f_n(x_i) \to f(x_i)$ for each $1 \le i \le m$. Thus there exist integers $k_i$ such that $|f_n(x_i) - f(x_i)| < \varepsilon$ whenever $n > k_i$. Therefore, for all $n > k = \max(k_1, \dots, k_m)$, we have
$$f_n \in \omega(f; x_1, \dots, x_m; \varepsilon) \subset U.$$
By definition, $(f_n)$ converges to $f$ in the topological space $(X, \mathcal{T}_{\text{p.c.}})$.

Conversely, suppose $(f_n)$ converges to $f$ in $(X, \mathcal{T}_{\text{p.c.}})$. For any $x \in [0, 1]$ and any $\varepsilon > 0$, consider the open neighborhood $U = \omega(f; x; \varepsilon)$ of $f$. Then there exists $k > 0$ such that $f_n \in U$ for all $n > k$, which means $|f_n(x) - f(x)| < \varepsilon$ holds for all $n > k$. Thus $f_n(x) \to f(x)$ for every $x \in [0, 1]$. $\square$

### Continuous Mappings Between Topological Spaces
Let us first define continuity in terms of convergent sequences.

> [!ABSTRACT] Definition 8 (Sequential Continuity)
> For a mapping $f: (X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ between topological spaces:
> (1) If for every convergent sequence $x_n \to x_0$ in $X$, we have $f(x_n) \to f(x_0)$ in $Y$, then $f$ is said to be **sequentially continuous at** $x_0$.
> (2) If $f$ is sequentially continuous at every point in $X$, then $f$ is called a **sequentially continuous mapping**.

We can also define continuous mappings using the topological structure itself.

> [!ABSTRACT] Definition 9 (Continuity)
> For a mapping between topological spaces $\displaystyle f:(X,\mathcal{T}_{X})\to(Y,\mathcal{T}_{Y})$ :
> (1) If the preimage $\displaystyle f^{-1}(B)$ of any neighborhood $\displaystyle B$ of the point $\displaystyle f(x_{0})$ in $\displaystyle Y$ is a neighborhood of the point $\displaystyle x_{0}$ in $\displaystyle X$, then we say that $\displaystyle f$ is **continuous at** the point $\displaystyle x_{0}$.
> (2) If $\displaystyle f$ is continuous at every point in $\displaystyle X$, then we call $\displaystyle f$ a **continuous mapping**.

> [!Question] Question 3 (Composition)
> Prove directly from the neighborhood definitions that a composition of continuous maps is continuous. Then prove the analogous statement for sequentially continuous maps.

> [!TIP] Proposition 7 (Composition of Continuous Maps)
> Let $X, Y,$ and $Z$ be topological spaces.
> (1) If $f: X \to Y$ is continuous at $x_0$ and $g: Y \to Z$ is continuous at $f(x_0)$, then the composition $g \circ f: X \to Z$ is continuous at $x_0$.
> (2) If $f: X \to Y$ is sequentially continuous at $x_0$ and $g: Y \to Z$ is sequentially continuous at $f(x_0)$, then $g \circ f: X \to Z$ is sequentially continuous at $x_0$.

#### Sequential Continuity vs. Continuity
In metric spaces, sequential continuity and continuity are equivalent. For general topological spaces, we have the following:

> [!TIP] Proposition 8 (Continuity Implies Sequential Continuity)
> If $f: (X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ is continuous at $x_0$, then it is also sequentially continuous at $x_0$. In particular, any continuous mapping $f: (X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ is sequentially continuous.

Proof. Suppose $x_n \to x_0$. Let $B$ be an arbitrary neighborhood of $f(x_0)$ in $Y$. By the continuity of $f$, the preimage $f^{-1}(B)$ is a neighborhood of $x_0$ in $X$. Since $x_n \to x_0$, there exists $k > 0$ such that $x_n \in f^{-1}(B)$ for all $n > k$. Consequently, $f(x_n) \in B$ for all $n > k$, which means $f(x_n) \to f(x_0)$. Thus, $f$ is sequentially continuous at $x_0$.

> [!Example] Example 7 (Sequential Continuity Need Not Imply Continuity)
> Consider the identity map
> $$\operatorname{Id}:(\mathbb{R},\mathcal{T}_{\text{cocountable}})
> \longrightarrow(\mathbb{R},\mathcal{T}_{\text{discrete}}).$$
> In both spaces, the convergent sequences are exactly the eventually constant sequences, so $\operatorname{Id}$ is sequentially continuous. It is not continuous: the singleton $\{x\}$ is open in the codomain, but its preimage $\{x\}$ is not open in the cocountable topology.

#### Characterizing Continuity Using Open Sets
We have already proved that $f : (X, d_X) \to (Y, d_Y)$ is a continuous mapping if and only if the preimage $f^{-1}(V)$ of every open set $V$ in $Y$ is an open set in $X$. By repeating the proof from that setting, we can easily establish the following characterization of continuous mappings in terms of open sets:

> [!TIP] Proposition 9 (Open Sets and Continuity)
> Let $f : (X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ be a mapping. Then $f$ is continuous if and only if "the preimage of an open set is open"; that is, for every $V \in \mathcal{T}_Y$, we have $f^{-1}(V) \in \mathcal{T}_X$.

We have the open-closed duality principle: facts described in terms of open sets have a "dual" formulation in terms of closed sets. The proof follows directly via standard complementation:

> [!TIP] Proposition 10 (Closed Sets and Continuity)
> A mapping $f : (X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ is continuous if and only if for every closed set $F$ in $Y$, its preimage $f^{-1}(F)$ is closed in $X$.

Note that $f^{-1}(F)$ is closed if and only if $X \setminus f^{-1}(F) = f^{-1}(Y \setminus F)$ is open. The result follows immediately from this.
#### Open and Closed Maps
Under a continuous mapping, the preimage of an open set is open, and the preimage of a closed set is closed. Generally, however, it is easy to find counterexamples showing that:

- The image of an open set under a continuous mapping is not necessarily open.
- The image of a closed set under a continuous mapping is not necessarily closed.

We define

> [!ABSTRACT] Definition 10 (Open and Closed Maps)
> For a mapping $f : (X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ between topological spaces:
> (1) If the image $f(U)$ of every open set $U$ in $X$ is an open set in $Y$, then $f$ is called an **open mapping**.
> (2) If the image $f(F)$ of every closed set $F$ in $X$ is a closed set in $Y$, then $f$ is called a **closed mapping**.

This is not central to the current section, but it becomes an important tool in functional analysis, complex analysis, and further topology.
#### Examples of Continuous Maps
We now present some examples of continuous mappings.

> [!Example] Example 8 (Basic Continuous Maps)
> (1) Any constant mapping $f : X \to Y$ is continuous.
> Suppose $f(x) \equiv y_0 \in Y$, and let $U$ be an arbitrary open set in $Y$. Then:
> - If $y_0 \in U$, then $f^{-1}(U) = X$, which is open in $X$.
>
> - If $y_0 \notin U$, then $f^{-1}(U) = \varnothing$, which is open in $X$.
> Thus, $f$ is continuous.
> Notice that this argument also explains why, in the axioms for open sets, we require $\varnothing$ and $X$ to be open in every topology: otherwise, constant mappings might fail to be continuous!
>
> (2) Any mapping $f : (X, \mathcal{T}_X) \to (Y, \mathcal{T}_{\text{trivial}})$ is continuous.
>
> (3) Any mapping $f : (X, \mathcal{T}_{\text{discrete}}) \to (Y, \mathcal{T}_Y)$ is continuous.
>
> (4) The identity mapping $\mathrm{Id} : (X, \mathcal{T}_2) \to (X, \mathcal{T}_1)$ is continuous if and only if $\mathcal{T}_1 \subset \mathcal{T}_2$, i.e., $\mathcal{T}_1$ is weaker (coarser) than $\mathcal{T}_2$.

> [!Example] Example 9 (Continuous Images Need Not Be Open or Closed)
> The constant map $f:\mathbb{R}\to\mathbb{R}$, $f(x)=0$, is continuous, but the image of the open set $\mathbb{R}$ is the nonopen set $\{0\}$. Likewise, the continuous map
> $$g:\mathbb{R}\to\mathbb{R},\qquad g(x)=\arctan x,$$
> maps the closed set $\mathbb{R}$ onto $(-\pi/2,\pi/2)$, which is not closed in $\mathbb{R}$.

The following two propositions show that natural mappings under the subspace topology and the product space topology are continuous:

> [!TIP] Proposition 11 (Inclusion Map of a Subspace)
> Let $(X, \mathcal{T}_X)$ be a topological space, and let $A \subset X$ be endowed with the subspace topology. Then the inclusion mapping $\iota : A \hookrightarrow X$ is continuous, and the subspace topology is the weakest topology on $A$ for which $\iota$ is continuous.

Proof. For every open set $U\in\mathcal{T}_X$,
$$\iota^{-1}(U)=U\cap A,$$
which is open in the subspace topology; hence $\iota$ is continuous. Conversely, suppose $\mathcal{T}$ is a topology on $A$ for which $\iota:(A,\mathcal{T})\hookrightarrow(X,\mathcal{T}_X)$ is continuous. Then $U\cap A=\iota^{-1}(U)$ belongs to $\mathcal{T}$ for every $U\in\mathcal{T}_X$. Thus $\mathcal{T}$ contains the subspace topology, so the subspace topology is the coarsest topology on $A$ making $\iota$ continuous. $\square$

This yields the following corollary.

> [!Danger] Corollary 1 (Maps and Subspaces)
> Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces, and endow $A \subset X$ with the subspace topology.
>
> (1) If the mapping $f : X \to Y$ is continuous, then its restriction $\left.f\right|_A : A \to Y$ is continuous.
> (2) A mapping $g : Y \to A$ is continuous if and only if $\iota \circ g : Y \to X$ is continuous.

> [!Question] Question 4 (Restrictions and Corestrictions)
> Prove the corollary.

> [!TIP] Proposition 12 (Projection Maps of Product Spaces)
>
> Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces, and let $(X \times Y, \mathcal{T}_{X \times Y})$ be their product topological space. Then the projection mappings
> $$\begin{aligned} \pi_X : X \times Y &\to X, \quad (x, y) \mapsto x, \\ \pi_Y : X \times Y &\to Y, \quad (x, y) \mapsto y \end{aligned}$$
> are both continuous mappings and open mappings.

Proof. We prove the assertion for $\pi_X$ only; the proof for $\pi_Y$ is completely analogous.
$\pi_X$ is continuous because for every open set $U \in \mathcal{T}_X$, we have
$$\pi_X^{-1}(U) = U \times Y \in \mathcal{T}_{X \times Y}.$$
To see that $\pi_X$ is an open mapping, let $W \in \mathcal{T}_{X \times Y}$ be an arbitrary open set, and let $x \in \pi_X(W)$. Then there exists a point $(x, y) \in W$. By the definition of the product topology, there exist an open set $U \ni x$ in $X$ and an open set $V \ni y$ in $Y$ such that $(x, y) \in U \times V \subset W$. Thus, $x \in U \subset \pi_X(W)$. Consequently, $\pi_X(W)$ is open in $X$, which shows that $\pi_X$ is an open mapping. $\square$

> [!Warning] Remark 3 (Projections Need Not Be Closed)
> Projection mappings are not necessarily closed mappings. For example, the set $\{(x, 1/x) \mid x > 0\}$ is closed in the plane $\mathbb{R} \times \mathbb{R}$, but its projection onto the first factor $\mathbb{R}$ is $(0, +\infty)$, which is not closed in $\mathbb{R}$.

### Homeomorphism
Using continuous mappings, we can define the notion of equivalence between topological spaces.

> [!ABSTRACT] Definition 11 (Homeomorphism)
>
> Let $X$ and $Y$ be topological spaces. If there exists a bijective (invertible) mapping $f : X \to Y$ such that both $f$ and $f^{-1}$ are continuous, then we say that the topological spaces $X$ and $Y$ are **homeomorphic**, denoted by $X \cong Y$. The mapping $f$ is called a **homeomorphism** between $X$ and $Y$.

If a property is preserved under homeomorphisms, it is called a **topological property**.
The following proposition records the formal properties of this notion.

> [!TIP] Proposition 13 (Homeomorphism Is an Equivalence Relation)
> Homeomorphism is an equivalence relation on the class of topological spaces.

Proof. We check the three properties:
- **Reflexivity ($X \cong X$):** The identity mapping $\mathrm{Id} : (X, \mathcal{T}_X) \to (X, \mathcal{T}_X)$ is a homeomorphism.
- **Symmetry ($X \cong Y \implies Y \cong X$):** If $f : X \to Y$ is a homeomorphism, then its inverse $f^{-1} : Y \to X$ is also a homeomorphism.
- **Transitivity ($X \cong Y, Y \cong Z \implies X \cong Z$):** If $f : X \to Y$ and $g : Y \to Z$ are homeomorphisms, then $g \circ f : X \to Z$ is a bijection. Proposition 7 shows that both $g \circ f$ and $(g \circ f)^{-1} = f^{-1} \circ g^{-1}$ are continuous. $\square$

We treat homeomorphic topological spaces as topological copies of the same space.

> [!Example] Example 10 (Homeomorphic and Nonhomeomorphic Spaces)
> Under the standard Euclidean topology:
>
> (1) $(0,1)\cong\mathbb{R}$ via
> $$x\longmapsto\tan\!\bigl(\pi(x-\tfrac12)\bigr).$$
>
> (2) $S^n\setminus\{\text{North Pole}\}\cong\mathbb{R}^n$ via stereographic projection.
>
> (3) $S^1\setminus\{(1,0)\}\cong\mathbb{R}\cong(0,1)$.
>
> (4) $[0,1)$ is **not** homeomorphic to $(0,1)$. Removing $0$ from $[0,1)$ leaves a connected space, whereas removing any point from $(0,1)$ disconnects it.
>
> (5) $[0,1]$ is not homeomorphic to $(0,1)$ because compactness is a topological property.

In addition to being continuous and bijective, it is clear from the definition that a homeomorphism must be both an open mapping and a closed mapping. Conversely, by definition, if $f$ is invertible, then $f^{-1}$ is continuous if and only if $f$ is an open mapping (or equivalently, if and only if $f$ is a closed mapping). Thus we have:

> [!TIP] Proposition 14 (Homeomorphisms and Open/Closed Maps)
>
> Let $f : X \to Y$ be a continuous bijection. If $f$ is an open mapping or a closed mapping, then $f$ is a homeomorphism.

Similar to the case for metric spaces, we can define the concept of a topological embedding:

> [!ABSTRACT] Definition 12 (Topological Embedding)
>
> Let $X$ and $Y$ be topological spaces, and let $f : X \to Y$ be a continuous injection. If $f$ is a homeomorphism from $X$ onto $f(X) \subset Y$ (endowed with the subspace topology), then we call $f$ a **topological embedding** from $X$ into $Y$.
