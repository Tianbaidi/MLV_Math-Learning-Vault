---
tags:
  - Algebra
  - Linear_Algebra
---
一个线性变化 $T:V\to W$ 是从一个数域 $F$ 上的线性空间到另一个线性空间的映射，它对数乘和加法完备 
$$T(v_{1}+v_{2})=T(v_{1})+T(v_{2}) \qquad ,\quad T(cv_{1})=cT(v_{1})$$
我们类似群同态，我们也将其称为 **同态** ( Homomorphism )  , 线性变化也具有一定的线性性 
$$T\left( \sum_{i}c_{i}v_{i} \right)=\sum_{i}T(v_{i})c_{i}$$
域 $F$ 中的一个 $m\times n$ 矩阵的有左乘映射 
$$F^n\overset{A}\longrightarrow F^m \qquad X\mapsto AX$$
这是一个线性映射，自然我们有 $A(X_{1}+X_{2})=AX_{1}+AX_{2}$ 以及 $A(cX)=cAX$ 

如果 $\mathbf{B}=(\nu_{1},\ldots,\nu_{n})$ 是域 $F$ 上向量空间 $V$ 的一个子集，则映射 $F^{n}\to V$（$X\mapsto \mathbf{B}X$）是一个线性变换。

> [!Example] EXAMPLE
>    令 $P_{n}$ 为线性空间下的实多项式方程： 
>$$a_{n}t^n+a_{n-1}t^{n-1}+\cdots+a_{1}t+a_{0}=0$$
>次数至多为 $n$ 构成的向量空间。导数 $\frac{d}{dt}$ 定义了从 $P_{n}$ 到 $P_{n-1}$ 的一个线性变换。

与一个线性变换相关的有两个重要的子空间：它的核和它的像：
$$\begin{array}{l}{\ker T}&{=}&{kernel~of~T}&{=}&{\{\upsilon\in V|T(\upsilon)=0\},}\\{\mathrm{im}T}&{=}&{image~of~T}&{=}&{\{\upsilon\in W|w=T(\upsilon)\mathrm{for~some~}\upsilon\in V\}.}\end{array} \quad $$
我们常称核线性变化中的 **零子空间** (nullspace) 。类比群同态，Ker 是 $V$ 的子空间，Im 则是 $W$ 的子空间。

> [!NOTE] Theorem **Dimension Formula.**
> Let $T:V\to W$ be a linear transformation. Then 
>$$dim(ker\ T)+dim(ker\ T)=dim\ V$$
>线性变换 $T$ 的 nullity 和 rank 分别是 kernel 和 image 的维数

于是，我们可以转述为 
$$\text{nullity}+\text{rank}=\text{dimension of V}$$
这个定义类似矩阵的 nullity 和 rank . 

**Proof.** 我们设 $V$ 是一个有限维线性空间，记维度为 $n$ . 令  $K$ 为 $\ker T$ 的维数，其基为 $(u_{1},u_{2},\cdots,u_{k})$ . 我们对这组基扩展得到 $V$ 的基 : 
$$(u_{1},u_{2},\cdots,u_{k};v_{1},v_{2},\cdots,v_{n-k})$$
>对 $i=1,\ldots,n-k$，令 $w_{i}=T(v_{i})$。如果我们能证明 $\mathbf{C}=(w_{1},\ldots,w_{n-k})$ 是像的一组基，那么像的维数就是 $n-k$，这就证明了定理。

我们必须证明 $\mathbf{C}$ 张成像并且它是一个线性无关集。设 $w$ 是像中的一个元素。则存在某个 $v\in V$ 使得 $w=T(v)$。我们将 $v$ 用基表示： 
$$v = a_{1}u_{1} + \dots +a_{k}u_{k} + b_{1}v_{1} + \dots +b_{n - k}v_{n - k}$$
然后应用 $T$，注意到 $T(u_{i})=0$：
$$w = T(v) = b_{1}w_{1} + \dots +b_{n - k}w_{n - k}.$$
因此 $w$ 在 $\mathbf{C}$ 的张成空间中

假设我们有一个线性关系
$$c_{1}w_{1} + \dots +c_{n - k}w_{n - k} = 0.$$
令 $v = c_{1}v_{1} + \dots +c_{n - k}v_{n - k}$，其中 $v_{i}$ 是 $(u_{1},u_{2},\cdots,u_{k};v_{1},v_{2},\cdots,v_{n-k})$ 中的向量。则
$$T(v) = c_{1}w_{1} + \dots +c_{n - k}w_{n - k} = 0,$$
所以 $v$ 在零空间中。我们用零空间的基 $(u_{1},\ldots,u_{k})$ 表示 $v$，设 $v = a_{1}u_{1} + \dots +a_{k}u_{k}$。则
$$-a_{1}u_{1} - \dots -a_{k}u_{k} + c_{1}v_{1} + \dots +c_{n - k}v_{n - k} = -v + v = 0.$$
但是 $(u_{1},u_{2},\cdots,u_{k};v_{1},v_{2},\cdots,v_{n-k})$ 是线性无关的。所以 $-a_{1}=0,\ldots,-a_{k}=0$，且 $c_{1}=0,\ldots,c_{n-k}=0$。因此 $\mathbf{C}$ 是线性无关的  $Q.E.D$

当 $T$ 是矩阵 $A$ 的左乘时，$T$ 的核，即 $A$ 的零空间，是齐次方程 $AX=0$ 的解集。$T$ 的像是列空间 (column space)，即 $A$ 的列张成的空间，也是使线性方程 $AX=B$ 有解 $F^{m}$ 中的向量 $B$ 的集合 

> [!Example] EXAMPLE
> 将齐次方程 $AX=0$ 的解加到非齐次方程 $AX=B$ 的一个特解 $X_{0}$ 上，就得到非齐次方程的所有解。另一种说法是，$AX=B$ 的解集是零空间 $N$ 在 $F^{n}$ 中的加法陪集 $X_{0}+N$。

行列式非零的 $n\times n$ 矩阵 $A$ 是可逆的，且方程组 $AX=B$ 对每个 $B$ 都有唯一解。此时，零空间为 $\{0\}$，列空间为整个空间 $F^{n}$。另一方面，如果行列式为零，则零空间 $N$ 具有正维数，而像（列空间）的维数小于 $n$。并非所有方程 $AX=B$ 都有解，但有解的方程会有多个解，因为解集是 $N$ 的一个陪集。

