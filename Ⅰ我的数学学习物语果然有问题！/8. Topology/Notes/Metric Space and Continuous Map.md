---
tags:
  - Mathematical_Analysis
  - Topology
---
# Metric Spaces
 > In 1906, Maurice Fréchet introduced the concept of a metric space.
 
> [!ABSTRACT] Definition 1 (Metric)
> Let $X$ be a set. We say that
> $$d: X\times X\to \mathbb{R}$$
> is a metric on $X$ if:
> - **(Positivity)** $\displaystyle d(x,y)\geq 0$, and $\displaystyle d(x,y)=0$ if and only if $\displaystyle x=y$.
> - **(Symmetry)** $\displaystyle d(x,y)=d(y,x)$
> - **(Triangle Inequality)** $\displaystyle d(x,z)\leq d(x,y)+d(y,z)$.

Note: Many metric-related concepts from Euclidean spaces can be generalized naturally to arbitrary metric spaces.

> [!ABSTRACT] Definition 2 (Diameter and Boundedness)
> Let $(X,d)$ be a metric space, and let $A\subset X$ be a nonempty subset. The **diameter** of $A$ is defined by
> $$\operatorname{diam}(A) := \sup_{x,y \in A} d(x, y)$$
> If $\operatorname{diam}(A) < +\infty$, we say $A$ is a **bounded set**; otherwise, it is called an **unbounded set**.
> In particular, if $\operatorname{diam}(X) < +\infty$, we call $(X, d)$ a **bounded metric space**.

Moreover, a metric naturally gives rise to geometric concepts such as open balls, closed balls, and spheres.

> [!ABSTRACT] Definition 3 (Balls and Spheres)
> The **open ball**, **closed ball**, and **sphere** centered at $x_0 \in X$ with radius $r > 0$ are defined respectively as:
> $$\begin{aligned} B(x_0, r) &= \{x \in X \mid d(x, x_0) < r\}, \\ \bar{B}(x_0, r) &= \{x \in X \mid d(x, x_0) \le r\}, \\ S(x_0, r) &= \{x \in X \mid d(x, x_0) = r\}. \end{aligned}$$
We also introduce open and closed sets, which will be used later.

> [!ABSTRACT] Definition 4 (Open and Closed Sets)
> Let $(X, d)$ be a metric space and $U \subset X$. If for every $x \in U$, there exists an $\epsilon > 0$ such that
> $$B(x, \epsilon) \subset U,$$
> then $U$ is called an **open set**. A subset $F\subset X$ is called a **closed set** if its complement $F^c=X\setminus F$ is open.
> It is straightforward to verify from the definitions that open balls are open sets and closed balls are closed sets in any metric space.

> [!Warning] Remark 1 (Open Balls and Closed Balls)
> In every metric space, open balls are open sets and closed balls are closed sets. However, the closure of an open ball need not equal the corresponding closed ball. For example, in a discrete metric space, $B(x,1)=\{x\}$ and $\overline{B(x,1)}=\{x\}$, whereas $\bar B(x,1)=X$.

Here are some examples:
1. **(Discrete Metric)** On any set $X$, we can define the discrete metric by
$$d(x, y) = \begin{cases} 0 & x = y, \\ 1 & x \neq y. \end{cases}$$
> [!Question] Question 1 (Balls in the Discrete Metric)
> In a discrete metric space $(X, d_{\text{discrete}})$, what do the open balls, closed balls, and spheres look like?

2. **(Various Metrics on $\displaystyle \mathbb{R}^n$)**
On $X = \mathbb{R}$, besides the discrete metric defined above, we also have:
- The simplest absolute value metric: $d(x, y) = \vert{}x - y\vert{}$.
> The discrete metric reveals little about the usual geometry of a set, whereas the absolute value metric is unbounded. This motivates the following bounded metrics.
- Bounded metrics: 
$$\bar{d}(x, y) = \min\{\vert{}x - y\vert{}, 1\} \quad\text{or}\quad \bar{d}(x, y) = \frac{\vert{}x-y\vert{}}{1+\vert{}x-y\vert{}}$$
More generally, on $X = \mathbb{R}^n$, we have:

- **(Standard Euclidean Metric)** $d_2(x, y) = \sqrt{(x_1 - y_1)^2 + \dots + (x_n - y_n)^2}$.

- **($\ell^1$ Metric, or Taxicab Metric)** $d_1(x, y) = \vert{}x_1 - y_1\vert{} + \dots + \vert{}x_n - y_n\vert{}$.
![[Pasted image 20260715111346.png]]
- **($\ell^\infty$ Metric)** $d_\infty(x, y) = \max\{\vert{}x_1 - y_1\vert{}, \dots, \vert{}x_n - y_n\vert{}\}$.
For $1 \le p < \infty$, the $\ell^p$ metric is defined by
$$d_p(x, y) := \left( \vert{}x_1 - y_1\vert{}^p + \dots + \vert{}x_n - y_n\vert{}^p \right)^{1/p}.$$
The case $p=\infty$ is defined separately by the maximum formula above.

> [!Question] Question 2 (Limit of the $\ell^p$ Metrics)
> How can we derive the $\ell^\infty$ metric as the limit of the $\ell^p$ metrics as $p\to\infty$?
> 

![[Pasted image 20260715112052.png]]
3. **(Various Metrics on $\mathbb{R}^{\mathbb{N}}$)** Consider the infinite Cartesian product
$$X = \mathbb{R}^{\mathbb{N}} := \{(x_1, x_2, \dots, x_n, \dots) \mid x_n \in \mathbb{R}\},$$
We cannot define the $\ell^p$ metric on all of this space by the preceding formula because the sum may diverge. However, we can use a bounded metric on $\mathbb{R}$ to avoid convergence problems:

- **(Uniform Metric)** $d((x_n)_{n \in \mathbb{N}}, (y_n)_{n \in \mathbb{N}}) := \sup_{n \in \mathbb{N}} \bar{d}(x_n, y_n)$.

- **(Infinite Product Metric)** $d((x_n)_{n \in \mathbb{N}}, (y_n)_{n \in \mathbb{N}}) := \sum_{n=1}^{\infty} 2^{-n} \bar{d}(x_n, y_n)$.

```python
x = [0, 0, 0, 0, 0]
y = [0, 0, 0, 100, 100]

# Uniform metric (take the maximum coordinate distance)
uniform = max(min(abs(a - b), 1) for a, b in zip(x, y))

# Product metric (take a weighted sum)
product = sum((1 / (2 ** i)) * min(abs(a - b), 1) for i, (a, b) in enumerate(zip(x, y), 1))

print(uniform)  # 1.0
print(product)  # 0.09375
```

Additionally, we can restrict the $\ell^p$ metric to a suitable subset to ensure convergence:
- **($\ell^p$ Space, $1 \le p < \infty$)** Consider the subspace
$$\ell^p(\mathbb{R}) := \left\{ (x_n)_{n \in \mathbb{N}} \ \middle\vert{}\ \Vert{}x\Vert{}_p := \left( \sum_{n} \vert{}x_n\vert{}^p \right)^{1/p} < +\infty \right\} \subset \mathbb{R}^{\mathbb{N}},$$
where we define the $\ell^p$ metric as $d(x, y) = \Vert{}x - y\Vert{}_p$.

- **(Hilbert Cube)** Let $X = \prod_{n} [0, 1/n] \subset \mathbb{R}^{\mathbb{N}}$. This is a subset of $\ell^2(\mathbb{R})$ and naturally inherits the $\ell^2$ metric.

4. **(Metrics on Function Spaces)** On the space $C([a,b])$ of continuous functions on $[a,b]$, we have:
- **($L^1$ Metric)** $d(f, g) = \int_{a}^{b} \vert{}f(x) - g(x)\vert{} \, dx$.

- **($L^\infty$ Metric)** $d(f, g) = \sup_{x \in [a, b]} \vert{}f(x) - g(x)\vert{}$.

- **($L^2$ Metric)** $d(f, g) = \left( \int_{a}^{b} \vert{}f(x) - g(x)\vert{}^2 \, dx \right)^{1/2}$.

For $1 \le p < \infty$, the $L^p$ metric is
$$d(f, g) = \left( \int_{a}^{b} \vert{}f(x) - g(x)\vert{}^p \, dx \right)^{1/p}.$$
The case $p=\infty$ is defined separately by the supremum formula above. Furthermore, on the space of $k$-times continuously differentiable functions, we can define the **Sobolev $W^{k,p}$ metric** for $1\le p<\infty$ by
$$d(f, g) = \left( \sum_{i=0}^{k} \int_{a}^{b} \vert{}f^{(i)}(x) - g^{(i)}(x)\vert{}^p \, dx \right)^{1/p}.$$
If you have studied abstract algebra, you may have encountered the word metric. Given a group $G$ and a generating set $S\subset G$, the set $S$ induces a word metric on $G$. If you are interested in graph metrics, our TA's area of expertise is geometric group theory.

## Constructing New Spaces from Existing Ones

> Having established the foundational definitions of metric spaces and explored a variety of classical examples, a natural question arises: how can we construct new metric spaces from these existing building blocks? In this section, we will study two of the most fundamental geometric constructions: inheriting a metric on a subset (subspace metrics) and combining metrics on Cartesian products (product metrics).

Two common constructions are subspaces, which inherit a metric from the ambient space, and Cartesian products, which can be equipped with suitable product metrics.

> [!TIP] Proposition 1 (Subspace Metric)
> Let $(X, d)$ be a metric space, and let $Y \subset X$ be a subset. Then
> $$d_Y := d\vert{}_{Y \times Y}$$
> is a metric on $Y$.

Proof. Let $y_1,y_2,y_3\in Y$. Since $Y\subset X$, the following properties are inherited from $d$:
- $\displaystyle d_{Y}(y_{1},y_{2})=0$ if and only if $\displaystyle y_{1}=y_{2}$.

- $\displaystyle d_{Y}(y_{1},y_{2})=d(y_{1},y_{2})=d(y_{2},y_{1})=d_{Y}(y_{2},y_{1})$.

- $\displaystyle d_{Y}(y_{1},y_{3})=d(y_{1},y_{3})\leq d(y_{1},y_{2})+d(y_{2},y_{3})=d_{Y}(y_{1},y_{2})+d_{Y}(y_{2},y_{3})$. $\square$

More generally, given an injective map $f: Y \to X$, we can identify $Y$ with the subset $f(Y) \subset X$ and define the induced metric on $Y$ via the metric $d_X$ on $X$:
$$d(y_1, y_2) := d_X(f(y_1), f(y_2)).$$
We now explain how to construct a reasonable metric on a Cartesian product.

> [!TIP] Proposition 2 (Product Metric)
> If $(X_1,d_1)$ and $(X_2,d_2)$ are metric spaces, then
> $$d((x_1, x_2), (y_1, y_2)) := d_1(x_1, y_1) + d_2(x_2, y_2)$$
> is a metric on $X_1 \times X_2$.

Proof. For any points $(x_1, x_2)$, $(y_1, y_2)$, and $(z_1, z_2)$ in $X_1 \times X_2$, we have:

-  $d((x_1, x_2), (y_1, y_2)) = 0 \iff d_1(x_1, y_1) = 0 \text{ and } d_2(x_2, y_2) = 0\iff x_1 = y_1 \text{ and } x_2 = y_2.$

-  $d((x_1, x_2), (y_1, y_2)) = d_1(x_1, y_1) + d_2(x_2, y_2) = d_1(y_1, x_1) + d_2(y_2, x_2)= d((y_1, y_2), (x_1, x_2)).$

- $d((x_1, x_2), (z_1, z_2)) =$
	$d_1(x_1, z_1) + d_2(x_2, z_2)\le$
	$d_1(x_1, y_1) + d_1(y_1, z_1) + d_2(x_2, y_2) + d_2(y_2, z_2)= d((x_1, x_2), (y_1, y_2)) + d((y_1, y_2), (z_1, z_2)).$
$\square$

Unlike the inherited metric on a subspace, a product space can be equipped with several natural metrics. For example, we can also define
$$d((x_1, x_2), (y_1, y_2)) := \sqrt{d_1(x_1, y_1)^2 + d_2(x_2, y_2)^2}$$
It can be verified that this is a metric on $X_1 \times X_2$. More generally, if $(X_1, d_1), \cdots, (X_n, d_n)$ are metric spaces, then for any $1 \le p < \infty$, the **$\ell^p$-type product metric** on $X_1 \times \cdots \times X_n$ is defined by
$$d_p((x_1, \cdots, x_n), (y_1, \cdots, y_n)) := \left( d_1(x_1, y_1)^p + \cdots + d_n(x_n, y_n)^p \right)^{1/p}.$$
For $p=\infty$, define
$$d_\infty((x_1,\ldots,x_n),(y_1,\ldots,y_n)):=\max_{1\le i\le n}d_i(x_i,y_i).$$

> [!Question] Question 3 (Metric on a Countable Product)
> How can we construct a metric on a countable product of metric spaces?

To define a metric on the Cartesian product $\prod_{n=1}^{\infty} X_n$ of countably many metric spaces $(X_n, d_n)$, first replace each $d_n$ with the bounded metric
$$\tilde{d}_n(x, y) = \min\{d_n(x, y), 1\}.$$
We can then define the **uniform metric** on $\prod_{n=1}^{\infty} X_n$ by
$$d_u((x_n)_{n \in \mathbb{N}}, (y_n)_{n \in \mathbb{N}}) = \sup_{n \in \mathbb{N}} \tilde{d}_n(x_n, y_n).$$
This metric generally induces the uniform topology, which may be finer than the product topology. A standard metric that induces the product topology is
$$d((x_n),(y_n)):=\sum_{n=1}^{\infty}2^{-n}\tilde d_n(x_n,y_n).$$

## Isometries, Embeddings, and Lipschitz Maps

> [!ABSTRACT] Definition 5 (Isometry)
> Let $(X,d_X)$ and $(Y,d_Y)$ be metric spaces. A bijection $f:X\to Y$ is called an **isometry** if, for every $x_1,x_2\in X$,
> $$d_Y(f(x_1), f(x_2)) = d_X(x_1, x_2).$$

Since isometric metric spaces have exactly the same metric properties, we usually regard them as equivalent. Two useful relaxations of an isometry are introduced below.

> [!ABSTRACT] Definition 6 (Isometric Embedding)
> An injective map $f:X\to Y$ is called an **isometric embedding** if, for every $x_1,x_2\in X$,
> $$d_Y(f(x_1), f(x_2)) = d_X(x_1, x_2).$$

If $f:(X,d_X)\to(Y,d_Y)$ is an isometric embedding, then $f$ is an isometry from $(X,d_X)$ onto the subspace $(f(X),d_Y|_{f(X)\times f(X)})$.

> [!ABSTRACT] Definition 7 (Lipschitz Map)
> A map $f:X\to Y$ is called a **Lipschitz map** with Lipschitz constant $L\geq0$ if, for every $x_1,x_2\in X$,
> $$d_Y(f(x_1), f(x_2)) \le L d_X(x_1, x_2).$$

> [!Warning] Remark 2 (Lipschitz Maps and Continuity)
> On an interval, or more generally on a convex domain, a differentiable function with bounded derivative is Lipschitz. Moreover,
> $$\text{Lipschitz}\implies\text{uniformly continuous}\implies\text{continuous}.$$

> [!Example] Example 1 (Identity Maps between Metrics)
> Let $X = \mathbb{R}$ with $d(x, y) = \vert{}x - y\vert{}$ and $\bar{d}(x, y) = \min(1, \vert{}x - y\vert{})$.
>
> - The identity maps $\text{id}:(\mathbb{R},d)\to(\mathbb{R},d)$ and $\text{id}:(\mathbb{R},\bar d)\to(\mathbb{R},\bar d)$ are isometries.
> - The map $\text{id}: (\mathbb{R}, d) \to (\mathbb{R}, \bar{d})$ is **Lipschitz** but not an isometry.
> - The map $\text{id}: (\mathbb{R}, \bar{d}) \to (\mathbb{R}, d)$ is **NOT Lipschitz**.

# Continuous Maps Between Metric Spaces
As in Euclidean spaces, we first define convergence of sequences and then use it to characterize continuity.

> [!ABSTRACT] Definition 8 (Convergence)
> Let $(X, d)$ be a metric space, and let $(x_n)$ be a sequence in $X$. The sequence $(x_n)$ is said to **converge** to $x_0 \in X$ (denoted by $x_n \to x_0$) if for every $\epsilon > 0$, there exists $N \in \mathbb{N}$ such that for all $n \ge N$:
> $$d(x_n, x_0) < \epsilon.$$

> [!ABSTRACT] Definition 9 (Continuity)
> Let $(X,d_X)$ and $(Y,d_Y)$ be metric spaces, and let $f:X\to Y$ be a map.
> 1. $f$ is **continuous at $x_0 \in X$** if, for every sequence $(x_n)$ converging to $x_0$ in $X$, the sequence $(f(x_n))$ converges to $f(x_0)$ in $Y$.
> 2. $f$ is a **continuous map** if it is continuous at every point $x_0 \in X$.

> [!ABSTRACT] Definition 10 (Equivalent Characterizations of Continuity at a Point)
> For a map $f:X\to Y$ and a point $x_0\in X$, the following conditions are equivalent:
> $$\begin{aligned} f\text{ is continuous at }x_0
> &\iff \forall \epsilon > 0, \exists \delta > 0 \text{ such that } \forall x \in X, d_X(x, x_0) < \delta \implies d_Y(f(x), f(x_0)) < \epsilon \\
> &\iff \forall \epsilon > 0, \exists \delta > 0 \text{ such that } f(B_X(x_0, \delta)) \subset B_Y(f(x_0), \epsilon) \\
> &\iff \forall \epsilon > 0, \exists \delta > 0 \text{ such that } B_X(x_0, \delta) \subset f^{-1}(B_Y(f(x_0), \epsilon)). \end{aligned}$$

> [!Example] Example 2 (Basic Continuous Maps)
> The continuity of maps between metric spaces generalizes the familiar notion of continuity in Euclidean spaces. The following examples illustrate this definition.

(1) Let $(X, d)$ be any metric space.
- For a fixed $\bar{x} \in X$, consider the function
$$d_{\bar{x}} : X \to \mathbb{R}, \quad x \mapsto d(x, \bar{x})$$

is continuous. In fact, it is $1$-Lipschitz.

Proof. For all $x,x_0\in X$, the reverse triangle inequality gives
$$\vert{}d_{\bar{x}}(x) - d_{\bar{x}}(x_0)\vert{} = \vert{}d(x, \bar{x}) - d(x_0, \bar{x})\vert{} \le d(x, x_0).$$

Therefore, $d_{\bar x}$ is $1$-Lipschitz and hence continuous. $\square$
- More generally, for any nonempty subset $A \subset X$, we can define
$$d_A : X \to \mathbb{R}, \quad x \mapsto d_A(x) := \inf\{d(x, y) : y \in A\}.$$
The reverse triangle inequality shows that $d_A$ is $1$-Lipschitz and hence continuous.
> [!Question] Question 4 (Distance to a Set)
> For any nonempty subset $A \subset X$, define the distance to $A$ by
> $$d_A(x) := \inf_{y \in A} d(x, y)$$
> Prove that $d_A: X \to \mathbb{R}$ is $1$-Lipschitz and hence continuous. If $A$ is closed, also prove that $d_A(x)=0$ if and only if $x\in A$.

> [!Question] Question 5 (Continuity of the Metric)
> Equip $X\times X$ with the sum metric
> $$d_{X\times X}((x_1,x_2),(y_1,y_2)):=d(x_1,y_1)+d(x_2,y_2).$$
> Prove that the metric $d:X\times X\to\mathbb{R}$ is continuous.
 
(2) On the space $X = C([a, b])$ endowed with the $\ell^\infty$ metric
$$d(f, g) := \sup_{x \in [a, b]} \vert{}f(x) - g(x)\vert{}.$$
The integration functional
$$\int : X \to \mathbb{R}, \quad f \mapsto \int_{a}^{b} f(x) \, dx$$
is continuous, because
$$\left\vert{} \int_{a}^{b} f(x) \, dx - \int_{a}^{b} g(x) \, dx \right\vert{} \le \int_{a}^{b} \vert{}f(x) - g(x)\vert{} \, dx \le (b - a) \cdot d(f, g).$$
(3) Let $X$ be any set, and $d_X$ be the discrete metric on $X$. Let $(Y, d_Y)$ be any metric space.
- Any map $f : X \to Y$ is continuous.
Proof. For any $\epsilon>0$, choose $\delta=1$. If $x,x_0\in X$ satisfy $d_X(x,x_0)<1$, then the definition of the discrete metric gives $x=x_0$. Thus, $d_Y(f(x),f(x_0))=0<\epsilon$. $\square$
- A map $f:Y\to X$, where $X$ carries the discrete metric, is continuous if and only if it is locally constant.
A map $f:Y\to X$ is **locally constant** if, for every $y_0\in Y$, there exists $\delta>0$ such that $d_Y(y_0,y)<\delta$ implies $f(y)=f(y_0)$.

## Strongly Equivalent and Topologically Equivalent Metrics
> At first glance, continuity appears to depend on the particular metrics chosen on the domain and codomain. The following examples show that different metrics may nevertheless determine exactly the same continuous maps.

> [!Example] Example 3 (The Metrics $d_1$ and $d_\infty$)
> Consider a function $f:\mathbb{R}^n\to\mathbb{R}$ and the two metrics $d_1$ and $d_\infty$ on $\mathbb{R}^n$. The function $f:(\mathbb{R}^n,d_1)\to\mathbb{R}$ is continuous if and only if $f:(\mathbb{R}^n,d_\infty)\to\mathbb{R}$ is continuous.

Proof. For all $x,y\in\mathbb{R}^n$,
$$d_\infty(x,y)\leq d_1(x,y)\leq n\max_i|x_i-y_i|=n\,d_\infty(x,y).$$
Thus, the identity maps in both directions between $(\mathbb{R}^n,d_1)$ and $(\mathbb{R}^n,d_\infty)$ are Lipschitz and therefore continuous. It follows that $f$ is continuous with respect to $d_1$ if and only if it is continuous with respect to $d_\infty$. $\square$

Motivated by this example, we introduce the following relation.

> [!ABSTRACT] Definition 11 (Strongly Equivalent Metrics)
> Let $d_1$ and $d_2$ be two metrics on a set $X$. If there exist constants $C_1,C_2>0$ such that, for all $x,y\in X$,
> $$C_1d_1(x, y) \le d_2(x, y) \le C_2d_1(x, y),$$
> then $d_1$ and $d_2$ are said to be **strongly equivalent**.

> [!Question] Question 6 (Strongly Equivalent Metrics)
> Prove the following proposition. Let $d_X$ and $\tilde{d}_X$ be strongly equivalent metrics on $X$, and let $d_Y$ and $\tilde{d}_Y$ be strongly equivalent metrics on $Y$. Then $f:(X,d_X)\to(Y,d_Y)$ is continuous if and only if $f:(X,\tilde d_X)\to(Y,\tilde d_Y)$ is continuous.

> Strong equivalence is sufficient but not necessary for two metrics to induce the same continuous maps. The next example motivates a weaker notion of equivalence.

> [!Example] Example 4 (The Metrics $d_2$ and $\bar d_2$)
> Consider another pair of metrics on $\mathbb{R}^n$: the Euclidean metric $d_2(x, y) = \Vert{}x - y\Vert{}_2$ and the bounded metric induced by $d_2$, defined by
>
> $$\bar{d}_2(x, y) := \min \{1, d_2(x, y)\}.$$
>
> Clearly, $\bar{d}_2(x, y) \le d_2(x, y)$. However, $d_2$ and $\bar{d}_2$ are **not** strongly equivalent. Indeed, if there were a constant $c>0$ such that $c\,d_2(x,y)\leq\bar d_2(x,y)$ for all $x,y$, we could choose $x,y$ with $d_2(x,y)>1/c$. Then
> $$c\,d_2(x,y)>1=\bar d_2(x,y),$$
> a contradiction.
>
> Nevertheless, $d_2$ and $\bar d_2$ induce the same topology. Consequently, a function $f:\mathbb{R}^n\to\mathbb{R}$ is continuous with respect to $d_2$ if and only if it is continuous with respect to $\bar d_2$.

> [!Question] Question 7 (Topological Equivalence of $d_2$ and $\bar d_2$)
> Prove this fact.

# Axiomatization of Neighborhoods and Introduction to Topology
> Note that we are not confined to the metric itself; we may instead introduce the neighborhood system to discuss continuity.

> [!ABSTRACT] Definition 12 (Neighborhoods)
> Let $x\in X$ and $N\subset X$. If there exists an open set $U\subset X$ such that $x\in U\subset N$, then $N$ is called a neighborhood of $x$.

If $\mathcal{N}(x)$ denotes the set of all neighborhoods of $x$, it is easy to verify that:

(N1) If $N \in \mathcal{N}(x)$, then $x \in N$.
(N2) If $M \supset N$ and $N \in \mathcal{N}(x)$, then $M \in \mathcal{N}(x)$.
(N3) If $N_1, N_2 \in \mathcal{N}(x)$, then $N_1 \cap N_2 \in \mathcal{N}(x)$.
(N4) If $N \in \mathcal{N}(x)$, then there exists $M \in \mathcal{N}(x)$ such that $M \subset N$ and, for every $y \in M$, $N \in \mathcal{N}(y)$.

The continuity of a map at a point can be characterized using neighborhoods:

> [!TIP] Proposition 3 (Neighborhoods and Continuity at a Point)
> Let $f : (X, d_X) \to (Y, d_Y)$ be a map between metric spaces. Then $f$ is continuous at $x \in X$ if and only if the preimage of any neighborhood of $f(x)$ is a neighborhood of $x$.

Proof. Suppose that $f$ is continuous at $x$, and let $M\subset Y$ be a neighborhood of $f(x)$. By definition, there exists an open set $V\subset Y$ such that $f(x)\in V\subset M$. Since $V$ is open, there exists $\varepsilon>0$ such that $B(f(x),\varepsilon)\subset V$. By the continuity of $f$ at $x$, there exists $\delta>0$ such that
$$B(x, \delta) \subset f^{-1}(B(f(x), \varepsilon)) \subset f^{-1}(V) \subset f^{-1}(M).$$
Therefore, $f^{-1}(M)$ is a neighborhood of $x$.
Conversely, assume that the preimage of every neighborhood of $f(x)$ is a neighborhood of $x$. In particular, for every $\varepsilon>0$, the set $f^{-1}(B(f(x),\varepsilon))$ is a neighborhood of $x$. Hence it contains an open set $U$ containing $x$. Since $U$ is open, there exists $\delta>0$ such that $B(x,\delta)\subset U$. Therefore, $B(x,\delta)\subset f^{-1}(B(f(x),\varepsilon))$, and $f$ is continuous at $x$. $\square$

### Characterizing Continuity Using Open Sets
As a corollary of the preceding proposition, we obtain the following characterization of continuous maps between metric spaces.
> [!NOTE] Theorem 1 (Characterization of Continuous Maps)
> A map $f:(X,d_X)\to(Y,d_Y)$ is continuous if and only if the preimage $f^{-1}(V)$ of every open set $V\subset Y$ is open in $X$.

Proof.
Suppose $f$ is continuous, and let $V\subset Y$ be open. For every $x\in f^{-1}(V)$, the preceding proposition implies that $f^{-1}(V)$ is a neighborhood of $x$ and therefore contains an open neighborhood of $x$. Hence $f^{-1}(V)$ is open in $X$.
Conversely, suppose that the preimage of every open set in $Y$ is open in $X$. Let $x\in X$ and let $V\subset Y$ be an open neighborhood of $f(x)$. Then $f^{-1}(V)$ is an open neighborhood of $x$. Thus, $f$ is continuous. $\square$

This suggests that continuity does not fundamentally depend on the numerical values of a metric, but rather on the family of open sets induced by it. We therefore make the following definition.

> [!ABSTRACT] Definition 13 (Topologically Equivalent Metrics)
> Let $d_1$ and $d_2$ be two metrics on a set $X$. If the families of open sets induced by them are identical, then $d_1$ and $d_2$ are said to be **topologically equivalent**.

> [!Question] Question 8 (Continuity and Uniform Continuity)
> Show that continuity is a topological concept; "uniform continuity" is not a topological concept.

We immediately obtain the following corollary.

> [!Danger] Corollary 1 (Continuity under Topologically Equivalent Metrics)
> Let $\tilde{d}_X$ and $\tilde{d}_Y$ be metrics that are topologically equivalent to $d_X$ and $d_Y$, respectively. Then the map $f : (X, d_X) \to (Y, d_Y)$ is a continuous map if and only if the map $f : (X, \tilde{d}_X) \to (Y, \tilde{d}_Y)$ is a continuous map.

### Axiomatization of Neighborhoods
> In this section, we introduce neighborhoods and open sets axiomatically, thereby defining general topological spaces.

Motivated by the properties of the neighborhood system $\mathcal{N}(x)$, we introduce the following axioms:

(N1) If $N \in \mathcal{N}(x)$, then $x \in N$.
(N2) If $M \supset N$ and $N \in \mathcal{N}(x)$, then $M \in \mathcal{N}(x)$.
(N3) If $N_1, N_2 \in \mathcal{N}(x)$, then $N_1 \cap N_2 \in \mathcal{N}(x)$.
(N4) If $N \in \mathcal{N}(x)$, then there exists $M \in \mathcal{N}(x)$ such that $M \subset N$ and, for every $y \in M$, $N \in \mathcal{N}(y)$.

The fourth axiom relates the neighborhoods of different points. It may be viewed as a topological analogue of the role played by the triangle inequality in metric spaces.

In 1912, Hausdorff axiomatized the concept of a neighborhood to define a general notion of space encompassing $\mathbb{R}^n$, Riemann surfaces, infinite-dimensional spaces, and function spaces. He emphasized two benefits: simplifying the theory and preventing the misuse of intuition.

> [!ABSTRACT] Definition 14 (Neighborhood Structure)
> Let
> $$\mathcal{N} : X \to \mathcal{P}(\mathcal{P}(X)) \setminus \{\emptyset\}$$
> be a map satisfying axioms (N1)–(N4). Then $\mathcal{N}$ is called a **neighborhood structure** on $X$. We call $\mathcal{N}(x)$ the **neighborhood system** (or neighborhood filter) at $x$, and each element of $\mathcal{N}(x)$ a **neighborhood** of $x$.

Given a neighborhood structure $\mathcal{N}$ on $X$, we call $(X,\mathcal{N})$ a **topological space defined by a neighborhood structure**.

#### Axiom of Open Sets

> [!ABSTRACT] Definition 15 (Interior)
> Let $(X,\mathcal{N})$ be a topological space defined by a neighborhood structure. For any subset $A\subset X$, its **interior** is defined by
> $$\text{Int}(A) := \{x \in A \mid A \in \mathcal{N}(x)\}. \quad (1.2.1)$$
By the definition and axioms (N1)–(N4), the map
$$\text{Int} : \mathcal{P}(X) \to \mathcal{P}(X), \quad A \mapsto \text{Int}(A)$$
satisfies the following properties:

(I1) $\text{Int}(A) \subset A$.
(I2) $\text{Int}(A) \cap \text{Int}(B) = \text{Int}(A \cap B)$.
(I3) $\text{Int}(\text{Int}(A)) = \text{Int}(A)$.
(I4) $\text{Int}(X) = X$.

> [!ABSTRACT] Definition 16 (Interior Structure)
> Let $X$ be a set. We call a map $\text{Int} : \mathcal{P}(X) \to \mathcal{P}(X)$ satisfying axioms (I1)–(I4) an **interior structure** on $X$.

Given an interior structure $\text{Int}$ on $X$, we call $(X,\text{Int})$ a **topological space defined via an interior structure**. The neighborhood and interior formulations are equivalent. A neighborhood structure determines the interior structure defined above; conversely, an interior structure determines a neighborhood structure by
$$\mathcal{N}(x) = \{A \subset X \mid x \in \text{Int}(A)\}.$$
> [!Question] Question 9 (Neighborhood and Interior Structures)
> Show that for any neighborhood structure $\mathcal{N}$ on a set $X$, the map $\text{Int} : \mathcal{P}(X) \to \mathcal{P}(X)$ is an interior structure on $X$; conversely, for any interior structure $\text{Int}$ on a set $X$, the family of subsets $\mathcal{N}$ is a neighborhood structure on $X$. Furthermore, show that these two constructions are mutually inverse.

From the concept of an interior structure, we can define open sets.
> [!ABSTRACT] Definition 17 (Open Sets)
> In a topological space defined via a neighborhood structure, a set $U$ is called **open** if
> $$U\in\mathcal{N}(x)\quad\text{for every }x\in U.$$
By the equivalence of neighborhood structures and interior structures, we immediately obtain the following equivalent characterization:

> [!TIP] Proposition 4 (Open Sets and Interior)
> A set $U$ in a topological space defined via neighborhood structures (or interior structures) is an open set if and only if $\text{Int}(U) = U$.
Given $(X, \mathcal{N})$, if we denote by
$$\mathcal{T} = \{U \subset X \mid U \text{ is an open set}\} $$
the family of all open sets in $(X,\mathcal{N})$, then the following properties hold:

(O1) $\emptyset \in \mathcal{T}$ and $X \in \mathcal{T}$.
(O2) If $U_1, U_2 \in \mathcal{T}$, then $U_1 \cap U_2 \in \mathcal{T}$.
(O3) If $\{U_\alpha : \alpha \in \Lambda\} \subset \mathcal{T}$, then $\bigcup_{\alpha \in \Lambda} U_\alpha \in \mathcal{T}$.

In the next section, we will give the formal definition of a topology.
