---
tags:
  - Topology
  - Set_Theory
  - English
---

# Points and Sets in Topological Spaces

> [!Quote] Introduction
> Point-set topology studies the relationship between points and sets. This note introduces the basic notions of open sets, closed sets, limit points, closure, interior, and boundary.

## Open Sets, Closed Sets, and Clopen Sets

> [!ABSTRACT] Definition
> Let us first recall the definitions of open and closed sets. Let $(X, \mathcal T)$ be a topological space. If $U \subseteq X$ and $U \in \mathcal T$, then $U$ is called an **open set**. If the complement $A^c=X\setminus A$ of a set $A \subseteq X$ is open, then $A$ is called a **closed set**.

A set may be both open and closed, or neither. A set that is both open and closed is called a **clopen set**.

> [!Example] Examples
> The following examples illustrate these definitions.

**Examples:**

1. In every topological space, $X$ and $\varnothing$ are clopen.
2. In the discrete topology, every subset is clopen.
3. In the usual topology on the real line $\mathbb R$:
   - every singleton $\{x\}$ is closed;
   - $(a,b)$ is open, while $[a,b]$ is closed;
   - the Cantor set

     $$
     C=[0,1]\setminus \bigcup_{n=1}^{\infty}\bigcup_{k=0}^{3^{n-1}-1}
     \left(\frac{3k+1}{3^n},\frac{3k+2}{3^n}\right)
     $$

     is closed.
4. Regard $\mathbb Q$ as a subspace of $\mathbb R$:
   - if $a,b\in\mathbb Q$ and $a<b$, then $(a,b)\cap\mathbb Q$ is open but not closed;
   - if $a,b\in\mathbb R\setminus\mathbb Q$ and $a<b$, then $(a,b)\cap\mathbb Q$ is clopen.

### A Note on Cardinality

> [!Info] Cardinality Note
> The cardinality of the real numbers is $\mathfrak c=2^{\aleph_0}$, and the cardinality of their power set $\mathcal P(\mathbb R)$ is $2^{\mathfrak c}$. Under the usual topology, there are exactly $\mathfrak c$ open subsets of $\mathbb R$, and exactly $\mathfrak c$ closed subsets as well. Thus open and closed sets form a very small portion of all $2^{\mathfrak c}$ subsets. Without additionally assuming the continuum hypothesis, one must not write $\mathfrak c=\aleph_1$.

## Describing Closed Sets with Sequences

> [!Question] Question
> Recall a familiar necessary condition for closedness: if $x_n\in A$ and $x_n\to x_0$, then $x_0\in A$. Does the converse imply that $A$ is closed? In metric spaces, the answer is yes. If $x_0\in A^c$ but $A^c$ is not a neighborhood of $x_0$, choose $x_n\in A\cap B(x_0,1/n)$ for every $n$. Then $x_n\to x_0$, which gives a contradiction.

This argument naturally uses open balls, so it suggests that the converse works in metric spaces. Does it still work in arbitrary topological spaces? Consider the function space

$$
X=\mathbb R^{[0,1]}
$$

with the topology of pointwise convergence (the product topology), and let

$$
A=\left\{f:[0,1]\to\mathbb R \middle| \{x\in[0,1]:f(x)\ne0\}\text{ is countable}\right\}.
$$

If $f_n\in A$ and $f_n\to f$ pointwise, then

$$
\{x:f(x)\ne0\}\subseteq\bigcup_{n=1}^{\infty}\{x:f_n(x)\ne0\},
$$

so $f\in A$. In other words, $A$ contains the limits of all of its convergent sequences.

Yet $A$ is not closed. Indeed, take $g\in A^c$ and a basic open neighborhood $U$ of $g$. There are a finite set $F\subset[0,1]$ and $\varepsilon>0$ such that

$$
\omega(g;F,\varepsilon)
=\{f:|f(x)-g(x)|<\varepsilon\text{ for every }x\in F\}
\subseteq U.
$$

Define

$$
\widetilde g(x)=
\begin{cases}
g(x), & x\in F,\\
0, & x\notin F.
\end{cases}
$$

Then $\widetilde g\in A\cap U$. Hence $A^c$ is not open, and $A$ is not closed.

> [!Warning] Remark
> This example tells us that, in an arbitrary topological space, sequences alone need not detect closed sets. One direction, however, always remains valid.

> [!TIP] Proposition
>
> If $F$ is a closed subset of a topological space $X$, $x_n\in F$, and $x_n\to x_0\in X$, then $x_0\in F$.

**Proof.** If $x_0\notin F$, then $F^c$ is an open neighborhood of $x_0$. By the definition of convergence, there is an $N$ such that $x_n\in F^c$ whenever $n\ge N$, contradicting $x_n\in F$. $\square$

## First Countability

So when are sequences enough? We need, at every point, a countable collection of open neighborhoods that can be made as small as necessary. This is precisely the first countability axiom.

> [!ABSTRACT] Definition — First Countability
>
> If for every $x\in X$ there is a countable family of open neighborhoods $\{U_n^x:n\in\mathbb N\}$ containing $x$, such that every neighborhood $U$ of $x$ contains some $U_n^x$, then $X$ satisfies the **first countability axiom**, or equivalently, $X$ is a **first-countable space**.

> [!TIP] Proposition
>
> If $X$ is a first-countable space, then $F\subseteq X$ is closed if and only if, for every sequence $(x_n)\subseteq F$, the implication $x_n\to x\Rightarrow x\in F$ holds.

## Limit Points, Isolated Points, and the Derived Set

One may now ask what becomes of the preceding counterexample. Although $g\in A^c$ is not the limit of any sequence of functions from $A$, it is still arbitrarily close to $A$: every neighborhood of $g$ meets $A$. This leads to the notion of a limit point.

> [!ABSTRACT] Definition — Limit Point
>
> Let $A\subseteq X$ and $x\in X$. If every neighborhood $U$ of $x$ satisfies
>
> $$
> U\cap(A\setminus\{x\})\ne\varnothing,
> $$
>
> then $x$ is called a **limit point** (or an **accumulation point**) of $A$. The set of all limit points of $A$ is called the **derived set** of $A$, denoted by $A'$.

$$
A'=\{x\in X:x\text{ is a limit point of }A\}.
$$

The derived set has the following properties:

1. $\varnothing'=\varnothing$;
2. if $a\in A'$, then $a\in(A\setminus\{a\})'$;
3. if $A\subseteq B$, then $A'\subseteq B'$;
4. $(A\cup B)'=A'\cup B'$;
5. $(A')'\subseteq A\cup A'$.

> [!ABSTRACT] Definition — Isolated Point
>
> If $x\in A$ and there is an open set $U$ containing $x$ such that $U\cap A=\{x\}$, then $x$ is called an **isolated point** of $A$.

By definition, $x$ is an isolated point of $A$ if and only if $x\in A\setminus A'$.

> [!NOTE] Theorem
>
> A subset $A$ of a topological space $X$ is closed if and only if $A'\subseteq A$.

**Proof.** If $A$ is closed, then for any $x\in A^c$, the open set $A^c$ is a neighborhood of $x$, so $x\notin A'$. Hence $A'\subseteq A$. Conversely, suppose $A'\subseteq A$. For every $x\in A^c$, we have $x\notin A'$, so there is a neighborhood $U$ of $x$ with $U\cap(A\setminus\{x\})=\varnothing$. Since $x\notin A$, this gives $U\cap A=\varnothing$, hence $U\subseteq A^c$. Therefore $A^c$ is open, and $A$ is closed. $\square$

## Closure

Limit points let us describe closed sets again: a set is closed exactly when it contains all of its limit points. If a set does not contain the points that cling to it in this way, adding them produces its closure.

> [!ABSTRACT] Definition — Closure
>
> The **closure** of $A\subseteq X$ is the smallest closed set containing $A$, denoted by $\overline A$ or $\operatorname{Cl}(A)$.

It can be written as

$$
\overline A=\bigcap_{\substack{F\text{ is closed}\\A\subseteq F}}F=A\cup A'.
$$

> [!Info] Closure Properties
> The basic properties of closure are:
>
> 1. $A\subseteq\overline A$;
> 2. $\overline{A\cup B}=\overline A\cup\overline B$;
> 3. $\overline{\overline A}=\overline A$;
> 4. $\overline\varnothing=\varnothing$;
> 5. $A$ is closed if and only if $A=\overline A$;
> 6. if $A\subseteq B$, then $\overline A\subseteq\overline B$;
> 7. $\overline{A\cap B}\subseteq\overline A\cap\overline B$;
> 8. in the product topology, for $A\subseteq X$ and $B\subseteq Y$, $\overline{A\times B}=\overline A\times\overline B$.
>

Closure also has the following neighborhood characterization:

$$
x\in\overline A
\iff
\text{for every open set }U\text{ containing }x,\ U\cap A\ne\varnothing.
$$

## Interior

Closure is the smallest closed set that contains $A$. Dually, we can look at the question from inside the set.

> [!ABSTRACT] Definition — Interior
>
> If there is an open set $U$ containing $x$ such that $U\subseteq A$, then $x$ is an **interior point** of $A$. The set of all interior points is called the **interior** of $A$, denoted by $\operatorname{Int}(A)$ or $A^\circ$.

$$
\operatorname{Int}(A)=\{x\in X:\exists\text{ an open set }U,\ x\in U\subseteq A\}
=\bigcup_{\substack{U\text{ is open}\\U\subseteq A}}U.
$$

Thus $\operatorname{Int}(A)$ is the largest open set contained in $A$; in particular, $A$ is open if and only if $A=\operatorname{Int}(A)$.

Its basic properties are:

1. $\operatorname{Int}(A)\subseteq A$;
2. $\operatorname{Int}(A\cap B)=\operatorname{Int}(A)\cap\operatorname{Int}(B)$;
3. $\operatorname{Int}(\operatorname{Int}(A))=\operatorname{Int}(A)$;
4. $\operatorname{Int}(X)=X$;
5. if $A\subseteq B$, then $\operatorname{Int}(A)\subseteq\operatorname{Int}(B)$;
6. $\operatorname{Int}(A)\cup\operatorname{Int}(B)\subseteq\operatorname{Int}(A\cup B)$;
7. in the product topology, for $A\subseteq X$ and $B\subseteq Y$, $\operatorname{Int}(A\times B)=\operatorname{Int}(A)\times\operatorname{Int}(B)$.

## Dense and Nowhere Dense Sets

With closure and interior in hand, we can describe how fully a set fills its ambient space.

> [!ABSTRACT] Definition — Density
>
> Let $A\subseteq X$.
>
> 1. If $\overline A=X$, then $A$ is **dense** in $X$.
> 2. If $\operatorname{Int}(\overline A)=\varnothing$, then $A$ is **nowhere dense**.

> [!Example] Examples
> The following examples illustrate density and nowhere denseness.

**Examples:**

1. In the Euclidean topology, $\mathbb Q$ is dense in $\mathbb R$: every nonempty open interval contains a rational number. Similarly, $\mathbb R\setminus\mathbb Q$ is dense in $\mathbb R$.
2. In the usual topology, $\mathbb N\subseteq\mathbb R$ is nowhere dense. Since $\mathbb N$ is closed and contains no nonempty open interval, $\operatorname{Int}(\overline{\mathbb N})=\operatorname{Int}(\mathbb N)=\varnothing$.
3. The Cantor set $C$ is nowhere dense. It is closed, and the open intervals removed during its construction are dense in $[0,1]$; thus $C$ contains no nonempty open interval.
4. In the trivial topology $\{\varnothing,X\}$, every nonempty subset $A$ has $\overline A=X$; equivalently, every nonempty subset is dense. This differs sharply from the Euclidean intuition.
5. Let $W$ be the graph of the standard Weierstrass function. Since this function is continuous, $W$ is closed in $\mathbb R^2$. Moreover, $W$ has empty interior, so it is nowhere dense. In the subspace topology induced on $W$ itself, however, it is of course dense. This reminds us that density is always relative to the ambient space.

## Boundary

Likewise, the part left between closure and interior gives the boundary of a set.

> [!ABSTRACT] Definition — Boundary
>
> The **boundary** of a set $A\subseteq X$ is
>
> $$
> \partial A=\overline A\setminus A^\circ.
> $$

The whole space has the disjoint decomposition

$$
X=A^\circ\sqcup\partial A\sqcup(\overline A)^c.
$$

A point $x$ lies on the boundary of $A$ if and only if every open set $U$ containing $x$ satisfies both

$$
U\cap A\ne\varnothing
\quad\text{and}\quad
U\cap A^c\ne\varnothing.
$$

The boundary has the following basic properties:

1. $\partial A$ is always closed;
2. $\partial A=\partial(A^c)$;
3. $\partial(A^\circ)\subseteq\partial A$ and $\partial(\overline A)\subseteq\partial A$;
4. $\partial(\partial A)\subseteq\partial A$;
5. if $A$ is open or closed, then $\partial(\partial A)=\partial A$;
6. if $A$ is open or closed, then $\operatorname{Int}(\partial A)=\varnothing$, so $\partial A$ is nowhere dense;
7. $\partial(A\cup B)\subseteq\partial A\cup\partial B$.

## Characterizing Continuity with Closure

Finally, let us return to maps. Closure not only describes sets; it also gives a concise characterization of continuity.

> [!TIP] Proposition
>
> Let $f:X\to Y$ be a map between topological spaces. Then $f$ is continuous if and only if, for every $A\subseteq X$,
>
> $$
> f(\overline A)\subseteq\overline{f(A)}.
> $$

**Proof.** If $f$ is continuous, then $f^{-1}(\overline{f(A)})$ is a closed set containing $A$. Hence

$$
\overline A\subseteq f^{-1}(\overline{f(A)}),
$$

which is equivalent to $f(\overline A)\subseteq\overline{f(A)}$.

Conversely, suppose this inclusion holds for every $A\subseteq X$. Take any closed set $B\subseteq Y$ and let $A=f^{-1}(B)$. Then

$$
f(\overline{f^{-1}(B)})
\subseteq\overline{f(f^{-1}(B))}
\subseteq\overline B=B.
$$

Therefore $\overline{f^{-1}(B)}\subseteq f^{-1}(B)$, so $f^{-1}(B)$ is closed. Thus $f$ is continuous. $\square$
