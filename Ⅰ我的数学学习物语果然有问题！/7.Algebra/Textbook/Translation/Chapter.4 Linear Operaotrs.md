---
tags:
  - Algebra
  - Translation
---



# Linear Operators

# 线性算子

That confusions of thought and errors of reasoning still darken the beginnings of Algebra, is the earnest and just complaint of sober and thoughtful men.

Sir William Rowan Hamilton

思想上的混乱和推理上的错误仍然笼罩着代数的开端，这是清醒而有思想的人们真诚而公正的抱怨。

——威廉·罗温·哈密顿爵士

### 4.1 THE DIMENSION FORMULA

### 4.1 维数公式

A linear transformation $T:V\to W$ from one vector space over a field $F$ to another is a map that is compatible with addition and scalar multiplication:

从域 $F$ 上的一个向量空间到另一个向量空间的线性变换 $T:V\to W$ 是一个与加法和标量乘法相容的映射：

$$T(\nu_{1} + \nu_{2}) = T(\nu_{1}) + T(\nu_{2})\quad \mathrm{and}\quad T(c\nu_{1}) = cT(\nu_{1}),$$

for all $\nu_{1}$ and $\nu_{2}$ in $V$ and all $c$ in $F$ . This is analogous to a homomorphism of groups, and calling it a homomorphism would be appropriate too. A linear transformation is compatible with arbitrary linear combinations:

对所有 $\nu_{1}, \nu_{2}\in V$ 和所有 $c\in F$ 成立。这类似于群同态，称之为同态也是恰当的。线性变换与任意线性组合相容：

$$T\Big(\sum_{i}\nu_{i}c_{i}\Big) = \sum_{i}T(\nu_{i})c_{i}.$$

Left multiplication by an $m\times n$ matrix $A$ with entries in $F$ , the map

一个 $m\times n$ 矩阵 $A$（其元素在 $F$ 中）的左乘映射

$$F^{n}\stackrel {A}{\longrightarrow}F^{m}\mathrm{~that~sends~}X\hookrightarrow AX$$

is a linear transformation. Indeed, $A(X_{1} + X_{2}) = AX_{1} + AX_{2}$ , and $A(cX) = cAX$ .

是一个线性变换。确实，$A(X_{1}+X_{2})=AX_{1}+AX_{2}$，且 $A(cX)=cAX$。

If $\mathbf{B} = (\nu_{1},\ldots ,\nu_{n})$ is a subset of a vector space $V$ over the field $F$ , the map $F^{n}\to V$ that sends $X\hookrightarrow \mathbf{B}X$ is a linear transformation.

如果 $\mathbf{B}=(\nu_{1},\ldots,\nu_{n})$ 是域 $F$ 上向量空间 $V$ 的一个子集，则映射 $F^{n}\to V$（$X\mapsto \mathbf{B}X$）是一个线性变换。

Another example: Let $P_{n}$ be the vector space of real polynomial functions

另一个例子：设 $P_{n}$ 是实多项式函数

$$a_{n}t^{n} + a_{n - 1}t^{n - 1} + \dots +a_{1}t + a_{0}$$

of degree at most $n$ . The derivative $\frac{d}{dt}$ defines a linear transformation from $P_{n}$ to $P_{n - 1}$ .

（次数至多为 $n$）构成的向量空间。导数 $\frac{d}{dt}$ 定义了从 $P_{n}$ 到 $P_{n-1}$ 的一个线性变换。

There are two important subspaces associated with a linear transformation: its kernel and its image:

与一个线性变换相关的有两个重要的子空间：它的核和它的像：

$$\begin{array}{rlr}{\ker T}&{=}&{kernelofT}&{=\{\upsilon\in V|T(\upsilon)=0\},}\\{\mathrm{im}T}&{=}&{imageofT}&{=\{\upsilon\in W|w=T(\upsilon)\mathrm{for~some~}\upsilon\in V\}.}\end{array} \quad (4.1.5)$$

===== Page 115 =====

The kernel is often called the nullspace of the linear transformation. As one may guess from the analogy with group homomorphisms, the kernel is a subspace of $V$ and the image is a subspace of $W$ .

核通常被称为线性变换的零空间。从与群同态的类比中可以看出，核是 $V$ 的子空间，像则是 $W$ 的子空间。

The main result of this section is the next theorem.

本节的主要结果是下面的定理。

Theorem 4.1.6 Dimension Formula. Let $T:V\to W$ be a linear transformation. Then

定理 4.1.6 维数公式。设 $T:V\to W$ 是一个线性变换。则

$$\dim (\ker T) + \dim (\operatorname {im}T) = \dim V.$$

The nullity and the rank of a linear transformation $T$ are the dimensions of the kernel and the image, respectively, and the nullity and rank of a matrix $A$ are defined analogously. With this terminology, (4.1.6) becomes

线性变换 $T$ 的零度和秩分别是核和像的维数，矩阵 $A$ 的零度和秩也类似地定义。在这个术语下，(4.1.6) 变为

$$\mathrm{nullity} + \mathrm{rank} = \mathrm{dimension} of V. \quad (4.1.7)$$

Proof of Theorem (4.1.6). We'll assume that $V$ is finite- dimensional, say of dimension $n$ . Let $k$ be the dimension of $\ker T$ , and let $(u_{1}, \ldots , u_{k})$ be a basis for the kernel. We extend this set to a basis of $V$ :

定理 (4.1.6) 的证明。我们假设 $V$ 是有限维的，设维数为 $n$。令 $k$ 为 $\ker T$ 的维数，并令 $(u_{1},\ldots,u_{k})$ 为核的一组基。我们将这个集合扩充为 $V$ 的一组基：

$$(u_{1},\ldots ,u_{k};v_{1},\ldots ,v_{n - k}). \quad (4.1.8)$$

(see (3.4.15)). For $i = 1, \ldots , n - k$ , let $w_{i} = T(v_{i})$ . If we prove that $\mathbf{C} = (w_{1}, \ldots , w_{n - k})$ is a basis for the image, it will follow that the image has dimension $n - k$ , and this will prove the theorem.

（见 (3.4.15)）。对 $i=1,\ldots,n-k$，令 $w_{i}=T(v_{i})$。如果我们能证明 $\mathbf{C}=(w_{1},\ldots,w_{n-k})$ 是像的一组基，那么像的维数就是 $n-k$，这就证明了定理。

We must show that $\mathbf{C}$ spans the image and that it is an independent set. Let $w$ be an element of the image. Then $w = T(v)$ for some $v$ in $V$ . We write $v$ in terms of the basis:

我们必须证明 $\mathbf{C}$ 张成像并且它是一个线性无关集。设 $w$ 是像中的一个元素。则存在某个 $v\in V$ 使得 $w=T(v)$。我们将 $v$ 用基表示：

$$v = a_{1}u_{1} + \dots +a_{k}u_{k} + b_{1}v_{1} + \dots +b_{n - k}v_{n - k}$$

and apply $T$ , noting that $T(u_{i}) = 0$ :

然后应用 $T$，注意 $T(u_{i})=0$：

$$w = T(v) = b_{1}w_{1} + \dots +b_{n - k}w_{n - k}.$$

Thus $w$ is in the span of $\mathbf{C}$ .

因此 $w$ 在 $\mathbf{C}$ 的张成空间中。

Next, we show that $\mathbf{C}$ is independent. Suppose we have a linear relation

接下来，我们证明 $\mathbf{C}$ 是线性无关的。假设我们有一个线性关系

$$c_{1}w_{1} + \dots +c_{n - k}w_{n - k} = 0. \quad (4.1.9)$$

Let $v = c_{1}v_{1} + \dots +c_{n - k}v_{n - k}$ , where $v_{i}$ are the vectors in (4.1.8). Then

令 $v = c_{1}v_{1} + \dots +c_{n - k}v_{n - k}$，其中 $v_{i}$ 是 (4.1.8) 中的向量。则

$$T(v) = c_{1}w_{1} + \dots +c_{n - k}w_{n - k} = 0,$$

so $v$ is in the nullspace. We write $v$ in terms of the basis $(u_{1}, \ldots , u_{k})$ of the nullspace, say $v = a_{1}u_{1} + \dots +a_{k}u_{k}$ . Then

所以 $v$ 在零空间中。我们用零空间的基 $(u_{1},\ldots,u_{k})$ 表示 $v$，设 $v = a_{1}u_{1} + \dots +a_{k}u_{k}$。则

$$-a_{1}u_{1} - \dots -a_{k}u_{k} + c_{1}v_{1} + \dots +c_{n - k}v_{n - k} = -v + v = 0.$$

But the basis (4.1.8) is independent. So $- a_{1} = 0, \ldots , - a_{k} = 0$ , and $c_{1} = 0, \ldots , c_{n - k} = 0$ . The relation (4.1.9) was trivial. Therefore $\mathbf{C}$ is independent.

但是基 (4.1.8) 是线性无关的。所以 $-a_{1}=0,\ldots,-a_{k}=0$，且 $c_{1}=0,\ldots,c_{n-k}=0$。关系 (4.1.9) 是平凡的。因此 $\mathbf{C}$ 是线性无关的。

===== Page 116 =====

When $T$ is left multiplication by a matrix $A$ (4.1.3), the kernel of $T$ , the nullspace of $A$ is the set of solutions of the homogeneous equation $AX = 0$ . The image of $T$ is the column space, the space spanned by the columns of $A$ , which is also the set of vectors $B$ in $F^{m}$ such that the linear equation $AX = B$ has a solution (3.4.6).

当 $T$ 是矩阵 $A$ 的左乘时 (4.1.3)，$T$ 的核，即 $A$ 的零空间，是齐次方程 $AX=0$ 的解集。$T$ 的像是列空间，即 $A$ 的列张成的空间，也是使得线性方程 $AX=B$ 有解的 $F^{m}$ 中的向量 $B$ 的集合 (3.4.6)。

It is a familiar fact that by adding the solutions of the homogeneous equation $AX = 0$ to a particular solution $X_{0}$ of the inhomogeneous equation $AX = B$ , one obtains all solutions of the inhomogeneous equation. Another way to say this is that the set of solutions of $AX = B$ is the additive coset $X_{0} + N$ of the nullspace $N$ in $F^{n}$ .

一个熟悉的事实是：将齐次方程 $AX=0$ 的解加到非齐次方程 $AX=B$ 的一个特解 $X_{0}$ 上，就得到非齐次方程的所有解。另一种说法是，$AX=B$ 的解集是零空间 $N$ 在 $F^{n}$ 中的加法陪集 $X_{0}+N$。

An $n\times n$ matrix $A$ whose determinant isn't zero is invertible, and the system of equations $AX = B$ has a unique solution for every $B$ . In this case, the nullspace is $\{0\}$ , and the column space is the whole space $F^{n}$ . On the other hand, if the determinant is zero, the nullspace $N$ has positive dimension, and the image, the column space, has dimension less than $n$ . Not all equations $AX = B$ have solutions, but those that do have a solution have more than one solution, because the set of solutions is a coset of $N$ .

行列式非零的 $n\times n$ 矩阵 $A$ 是可逆的，且方程组 $AX=B$ 对每个 $B$ 都有唯一解。此时，零空间为 $\{0\}$，列空间为整个空间 $F^{n}$。另一方面，如果行列式为零，则零空间 $N$ 具有正维数，而像（列空间）的维数小于 $n$。并非所有方程 $AX=B$ 都有解，但有解的方程会有多个解，因为解集是 $N$ 的一个陪集。

### 4.2 THE MATRIX OF A LINEAR TRANSFORMATION

### 4.2 线性变换的矩阵

Every linear transformation from one space of column vectors to another is left multiplication by a matrix.

从一个列向量空间到另一个列向量空间的每一个线性变换都是某个矩阵的左乘。

Lemma 4.2.1 Let $T:F^{n}\to F^{m}$ be a linear transformation between spaces of column vectors, and let the coordinate vector of $T(e_{j})$ be $A_{j} = (a_{1j},\ldots ,a_{mj})^{\mathrm{t}}$ . Let $A$ be the $m\times n$ matrix whose columns are $A_{1},\ldots ,A_{n}$ . Then $T$ acts on vectors in $F^{n}$ as multiplication by $A$ .

引理 4.2.1 设 $T:F^{n}\to F^{m}$ 是列向量空间之间的一个线性变换，并设 $T(e_{j})$ 的坐标向量为 $A_{j}=(a_{1j},\ldots,a_{mj})^{\mathrm{t}}$。令 $A$ 是以 $A_{1},\ldots,A_{n}$ 为列的 $m\times n$ 矩阵。则 $T$ 对 $F^{n}$ 中向量的作用即为左乘 $A$。

$$T(X) = T(\sum_{j}e_{j}x_{j}) = \sum_{j}T(e_{j})x_{j} = \sum_{j}A_{j}x_{j} = AX.$$

For example, let $c = \cos \theta ,s = \sin \theta$ . Counterclockwise rotation $\rho :\mathbb{R}^{2}\to \mathbb{R}^{2}$ of the plane through the angle $\theta$ about the origin is a linear transformation. Its matrix is

例如，设 $c=\cos\theta, s=\sin\theta$。平面绕原点逆时针旋转角度 $\theta$ 的旋转 $\rho:\mathbb{R}^{2}\to\mathbb{R}^{2}$ 是一个线性变换。它的矩阵是

$$R=\left[\begin{array}{cc}{c}&{-s}\\{s}&{c}\end{array}\right]. \quad (4.2.2)$$

Let's verify that multiplication by this matrix rotates the plane. We write a vector $X$ in the form $r(\cos \alpha ,\sin \alpha)^{\mathrm{t}}$ , where $r$ is the length of $X$ . Let $c^{\prime} = \cos \alpha$ and $s^{\prime} = \sin \alpha$ . The addition formulas for cosine and sine show that

我们来验证左乘这个矩阵确实旋转了平面。将向量 $X$ 写成 $r(\cos\alpha,\sin\alpha)^{\mathrm{t}}$ 的形式，其中 $r$ 是 $X$ 的长度。令 $c'=\cos\alpha, s'=\sin\alpha$。余弦和正弦的加法公式表明：

$$R X = r\left[ \begin{array}{cc}{c} -s\] \[s c} \end{array} \right]\left[ \begin{array}{cc}{c^{\prime}}\] \[s^{\prime}} \end{array} \right] = r\left[ \begin{array}{cc}{c c^{\prime} - s s^{\prime}}\] \[s c^{\prime} + c s^{\prime}} \end{array} \right] = r\left[ \begin{array}{cc}{\cos (\theta +\alpha)}\] \[\sin (\theta +\alpha)} \end{array} \right].$$

So $RX$ is obtained from $X$ by rotating through the angle $\theta$ , as claimed.

因此，$RX$ 确实是由 $X$ 旋转角度 $\theta$ 得到的，如所述。

One can make a computation analogous to that of Lemma 4.2.1 with any linear transformation $T:V\to W$ , once bases of the two spaces are chosen. If $\mathbf{B} = (v_{1},\ldots ,v_{n})$ is a basis of $V$ , we use the shorthand notation $T(\mathbf{B})$ to denote the hypervector

一旦选定了两个空间的基，就可以对任意线性变换 $T:V\to W$ 进行类似于引理 4.2.1 的计算。如果 $\mathbf{B}=(v_{1},\ldots,v_{n})$ 是 $V$ 的一组基，我们使用简写记号 $T(\mathbf{B})$ 来表示超向量

$$T(\mathbf{B}) = (T(v_{1}),\ldots ,T(v_{n})). \quad (4.2.3)$$

===== Page 117 =====

If $\mathbf{v} = \mathbf{B}X = \upsilon_{1}x_{1} + \dots +\upsilon_{n}x_{n}$ ,then

如果 $\mathbf{v} = \mathbf{B}X = \upsilon_{1}x_{1} + \dots +\upsilon_{n}x_{n}$，则

$$T(\upsilon) = T(\upsilon_{1})x_{1} + \dots +T(\upsilon_{n})x_{n} = T(\mathbf{B})X. \quad (4.2.4)$$

Proposition 4.2.5 Let $T:V\to W$ be a linear transformation, and let $\mathbf{B} = (\upsilon_{1},\ldots ,\upsilon_{n})$ and $\mathbf{C} = (\upsilon_{1},\ldots ,\upsilon_{m})$ be bases of $V$ and $W$ , respectively. Let $X$ be the coordinate vector of an arbitrary vector $\upsilon$ with respect to the basis $\mathbf{B}$ and let $Y$ be the coordinate vector of its image $T(\upsilon)$ . So $\upsilon = \mathbf{B}X$ and $T(\upsilon) = \mathbf{C}Y$ . There is an $m\times n$ matrix $A$ with the dual properties

命题 4.2.5 设 $T:V\to W$ 是一个线性变换，并设 $\mathbf{B}=(\upsilon_{1},\ldots,\upsilon_{n})$ 和 $\mathbf{C}=(\upsilon_{1},\ldots,\upsilon_{m})$ 分别是 $V$ 和 $W$ 的基。设 $X$ 是任意向量 $\upsilon$ 关于基 $\mathbf{B}$ 的坐标向量，$Y$ 是其像 $T(\upsilon)$ 的坐标向量。因此 $\upsilon = \mathbf{B}X$ 且 $T(\upsilon) = \mathbf{C}Y$。存在一个 $m\times n$ 矩阵 $A$ 具有对偶性质：

$$T(\mathbf{B}) = \mathbf{C}A\qquad \mathrm{and}\qquad AX = Y. \quad (4.2.6)$$

This matrix $A$ is the matrix of the transformation $T$ with respect to the two bases. Either of the properties (4.2.6) characterizes the matrix.

这个矩阵 $A$ 是变换 $T$ 关于这两个基的矩阵。性质 (4.2.6) 中的任何一个都刻画了这个矩阵。

Proof. We write $T(\upsilon_{j})$ as a linear combination of the basis $\mathbf{C}$ , say

证明。我们将 $T(\upsilon_{j})$ 写成基 $\mathbf{C}$ 的线性组合，设

$$T(\upsilon_{j}) = w_{1}a_{1j} + \dots +w_{m}a_{mj},$$

and we assemble the coefficients $a_{ij}$ into a column vector $A_{j} = (a_{1j},\ldots ,a_{mj})^{\mathrm{t}}$ , so that $T(\upsilon_{j}) = \mathbf{C}A_{j}$ . Then if $A$ is the matrix whose columns are $A_{1},\ldots ,A_{n}$

并将系数 $a_{ij}$ 组装成一个列向量 $A_{j}=(a_{1j},\ldots,a_{mj})^{\mathrm{t}}$，使得 $T(\upsilon_{j}) = \mathbf{C}A_{j}$。那么，如果 $A$ 是以 $A_{1},\ldots,A_{n}$ 为列的矩阵，

$$\begin{array}{r}T(\mathbf{B}) = (T(\upsilon_{1}),\ldots ,T(\upsilon_{n})) = (\upsilon_{1},\ldots ,\upsilon_{m})\left[ \begin{array}{cc}A & \\ & A \end{array} \right] = \mathbf{C}A, \end{array} \quad (4.2.8)$$

as claimed. Next, if $\upsilon = \mathbf{B}X$ , then

如所述。接下来，如果 $\upsilon = \mathbf{B}X$，则

$$T(\upsilon) = T(\mathbf{B})X = \mathbf{C}AX.$$

Therefore the coordinate vector of $T(\upsilon)$ , which we named $Y$ , is equal to $AX$ .

因此，我们记作 $Y$ 的 $T(\upsilon)$ 的坐标向量等于 $AX$。

The isomorphisms $F^{n}\to V$ and $F^{m}\to W$ determined by the two bases (3.5.3) help to explain the relationship between $T$ and $A$ . If we use those isomorphisms to identify $V$ and $W$ with $F^{n}$ and $F^{m}$ , then $T$ corresponds to multiplication by $A$ , as shown in the diagram below:

由这两个基 (3.5.3) 确定的同构 $F^{n}\to V$ 和 $F^{m}\to W$ 有助于解释 $T$ 和 $A$ 之间的关系。如果我们使用这些同构将 $V$ 和 $W$ 等同于 $F^{n}$ 和 $F^{m}$，那么 $T$ 就对应于左乘 $A$，如下图所示：

$$\begin{array}{r}F^{n}\xrightarrow{A}F^{m}\qquad X\xrightarrow{\quad}\quad AX\\\downarrow\\V\xrightarrow{T}W\qquad BX\xrightarrow{\quad}\quad T(\mathbf{B})X=\mathbf{C}AX\end{array} \quad (4.2.9)$$

Going from $F^{n}$ to $W$ along the two paths gives the same answer. A diagram that has this property is said to be commutative. All diagrams in this book are commutative.

沿着两条路径从 $F^{n}$ 到 $W$ 得到相同的结果。具有这种性质的图被称为可交换的。本书中的所有图都是可交换的。

Thus any linear transformation between finite- dimensional vector spaces $V$ and $W$ corresponds to matrix multiplication, once bases for the two spaces are chosen. This is a nice result, but if we change bases we can do much better.

因此，一旦选定了两个空间的基，有限维向量空间 $V$ 和 $W$ 之间的任何线性变换都对应于矩阵乘法。这是一个很好的结果，但如果改变基，我们可以做得更好。

===== Page 118 =====

## Theorem 4.2.10

## 定理 4.2.10

(a) Vector space form: Let $T:V\to W$ be a linear transformation between finite-dimensional vector spaces. There are bases $\mathbf{B}$ and $\mathbf{C}$ of $V$ and $W$ , respectively, such that the matrix of $T$ with respect to these bases has the form

(a) 向量空间形式：设 $T:V\to W$ 是有限维向量空间之间的一个线性变换。存在 $V$ 和 $W$ 的基 $\mathbf{B}$ 和 $\mathbf{C}$，使得 $T$ 关于这些基的矩阵具有如下形式：

equation[[398, 181, 639, 270]]

where $I_{r}$ is the $r\times r$ identity matrix and $r$ is the rank of $T$

其中 $I_{r}$ 是 $r\times r$ 单位矩阵，$r$ 是 $T$ 的秩。

(b) Matrix form: Given an $m\times n$ matrix $A$ , there are invertible matrices $Q$ and $P$ such that $A^{\prime} = Q^{-1}AP$ has the form shown above.

(b) 矩阵形式：给定一个 $m\times n$ 矩阵 $A$，存在可逆矩阵 $Q$ 和 $P$，使得 $A' = Q^{-1}AP$ 具有如上所示的形式。

Proof. (a) Let $(u_{1},\ldots ,u_{k})$ be a basis for the kernel of $T$ . We extend this set to a basis $\mathbf{B}$ of $V$ , listing the additional vectors first, say $(v_{1},\ldots ,v_{r};u_{1},\ldots ,u_{k})$ , where $r + k = n$ . Let $w_{i} = T(v_{i})$ . Then, as in the proof of (4.1.6), one sees that $(w_{1},\ldots ,w_{r})$ is a basis for the image of $T$ . We extend this set to a basis $\mathbf{C}$ of $W$ , say $(w_{1},\ldots ,w_{r};z_{1},\ldots ,z_{s})$ , listing the additional vectors last. The matrix of $T$ with respect to these bases has the form (4.2.11).

证明。(a) 设 $(u_{1},\ldots,u_{k})$ 是 $T$ 的核的一组基。我们将这个集合扩充为 $V$ 的一组基 $\mathbf{B}$，把添加的向量放在前面，设为 $(v_{1},\ldots,v_{r};u_{1},\ldots,u_{k})$，其中 $r+k=n$。令 $w_{i}=T(v_{i})$。然后，如 (4.1.6) 的证明中所见，$(w_{1},\ldots,w_{r})$ 是 $T$ 的像的一组基。我们将这个集合扩充为 $W$ 的一组基 $\mathbf{C}$，设为 $(w_{1},\ldots,w_{r};z_{1},\ldots,z_{s})$，把添加的向量放在最后。$T$ 关于这些基的矩阵具有形式 (4.2.11)。

Part (b) of the theorem can be proved using row and column operations. The proof is Exercise 2.4.

定理的第 (b) 部分可以使用行和列运算来证明。证明见习题 2.4。

This theorem is a prototype for a number of results that are to come. It shows the advantage of working in vector spaces without fixed bases (or coordinates), because the structure of an arbitrary linear transformation is described by the very simple matrix (4.2.11). But why are (a) and (b) considered two versions of the same theorem? To answer this, we need to analyze the way that the matrix of a linear transformation changes when we make other choices of bases.

这个定理是后续许多结果的原型。它展示了在没有固定基（或坐标）的向量空间中工作的优势，因为任意线性变换的结构都可以用非常简单的矩阵 (4.2.11) 来描述。但是，为什么 (a) 和 (b) 被认为是同一个定理的两个版本？要回答这个问题，我们需要分析当我们选择其他基时，线性变换的矩阵是如何变化的。

Let $A$ be the matrix of $T$ with respect to bases $\mathbf{B}$ and $\mathbf{C}$ of $V$ and $W$ , as in (4.2.6), and let $\mathbf{B}^{\prime} = (v_{1}^{\prime},\ldots ,v_{n}^{\prime})$ and $\mathbf{C}^{\prime} = (w_{1}^{\prime},\ldots ,w_{m}^{\prime})$ be new bases for $V$ and $W$ . We can relate the new basis $\mathbf{B}^{\prime}$ to the old basis $\mathbf{B}$ by an invertible $n\times n$ matrix $P$ , as in (3.5.11). Similarly, $\mathbf{C}^{\prime}$ is related to $\mathbf{C}$ by an invertible $m\times m$ matrix $Q$ . These matrices have the properties

设 $A$ 是 $T$ 关于 $V$ 和 $W$ 的基 $\mathbf{B}$ 和 $\mathbf{C}$ 的矩阵，如 (4.2.6) 所示，并设 $\mathbf{B}'=(v_{1}',\ldots,v_{n}')$ 和 $\mathbf{C}'=(w_{1}',\ldots,w_{m}')$ 是 $V$ 和 $W$ 的新基。我们可以用一个可逆的 $n\times n$ 矩阵 $P$ 将新基 $\mathbf{B}'$ 与旧基 $\mathbf{B}$ 联系起来，如 (3.5.11) 所示。类似地，$\mathbf{C}'$ 通过一个可逆的 $m\times m$ 矩阵 $Q$ 与 $\mathbf{C}$ 相关。这些矩阵具有性质：

$$\mathbf{B}^{\prime} = \mathbf{B}P,\quad P X^{\prime} = X\qquad \mathrm{and}\qquad \mathbf{C}^{\prime} = \mathbf{C}Q,\quad Q Y^{\prime} = Y.$$

Proposition 4.2.13 Let $A$ be the matrix of a linear transformation $T$ with respect to given bases $\mathbf{B}$ and $\mathbf{C}$ .

命题 4.2.13 设 $A$ 是线性变换 $T$ 关于给定基 $\mathbf{B}$ 和 $\mathbf{C}$ 的矩阵。

(a) Suppose that new bases $\mathbf{B}^{\prime}$ and $\mathbf{C}^{\prime}$ are related to the given bases by the matrices $P$ and $Q$ , as above. The matrix of $T$ with respect to the new bases is $A^{\prime} = Q^{-1}AP$ .

(a) 假设新基 $\mathbf{B}'$ 和 $\mathbf{C}'$ 通过矩阵 $P$ 和 $Q$ 与给定基相关，如上所述。则 $T$ 关于新基的矩阵是 $A' = Q^{-1}AP$。

(b) The matrices $A^{\prime}$ that represent $T$ with respect to other bases are those of the form $A^{\prime} = Q^{-1}AP$ , where $Q$ and $P$ can be any invertible matrices of the appropriate sizes.

(b) 表示 $T$ 关于其他基的矩阵 $A'$ 是那些形如 $A' = Q^{-1}AP$ 的矩阵，其中 $Q$ 和 $P$ 可以是任意适当大小的可逆矩阵。

Proof. (a) We substitute $X = P X^{\prime}$ and $Y = Q Y^{\prime}$ into the equation $Y = A X$ (4.2.6), obtaining $Q Y^{\prime} = A P X^{\prime}$ . So $Y^{\prime} = (Q^{- 1}A P)X^{\prime}$ . Since $A^{\prime}$ is the matrix such that $A^{\prime}X^{\prime} = Y^{\prime}$ , this shows that $A^{\prime} = Q^{- 1}A P$ . Part (b) follows because the basechange matrices can be any invertible matrices (3.5.9).

证明。(a) 我们将 $X = P X'$ 和 $Y = Q Y'$ 代入方程 $Y = A X$ (4.2.6)，得到 $Q Y' = A P X'$。所以 $Y' = (Q^{-1}AP)X'$。由于 $A'$ 是满足 $A'X' = Y'$ 的矩阵，这表明 $A' = Q^{-1}AP$。第 (b) 部分成立，因为基变换矩阵可以是任何可逆矩阵 (3.5.9)。

===== Page 119 =====

It follows from the proposition that the two parts of the theorem amount to the same thing. To derive (a) from (b), we suppose given the linear transformation $T$ , and we begin with arbitrary choices of bases for $V$ and $W$ , obtaining a matrix $A$ . Part (b) tells us that there are invertible matrices $P$ and $Q$ such that $A' = Q^{- 1}AP$ has the form (4.2.11). When we use these matrices to change bases in $V$ and $W$ , the matrix $A$ is changed to $A'$ .

由该命题可知，定理的两个部分是等价的。为了从 (b) 推导出 (a)，我们假设给定了线性变换 $T$，并任意选择 $V$ 和 $W$ 的基，得到矩阵 $A$。第 (b) 部分告诉我们存在可逆矩阵 $P$ 和 $Q$，使得 $A' = Q^{-1}AP$ 具有形式 (4.2.11)。当我们使用这些矩阵来改变 $V$ 和 $W$ 中的基时，矩阵 $A$ 就变成了 $A'$。

To derive (b) from (a), we view an arbitrary matrix $A$ as the matrix of the linear transformation "left multiplication by $A$" on column vectors. Then $A$ is the matrix of $T$ with respect to the standard bases of $F^{n}$ and $F^{m}$ , and (a) guarantees the existence of $P$ , $Q$ so that $Q^{- 1}AP$ has the form (4.2.11).

为了从 (a) 推导出 (b)，我们将任意矩阵 $A$ 视为列向量上的线性变换“左乘 $A$”的矩阵。那么 $A$ 就是 $T$ 关于 $F^{n}$ 和 $F^{m}$ 的标准基的矩阵，而 (a) 保证了存在 $P$ 和 $Q$，使得 $Q^{-1}AP$ 具有形式 (4.2.11)。

We also learn something remarkable about matrix multiplication here, because left multiplication by a matrix is a linear transformation. Left multiplication by an arbitrary matrix $A$ is the same as left multiplication by a matrix of the form (4.2.11), but with reference to different coordinates.

我们在这里还学到了关于矩阵乘法的某些显著事实，因为矩阵的左乘是一个线性变换。任意矩阵 $A$ 的左乘等同于形如 (4.2.11) 的矩阵的左乘，但参考的是不同的坐标。

In the future, we will often state a result in two equivalent ways, a vector space form and a matrix form, without stopping to show that the two forms are equivalent. Then we will present whichever proof seems simpler to write down.

在以后，我们通常会以两种等价的方式陈述一个结果：向量空间形式和矩阵形式，而不会停下来证明这两种形式是等价的。然后我们将给出看起来更容易写下的那种证明。

We can use Theorem 4.2.10 to derive another interesting property of matrix multiplication. Let $N$ and $U$ denote the nullspace and column space of the transformation $A: F^{n} \to F^{m}$ . So $N$ is a subspace of $F^{n}$ and $U$ is a subspace of $F^{m}$ . Let $k$ and $r$ denote the dimensions of $N$ and $U$ . So $k$ is the nullity of $A$ and $r$ is its rank.

我们可以使用定理 4.2.10 推导出矩阵乘法的另一个有趣性质。设 $N$ 和 $U$ 分别表示变换 $A: F^{n}\to F^{m}$ 的零空间和列空间。所以 $N$ 是 $F^{n}$ 的子空间，$U$ 是 $F^{m}$ 的子空间。设 $k$ 和 $r$ 分别表示 $N$ 和 $U$ 的维数。因此 $k$ 是 $A$ 的零度，$r$ 是它的秩。

Left multiplication by the transpose matrix $A^{t}$ defines a transformation $A^{t}: F^{m} \to F^{n}$ in the opposite direction, and therefore two more subspaces, the nullspace $N_{1}$ and the column space $U_{1}$ of $A^{t}$ . Here $U_{1}$ is a subspace of $F^{n}$ , and $N_{1}$ is a subspace of $F^{m}$ . Let $k_{1}$ and $r_{1}$ denote the dimensions of $N_{1}$ and $U_{1}$ , respectively. Theorem 4.1.6 tells us that $k + r = n$ , and also that $k_{1} + r_{1} = m$ . Theorem 4.2.14 below gives one more relation among these integers:

左乘转置矩阵 $A^{t}$ 定义了相反方向的变换 $A^{t}: F^{m}\to F^{n}$，因此又多了两个子空间：$A^{t}$ 的零空间 $N_{1}$ 和列空间 $U_{1}$。这里 $U_{1}$ 是 $F^{n}$ 的子空间，$N_{1}$ 是 $F^{m}$ 的子空间。设 $k_{1}$ 和 $r_{1}$ 分别表示 $N_{1}$ 和 $U_{1}$ 的维数。定理 4.1.6 告诉我们 $k+r=n$，并且 $k_{1}+r_{1}=m$。下面的定理 4.2.14 给出了这些整数之间的另一个关系：

Theorem 4.2.14 With the above notation, $r_{1} = r$ : The rank of a matrix is equal to the rank of its transpose.

定理 4.2.14 使用上述记号，$r_{1}=r$：矩阵的秩等于其转置的秩。

Proof. Let $P$ and $Q$ be invertible matrices such that $A' = Q^{- 1}AP$ has the form (4.2.11). We begin by noting that the assertion is obvious for the matrix $A'$ . Next, we examine the diagrams

证明。设 $P$ 和 $Q$ 是可逆矩阵，使得 $A' = Q^{-1}AP$ 具有形式 (4.2.11)。我们首先注意到，对于矩阵 $A'$，该断言是显然的。接下来，我们检查下面的图表：

$$\begin{array}{r}\underbrace{F^{n}\underbrace{A}_{P}\underbrace{F^{m}}_{Q}}_{F^{n}\underbrace{A^{\prime}}_{F^{m}}}\underbrace{F^{n}\underbrace{A^{\prime}}_{F^{n}}\underbrace{F^{m}}_{F^{n}\underbrace{A^{\prime}}_{F^{m}}}}\end{array} \quad (4.2.15)$$

The vertical arrows are bijective maps. Therefore, in the left- hand diagram, $Q$ carries the column space of $A'$ (the image of multiplication by $A'$ ) bijectively to the column space of $A$ . The dimensions of these two column spaces, the ranks of $A$ and $A'$ , are equal. Similarly, the ranks of $A'$ and $A'^{t}$ are equal. So to prove the theorem, we may replace the matrix $A$ by $A'$ . This reduces the proof to the trivial case of the matrix (4.2.11).

垂直箭头是双射。因此，在左侧的图中，$Q$ 将 $A'$ 的列空间（左乘 $A'$ 的像）双射地映到 $A$ 的列空间。这两个列空间的维数，即 $A$ 和 $A'$ 的秩，相等。类似地，$A'$ 和 $A'^{t}$ 的秩也相等。因此，为了证明定理，我们可以用 $A'$ 替换矩阵 $A$。这便将证明归结为矩阵 (4.2.11) 的平凡情形。

===== Page 120 =====

We can reinterpret the rank $r_1$ of the transpose matrix $A^1$ . By definition, it is the dimension of the space spanned by the columns of $A^1$ , and this can equally well be thought of as the dimension of the space of row vectors spanned by the rows of $A$ . Because of this, people often refer to $r_1$ as the row rank of $A$ , and to $r$ as the column rank.

我们可以重新解释转置矩阵 $A^{t}$ 的秩 $r_{1}$。根据定义，它是 $A^{t}$ 的列张成的空间的维数，这同样可以被认为是 $A$ 的行张成的行向量空间的维数。因此，人们通常称 $r_{1}$ 为 $A$ 的行秩，称 $r$ 为列秩。

The row rank is the maximal number of independent rows of the matrix, and the column rank is the maximal number of independent columns. Theorem 4.2.14 can be stated this way:

行秩是矩阵的线性无关行的最大数目，列秩是线性无关列的最大数目。定理 4.2.14 可以这样表述：

Corollary 4.2.16 The row rank and the column rank of an $m\times n$ matrix $A$ are equal.

推论 4.2.16 $m\times n$ 矩阵 $A$ 的行秩和列秩相等。

### 4.3 LINEAR OPERATORS

### 4.3 线性算子

In this section, we study linear transformations $T:V\to V$ that map a vector space to itself. They are called linear operators. Left multiplication by a (square) $n\times n$ matrix with entries in a field $F$ defines a linear operator on the space $F^{n}$ of column vectors.

在本节中，我们研究将向量空间映射到自身的线性变换 $T:V\to V$。它们被称为线性算子。左乘一个元素在域 $F$ 中的（方）$n\times n$ 矩阵定义了列向量空间 $F^{n}$ 上的一个线性算子。

For example, let $c = \cos \theta$ and $s = \sin \theta$ . The rotation matrix (4.2.2)

例如，设 $c=\cos\theta, s=\sin\theta$。旋转矩阵 (4.2.2)

equation[[453, 371, 546, 415]]

is a linear operator on the plane $\mathbb{R}^2$

是平面 $\mathbb{R}^{2}$ 上的一个线性算子。

The dimension formula $\dim (\ker T) + \dim (\operatorname {im}T) = \dim V$ is valid for linear operators. But here, since the domain and range are equal, we have extra information that can be combined with the formula. Both the kernel and the image of $T$ are subspaces of $V$ .

维数公式 $\dim(\ker T) + \dim(\operatorname{im}T) = \dim V$ 对线性算子也成立。但在这里，由于定义域和值域相同，我们有了可以与该公式结合使用的额外信息。$T$ 的核和像都是 $V$ 的子空间。

Proposition 4.3.1 Let $K$ and $W$ denote the kernel and image, respectively, of a linear operator $T$ on a finite- dimensional vector space $V$ .

命题 4.3.1 设 $K$ 和 $W$ 分别表示有限维向量空间 $V$ 上线性算子 $T$ 的核和像。

(a) The following conditions are equivalent:

(a) 以下条件等价：

$T$ is bijective, $K = \{0\}$ $W = V$

$T$ 是双射 $\iff$ $K = \{0\}$ $\iff$ $W = V$

(b) The following conditions are equivalent:

(b) 以下条件等价：

$V$ is the direct sum $K\oplus W$ $K\cap W = \{0\}$ $K + W = V$

$V$ 是直和 $K\oplus W$ $\iff$ $K\cap W = \{0\}$ $\iff$ $K + W = V$

Proof. (a) $T$ is bijective if and only if the kernel $K$ is zero and the image $W$ is the whole space $V$ . If the kernel is zero, the dimension formula tells us that $\dim W = \dim V$ , and therefore $W = V$ . Similarly, if $W = V$ , the dimension formula shows that $\dim K = 0$ , and therefore $K = 0$ . In both cases, $T$ is bijective.

证明。(a) $T$ 是双射当且仅当核 $K$ 为零且像 $W$ 是整个空间 $V$。如果核为零，维数公式告诉我们 $\dim W = \dim V$，因此 $W = V$。类似地，如果 $W = V$，维数公式表明 $\dim K = 0$，因此 $K = 0$。在这两种情况下，$T$ 都是双射。

(b) $V$ is the direct sum $K\oplus W$ if and only if both of the conditions $K\cap W = \{0\}$ and $K + W = V$ hold. If $K\cap W = \{0\}$ , then $K$ and $W$ are independent, so the sum $U = K + W$ is the direct sum $K\oplus W$ , and $\dim U = \dim K + \dim W$ (3.6.6)(a). The dimension formula shows that $\dim U = \dim V$ , so $U = V$ , and this shows that $K\oplus W = V$ . If $K + W = V$ , the dimension formula and Proposition 3.6.6(a) show that $K$ and $W$ are independent, and again, $V$ is the direct sum.

(b) $V$ 是直和 $K\oplus W$ 当且仅当条件 $K\cap W = \{0\}$ 和 $K+W = V$ 同时成立。如果 $K\cap W = \{0\}$，则 $K$ 和 $W$ 是独立的，因此和 $U = K+W$ 是直和 $K\oplus W$，并且 $\dim U = \dim K + \dim W$ (3.6.6)(a)。维数公式表明 $\dim U = \dim V$，所以 $U = V$，这表明 $K\oplus W = V$。如果 $K+W = V$，维数公式和命题 3.6.6(a) 表明 $K$ 和 $W$ 是独立的，同样，$V$ 是直和。

===== Page 121 =====

A linear operator that satisfies the conditions (4.3.1)(a) is called an invertible operator. Its inverse function is also a linear operator. An operator that is not invertible is a singular operator.

满足条件 (4.3.1)(a) 的线性算子称为可逆算子。它的逆函数也是一个线性算子。不可逆的算子称为奇异算子。

The conditions of Proposition 4.3.1(a) are not equivalent when the dimension of $V$ is infinite. For example, let $V = \mathbb{R}^{\infty}$ be the space of infinite row vectors $(a_{1},a_{2},\ldots)$ (see Section 3.7). The kernel of the right shift operator $S^{+}$ , defined by

当 $V$ 的维数无限时，命题 4.3.1(a) 的条件并不等价。例如，设 $V = \mathbb{R}^{\infty}$ 是无限行向量 $(a_{1},a_{2},\ldots)$ 的空间（见第 3.7 节）。右移位算子 $S^{+}$ 定义为

$$S^{+}(a_{1},a_{2},\ldots) = (0,a_{1},a_{2},\ldots),$$

is the zero space, and its image is a proper subspace of $V$ . The kernel of the left shift operator $S^{- }$ , defined by

其核是零空间，而其像是 $V$ 的一个真子空间。左移位算子 $S^{-}$ 定义为

$$S^{-}(a_{1},a_{2},a_{3},\ldots) = (a_{2},a_{3},\ldots),$$

is a proper subspace of $V$ , and its image is the whole space.

其像是整个空间，而核是 $V$ 的一个真子空间。

The discussion of bases in the previous section must be changed slightly when we are dealing with linear operators. We should pick only one basis $\mathbf{B}$ for $V$ , and use it in place of both of the bases $\mathbf{B}$ and $\mathbf{C}$ in (4.2.6). In other words, to define the matrix $A$ of $T$ with respect to the basis $\mathbf{B}$ , we should write

当处理线性算子时，上一节关于基的讨论必须稍作修改。我们应该只为 $V$ 选择一个基 $\mathbf{B}$，并用它来代替 (4.2.6) 中的两个基 $\mathbf{B}$ 和 $\mathbf{C}$。换句话说，为了定义 $T$ 关于基 $\mathbf{B}$ 的矩阵 $A$，我们应该写

$$T(\mathbf{B}) = \mathbf{B}A,\quad \mathrm{and}\quad AX = Y\mathrm{~as~before.} \quad (4.3.3)$$

As with any linear transformation (4.2.7), the columns of $A$ are the coordinate vectors of the images $T(v_{j})$ of the basis vectors:

与任何线性变换 (4.2.7) 一样，$A$ 的列是基向量 $v_{j}$ 的像 $T(v_{j})$ 的坐标向量：

$$T(v_{j}) = v_{1}a_{1j} + \dots +v_{n}a_{nj}. \quad (4.3.4)$$

A linear operator is invertible if and only if its matrix with respect to an arbitrary basis is an invertible matrix.

线性算子可逆当且仅当其关于任意基的矩阵是可逆矩阵。

When one speaks of the the matrix of a linear operator on the space $F^{n}$ , it is assumed that the basis is the standard basis $\mathbf{E}$ , unless a different basis is specified. The operator is then multiplication by that matrix.

当谈到空间 $F^{n}$ 上线性算子的矩阵时，除非指定了不同的基，否则默认基是标准基 $\mathbf{E}$。此时算子就是左乘那个矩阵。

A new feature arises when we study the effect of a change of basis. Suppose that $\mathbf{B}$ is replaced by a new basis $\mathbf{B}^{\prime}$ .

当我们研究基变换的影响时，会出现一个新的特征。假设 $\mathbf{B}$ 被一个新基 $\mathbf{B}'$ 替换。

Proposition 4.3.5 Let $A$ be the matrix of a linear operator $T$ with respect to a basis $\mathbf{B}$ .

命题 4.3.5 设 $A$ 是线性算子 $T$ 关于基 $\mathbf{B}$ 的矩阵。

(a) Suppose that a new basis $\mathbf{B}^{\prime}$ is described by $\mathbf{B}^{\prime} = \mathbf{B}P$ . The matrix that represents $T$ with respect to this basis is $A^{\prime} = P^{-1}AP$ .

(a) 假设新基 $\mathbf{B}'$ 由 $\mathbf{B}' = \mathbf{B}P$ 描述。则 $T$ 关于这个新基的矩阵是 $A' = P^{-1}AP$。

(b) The matrices $A^{\prime}$ that represent the operator $T$ for different bases are the matrices of the form $A^{\prime} = P^{-1}AP$ , where $P$ can be any invertible matrix.

(b) 表示算子 $T$ 关于不同基的矩阵 $A'$ 是那些形如 $A' = P^{-1}AP$ 的矩阵，其中 $P$ 可以是任何可逆矩阵。

In other words, the matrix changes by conjugation. This is a confusing fact to grasp. So, though it follows from (4.2.13), we will rederive it. Since $\mathbf{B}^{\prime} = \mathbf{B}P$ and since $T(\mathbf{B}) = \mathbf{B}A$ , we have

换句话说，矩阵通过共轭改变。这是一个难以理解的事实。因此，尽管它可以从 (4.2.13) 推出，我们还是重新推导一下。因为 $\mathbf{B}' = \mathbf{B}P$ 且 $T(\mathbf{B}) = \mathbf{B}A$，我们有

$$T(\mathbf{B}^{\prime}) = T(\mathbf{B})P = \mathbf{B}AP.$$

We are not done. The formula we have obtained expresses $T(\mathbf{B}^{\prime})$ in terms of the old basis $\mathbf{B}$ . To obtain the new matrix, we must write $T(\mathbf{B}^{\prime})$ in terms of the new basis $\mathbf{B}^{\prime}$ . So we substitute $\mathbf{B} = \mathbf{B}^{\prime}P^{- 1}$ into the equation. Doing so gives us $T(\mathbf{B}^{\prime}) = \mathbf{B}^{\prime}P^{- 1}AP$ .

我们还没完成。我们得到的公式是用旧基 $\mathbf{B}$ 来表示 $T(\mathbf{B}')$。为了得到新矩阵，我们必须用新基 $\mathbf{B}'$ 来表示 $T(\mathbf{B}')$。因此我们将 $\mathbf{B} = \mathbf{B}'P^{-1}$ 代入方程。这样得到 $T(\mathbf{B}') = \mathbf{B}'P^{-1}AP$。

===== Page 122 =====

In general, we say that a square matrix $A$ is similar to another matrix $A^{\prime}$ if $A^{\prime} = P^{- 1}AP$ for some invertible matrix $P$ . Such a matrix $A^{\prime}$ is obtained from $A$ by conjugating by $P^{- 1}$ and since $P$ can be any invertible matrix, $P^{- 1}$ is also arbitrary. It would be correct to use the term conjugate in place of similar.

一般来说，如果存在可逆矩阵 $P$ 使得 $A' = P^{-1}AP$，我们就说方阵 $A$ 相似于另一个矩阵 $A'$。这样的矩阵 $A'$ 是通过用 $P^{-1}$ 对 $A$ 进行共轭得到的，并且由于 $P$ 可以是任何可逆矩阵，$P^{-1}$ 也是任意的。使用术语“共轭”来代替“相似”也是正确的。

Now if we are given the matrix $A$ , it is natural to look for a similar matrix $A^{\prime}$ that is particularly simple. One would like to get a result somewhat like Theorem 4.2.10. But here our allowable change is much more restricted, because we have only one basis, and therefore one matrix $P$ , to work with. Having domain and range of a linear transformation equal, which seems at first to be a simplification, actually makes things more difficult.

现在，给定矩阵 $A$，很自然地会寻找一个特别简单的相似矩阵 $A'$。人们希望得到类似于定理 4.2.10 的结果。但这里允许的变换受到更多限制，因为我们只有一个基，因此只有一个矩阵 $P$ 可供使用。线性变换的定义域和值域相等，这起初看似简化了问题，实际上却使事情变得更加困难。

We can get some insight into the problem by writing the hypothetical basechange matrix as a product of elementary matrices, say $P = E_{1}\dots E_{r}$ . Then

我们可以通过将假设的基变换矩阵写成初等矩阵的乘积来获得一些洞察，例如 $P = E_{1}\dots E_{r}$。那么

$$P^{-1}AP = E_{r}^{-1}\dots E_{1}^{-1}A E_{1}\dots E_{r}.$$

In terms of elementary operations, we are allowed to change $A$ by a sequence of steps $A\hookrightarrow E^{- 1}AE$ . In other words, we may perform an arbitrary column operation $E$ on $A$ but we must also make the row operation that corresponds to the inverse matrix $E^{- 1}$ . Unfortunately, these row and column operations interact, and analyzing them becomes confusing.

就初等运算而言，我们被允许通过一系列步骤 $A \mapsto E^{-1}AE$ 来改变 $A$。换句话说，我们可以对 $A$ 执行任意的列运算 $E$，但还必须执行对应于逆矩阵 $E^{-1}$ 的行运算。不幸的是，这些行和列运算是相互影响的，分析它们变得混乱。

### 4.4 EIGENVECTORS

### 4.4 特征向量

The main tools for analyzing a linear operator $T:V\to V$ are invariant subspaces and eigenvectors.

分析线性算子 $T:V\to V$ 的主要工具是不变子空间和特征向量。

A subspace $W$ of $V$ is invariant, or more precisely $T$ - invariant, if it is carried to itself by the operator:

$V$ 的子空间 $W$ 称为不变的，或者更精确地说 $T$-不变的，如果它被算子映射到自身：

$$T W\subset W. \quad (4.4.1)$$

In other words, $W$ is invariant if, whenever $w$ is in $W$ , $T(w)$ is also in $W$ . When this is so, $T$ defines a linear operator on $W$ , called its restriction to $W$ . We often denote this restriction by $T|w$ .

换句话说，如果每当 $w\in W$ 时，$T(w)\in W$，则 $W$ 是不变的。当这种情况发生时，$T$ 定义了 $W$ 上的一个线性算子，称为 $T$ 在 $W$ 上的限制。我们通常将这个限制记为 $T|_{W}$。

If $W$ is a $T$ - invariant subspace, we may form a basis $\mathbf{B}$ of $V$ by appending vectors to a basis $(w_{1},\ldots ,w_{k})$ of $W$ , say

如果 $W$ 是一个 $T$-不变子空间，我们可以通过将向量附加到 $W$ 的一组基 $(w_{1},\ldots,w_{k})$ 上来形成 $V$ 的一组基 $\mathbf{B}$，例如

$$\mathbf{B} = (w_{1},\ldots ,w_{k};v_{1},\ldots ,v_{n - k}). \quad (4.4.2)$$

Then the fact that $W$ is invariant is reflected in the matrix of $T$ . The columns of this matrix, we'll call it $M$ , are the coordinate vectors of the image vectors (see (4.3.3)). But $T(w_{j})$ is in the subspace $W$ , so it is a linear combination of the basis $(w_{1},\ldots ,w_{k})$ . When we write $T(w_{j})$ in terms of the basis $\mathbf{B}$ , the coefficients of the vectors $v_{1},\ldots ,v_{n - k}$ will be zero. It follows that $M$ will have the block form

那么 $W$ 的不变性将反映在 $T$ 的矩阵中。这个矩阵（我们称之为 $M$）的列是像向量的坐标向量（见 (4.3.3)）。但 $T(w_{j})$ 在子空间 $W$ 中，因此它是基 $(w_{1},\ldots,w_{k})$ 的线性组合。当我们用基 $\mathbf{B}$ 表示 $T(w_{j})$ 时，向量 $v_{1},\ldots,v_{n-k}$ 的系数将为零。由此可知，$M$ 将具有分块形式

$$M = \left[ \begin{array}{cc}A & B\\ 0 & D \end{array} \right], \quad (4.4.3)$$

where $A$ is a $k\times k$ matrix, the matrix of the restriction of $T$ to $W$ .

其中 $A$ 是一个 $k\times k$ 矩阵，是 $T$ 在 $W$ 上的限制的矩阵。

===== Page 123 =====

If $V$ happens to be the direct sum $W_{1} \oplus W_{2}$ of two $T$ - invariant subspaces, and if we make a basis $\mathbf{B} = (\mathbf{B}_{1}, \mathbf{B}_{2})$ of $V$ by appending bases of $W_{1}$ and $W_{2}$ , the matrix of $T$ will have the block diagonal form

如果 $V$ 恰好是两个 $T$-不变子空间 $W_{1}$ 和 $W_{2}$ 的直和 $W_{1}\oplus W_{2}$，并且我们通过将 $W_{1}$ 和 $W_{2}$ 的基附加在一起来构成 $V$ 的基 $\mathbf{B}=(\mathbf{B}_{1},\mathbf{B}_{2})$，那么 $T$ 的矩阵将具有分块对角形式

equation[[411, 155, 583, 199]]

where $A_{i}$ is the matrix of the restriction of $T$ to $W_{i}$ .

其中 $A_{i}$ 是 $T$ 在 $W_{i}$ 上的限制的矩阵。

The concept of an eigenvector is closely related to that of an invariant subspace.

特征向量的概念与不变子空间的概念密切相关。

An eigenvector $\upsilon$ of a linear operator $T$ is a nonzero vector such that

线性算子 $T$ 的特征向量 $\upsilon$ 是一个非零向量，使得

$$T(\upsilon) = \lambda \upsilon \quad (4.4.5)$$

for some scalar $\lambda$ , i.e., some element of $F$ . A nonzero column vector is an eigenvector of a square matrix $A$ if it is an eigenvector for the operation of left multiplication by $A$ .

其中 $\lambda$ 是某个标量，即 $F$ 中的某个元素。如果一个非零列向量是左乘 $A$ 这一运算的特征向量，那么它就是方阵 $A$ 的特征向量。

The scalar $\lambda$ that appears in (4.4.5) is called the eigenvalue associated to the eigenvector $\upsilon$ . When we speak of an eigenvalue of a linear operator $T$ or of a matrix $A$ without specifying an eigenvector, we mean a scalar $\lambda$ that is the eigenvalue associated to some eigenvector. An eigenvalue may be any element of $F$ , including zero, but an eigenvector is not allowed to be zero. Eigenvalues are often denoted, as here, by the Greek letter $\lambda$ (lambda).

出现在 (4.4.5) 中的标量 $\lambda$ 被称为与特征向量 $\upsilon$ 相关联的特征值。当我们谈论线性算子 $T$ 或矩阵 $A$ 的特征值而不指定特征向量时，我们指的是某个特征向量所关联的标量 $\lambda$。特征值可以是 $F$ 中的任何元素，包括零，但特征向量不允许为零。特征值通常像这里一样用希腊字母 $\lambda$（lambda）表示。

An eigenvector with eigenvalue 1 is a fixed vector: $T(\upsilon) = \upsilon$ . An eigenvector with eigenvalue zero is in the nullspace: $T(\upsilon) = 0$ . When $V = \mathbb{R}^{n}$ , a nonzero vector $\upsilon$ is an eigenvector if $\upsilon$ and $T(\upsilon)$ are parallel.

特征值为 1 的特征向量是固定向量：$T(\upsilon)=\upsilon$。特征值为零的特征向量在零空间中：$T(\upsilon)=0$。当 $V=\mathbb{R}^{n}$ 时，非零向量 $\upsilon$ 是特征向量当且仅当 $\upsilon$ 和 $T(\upsilon)$ 平行。

If $\upsilon$ is an eigenvector of a linear operator $T$ , with eigenvalue $\lambda$ , the subspace $W$ spanned by $\upsilon$ will be $T$ - invariant, because $T(\upsilon) = c\lambda \upsilon$ is in $W$ for all scalars $c$ . Conversely, if the one- dimensional subspace spanned by $\upsilon$ is invariant, then $\upsilon$ is an eigenvector. So an eigenvector can be described as a basis of a one- dimensional invariant subspace.

如果 $\upsilon$ 是线性算子 $T$ 的具有特征值 $\lambda$ 的特征向量，那么由 $\upsilon$ 张成的子空间 $W$ 将是 $T$-不变的，因为对所有标量 $c$，$T(c\upsilon)=c\lambda\upsilon\in W$。反之，如果由 $\upsilon$ 张成的一维子空间是不变的，那么 $\upsilon$ 是特征向量。因此，特征向量可以被描述为一维不变子空间的一组基。

It is easy to tell whether or not a given vector $X$ is an eigenvector of a matrix $A$ . We simply check whether or not $AX$ is a multiple of $X$ . And, if $A$ is the matrix of $T$ with respect to a basis $\mathbf{B}$ , and if $X$ is the coordinate vector of a vector $\upsilon$ , then $X$ is an eigenvector of $A$ if and only if $\upsilon$ is an eigenvector for $T$ .

判断给定向量 $X$ 是否是矩阵 $A$ 的特征向量很容易。我们只需检查 $AX$ 是否是 $X$ 的倍数。此外，如果 $A$ 是 $T$ 关于基 $\mathbf{B}$ 的矩阵，并且 $X$ 是向量 $\upsilon$ 的坐标向量，那么 $X$ 是 $A$ 的特征向量当且仅当 $\upsilon$ 是 $T$ 的特征向量。

The standard basis vector $e_{1} = (1, 0)^{\mathrm{t}}$ is an eigenvector, with eigenvalue 3, of the matrix

标准基向量 $e_{1}=(1,0)^{\mathrm{t}}$ 是矩阵

equation[[453, 732, 545, 778]]

的特征向量，特征值为 3。

The vector $(1, - 1)^{\mathrm{t}}$ is another eigenvector, with eigenvalue 2. The vector $(0,1,1)^{\mathrm{t}}$ is an eigenvector, with eigenvalue 2, of the matrix

向量 $(1,-1)^{\mathrm{t}}$ 是另一个特征向量，特征值为 2。向量 $(0,1,1)^{\mathrm{t}}$ 是矩阵

===== Page 124 =====

的特征向量，特征值为 2。

If $(\upsilon_{1},\ldots ,\upsilon_{n})$ is a basis of $V$ and if $\upsilon_{1}$ is an eigenvector of a linear operator $T$ ,the matrix of $T$ will have the block form

如果 $(\upsilon_{1},\ldots,\upsilon_{n})$ 是 $V$ 的一组基，并且 $\upsilon_{1}$ 是线性算子 $T$ 的一个特征向量，那么 $T$ 的矩阵将具有分块形式

equation[[64, 130, 656, 231]]

where $\lambda$ is the eigenvalue of $\upsilon_{1}$ . This is the block form (4.4.3) in the case of an invariant subspace of dimension 1.

其中 $\lambda$ 是 $\upsilon_{1}$ 的特征值。这是一维不变子空间情况下的分块形式 (4.4.3)。

Proposition 4.4.7 Similar matrices $(A^{\prime} = P^{- 1}AP)$ have the same eigenvalues.

命题 4.4.7 相似矩阵 $(A' = P^{-1}AP)$ 具有相同的特征值。

This is true because similar matrices represent the same linear transformation.

这是因为相似矩阵表示相同的线性变换。

## Proposition 4.4.8

## 命题 4.4.8

(a) Let $T$ be a linear operator on a vector space $V$ . The matrix of $T$ with respect to a basis $\mathbf{B} = (\upsilon_{1},\ldots ,\upsilon_{n})$ is diagonal if and only if each of the basis vectors $\upsilon_{j}$ is an eigenvector.

(a) 设 $T$ 是向量空间 $V$ 上的一个线性算子。$T$ 关于基 $\mathbf{B}=(\upsilon_{1},\ldots,\upsilon_{n})$ 的矩阵是对角矩阵当且仅当每个基向量 $\upsilon_{j}$ 都是特征向量。

(b) An $n\times n$ matrix $A$ is similar to a diagonal matrix if and only if there is a basis of $F^{n}$ that consists of eigenvectors.

(b) $n\times n$ 矩阵 $A$ 相似于一个对角矩阵当且仅当 $F^{n}$ 存在一组由特征向量组成的基。

This follows from the definition of the matrix $A$ (see (4.3.4)). If $T(\upsilon_{j}) = \lambda_{j}\upsilon_{j}$ , then

这由矩阵 $A$ 的定义（见 (4.3.4)）得出。如果 $T(\upsilon_{j}) = \lambda_{j}\upsilon_{j}$，则

$$T(\mathbf{B}) = (\upsilon_{1}\lambda_{1},\ldots \upsilon_{n}\lambda_{n}) = (\upsilon_{1},\ldots ,\upsilon_{n})\left[ \begin{array}{ccc}\lambda_{1} & & \\ & \ddots & \\ & & \lambda_{n} \end{array} \right]. \quad (4.4.9)$$

This proposition shows that we can represent a linear operator simply by a diagonal matrix, provided that it has enough eigenvectors. We will see in Section 4.5 that every linear operator on a complex vector space has at least one eigenvector, and in Section 4.6 that in most cases there is a basis of eigenvectors. But a linear operator on a real vector space needn't have any eigenvector. For example, a rotation of the plane through an angle $\theta$ doesn't carry any vector to a parallel one unless $\theta$ is 0 or $\pi$ . The rotation matrix (4.2.2) with $\theta \neq 0$ , $\pi$ has no real eigenvector.

该命题表明，只要线性算子有足够多的特征向量，我们就可以用一个简单的对角矩阵来表示它。我们将在第 4.5 节看到，复向量空间上的每个线性算子至少有一个特征向量，并且在第 4.6 节看到，在大多数情况下存在一组由特征向量组成的基。但是实向量空间上的线性算子不一定有特征向量。例如，平面旋转一个角度 $\theta$ 不会将任何向量映射到平行向量，除非 $\theta = 0$ 或 $\pi$。旋转矩阵 (4.2.2) 当 $\theta\neq 0,\pi$ 时没有实特征向量。

A general example of a real matrix that has at least one real eigenvalue is one all of whose entries are positive. Such matrices, called positive matrices, occur often in applications, and one of their most important properties is that they always have an eigenvector whose coordinates are positive (a positive eigenvector).

一个至少有一个实特征值的实矩阵的常见例子是其所有元素均为正数的矩阵。这样的矩阵称为正矩阵，经常出现在应用中，它们最重要的性质之一是始终有一个坐标全为正的特征向量（正特征向量）。

Instead of proving this fact, we'll illustrate it by examining the effect of multiplication by a positive $2\times 2$ matrix $A$ on $\mathbb{R}^{2}$ . Let $w_{i} = A e_{i}$ be the columns of $A$ . The parallelogram law for vector addition shows that $A$ sends the first quadrant $S$ to the sector bounded by the vectors $w_{1}$ and $w_{2}$ . The coordinate vector of $w_{i}$ is the $i$ th column of $A$ . Since the entries of

我们不打算证明这个事实，而是通过考察左乘一个正 $2\times 2$ 矩阵 $A$ 对 $\mathbb{R}^{2}$ 的影响来说明。令 $w_{i}=A e_{i}$ 为 $A$ 的列。向量加法的平行四边形法则表明，$A$ 将第一象限 $S$ 映到由向量 $w_{1}$ 和 $w_{2}$ 张成的扇形区域。$w_{i}$ 的坐标向量是 $A$ 的第 $i$ 列。由于

===== Page 125 =====

$A$ are positive, this sector lies inside $S$ , as illustrated below for the matrix $A = \left[ \begin{array}{cc}3 & 2 \\ 1 & 4 \end{array} \right]$ . So we have

$A$ 的元素为正，这个扇形区域位于 $S$ 内部，如下面的矩阵 $A = \begin{bmatrix} 3 & 2 \\ 1 & 4 \end{bmatrix}$ 所示。因此我们有

(4.4.10)

$$S\supset A S\supset A^{2}S\supset A^{3}S\supset \ldots ,$$

as is illustrated below for the matrix $A = \left[ \begin{array}{cc}3 & 2 \\ 1 & 4 \end{array} \right]$ .

如下面的矩阵 $A = \begin{bmatrix} 3 & 2 \\ 1 & 4 \end{bmatrix}$ 所示。

Now, the intersection of a nested set of sectors is either a sector or a half- line. In our case, the intersection $Z = \bigcap A^{r}S$ turns out to be a half- line. This is intuitively plausible, and it can be shown in various ways, but we'll omit the proof. We multiply the relation $Z = \bigcap A^{r}S$ on both sides by $A$ :

现在，嵌套扇形族的交集要么是一个扇形，要么是一条射线。在我们的例子中，交集 $Z = \bigcap A^{r}S$ 结果是一条射线。这在直觉上是合理的，并且可以用多种方式证明，但我们将省略证明。我们将关系式 $Z = \bigcap A^{r}S$ 两边左乘 $A$：

$$A Z = A\left(\bigcap_{0}^{\infty}A^{r}S\right) = \bigcap_{1}^{\infty}A^{r}S = Z.$$

Hence $Z = AZ$ . Therefore the nonzero vectors in $Z$ are eigenvectors.

因此 $Z = AZ$。所以 $Z$ 中的非零向量是特征向量。

image[[136, 417, 852, 585]]

(4.4.11) Images of the First Quadrant Under Repeated Multiplication by a Positive Matrix.

(4.4.11) 第一象限在正矩阵重复乘法下的像。

### 4.5 THE CHARACTERISTIC POLYNOMIAL

### 4.5 特征多项式

In this section we determine the eigenvectors of an arbitrary linear operator. We recall that an eigenvector of a linear operator $T$ is a nonzero vector $v$ such that

在本节中，我们将确定任意线性算子的特征向量。我们回忆一下，线性算子 $T$ 的特征向量是一个非零向量 $v$，使得

$$T(v) = \lambda v, \quad (4.5.1)$$

for some $\lambda$ in $F$ . If we don't know $\lambda$ , it can be difficult to find the eigenvector directly when the matrix of the operator is complicated. The trick is to solve a different problem, namely to determine the eigenvalues first. Once an eigenvalue $\lambda$ is determined, equation (4.5.1) becomes linear in the coordinates of $v$ , and solving it presents no problem.

其中 $\lambda\in F$。如果我们不知道 $\lambda$，当算子的矩阵很复杂时，直接找到特征向量可能很困难。技巧是解决另一个问题，即首先确定特征值。一旦确定了特征值 $\lambda$，方程 (4.5.1) 就变成了关于 $v$ 坐标的线性方程，求解它就没有问题了。

We begin by writing (4.5.1) in the form

我们首先将 (4.5.1) 写成

$$[\lambda I - T](v) = 0, \quad (4.5.2)$$

===== Page 126 =====

where $I$ stands for the identity operator and $\lambda I - T$ is the linear operator defined by

其中 $I$ 表示恒等算子，$\lambda I - T$ 是由下式定义的线性算子

$$[\lambda I - T](v) = \lambda v - T(v). \quad (4.5.3)$$

It is easy to check that $\lambda I - T$ is indeed a linear operator. We can restate (4.5.2) as follows:

很容易验证 $\lambda I - T$ 确实是一个线性算子。我们可以将 (4.5.2) 重述如下：

(4.5.4)

A nonzero vector $v$ is an eigenvector with eigenvalue $\lambda$ if and only if it is in the kernel of $\lambda I - T$ .

非零向量 $v$ 是特征值为 $\lambda$ 的特征向量当且仅当它属于 $\lambda I - T$ 的核。

Corollary 4.5.5 Let $T$ be a linear operator on a finite- dimensional vector space $V$ .

推论 4.5.5 设 $T$ 是有限维向量空间 $V$ 上的一个线性算子。

(a) The eigenvalues of $T$ are the scalars $\lambda$ in $F$ such that the operator $\lambda I - T$ is singular, i.e., its nullspace is not zero.

(a) $T$ 的特征值是 $F$ 中的标量 $\lambda$，使得算子 $\lambda I - T$ 是奇异的，即它的零空间非零。

(b) The following conditions are equivalent:

(b) 以下条件等价：

$T$ is a singular operator. $T$ has an eigenvalue equal to zero. If $A$ is the matrix of $T$ with respect to an arbitrary basis, then $\operatorname *{det}A = 0$

$T$ 是奇异算子 $\iff$ $T$ 有等于零的特征值 $\iff$ 如果 $A$ 是 $T$ 关于任意基的矩阵，则 $\det A = 0$

If $A$ is the matrix of $T$ with respect to some basis, then the matrix of $\lambda I - T$ is $\lambda I - A$ . So $\lambda I - T$ is singular if and only if $\operatorname *{det}(\lambda I - A) = 0$ . This determinant can be computed with indeterminate $\lambda$ , and doing so provides us, at least in principle, with a method for determining the eigenvalues and eigenvectors.

如果 $A$ 是 $T$ 关于某个基的矩阵，那么 $\lambda I - T$ 的矩阵是 $\lambda I - A$。因此 $\lambda I - T$ 是奇异的当且仅当 $\det(\lambda I - A) = 0$。这个行列式可以用未定元 $\lambda$ 计算，这样做至少原则上为我们提供了一种确定特征值和特征向量的方法。

Suppose for example that $A$ is the matrix $\left[ \begin{array}{cc}3 & 2 \\ 1 & 4 \end{array} \right]$ whose action on $\mathbb{R}^2$ is illustrated in Figure (4.4.11). Then

例如，假设 $A$ 是矩阵 $\begin{bmatrix} 3 & 2 \\ 1 & 4 \end{bmatrix}$，它对 $\mathbb{R}^{2}$ 的作用如图 (4.4.11) 所示。那么

equation[[386, 543, 614, 586]]

and

且

$$\operatorname *{det}(\lambda I - A) = \lambda^2 -7\lambda +10 = (\lambda -5)(\lambda -2).$$

The determinant vanishes when $\lambda = 5$ or 2, so the eigenvalues of $A$ are 5 and 2. To find the eigenvectors, we solve the two systems of equations $[5I - A]X = 0$ and $[2I - A]X = 0$ . The solutions are determined up to scalar factor:

当 $\lambda = 5$ 或 2 时行列式为零，因此 $A$ 的特征值是 5 和 2。为了找到特征向量，我们解两个方程组 $[5I - A]X = 0$ 和 $[2I - A]X = 0$。解由标量因子确定：

$$v_{1} = \left[ \begin{array}{c}1\\ 1 \end{array} \right],\quad v_{2} = \left[ \begin{array}{c}2\\ -1 \end{array} \right]. \quad (4.5.6)$$

We now consider the same computation for an indeterminate matrix of arbitrary size. It is customary to replace the symbol $\lambda$ by a variable $t$ . We form the matrix $tI - A$ :

现在我们考虑对任意大小的未定元矩阵进行相同的计算。通常用变量 $t$ 替换符号 $\lambda$。我们形成矩阵 $tI - A$：

$$tI - A = \left[ \begin{array}{cccc}(t - a_{11}) & -a_{12} & \dots & -a_{1n}\\ -a_{21} & (t - a_{22}) & \dots & -a_{2n}\\ \vdots & \vdots & \ddots & \vdots \\ -a_{n1} & \dots & \dots & (t - a_{nn}) \end{array} \right]. \quad (4.5.7)$$

The complete expansion of the determinant [Chapter 1 (1.6.4)] shows that $\operatorname *{det}(tI - A)$ is a polynomial of degree $n$ in $t$ whose coefficients are scalars, elements of $F$ .

行列式的完全展开 [第 1 章 (1.6.4)] 表明 $\det(tI - A)$ 是 $t$ 的一个 $n$ 次多项式，其系数是标量，即 $F$ 中的元素。

===== Page 127 =====

(4.5.8) The characteristic polynomial of a linear operator $T$ is the polynomial

(4.5.8) 线性算子 $T$ 的特征多项式是

$$p(t) = \operatorname *{det}(tI - A),$$

where $A$ is the matrix of $T$ with respect to some basis.

其中 $A$ 是 $T$ 关于某个基的矩阵。

The eigenvalues of $T$ are determined by combining (4.5.5) and (4.5.8):

结合 (4.5.5) 和 (4.5.8) 可以确定 $T$ 的特征值：

(4.5.9) The eigenvalues of a linear operator are the roots of its characteristic polynomial.

(4.5.9) 线性算子的特征值是其特征多项式的根。

(4.5.10) Let $A$ be an upper or lower triangular $n\times n$ matrix with diagonal entries $a_{11},\ldots ,a_{nn}$ . The characteristic polynomial of $A$ is $(t - a_{11})\cdot \cdot \cdot (t - a_{nn})$ . The diagonal entries of $A$ are its eigenvalues.

(4.5.10) 设 $A$ 是一个上三角或下三角 $n\times n$ 矩阵，其对角元为 $a_{11},\ldots,a_{nn}$。则 $A$ 的特征多项式是 $(t - a_{11})\cdots(t - a_{nn})$。$A$ 的对角元就是它的特征值。

If $A$ is upper triangular, so is $tI - A$ , and the diagonal entries of $tI - A$ are $t - a_{ii}$ . The determinant of a triangular matrix is the product of its diagonal entries.

如果 $A$ 是上三角矩阵，那么 $tI - A$ 也是上三角矩阵，且 $tI - A$ 的对角元是 $t - a_{ii}$。三角矩阵的行列式是其对角元的乘积。

(4.5.11) The characteristic polynomial of an operator $T$ does not depend on the choice of a basis.

(4.5.11) 算子 $T$ 的特征多项式不依赖于基的选择。

Proof. A second basis leads to a matrix $A^{\prime} = P^{- 1}AP$ (4.3.5), and

证明。另一组基给出矩阵 $A' = P^{-1}AP$ (4.3.5)，且

$$tI - A^{\prime} = tI - P^{-1}AP = P^{-1}(tI - A)P.$$

$$\operatorname *{det}(tI - A^{\prime}) = \operatorname *{det}P^{-1}\operatorname *{det}(tI - A)\operatorname *{det}P = \operatorname *{det}(tI - A).$$

The characteristic polynomial of the $2\times 2$ matrix $A = \left[ \begin{array}{cc}a & b\\ c & d \end{array} \right]$ is

$2\times 2$ 矩阵 $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ 的特征多项式是

$$p(t) = \operatorname *{det}(tI - A) = \operatorname *{det}\left[ \begin{array}{cc}t - a & -b\\ -c & t - d \end{array} \right] = t^{2} - (\operatorname {trace}A)t + (\operatorname *{det}A), \quad (4.5.12)$$

where trace $A = a + d$

其中 $\operatorname{trace}A = a + d$。

An incomplete description of the characteristic polynomial of an $n\times n$ matrix is given by the next proposition, which is proved by computation. It wouldn't be very difficult to determine the remaining coefficients, but explicit formulas for them aren't often used.

下面的命题给出了 $n\times n$ 矩阵特征多项式的一个不完整的描述，该命题通过计算证明。确定其余的系数不会非常困难，但它们的显式公式并不常用。

(4.5.13) The characteristic polynomial of an $n\times n$ matrix $A$ has the form

(4.5.13) $n\times n$ 矩阵 $A$ 的特征多项式具有形式

$$p(t) = t^{n} - (\operatorname {trace}A)t^{n - 1} + (\text{intermediate terms}) + (-1)^{n}(\operatorname *{det}A),$$

where trace $A$ , the trace of $A$ , is the sum of its diagonal entries:

其中 $\operatorname{trace}A$，即 $A$ 的迹，是其对角元之和：

$$\operatorname {trace}A = a_{11} + a_{22} + \dots +a_{nn}.$$

(4.5.11) shows that all coefficients of the characteristic polynomial are independent of the basis. For instance, $\operatorname {trace}(P^{- 1}AP) = \operatorname {trace}A$ .

(4.5.11) 表明特征多项式的所有系数都与基无关。例如，$\operatorname{trace}(P^{-1}AP) = \operatorname{trace}A$。

===== Page 128 =====

Since the characteristic polynomial, the trace, and the determinant are independent of the basis, they depend only on the operator $T$ . So we may define the terms characteristic polynomial, trace, and determinant of a linear operator $T$ . They are the ones obtained using the matrix of $T$ with respect to any basis.

由于特征多项式、迹和行列式与基无关，它们仅依赖于算子 $T$。因此我们可以定义线性算子 $T$ 的特征多项式、迹和行列式这些术语。它们就是使用 $T$ 关于任意基的矩阵所得到的那些量。

Proposition 4.5.14 Let $T$ be a linear operator on a finite- dimensional vector space $V$ .

命题 4.5.14 设 $T$ 是有限维向量空间 $V$ 上的一个线性算子。

(a) If $V$ has dimension $n$ , then $T$ has at most $n$ eigenvalues.

(a) 如果 $V$ 的维数为 $n$，则 $T$ 至多有 $n$ 个特征值。

(b) If $F$ is the field of complex numbers and $V \neq \{0\}$ , then $T$ has at least one eigenvalue, and hence at least one eigenvector.

(b) 如果 $F$ 是复数域且 $V \neq \{0\}$，则 $T$ 至少有一个特征值，因此至少有一个特征向量。

Proof. (a) The eigenvalues are the roots of the characteristic polynomial, which has degree $n$ . A polynomial of degree $n$ can have at most $n$ roots. This is true for a polynomial with coefficients in any field $F$ (see (12.2.20)).

证明。(a) 特征值是特征多项式的根，特征多项式是 $n$ 次的。$n$ 次多项式至多有 $n$ 个根。这对于系数在任何域 $F$ 中的多项式都成立（见 (12.2.20)）。

(b) The Fundamental Theorem of Algebra asserts that every polynomial of positive degree with complex coefficients has at least one complex root. There is a proof of this theorem in Chapter 15 (15.10.1).

(b) 代数基本定理断言，每个具有复系数的正次数多项式至少有一个复根。该定理的证明见第 15 章 (15.10.1)。

For example, let $R_{\theta}$ be the matrix (4.2.2) that represents the counterclockwise rotation of $\mathbb{R}^{2}$ through an angle $\theta$ . Its characteristic polynomial, $p(t) = t^{2} - (2\cos \theta)t + 1$ , has no real root provided that $\theta \neq 0$ , $\pi$ , so no real eigenvalue. We have observed this before. But the operator on $\mathbb{C}^{2}$ defined by $R_{\theta}$ does have the complex eigenvalues $e^{\pm i\theta}$ .

例如，设 $R_{\theta}$ 是表示 $\mathbb{R}^{2}$ 逆时针旋转角度 $\theta$ 的矩阵 (4.2.2)。其特征多项式 $p(t) = t^{2} - (2\cos\theta)t + 1$，当 $\theta \neq 0, \pi$ 时没有实根，因此没有实特征值。我们之前已经注意到这一点。但是由 $R_{\theta}$ 定义的 $\mathbb{C}^{2}$ 上的算子确实具有复特征值 $e^{\pm i\theta}$。

Note: When we speak of the roots of a polynomial $p(t)$ or the eigenvalues of a matrix or linear operator, repetitions corresponding to multiple roots are supposed to be included. This terminology is convenient, though imprecise.

注意：当我们谈论多项式 $p(t)$ 的根或矩阵/线性算子的特征值时，通常包括对应于重根的重数。这种术语很方便，尽管不精确。

Corollary 4.5.15 If $\lambda_{1}, \ldots , \lambda_{n}$ are the eigenvalues of an $n \times n$ complex matrix $A$ , then $\operatorname *{det} A$ is the product $\lambda_{1} \cdots \lambda_{n}$ , and $\operatorname *{trace} A$ is the sum $\lambda_{1} + \ldots + \lambda_{n}$ .

推论 4.5.15 如果 $\lambda_{1},\ldots,\lambda_{n}$ 是 $n\times n$ 复矩阵 $A$ 的特征值，则 $\det A = \lambda_{1}\cdots\lambda_{n}$，且 $\operatorname{trace}A = \lambda_{1}+\cdots+\lambda_{n}$。

Proof. Let $p(t)$ be the characteristic polynomial of $A$ . Then

证明。设 $p(t)$ 是 $A$ 的特征多项式。则

$$(t - \lambda_{1})\cdot \cdot \cdot (t - \lambda_{n}) = p(t) = t^{n} - (\operatorname {trace} A)t^{n - 1} + \cdot \cdot \cdot \pm (\operatorname *{det} A).$$

### 4.6 TRIANGULAR AND DIAGONAL FORMS

### 4.6 三角形式与对角形式

In this section, we show that for "most" linear operators on a complex vector space there is a basis such that the matrix of the operator is diagonal. The key fact, which was noted at the end of Section 4.5, is that every complex polynomial of positive degree has a root. This tells us that every linear operator has at least one eigenvector.

在本节中，我们将证明对于复向量空间上的“大多数”线性算子，存在一组基使得算子的矩阵是对角矩阵。关键事实在第 4.5 节末尾已经指出：每个正次数的复多项式都有一个根。这告诉我们每个线性算子至少有一个特征向量。

## Proposition 4.6.1

## 命题 4.6.1

(a) Vector space form: Let $T$ be a linear operator on a finite-dimensional complex vector space $V$ . There is a basis $\mathbf{B}$ of $V$ such that the matrix of $T$ with respect to that basis is upper triangular.

(a) 向量空间形式：设 $T$ 是有限维复向量空间 $V$ 上的一个线性算子。存在 $V$ 的一组基 $\mathbf{B}$，使得 $T$ 关于该基的矩阵是上三角矩阵。

(b) Matrix form: Every complex $n \times n$ matrix $A$ is similar to an upper triangular matrix: There is a matrix $P \in GL_{n}(\mathbb{C})$ such that $P^{-1}AP$ is upper triangular.

(b) 矩阵形式：每个 $n\times n$ 复矩阵 $A$ 都相似于一个上三角矩阵：存在矩阵 $P\in GL_{n}(\mathbb{C})$，使得 $P^{-1}AP$ 是上三角矩阵。

===== Page 129 =====

Proof. The two assertions are equivalent, because of (4.3.5). We will work with the matrix. Let $V = \mathbb{C}^{n}$ . Proposition 4.5.14(b) shows that $V$ contains an eigenvector of $A$ , call it $v_{1}$ . Let $\lambda$ be its eigenvalue. We extend $(v_{1})$ to a basis $\mathbf{B} = (v_{1},\ldots ,v_{n})$ for $V$ . The new matrix $A^{\prime} = P^{- 1}AP$ has the block form

证明。由于 (4.3.5)，这两个断言是等价的。我们将使用矩阵形式进行证明。设 $V = \mathbb{C}^{n}$。命题 4.5.14(b) 表明 $V$ 包含 $A$ 的一个特征向量，称之为 $v_{1}$。设 $\lambda$ 是其特征值。我们将 $(v_{1})$ 扩充为 $V$ 的一组基 $\mathbf{B} = (v_{1},\ldots,v_{n})$。新矩阵 $A' = P^{-1}AP$ 具有分块形式

$$A^{\prime} = \left[\lambda \mid \ast \right],$$

where $D$ is an $(n - 1)\times (n - 1)$ matrix (see (4.4.6)). By induction on $n$ , we may assume that the existence of a matrix $Q\in GL_{n - 1}(\mathbb{C})$ such that $Q^{- 1}DQ$ is upper triangular will have been proved. Let

其中 $D$ 是一个 $(n-1)\times (n-1)$ 矩阵（见 (4.4.6)）。通过对 $n$ 进行归纳，我们可以假设存在矩阵 $Q\in GL_{n-1}(\mathbb{C})$ 使得 $Q^{-1}DQ$ 是上三角矩阵已被证明。令

$$Q_{1} = \left[\frac{1}{0}\right]\left[\frac{0}{Q}\right].\quad \mathrm{Then}\quad A^{\prime \prime} = Q_{1}^{-1}A^{\prime}Q_{1} = \left[\frac{\lambda}{0}\right]\left[\frac{\ast}{Q^{-1}DQ}\right]$$

is upper triangular, and $A^{\prime \prime} = (PQ_{1})^{- 1}A(PQ_{1})$

是上三角矩阵，且 $A'' = (PQ_{1})^{-1}A(PQ_{1})$。

Corollary 4.6.3 Proposition 4.6.1 continues to hold when the phrase "upper triangular" is replaced by "lower triangular."

推论 4.6.3 当短语“上三角”被替换为“下三角”时，命题 4.6.1 仍然成立。

The lower triangular form is obtained by listing the basis $\mathbf{B}$ of (4.6.1)(a) in reverse order.

下三角形式可以通过将 (4.6.1)(a) 中的基 $\mathbf{B}$ 按相反顺序列出而得到。

The important point for the proof of Proposition 4.6.1 is that every complex polynomial has a root. The same proof will work for any field $F$ , provided that all the roots of the characteristic polynomial are in the field.

命题 4.6.1 证明中的关键点是每个复多项式都有一个根。同样的证明适用于任何域 $F$，只要特征多项式的所有根都在该域中。

## Corollary 4.6.4

## 推论 4.6.4

(a) Vector space form: Let $T$ be a linear operator on a finite-dimensional vector space $V$ over a field $F$ , and suppose that the characteristic polynomial of $T$ is a product of linear factors in the field $F$ . There is a basis $\mathbf{B}$ of $V$ such that the matrix $A$ of $T$ is upper (or lower) triangular.

(a) 向量空间形式：设 $T$ 是域 $F$ 上有限维向量空间 $V$ 的一个线性算子，并假设 $T$ 的特征多项式在域 $F$ 中可以分解为一次因式的乘积。存在 $V$ 的一组基 $\mathbf{B}$，使得 $T$ 的矩阵 $A$ 是上（或下）三角矩阵。

(b) Matrix form: Let $A$ be an $n\times n$ matrix with entries in $F$ , whose characteristic polynomial is a product of linear factors. There is a matrix $P\in GL_{n}(F)$ such that $P^{-1}AP$ is upper (or lower) triangular.

(b) 矩阵形式：设 $A$ 是一个元素在 $F$ 中的 $n\times n$ 矩阵，其特征多项式是一次因式的乘积。存在矩阵 $P\in GL_{n}(F)$ 使得 $P^{-1}AP$ 是上（或下）三角矩阵。

The proof is the same, except that to make the induction step one has to check that the characteristic polynomial of the matrix $D$ that appears in (4.6.2) is $p(t) / (t - \lambda)$ , where $p(t)$ is the characteristic polynomial of $A$ . Then the hypothesis that the characteristic polynomial factors into linear factors carries over from $A$ to $D$ .

证明是相同的，除了在归纳步骤中需要检查 (4.6.2) 中出现的矩阵 $D$ 的特征多项式是 $p(t)/(t-\lambda)$，其中 $p(t)$ 是 $A$ 的特征多项式。那么特征多项式可分解为一次因式的假设就从 $A$ 传递到了 $D$。

We now ask which matrices $A$ are similar to diagonal matrices. They are called diagonalizable matrices. As we saw in (4.4.8) (b), they are the matrices that have bases of eigenvectors. Similarly, a linear operator that has a basis of eigenvectors is called a diagonalizable operator. The diagonal entries are determined, except for their order, by the linear operator $T$ . They are the eigenvalues.

现在我们问哪些矩阵 $A$ 相似于对角矩阵。它们被称为可对角化矩阵。正如我们在 (4.4.8)(b) 中看到的，它们是具有特征向量基的矩阵。类似地，具有特征向量基的线性算子称为可对角化算子。对角元（除了顺序外）由线性算子 $T$ 决定。它们就是特征值。

Theorem 4.6.6 below gives a partial answer to our question; a more complete answer will be given in the next section.

下面的定理 4.6.6 给出了我们问题的一个部分答案；更完整的答案将在下一节给出。

===== Page 130 =====

Proposition 4.6.5 Let $\nu_{1},\ldots ,\nu_{r}$ be eigenvectors of a linear operator $T$ with distinct eigenvalues $\lambda_{1},\ldots ,\lambda_{r}$ . The set $(\nu_{1},\ldots ,\nu_{r})$ is independent.

命题 4.6.5 设 $\nu_{1},\ldots,\nu_{r}$ 是线性算子 $T$ 的特征向量，对应的特征值 $\lambda_{1},\ldots,\lambda_{r}$ 互不相同。则集合 $(\nu_{1},\ldots,\nu_{r})$ 是线性无关的。

Proof. We use induction on $r$ . The assertion is true when $r = 1$ , because an eigenvector cannot be zero. Suppose that a dependence relation

证明。我们对 $r$ 使用归纳法。当 $r=1$ 时断言成立，因为特征向量不能为零。假设存在一个线性关系

$$0 = a_{1}\nu_{1} + \dots +a_{r}\nu_{r}$$

is given. We must show that $a_{i} = 0$ for all $i$ . We apply the operator $T$ :

我们被给出了。必须证明对所有 $i$ 有 $a_{i}=0$。我们应用算子 $T$：

$$0 = T(0) = a_{1}T(\nu_{1}) + \dots +a_{r}T(\nu_{r}) = a_{1}\lambda_{1}\nu_{1} + \dots +a_{r}\lambda_{r}\nu_{r}.$$

This is a second dependence relation among $(\nu_{1},\ldots ,\nu_{r})$ . We eliminate $\nu_{r}$ from the two relations, multiplying the first relation by $\lambda_{r}$ and subtracting the second:

这是在 $(\nu_{1},\ldots,\nu_{r})$ 之间的第二个线性关系。我们从两个关系中消去 $\nu_{r}$，将第一个关系乘以 $\lambda_{r}$ 然后减去第二个：

$$0 = a_{1}(\lambda_{r} - \lambda_{1})\nu_{1} + \dots +a_{r - 1}(\lambda_{r} - \lambda_{r - 1})\nu_{r - 1}.$$

Applying induction, we may assume that $(\nu_{1},\ldots ,\nu_{r - 1})$ is an independent set. This tells us that the coefficients $a_{i}(\lambda_{r} - \lambda_{i})$ , $i< r$ , are all zero. Since the $\lambda_{i}$ are distinct, $\lambda_{r} - \lambda_{i}$ is not zero if $i< r$ . Thus $a_{1} = \dots = a_{r - 1} = 0$ . The original relation reduces to $0 = a_{r}\nu_{r}$ . Since an eigenvector cannot be zero, $a_{r}$ is zero too.

应用归纳假设，我们可以认为 $(\nu_{1},\ldots,\nu_{r-1})$ 是线性无关集。这告诉我们系数 $a_{i}(\lambda_{r}-\lambda_{i})$（$i<r$）全为零。由于 $\lambda_{i}$ 互不相同，当 $i<r$ 时 $\lambda_{r}-\lambda_{i}\neq 0$。因此 $a_{1}=\cdots=a_{r-1}=0$。原始关系简化为 $0 = a_{r}\nu_{r}$。由于特征向量不能为零，所以 $a_{r}=0$ 也成立。

The next theorem follows by combining (4.4.8) and (4.6.5):

下面的定理结合了 (4.4.8) 和 (4.6.5)：

Theorem 4.6.6 Let $T$ be a linear operator on a vector space $V$ of dimension $n$ over a field $F$ . If its characteristic polynomial has $n$ distinct roots in $F$ , there is a basis for $V$ with respect to which the matrix of $T$ is diagonal.

定理 4.6.6 设 $T$ 是域 $F$ 上 $n$ 维向量空间 $V$ 上的一个线性算子。如果其特征多项式在 $F$ 中有 $n$ 个不同的根，则存在 $V$ 的一组基，使得 $T$ 关于该基的矩阵是对角矩阵。

Note: Diagonalization is a powerful tool. When one is presented with a diagonalizable operator, it should be an automatic response to work with a basis of eigenvectors.

注意：对角化是一个强大的工具。当面对一个可对角化算子时，自动的反应应该是使用特征向量基。

As an example of diagonalization, consider the real matrix

作为对角化的一个例子，考虑实矩阵

$$A = \left[ \begin{array}{cc}3 & 2\\ 1 & 4 \end{array} \right]. \quad (4.6.7)$$

Its eigenvectors were computed in (4.5.6). These eigenvectors form a basis $\mathbf{B} = (\nu_{1},\nu_{2})$ of $\mathbb{R}^{2}$ . According to (3.5.13), the matrix relating the standard basis $\mathbf{E}$ to this basis $\mathbf{B}$ is

其特征向量已在 (4.5.6) 中计算过。这些特征向量构成了 $\mathbb{R}^{2}$ 的一组基 $\mathbf{B}=(\nu_{1},\nu_{2})$。根据 (3.5.13)，将标准基 $\mathbf{E}$ 与基 $\mathbf{B}$ 联系起来的矩阵是

$$P = [\mathbf{B}] = \left[ \begin{array}{cc}1 & 2\\ 1 & -1 \end{array} \right],\quad P^{-1} = \frac{1}{3}\left[ \begin{array}{cc}1 & 2\\ 1 & -1 \end{array} \right],\mathrm{and} \quad (4.6.8)$$

$$P^{-1}AP = \frac{1}{3}\left[ \begin{array}{cc}1 & 2\\ 1 & -1 \end{array} \right]\left[ \begin{array}{cc}3 & 2\\ 1 & 4 \end{array} \right]\left[ \begin{array}{cc}1 & 2\\ 1 & -1 \end{array} \right] = \left[ \begin{array}{cc}5 & 2\\ 2 & 2 \end{array} \right] = \Lambda . \quad (4.6.9)$$

The next proposition is a variant of Proposition 4.4.8. We omit the proof.

下一个命题是命题 4.4.8 的一个变体。我们省略证明。

===== Page 131 =====

Proposition 4.6.10 Let $F$ be a field.

命题 4.6.10 设 $F$ 是一个域。

(a) Let $T$ be a linear operator on $F^{n}$ . If $\mathbf{B} = (\upsilon_{1},\ldots ,\upsilon_{n})$ is a basis of eigenvectors of $T$ , and if $P = [\mathbf{B}]$ , then $\Lambda = P^{-1}AP = [\mathbf{B}]^{-1}A[\mathbf{B}]$ is diagonal.

(a) 设 $T$ 是 $F^{n}$ 上的一个线性算子。如果 $\mathbf{B}=(\upsilon_{1},\ldots,\upsilon_{n})$ 是 $T$ 的一组特征向量基，且 $P = [\mathbf{B}]$，则 $\Lambda = P^{-1}AP = [\mathbf{B}]^{-1}A[\mathbf{B}]$ 是对角矩阵。

(b) Let $\mathbf{B} = (\upsilon_{1},\ldots ,\upsilon_{n})$ be a basis of $F^{n}$ , and let $\Lambda$ be the diagonal matrix with diagonal entries $\lambda_{1},\ldots ,\lambda_{n}$ that are not necessarily distinct. There is a unique matrix $A$ such that, for $i = 1,\ldots ,n$ $\upsilon_{i}$ is an eigenvector of $A$ with eigenvalue $\lambda_{i}$ , namely the matrix $[\mathbf{B}]\Lambda [\mathbf{B}]^{-1}$ .

(b) 设 $\mathbf{B}=(\upsilon_{1},\ldots,\upsilon_{n})$ 是 $F^{n}$ 的一组基，且 $\Lambda$ 是以 $\lambda_{1},\ldots,\lambda_{n}$（不一定互异）为对角元的对角矩阵。存在唯一的矩阵 $A$，使得对 $i=1,\ldots,n$，$\upsilon_{i}$ 是 $A$ 的具有特征值 $\lambda_{i}$ 的特征向量，即矩阵 $[\mathbf{B}]\Lambda[\mathbf{B}]^{-1}$。

A nice way to write the equation $[\mathbf{B}]^{- 1}A[\mathbf{B}] = \Lambda$ is

方程 $[\mathbf{B}]^{-1}A[\mathbf{B}] = \Lambda$ 的一种优美写法是

$$A[\mathbf{B}] = [\mathbf{B}]\Lambda . \quad (4.6.11)$$

One application of Theorem 4.6.6 is to compute the powers of a diagonalizable matrix. The next lemma needs to be pointed out, though it follows trivially when one expands the left sides of the equations and cancels $PP^{- 1}$ .

定理 4.6.6 的一个应用是计算可对角化矩阵的幂。下面的引理虽然通过展开方程左边并消去 $PP^{-1}$ 可以平凡地得到，但仍需要指出。

Lemma 4.6.12 Let $A,B$ , and $P$ be $n\times n$ matrices. If $P$ is invertible, then $(P^{- 1}AP)(P^{- 1}BP) =$ $P^{- 1}(AB)P$ , and for all $k\geq 1$ $(P^{- 1}AP)^{k} = P^{- 1}A^{k}P$ .

引理 4.6.12 设 $A, B, P$ 是 $n\times n$ 矩阵。如果 $P$ 可逆，则 $(P^{-1}AP)(P^{-1}BP) = P^{-1}(AB)P$，且对所有 $k\ge 1$，$(P^{-1}AP)^{k} = P^{-1}A^{k}P$。

Thus if $A,P$ ,and $\Lambda$ are as in (4.6.9),then

因此，如果 $A, P, \Lambda$ 如 (4.6.9) 所示，则

equation[[117, 490, 881, 541]]

If $f(t) = a_{0} + a_{1}t + \dots +a_{n}t^{n}$ is a polynomial in $t$ with coefficients in $F$ and if $A$ is an $n\times n$ matrix with entries in $F$ ,then $f(A)$ will denote the matrix obtained by substituting $A$ formally for $t$

如果 $f(t) = a_{0} + a_{1}t + \dots + a_{n}t^{n}$ 是系数在 $F$ 中的 $t$ 的多项式，且 $A$ 是元素在 $F$ 中的 $n\times n$ 矩阵，则 $f(A)$ 表示将 $A$ 形式地代入 $t$ 得到的矩阵：

$$f(A) = a_{0}I + a_{1}A + \dots +a_{n}A^{n}. \quad (4.6.13)$$

The constant term $a_{0}$ gets replaced by $a_{0}I$ . Then if $A = P\Lambda P^{- 1}$

常数项 $a_{0}$ 被替换为 $a_{0}I$。那么如果 $A = P\Lambda P^{-1}$，

$$f(A) = f(P\Lambda P^{-1}) = a_{0}I + a_{1}P\Lambda P^{-1} + \dots +a_{n}P\Lambda^{n}P^{-1} = P f(\Lambda)P^{-1}. \quad (4.6.14)$$

The analogous notation is used for linear operators: If $T$ is a linear operator on a vector space over a field $F$ , the linear operator $f(T)$ on $V$ is defined to be

类似的记号也用于线性算子：如果 $T$ 是域 $F$ 上向量空间上的一个线性算子，则 $V$ 上的线性算子 $f(T)$ 定义为

$$f(T) = a_{0}I + a_{1}T + \dots +a_{n}T^{n}, \quad (4.6.15)$$

where $I$ denotes the identity operator. The operator $f(T)$ acts on a vector by $f(T)\upsilon =$ $a_{0}\upsilon +a_{1}T\upsilon +\dots +a_{n}T^{n}\upsilon .$ (In order to avoid too many parentheses we have omitted some by writing $T\upsilon$ for $T(\upsilon)$

其中 $I$ 表示恒等算子。算子 $f(T)$ 作用于向量：$f(T)\upsilon = a_{0}\upsilon + a_{1}T\upsilon + \dots + a_{n}T^{n}\upsilon$。（为了避免过多的括号，我们省略了一些，用 $T\upsilon$ 表示 $T(\upsilon)$。）

===== Page 132 =====

### 4.7 JORDAN FORM

### 4.7 若尔当标准形

Suppose we are given a linear operator $T$ on a finite- dimensional complex vector space $V$ . We have seen that, if the roots of its characteristic polynomial are distinct, there is a basis of eigenvectors, and that the matrix of $T$ with respect to that basis is diagonal. Here we ask what can be done without assuming that the eigenvalues are distinct. When the characteristic polynomial has multiple roots there will most often not be a basis of eigenvectors, but we'll see that, nevertheless, the matrix can be made fairly simple.

假设我们给定了有限维复向量空间 $V$ 上的一个线性算子 $T$。我们已经看到，如果其特征多项式的根互异，则存在一组特征向量基，且 $T$ 关于该基的矩阵是对角矩阵。这里我们问，在不假设特征值互异的情况下能做些什么。当特征多项式有重根时，通常不会有特征向量基，但我们将看到，尽管如此，矩阵仍可以变得相当简单。

An eigenvector with eigenvalue $\lambda$ of a linear operator $T$ is a nonzero vector $v$ such that $(T - \lambda)v = 0$ . (We will write $T - \lambda$ for $T - \lambda I$ here.) Since our operator $T$ may not have enough eigenvectors, we work with generalized eigenvectors.

线性算子 $T$ 的具有特征值 $\lambda$ 的特征向量是一个非零向量 $v$，使得 $(T-\lambda)v = 0$。（这里我们将用 $T-\lambda$ 表示 $T-\lambda I$。）由于我们的算子 $T$ 可能没有足够的特征向量，我们将使用广义特征向量。

A generalized eigenvector with eigenvalue $\lambda$ of a linear operator $T$ is a nonzero vector $x$ such that $(T - \lambda)^{k}x = 0$ for some $k > 0$ . Its exponent is the smallest integer $d$ such that $(T - \lambda)^{d}x = 0$ .

线性算子 $T$ 的具有特征值 $\lambda$ 的广义特征向量是一个非零向量 $x$，使得对某个 $k>0$ 有 $(T-\lambda)^{k}x = 0$。其指数是满足 $(T-\lambda)^{d}x = 0$ 的最小整数 $d$。

Proposition 4.7.1 Let $x$ be a generalized eigenvector of $T$ , with eigenvalue $\lambda$ and exponent $d$ , and for $j \geq 0$ , let $u_{j} = (T - \lambda)^{j}x$ . Let $\mathbf{B} = (u_{0}, \ldots , u_{d - 1})$ , and let $X = \operatorname {Span} \mathbf{B}$ . Then $X$ is a $T$ - invariant subspace, and $\mathbf{B}$ is a basis of $X$ .

命题 4.7.1 设 $x$ 是 $T$ 的一个广义特征向量，具有特征值 $\lambda$ 和指数 $d$，并对 $j\ge 0$，令 $u_{j} = (T-\lambda)^{j}x$。设 $\mathbf{B} = (u_{0},\ldots,u_{d-1})$，且 $X = \operatorname{Span}\mathbf{B}$。则 $X$ 是一个 $T$-不变子空间，且 $\mathbf{B}$ 是 $X$ 的一组基。

We use the next lemma in the proof.

我们在证明中使用下面的引理。

Lemma 4.7.2 With $u_{j}$ as above, a linear combination $y = c_{j}u_{j} + \dots +c_{d - 1}u_{d - 1}$ with $j \leq d - 1$ and $c_{j} \neq 0$ is a generalized eigenvector, with eigenvalue $\lambda$ and exponent $d - j$ .

引理 4.7.2 使用上述的 $u_{j}$，一个线性组合 $y = c_{j}u_{j} + \dots +c_{d-1}u_{d-1}$，其中 $j\le d-1$ 且 $c_{j}\neq 0$，是一个广义特征向量，具有特征值 $\lambda$ 和指数 $d-j$。

Proof. Since the exponent of $x$ is $d$ , $(T - \lambda)^{d - 1}x = u_{d - 1} \neq 0$ . Therefore $(T - \lambda)^{d - j - 1}y = c_{j}u_{d - 1}$ isn't zero, but $(T - \lambda)^{d - j}y = 0$ . So $y$ is a generalized eigenvector with eigenvalue $\lambda$ and exponent $d - j$ , as claimed.

证明。由于 $x$ 的指数是 $d$，$(T-\lambda)^{d-1}x = u_{d-1} \neq 0$。因此 $(T-\lambda)^{d-j-1}y = c_{j}u_{d-1} \neq 0$，但 $(T-\lambda)^{d-j}y = 0$。所以 $y$ 是一个具有特征值 $\lambda$ 和指数 $d-j$ 的广义特征向量，如所述。

Proof of the Proposition. We note that

命题的证明。我们注意到

$$T u_{j} = \left\{ \begin{array}{ll}\lambda u_{j} + u_{j + 1} & \mathrm{if} j< d - 1\\ \lambda u_{j} & \mathrm{if} j = d - 1\\ 0 & \mathrm{if} j > d - 1. \end{array} \right. \quad (4.7.3)$$

Therefore $T u_{j}$ is in the subspace $X$ for all $j$ . This shows that $X$ is invariant. Next, $\mathbf{B}$ generates $X$ by definition. The lemma shows that every nontrivial linear combination of $\mathbf{B}$ is a generalized eigenvector, so it is not zero. Therefore $\mathbf{B}$ is an independent set.

因此对所有 $j$，$T u_{j}$ 都在子空间 $X$ 中。这表明 $X$ 是不变的。其次，根据定义，$\mathbf{B}$ 生成 $X$。引理表明，$\mathbf{B}$ 的每个非平凡线性组合都是一个广义特征向量，因此非零。所以 $\mathbf{B}$ 是线性无关集。

Corollary 4.7.4 Let $x$ be a generalized eigenvector for $T$ , with eigenvalue $\lambda$ . Then $\lambda$ is an ordinary eigenvalue - a root of the characteristic polynomial of $T$ .

推论 4.7.4 设 $x$ 是 $T$ 的一个广义特征向量，具有特征值 $\lambda$。则 $\lambda$ 是一个普通特征值——$T$ 的特征多项式的根。

Proof. If the exponent of $x$ is $d$ , then with notation as above, $u_{d - 1}$ is an eigenvector with eigenvalue $\lambda$ .

证明。如果 $x$ 的指数是 $d$，则使用上述记号，$u_{d-1}$ 是一个具有特征值 $\lambda$ 的特征向量。

===== Page 133 =====

Formula 4.7.3 determines the matrix that describes the action of T on the basis B of Proposition 4.7.1. It is the d *d Jordan block Jλ. Jordan blocks are shown below for low values of d:

公式 4.7.3 确定了描述 T 在命题 4.7.1 的基 B 上作用的矩阵。它就是 $d\times d$ 若尔当块 $J_{\lambda}$。下面展示了低维 $d$ 的若尔当块：

(4.7.5)
Jλ
=
[λ ],
�λ
1
λ
�
,
⎡
⎣
λ
1
λ
1
λ
⎤
⎦,
⎡
⎢⎢⎣
λ
1
λ
1
λ
1
λ
⎤
⎥⎥⎦, ...

The operation of a Jordan block is especially simple when λ = 0. The d *d block J0 operates on the standard basis of Cd as

当 $\lambda = 0$ 时，若尔当块的作用特别简单。$d\times d$ 块 $J_{0}$ 在 $\mathbb{C}^{d}$ 的标准基上的作用如下：

(4.7.6)
e1 ⇝e2 ⇝· · · ⇝ed ⇝0.

The 1 * 1 Jordan block J0 is zero.

$1\times 1$ 若尔当块 $J_{0}$ 是零矩阵。

The Jordan Decomposition Theorem below asserts that any complex n *n matrix is similar to a matrix J made up of diagonal Jordan blocks (4.7.5) – that it has the Jordan form

下面的若尔当分解定理断言，任何 $n\times n$ 复矩阵都相似于一个由对角若尔当块 (4.7.5) 组成的矩阵 $J$——即它具有若尔当标准形：

(4.7.7)
J =
⎡
⎢⎢⎢⎣
J1
J2 ...
Jℓ
⎤
⎥⎥⎥⎦,
where Ji = Jλi for some λi. The blocks Ji can have various sizes di, with �di = n,
and the diagonal entries λi aren’t necessarily distinct. The characteristic polynomial of the matrix J is

其中 $J_{i} = J_{\lambda_{i}}$。块 $J_{i}$ 可以有不同的大小 $d_{i}$，满足 $\sum d_{i} = n$，且对角元 $\lambda_{i}$ 不一定互异。矩阵 $J$ 的特征多项式是

(4.7.8)
p(t) = (t −λ1)d1(t −λ2)d2 · · ·(t −λℓ)dℓ.

The 2 * 2 and 3 * 3 Jordan forms are

$2\times 2$ 和 $3\times 3$ 若尔当标准形为：

(4.7.9)
�λ1
λ2
�
,
�λ1
1 λ1
�
;
⎡
⎣
λ1
λ2
λ3
⎤
⎦,
⎡
⎣
λ1
1 λ1
λ2
⎤
⎦,
⎡
⎣
λ1
1 λ1
1 λ1
⎤
⎦,
where the scalars λi may be equal or not, and in the fourth matrix, the blocks may be listed in the other order.

其中标量 $\lambda_{i}$ 可以相等也可以不等，并且在第四个矩阵中，块可以按另一种顺序列出。

Theorem 4.7.10 Jordan Decomposition.
(a) Vector space form: Let T be a linear operator on a finite-dimensional complex vector space V. There is a basis B of V such that the matrix of T with respect to B has Jordan form (4.7.7).
(b) Matrix form: Let A be an n *n complex matrix. There is an invertible complex matrix P such that P 1AP has Jordan form.

定理 4.7.10 若尔当分解。
(a) 向量空间形式：设 $T$ 是有限维复向量空间 $V$ 上的一个线性算子。存在 $V$ 的一组基 $\mathbf{B}$，使得 $T$ 关于 $\mathbf{B}$ 的矩阵具有若尔当标准形 (4.7.7)。
(b) 矩阵形式：设 $A$ 是一个 $n\times n$ 复矩阵。存在可逆复矩阵 $P$，使得 $P^{-1}AP$ 具有若尔当标准形。

It is also true that the Jordan form of an operator T or a matrix A is unique except for the order of the blocks.

同样成立的是，算子 $T$ 或矩阵 $A$ 的若尔当标准形除了块的顺序外是唯一的。

===== Page 134 =====

Proof. This proof is due to Filippov [Filippov]. Induction on the dimension of $V$ allows us to assume that the theorem is true for the restriction of $T$ to any proper invariant subspace. So if $V$ is the direct sum of proper $T$ - invariant subspaces, say $V_{1} \oplus \dots \oplus V_{r}$ , with $r > 1$ , then the theorem is true for $T$ .

证明。这个证明归功于 Filippov [Filippov]。通过对 $V$ 的维数进行归纳，我们可以假设定理对 $T$ 在任意真不变子空间上的限制成立。因此，如果 $V$ 是一些真 $T$-不变子空间的直和，例如 $V_{1}\oplus\cdots\oplus V_{r}$，且 $r>1$，那么定理对 $T$ 成立。

Suppose that we have generalized eigenvectors $v_{i}$ , for $i = 1, \ldots , r$ . Let $V_{i}$ be the subspace defined as in Proposition 4.7.1, with $x = v_{i}$ . If $V$ is the direct sum $V_{1} \oplus \dots \oplus V_{r}$ , the theorem will be true for $V$ , and we say that $v_{1}, \ldots , v_{r}$ are Jordan generators for $T$ . We will show that a set of Jordan generators exists.

假设我们有广义特征向量 $v_{i}$，$i=1,\ldots,r$。设 $V_{i}$ 是如命题 4.7.1 中定义的子空间，其中 $x=v_{i}$。如果 $V$ 是直和 $V_{1}\oplus\cdots\oplus V_{r}$，那么定理对 $V$ 成立，我们称 $v_{1},\ldots,v_{r}$ 是 $T$ 的若尔当生成元。我们将证明存在一组若尔当生成元。

Step 1: We choose an eigenvalue $\lambda$ of $T$ , and replace the operator $T$ by $T - \lambda I$ . If $A$ is the matrix of $T$ with respect to a basis, the matrix of $T - \lambda I$ with respect to the same basis will be $A - \lambda I$ , and if one of the matrices $A$ or $A - \lambda I$ is in Jordan form, so is the other. So replacing $T$ by $T - \lambda I$ is permissible. Having done this, our operator, which we still call $T$ , will have zero as an eigenvalue. This will simplify the notation.

步骤 1：我们选择 $T$ 的一个特征值 $\lambda$，并将算子 $T$ 替换为 $T-\lambda I$。如果 $A$ 是 $T$ 关于某基的矩阵，则 $T-\lambda I$ 关于同一基的矩阵是 $A-\lambda I$，并且如果 $A$ 或 $A-\lambda I$ 之一具有若尔当标准形，则另一个也具有。因此，将 $T$ 替换为 $T-\lambda I$ 是允许的。这样做之后，我们仍称之为 $T$ 的算子将以零为特征值。这将简化记号。

Step 2: We assume that 0 is an eigenvalue of $T$ . Let $K_{i}$ and $U_{i}$ denote the kernel and image, respectively, of the $i$ th power $T^{i}$ . Then $K_{1} \subset K_{2} \subset \dots$ and $U_{1} \supset U_{2} \supset \dots$ . Because $V$ is finite- dimensional, these chains of subspaces become constant for large $m$ , $K_{m} = K_{m + 1} = \dots$ and $U_{m} = U_{m + 1} = \dots$ . Let $K = K_{m}$ and $U = U_{m}$ . We verify that $K$ and $U$ are invariant subspaces, and that $V$ is the direct sum $K \oplus U$ .

步骤 2：我们假设 0 是 $T$ 的一个特征值。设 $K_{i}$ 和 $U_{i}$ 分别表示第 $i$ 次幂 $T^{i}$ 的核和像。则 $K_{1}\subset K_{2}\subset\cdots$ 且 $U_{1}\supset U_{2}\supset\cdots$。由于 $V$ 是有限维的，这些子空间链对大的 $m$ 变为常数：$K_{m}=K_{m+1}=\cdots$ 且 $U_{m}=U_{m+1}=\cdots$。设 $K=K_{m}$ 和 $U=U_{m}$。我们验证 $K$ 和 $U$ 是不变子空间，并且 $V$ 是直和 $K\oplus U$。

The subspaces are invariant because $T K_{m} \subset K_{m - 1} \subset K_{m}$ and $T U_{m} = U_{m + 1} = U_{m}$ . To show that $V = K \oplus U$ , it suffices to show that $K \cap U = \{0\}$ (see Proposition 4.3.1(b)). Let $z$ be an element of $K \cap U$ . Then $T^{m} z = 0$ , and also $z = T^{m} v$ for some $v$ in $V$ . Therefore $T^{2m} v = 0$ , so $v$ is an element of $K_{2m}$ . But $K_{2m} = K_{m}$ , so $T^{m} v = 0$ , i.e., $z = 0$ .

这些子空间是不变的，因为 $T K_{m}\subset K_{m-1}\subset K_{m}$ 且 $T U_{m} = U_{m+1}=U_{m}$。为了证明 $V = K\oplus U$，只需证明 $K\cap U = \{0\}$（见命题 4.3.1(b)）。设 $z$ 是 $K\cap U$ 中的一个元素。则 $T^{m}z = 0$，并且存在某个 $v\in V$ 使得 $z = T^{m}v$。因此 $T^{2m}v = 0$，所以 $v$ 是 $K_{2m}$ 中的元素。但 $K_{2m}=K_{m}$，所以 $T^{m}v = 0$，即 $z=0$。

Since $T$ has an eigenvalue 0, $K$ is not the zero subspace. Therefore $U$ has smaller dimension than $V$ , and by our induction assumption, the theorem is true for $T|_{U}$ . Unfortunately, we can't use this reasoning on $K$ , because $U$ might be zero. So we must still prove the existence of a Jordan form for $T|_{K}$ . We replace $V$ by $K$ and $T$ by $T|_{K}$ .

由于 $T$ 有特征值 0，$K$ 不是零子空间。因此 $U$ 的维数小于 $V$ 的维数，根据我们的归纳假设，定理对 $T|_{U}$ 成立。不幸的是，我们不能将这一推理应用于 $K$，因为 $U$ 可能为零。所以我们必须仍然证明 $T|_{K}$ 的若尔当标准形的存在性。我们将 $V$ 替换为 $K$，将 $T$ 替换为 $T|_{K}$。

- A linear operator $T$ on a vector space $V$ is called nilpotent if for some positive integer $r$ , the operator $T^{r}$ is zero.

- 向量空间 $V$ 上的线性算子 $T$ 称为幂零的，如果存在某个正整数 $r$，使得算子 $T^{r}$ 为零。

We have reduced the proof to the case of a nilpotent operator.

我们已经将证明归结为幂零算子的情形。

Step 3: We assume that our operator $T$ is nilpotent. Every nonzero vector will be a generalized eigenvector with eigenvalue 0. Let $N$ and $W$ denote the kernel and image of $T$ , respectively. Since $T$ is nilpotent, $N \neq \{0\}$ . Therefore the dimension of $W$ is smaller than that of $V$ , and by induction, the theorem is true for the restriction of the operator to $W$ . So there are Jordan generators $w_{1}, \ldots , w_{r}$ for $T|_{W}$ . Let $e_{i}$ denote the exponent of $w_{i}$ , and let $W_{i}$ denote the subspace formed as in Proposition 4.7.1, using the generalized eigenvector $w_{i}$ . So $W = W_{1} \oplus \dots \oplus W_{r}$ .

步骤 3：我们假设我们的算子 $T$ 是幂零的。每个非零向量都将是一个特征值为 0 的广义特征向量。设 $N$ 和 $W$ 分别表示 $T$ 的核和像。由于 $T$ 是幂零的，$N\neq\{0\}$。因此 $W$ 的维数小于 $V$ 的维数，由归纳法，定理对算子限制在 $W$ 上成立。所以存在 $T|_{W}$ 的若尔当生成元 $w_{1},\ldots,w_{r}$。设 $e_{i}$ 表示 $w_{i}$ 的指数，并设 $W_{i}$ 是如命题 4.7.1 中形成的子空间，使用广义特征向量 $w_{i}$。因此 $W = W_{1}\oplus\cdots\oplus W_{r}$。

For each $i$ , we choose an element $v_{i}$ of $V$ such that $T v_{i} = w_{i}$ . The exponent $d_{i}$ of $v_{i}$ will be equal to $e_{i} + 1$ . Let $V_{i}$ denote the subspace formed as in (4.7.1) using the vector $v_{i}$ . Then $T V_{i} = W_{i}$ . Let $U$ denote the sum $V_{1} + \dots + V_{r}$ . Since each $V_{i}$ is an invariant subspace, so is $U$ . We now verify that $v_{1}, \ldots , v_{r}$ are Jordan generators for the restriction $T|_{U}$ , i.e., that the subspaces $V_{i}$ are independent.

对每个 $i$，我们选择 $V$ 中的一个元素 $v_{i}$ 使得 $T v_{i} = w_{i}$。$v_{i}$ 的指数 $d_{i}$ 将等于 $e_{i}+1$。设 $V_{i}$ 是使用向量 $v_{i}$ 如 (4.7.1) 中形成的子空间。则 $T V_{i} = W_{i}$。设 $U$ 表示和 $V_{1}+\cdots+V_{r}$。由于每个 $V_{i}$ 都是不变子空间，$U$ 也是。我们现在验证 $v_{1},\ldots,v_{r}$ 是限制 $T|_{U}$ 的若尔当生成元，即子空间 $V_{i}$ 是独立的。

===== Page 135 =====

We notice two things: First, $TU = W$ because $TV_{i} = W_{i}$ . Second, $V_{i} \cap N \subset W_{i}$ . This follows from Lemma 4.7.2, which shows that $V_{i} \cap N$ is the span of the last basis vector $T^{d_{i} - 1} v_{i}$ . Since $d_{i} - 1 = e_{i}$ , which is positive, $T^{d_{i} - 1} v_{i}$ is in the image $W_{i}$ .

我们注意到两件事：第一，$TU = W$，因为 $T V_{i} = W_{i}$。第二，$V_{i} \cap N \subset W_{i}$。这由引理 4.7.2 得出，该引理表明 $V_{i} \cap N$ 是最后一个基向量 $T^{d_{i}-1}v_{i}$ 的张成空间。由于 $d_{i}-1 = e_{i} > 0$，$T^{d_{i}-1}v_{i}$ 在像 $W_{i}$ 中。

We suppose given a relation $\tilde{v}_{1} + \dots +\tilde{v}_{r} = 0$ , with $\tilde{v}_{i}$ in $V_{i}$ . We must show that $\tilde{v}_{i} = 0$ for all $i$ . Let $\tilde{w}_{i} = T\tilde{v}_{i}$ . Then $\tilde{w}_{1} + \dots +\tilde{w}_{r} = 0$ , and $\tilde{w}_{i}$ is in $W_{i}$ . Since the subspaces $W_{i}$ are independent, $\tilde{w}_{i} = 0$ for all $i$ . So $T\tilde{v}_{i} = 0$ , which means that $\tilde{v}_{i}$ is in $V_{i} \cap N$ . Therefore $\tilde{v}_{i}$ is in $W_{i}$ . Using the fact that the subspaces $W_{i}$ are independent once more, we conclude that, $\tilde{v}_{i} = 0$ for all $i$ .

假设给定一个关系 $\tilde{v}_{1}+\cdots+\tilde{v}_{r}=0$，其中 $\tilde{v}_{i}\in V_{i}$。我们必须证明对所有 $i$ 有 $\tilde{v}_{i}=0$。令 $\tilde{w}_{i}=T\tilde{v}_{i}$。则 $\tilde{w}_{1}+\cdots+\tilde{w}_{r}=0$，且 $\tilde{w}_{i}\in W_{i}$。由于子空间 $W_{i}$ 是独立的，对所有 $i$ 有 $\tilde{w}_{i}=0$。所以 $T\tilde{v}_{i}=0$，这意味着 $\tilde{v}_{i}\in V_{i}\cap N$。因此 $\tilde{v}_{i}\in W_{i}$。再次使用子空间 $W_{i}$ 是独立的事实，我们得出结论：对所有 $i$，$\tilde{v}_{i}=0$。

Step 4: We show that a set of Jordan generators for $T$ can be obtained by adding some elements of $N$ to the set $\{v_{1}, \ldots , v_{r}\}$ of Jordan generators for $T|_{U}$ .

步骤 4：我们证明，通过将 $N$ 中的一些元素添加到 $T|_{U}$ 的若尔当生成元集合 $\{v_{1},\ldots,v_{r}\}$ 中，可以得到 $T$ 的一组若尔当生成元。

Let $v$ be an arbitrary element of $V$ and let $Tv = w$ . Since $TU = W$ , there is a vector $u$ in $U$ such that $Tu = w = Tv$ . Then $z = v - u$ is in $N$ and $v = u + z$ . Therefore $U + N = V$ . This being so, we extend a basis of $U$ to a basis of $V$ by adding elements, say $z_{1}, \ldots , z_{\ell}$ , of $N$ (see Proposition 3.4.16(a)). Let $N'$ be the span of $(z_{1}, \ldots , z_{\ell})$ . Then $U \cap N' = \{0\}$ and $U + N' = V$ , so $V$ is the direct sum $U \oplus N'$ .

设 $v$ 是 $V$ 中的任意元素，并令 $Tv = w$。由于 $TU = W$，存在 $U$ 中的向量 $u$ 使得 $Tu = w = Tv$。则 $z = v - u$ 属于 $N$，且 $v = u + z$。因此 $U + N = V$。这样，我们通过添加 $N$ 中的元素，例如 $z_{1},\ldots,z_{\ell}$，将 $U$ 的一组基扩充为 $V$ 的一组基（见命题 3.4.16(a)）。设 $N'$ 是 $(z_{1},\ldots,z_{\ell})$ 的张成空间。则 $U\cap N' = \{0\}$ 且 $U+N' = V$，所以 $V$ 是直和 $U\oplus N'$。

The operator $T$ is zero on $N'$ , so $N'$ is an invariant subspace, and the matrix of $T|_{N'}$ is the zero matrix, which has Jordan form. Its Jordan blocks are $1 \times 1$ zero matrices. Therefore $\{v_{1}, \ldots , v_{r}; z_{1}, \ldots , z_{\ell}\}$ is a set of Jordan generators for $T$ .

算子 $T$ 在 $N'$ 上为零，所以 $N'$ 是一个不变子空间，且 $T|_{N'}$ 的矩阵是零矩阵，它具有若尔当标准形。它的若尔当块是 $1\times 1$ 的零矩阵。因此 $\{v_{1},\ldots,v_{r}; z_{1},\ldots,z_{\ell}\}$ 是 $T$ 的一组若尔当生成元。

It isn't difficult to determine the Jordan form for an operator $T$ , provided that the eigenvalues are known, and the analysis also proves uniqueness of the form. However, finding an appropriate basis of $V$ can be painful, and is best avoided.

如果已知特征值，确定算子 $T$ 的若尔当标准形并不困难，而且分析也证明了该标准形的唯一性。然而，找到 $V$ 的一个合适的基可能很痛苦，最好避免。

To determine the Jordan form, one chooses an eigenvalue $\lambda$ , and replaces $T$ by $T - \lambda I$ , to reduce to the case that $\lambda = 0$ . Let $K_{i}$ denote the kernel of $T^{i}$ , and let $k_{i}$ be the dimension of $K_{i}$ . In the case of a single $d \times d$ Jordan block with $\lambda = 0$ , these dimensions are:

为了确定若尔当标准形，我们选择一个特征值 $\lambda$，并将 $T$ 替换为 $T-\lambda I$，从而归结为 $\lambda = 0$ 的情形。设 $K_{i}$ 表示 $T^{i}$ 的核，$k_{i}$ 表示 $K_{i}$ 的维数。对于一个 $\lambda = 0$ 的 $d\times d$ 若尔当块，这些维数是：

equation[[380, 577, 618, 622]]

The dimensions $k_{i}$ for a general operator $T$ are obtained by adding the numbers $k_{i}^{block}$ for each block with $\lambda = 0$ . So $k_{1}$ will be the number of blocks with $\lambda = 0$ , $k_{2} - k_{1}$ will be the number of blocks of size $d \geq 2$ with $\lambda = 0$ , and so on.

对于一般算子 $T$，维数 $k_{i}$ 是通过将每个 $\lambda = 0$ 的块的数字 $k_{i}^{\text{block}}$ 相加得到的。因此 $k_{1}$ 将是 $\lambda = 0$ 的块的数量，$k_{2}-k_{1}$ 将是大小 $d\ge 2$ 且 $\lambda = 0$ 的块的数量，依此类推。

Two simple examples:

两个简单的例子：

equation[[272, 750, 725, 816]]

Here $A^{3} = 0$ , but $A^{2} \neq 0$ . If $v$ is a vector such that $A^{2} v \neq 0$ , for instance $v = e_{1}$ , then $(v, Tv, T^{2} v)$ will be a basis. The Jordan form consists of a single $3 \times 3$ block.

这里 $A^{3}=0$，但 $A^{2}\neq 0$。如果 $v$ 是一个使得 $A^{2}v\neq 0$ 的向量，例如 $v=e_{1}$，那么 $(v, Tv, T^{2}v)$ 将是一组基。若尔当标准形由一个 $3\times 3$ 块组成。

On the other hand, $B^{2} = 0$ . Taking $v = e_{1}$ again, the set $(v, Tv)$ is independent, and this gives us a $2 \times 2$ block. To obtain the Jordan form, we have to add a vector in $N$ , for example $v' = e_{2} + e_{3}$ , which will give a $1 \times 1$ block (equal to zero). The required basis is $(v, Tv, v')$ .

另一方面，$B^{2}=0$。再次取 $v=e_{1}$，集合 $(v, Tv)$ 是线性无关的，这给我们一个 $2\times 2$ 的块。为了得到若尔当标准形，我们需要在 $N$ 中添加一个向量，例如 $v' = e_{2}+e_{3}$，这将给出一个 $1\times 1$ 的块（等于零）。所需的基是 $(v, Tv, v')$。

===== Page 136 =====

It is often useful to write the Jordan form as $J = D + N$ ,where $D$ is the diagonal part of the matrix, and $N$ is the part below the diagonal. For a single Jordan block, we will have $D = \lambda I$ and $N = J_{0}$ , as is illustrated below for a $3\times 3$ block:

将若尔当标准形写成 $J = D + N$ 通常很有用，其中 $D$ 是矩阵的对角部分，$N$ 是对角线以下的部分。对于一个若尔当块，我们有 $D = \lambda I$ 和 $N = J_{0}$，如下面的 $3\times 3$ 块所示：

equation[[133, 147, 863, 214]]

Writing $J = D + N$ is convenient because $D$ and $N$ commute. The powers of $J$ can be computed by the binomial expansion:

写成 $J = D + N$ 很方便，因为 $D$ 和 $N$ 可交换。$J$ 的幂可以通过二项式展开计算：

$$J^{r} = (D + N)^{r} = D^{r} + \binom{r}{1} D^{r - 1}N + \binom{r}{2} D^{r - 2}N^{2} + \dots . \quad (4.7.11)$$

When $J$ is an $n\times n$ matrix, $N^{n} = 0$ , and this expansion has at most $n$ terms. In the case of a single block, the formula reads

当 $J$ 是 $n\times n$ 矩阵时，$N^{n}=0$，这个展开式至多有 $n$ 项。在单个块的情况下，公式为：

$$J^{r} = (\lambda I + J_{0})^{r} = \lambda^{r}I + \binom{r}{1}\lambda^{r - 1}J_{0} + \binom{r}{2}\lambda^{r - 2}J_{0}^{2} + \dots . \quad (4.7.12)$$

Corollary 4.7.13 Let $T$ be a linear operator on a finite- dimensional complex vector space. The following conditions are equivalent:

推论 4.7.13 设 $T$ 是有限维复向量空间上的一个线性算子。以下条件等价：

(a) $T$ is a diagonalizable operator,
(b) every generalized eigenvector is an eigenvector,
(c) all of the blocks in the Jordan form for $T$ are $1\times 1$ blocks.

(a) $T$ 是可对角化算子，
(b) 每个广义特征向量都是特征向量，
(c) $T$ 的若尔当标准形中的所有块都是 $1\times 1$ 的块。

The analogous statements are true for a square complex matrix $A$

类似的陈述对方阵复矩阵 $A$ 也成立。

Proof. (a) $\Rightarrow$ (b): Suppose that $T$ is diagonalizable, say that the matrix of $T$ with respect to the basis $\mathbf{B} = (\upsilon_{1},\ldots ,\upsilon_{n})$ is the diagonal matrix $\Lambda$ with diagonal entries $\lambda_{1},\ldots ,\lambda_{n}$ . Let $\upsilon$ be a generalized eigenvector in $V$ , say that $(T - \lambda)^{k}\upsilon = 0$ for some $\lambda$ and some $k > 0$ We replace $T$ by $T - \lambda$ to reduce to the case that $T^{k}\upsilon = 0$ . Let $X = (x_{1},\ldots ,x_{n})^{t}$ be the coordinate vector of $\upsilon$ . The coordinates of $T^{k}\upsilon$ will be $\lambda_{i}^{k}x_{i}$ . Since $T^{k}\upsilon = 0$ , either $\lambda_{i} = 0$ or $x_{i} = 0$ , and in either case, $\lambda_{i}^{k}x_{i} = 0$ . Therefore $T\upsilon = 0$ .

证明。(a) $\Rightarrow$ (b)：假设 $T$ 可对角化，即 $T$ 关于基 $\mathbf{B}=(\upsilon_{1},\ldots,\upsilon_{n})$ 的矩阵是以 $\lambda_{1},\ldots,\lambda_{n}$ 为对角元的对角矩阵 $\Lambda$。设 $\upsilon$ 是 $V$ 中的一个广义特征向量，即存在某个 $\lambda$ 和某个 $k>0$ 使得 $(T-\lambda)^{k}\upsilon = 0$。我们将 $T$ 替换为 $T-\lambda$ 以归结为 $T^{k}\upsilon = 0$ 的情形。设 $X = (x_{1},\ldots,x_{n})^{t}$ 是 $\upsilon$ 的坐标向量。$T^{k}\upsilon$ 的坐标将是 $\lambda_{i}^{k}x_{i}$。由于 $T^{k}\upsilon = 0$，要么 $\lambda_{i}=0$，要么 $x_{i}=0$，在任何一种情况下，$\lambda_{i}^{k}x_{i}=0$。因此 $T\upsilon = 0$。

(b) $\Rightarrow$ (c): We prove the contrapositive. If the Jordan form of $T$ has a $k\times k$ Jordan block with $k > 1$ , then looking back at the action (4.7.6) of $J_{\lambda} - \lambda I$ , we see that there is a generalized eigenvector that is not an eigenvector. So if (c) is false, (b) is false too. Finally, it is clear that (c) $\Rightarrow$ (a).

(b) $\Rightarrow$ (c)：我们证明逆否命题。如果 $T$ 的若尔当标准形有一个 $k\times k$ 的若尔当块且 $k>1$，那么回顾 $J_{\lambda} - \lambda I$ 的作用 (4.7.6)，我们看到存在一个不是特征向量的广义特征向量。因此如果 (c) 为假，则 (b) 也为假。最后，显然 (c) $\Rightarrow$ (a)。

Here is a nice application of Jordan form.

下面是若尔当标准形的一个很好的应用。

Theorem 4.7.14 Let $T$ be a linear operator on a finite- dimensional complex vector space $V$ . If some positive power of $T$ is the identity, say $T^{r} = I$ , then $T$ is diagonalizable.

定理 4.7.14 设 $T$ 是有限维复向量空间 $V$ 上的一个线性算子。如果 $T$ 的某个正整数次幂是恒等算子，即 $T^{r}=I$，则 $T$ 是可对角化的。

Proof. It suffices to show that every generalized eigenvector is an eigenvector. To do this, we assume that $(T - \lambda I)^{2}\upsilon = 0$ with $\upsilon \neq 0$ , and we show that $(T - \lambda)\upsilon = 0$ . Since $\lambda$ is an eigenvalue and since $T^{r} = I$ , $\lambda^{r} = 1$ . We divide the polynomial $t^{r} - 1$ by $t - \lambda$ :

证明。只需证明每个广义特征向量都是特征向量。为此，我们假设 $(T-\lambda I)^{2}\upsilon = 0$ 且 $\upsilon \neq 0$，并证明 $(T-\lambda)\upsilon = 0$。由于 $\lambda$ 是特征值且 $T^{r}=I$，所以 $\lambda^{r}=1$。我们将多项式 $t^{r}-1$ 除以 $t-\lambda$：

$$t^{r} - 1 = (t^{r - 1} + \lambda t^{r - 2} + \dots +\lambda^{r - 2}t + \lambda^{r - 1})(t - \lambda).$$

===== Page 137 =====

Substituting $t = T$ and applying to $v$:

代入 $t = T$ 并作用于 $v$：

$$0 = (T^{r} - I)v = (T^{r - 1} + \lambda T^{r - 2} + \dots +\lambda^{r - 2}T + \lambda^{r - 1})(T - \lambda)v$$ $$\qquad = \left(T^{r - 1} + \lambda T^{r - 2} + \dots +\lambda^{r - 2}T + \lambda^{r - 1}\right)w$$ $$\qquad = r\lambda^{r - 1}w.$$

(For the last equality, one uses the fact that $T w = \lambda w.$ ) Since $r\lambda^{r - 1}w = 0,\quad w = 0.$

（最后一个等式使用了事实 $T w = \lambda w$。）由于 $r\lambda^{r-1}w = 0$，所以 $w = 0$。

We go back for a moment to the results of this section. Where has the hypothesis that $V$ be a vector space over the complex numbers been used? The answer is that its only use is to ensure that the characteristic polynomial has enough roots.

我们暂时回到本节的结果。假设 $V$ 是复数域上的向量空间这一假设用在何处？答案是它仅用于确保特征多项式有足够的根。

Corollary 4.7.15 Let $V$ be a finite- dimensional vector space over a field $F$ and let $T$ be a linear operator on $V$ whose characteristic polynomial factors into linear factors in $F$ .The Jordan Decomposition theorem 4.7.10 is true for $T$

推论 4.7.15 设 $V$ 是域 $F$ 上的有限维向量空间，且 $T$ 是 $V$ 上的一个线性算子，其特征多项式在 $F$ 中分解为一次因式的乘积。则若尔当分解定理 4.7.10 对 $T$ 成立。

The proof is identical to the one given for the case that $F = \mathbb{C}$

证明与 $F=\mathbb{C}$ 情形给出的证明相同。

Corollary 4.7.16 Let $T$ be a linear operator on a finite- dimensional vector space over a field of characteristic zero. Assume that $T^{r} = I$ for some $r\geq 1$ and that the polynomial $t^{r} - 1$ factors into linear factors in $F$ . Then $T$ is diagonalizable.

推论 4.7.16 设 $T$ 是特征为零的域上有限维向量空间的一个线性算子。假设对某个 $r\ge 1$ 有 $T^{r}=I$，且多项式 $t^{r}-1$ 在 $F$ 中分解为一次因式的乘积。则 $T$ 是可对角化的。

The characteristic zero hypothesis is needed to carry through the last step of the proof of Theorem 4.7.14, where from the relation $r\lambda^{r - 1}w = 0$ we want to conclude that $w = 0$ . The theorem is false in characteristic different from zero.

需要特征为零的假设来完成定理 4.7.14 证明的最后一步，其中从关系式 $r\lambda^{r-1}w = 0$ 我们想得出 $w = 0$ 的结论。在特征非零时该定理不成立。

image[[723, 551, 933, 635]]

## EXERCISES

## 习题

## Section 1 The Dimension Formula

## 第 1 节 维数公式

1.1. Let $A$ be a $\ell \times m$ matrix and let $B$ be an $n\times p$ matrix. Prove that the rule $M\sim AMB$ defines a linear transformation from the space $F^{m\times n}$ of $m\times n$ matrices to the space $F^{\ell \times p}$

1.1. 设 $A$ 是一个 $\ell\times m$ 矩阵，$B$ 是一个 $n\times p$ 矩阵。证明规则 $M \mapsto AMB$ 定义了从 $m\times n$ 矩阵空间 $F^{m\times n}$ 到 $\ell\times p$ 矩阵空间 $F^{\ell\times p}$ 的一个线性变换。

1.2. Let $v_{1},\ldots ,v_{n}$ be elements of a vector space $V$ . Prove that the map $\phi :F^{n}\to V$ defined by $\phi (X) = v_{1}x_{1} + \dots +v_{n}x_{n}$ is a linear transformation.

1.2. 设 $v_{1},\ldots,v_{n}$ 是向量空间 $V$ 中的元素。证明由 $\phi(X) = v_{1}x_{1} + \dots + v_{n}x_{n}$ 定义的映射 $\phi: F^{n}\to V$ 是一个线性变换。

1.3. Let $A$ be an $m\times n$ matrix. Use the dimension formula to prove that the space of solutions of the linear system $AX = 0$ has dimension at least $n - m$

1.3. 设 $A$ 是一个 $m\times n$ 矩阵。使用维数公式证明线性方程组 $AX=0$ 的解空间的维数至少为 $n-m$。

1.4. Prove that every $m\times n$ matrix $A$ of rank 1 has the form $A = XY^{\mathrm{t}}$ , where $X,Y$ are $m$ - and $n$ -dimensional column vectors. How uniquely determined are these vectors?

1.4. 证明每个秩为 1 的 $m\times n$ 矩阵 $A$ 都具有形式 $A = XY^{\mathrm{t}}$，其中 $X, Y$ 分别是 $m$ 维和 $n$ 维列向量。这些向量被唯一确定到什么程度？

===== Page 138 =====

1.5. (a) Let $U$ and $W$ be vector spaces over a field $F$ . Show that the two operations $(u,w) + (u',w') = (u + u',w + w')$ and $c(u,w) = (cu,cw)$ on pairs of vectors make the product set $U\times W$ into a vector space. It is called the product space. (b) Let $U$ and $W$ be subspaces of a vector space $V$ . Show that the map $T:U\times W\to V$ defined by $T(u,w) = u + w$ is a linear transformation. (c) Express the dimension formula for $T$ in terms of the dimensions of subspaces of $V$ .

1.5. (a) 设 $U$ 和 $W$ 是域 $F$ 上的向量空间。证明向量对上的两种运算 $(u,w)+(u',w') = (u+u', w+w')$ 和 $c(u,w) = (cu, cw)$ 使得乘积集 $U\times W$ 成为一个向量空间。它被称为乘积空间。(b) 设 $U$ 和 $W$ 是向量空间 $V$ 的子空间。证明由 $T(u,w)=u+w$ 定义的映射 $T: U\times W\to V$ 是一个线性变换。(c) 用 $V$ 的子空间的维数表示 $T$ 的维数公式。

## Section 2 The Matrix of a Linear Transformation

## 第 2 节 线性变换的矩阵

2.1. Let $A$ and $B$ be $2\times 2$ matrices. Determine the matrix of the operator $T:M\sim AMB$ on the space $F^{2\times 2}$ of $2\times 2$ matrices, with respect to the basis $(e_{11},e_{12},e_{21},e_{22})$ of $F^{2\times 2}$

2.1. 设 $A$ 和 $B$ 是 $2\times 2$ 矩阵。确定算子 $T: M \mapsto AMB$ 在 $2\times 2$ 矩阵空间 $F^{2\times 2}$ 上关于 $F^{2\times 2}$ 的基 $(e_{11}, e_{12}, e_{21}, e_{22})$ 的矩阵。

2.2. Let $A$ be an $n\times n$ matrix, and let $V$ denote the space of $n$ -dimensional row vectors. What is the matrix of the linear operator "right multiplication by $A^{,}$ with respect to the standard basis of $V?$

2.2. 设 $A$ 是一个 $n\times n$ 矩阵，并令 $V$ 表示 $n$ 维行向量空间。线性算子“右乘 $A$”关于 $V$ 的标准基的矩阵是什么？

2.3. Find all real $2\times 2$ matrices that carry the line $y = x$ to the line $y = 3x$

2.3. 找出所有将直线 $y=x$ 映到直线 $y=3x$ 的实 $2\times 2$ 矩阵。

2.4. Prove Theorem 4.2.10(b) using row and column operations.

2.4. 使用行和列运算证明定理 4.2.10(b)。

2.5. Let $A$ be an $m\times n$ matrix of rank $r$ let $I$ be a set of $r$ row indices such that the corresponding rows of $A$ are independent, and let $J$ be a set of $r$ column indices such that the corresponding columns of $A$ are independent. Let $M$ denote the $r\times r$ submatrix of $A$ obtained by taking rows from $I$ and columns from $J$ . Prove that $M$ is invertible.

2.5. 设 $A$ 是一个秩为 $r$ 的 $m\times n$ 矩阵，令 $I$ 是一个 $r$ 个行指标的集合，使得 $A$ 的对应行是线性无关的，并令 $J$ 是一个 $r$ 个列指标的集合，使得 $A$ 的对应列是线性无关的。设 $M$ 表示通过取 $I$ 中的行和 $J$ 中的列得到的 $r\times r$ 子矩阵。证明 $M$ 是可逆的。

## Section 3 Linear Operators

## 第 3 节 线性算子

3.1. Determine the dimensions of the kernel and the image of the linear operator $T$ on the space $\mathbb{R}^n$ defined by $T(x_{1},\ldots ,x_{n})^{\mathrm{t}} = (x_{1} + x_{n},x_{2} + x_{n - 1},\ldots ,x_{n} + x_{1})^{\mathrm{t}}$

3.1. 确定空间 $\mathbb{R}^{n}$ 上由 $T(x_{1},\ldots,x_{n})^{\mathrm{t}} = (x_{1}+x_{n}, x_{2}+x_{n-1}, \ldots, x_{n}+x_{1})^{\mathrm{t}}$ 定义的线性算子 $T$ 的核和像的维数。

3.2. (a) Let $A = \left[ \begin{array}{cc}a & b\\ c & d \end{array} \right]$ be a real matrix, with $c$ not zero. Show that using conjugation by elementary matrices, one can eliminate the " $a$ " entry. (b) Which matrices with $c = 0$ are similar to a matrix in which the " $a$ " entry is zero?

3.2. (a) 设 $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ 是一个实矩阵，且 $c\neq 0$。证明通过使用初等矩阵的共轭，可以消去“$a$”项。(b) 哪些 $c=0$ 的矩阵相似于“$a$”项为零的矩阵？

3.3. Let $T:V\to V$ be a linear operator on a vector space of dimension 2. Assume that $T$ is not multiplication by a scalar. Prove that there is a vector $v$ in $V$ such that $(v,T(v))$ is a basis of $V$ , and describe the matrix of $T$ with respect to that basis.

3.3. 设 $T: V\to V$ 是 2 维向量空间上的一个线性算子。假设 $T$ 不是标量乘法。证明存在 $V$ 中的向量 $v$ 使得 $(v, T(v))$ 是 $V$ 的一组基，并描述 $T$ 关于该基的矩阵。

3.4. Let $B$ be a complex $n\times n$ matrix. Prove or disprove: The linear operator $T$ on the space of all $n\times n$ matrices defined by $T(A) = AB - BA$ is singular.

3.4. 设 $B$ 是一个 $n\times n$ 复矩阵。证明或反驳：在所有 $n\times n$ 矩阵空间上由 $T(A)=AB-BA$ 定义的线性算子 $T$ 是奇异的。

## Section 4 Eigenvectors

## 第 4 节 特征向量

4.1. Let $T$ be a linear operator on a vector space $V$ , and let $\lambda$ be a scalar. The eigenspace $V^{(\lambda)}$ is the set of eigenvectors of $T$ with eigenvalue $\lambda$ , together with 0. Prove that $V^{(\lambda)}$ is a $T$ -invariant subspace.

4.1. 设 $T$ 是向量空间 $V$ 上的一个线性算子，$\lambda$ 是一个标量。特征空间 $V^{(\lambda)}$ 是 $T$ 的具有特征值 $\lambda$ 的特征向量与 0 组成的集合。证明 $V^{(\lambda)}$ 是一个 $T$-不变子空间。

4.2. (a) Let $T$ be a linear operator on a finite- dimensional vector space $V$ , such that $T^2$ is the identity operator. Prove that for any vector $v$ in $V$ , $v - Tv$ is either an eigenvector with eigenvalue $-1$ , or the zero vector. With notation as in Exercise 4.1, prove that $V$ is the direct sum of the eigenspaces $V^{(1)}$ and $V^{(- 1)}$ .

4.2. (a) 设 $T$ 是有限维向量空间 $V$ 上的一个线性算子，使得 $T^{2}$ 是恒等算子。证明对 $V$ 中的任意向量 $v$，$v - Tv$ 要么是特征值为 $-1$ 的特征向量，要么是零向量。使用习题 4.1 中的记号，证明 $V$ 是特征空间 $V^{(1)}$ 和 $V^{(-1)}$ 的直和。

===== Page 139 =====

4.3. Let $T$ be a linear operator on a vector space $V$ . Prove that if $W_{1}$ and $W_{2}$ are $T$ - invariant subspaces of $V$ , then $W_{1} + W_{2}$ and $W_{1} \cap W_{2}$ are $T$ - invariant.

4.3. 设 $T$ 是向量空间 $V$ 上的一个线性算子。证明如果 $W_{1}$ 和 $W_{2}$ 是 $V$ 的 $T$-不变子空间，那么 $W_{1}+W_{2}$ 和 $W_{1}\cap W_{2}$ 也是 $T$-不变的。

4.4. A $2 \times 2$ matrix $A$ has an eigenvector $v_{1} = (1, 1)^{t}$ with eigenvalue 2 and also an eigenvector $v_{2} = (1, 2)^{t}$ with eigenvalue 3. Determine $A$ .

4.4. 一个 $2\times 2$ 矩阵 $A$ 有一个特征向量 $v_{1} = (1,1)^{\mathrm{t}}$，特征值为 2，还有一个特征向量 $v_{2} = (1,2)^{\mathrm{t}}$，特征值为 3。确定 $A$。

4.5. Find all invariant subspaces of the real linear operator whose matrix is

4.5. 找出矩阵如下的实线性算子的所有不变子空间：

equation[[144, 227, 435, 287]]

4.6. Let $P$ be the real vector space of polynomials $p(x) = a_{0} + a_{1} + \dots +a_{n}x^{n}$ of degree at most $n$ , and let $D$ denote the derivative $\frac{d}{dx}$ , considered as a linear operator on $P$ .

4.6. 设 $P$ 是次数至多为 $n$ 的多项式 $p(x)=a_{0}+a_{1}x+\cdots+a_{n}x^{n}$ 构成的实向量空间，并令 $D$ 表示导数 $\frac{d}{dx}$，视为 $P$ 上的一个线性算子。

(a) Prove that $D$ is a nilpotent operator, meaning that $D^{k} = 0$ for sufficiently large $k$ .
(b) Find the matrix of $D$ with respect to a convenient basis.
(c) Determine all $D$ -invariant subspaces of $P$ .

(a) 证明 $D$ 是一个幂零算子，即对充分大的 $k$ 有 $D^{k}=0$。
(b) 找出 $D$ 关于一个方便基的矩阵。
(c) 确定 $P$ 的所有 $D$-不变子空间。

4.7. Let $A = \left[ \begin{array}{cc}a & b\\ c & d \end{array} \right]$ be a real $2 \times 2$ matrix. The condition that a column vector $X$ be an eigenvector for left multiplication by $A$ is that $AX = Y$ be a scalar multiple of $X$ , which means that the slopes $s = x_{2} / x_{1}$ and $s' = y_{2} / y_{1}$ are equal.

4.7. 设 $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ 是一个实 $2\times 2$ 矩阵。列向量 $X$ 是左乘 $A$ 的特征向量的条件是 $AX = Y$ 是 $X$ 的标量倍，这意味着斜率 $s = x_{2}/x_{1}$ 和 $s' = y_{2}/y_{1}$ 相等。

(a) Find the equation in $s$ that expresses this equality.
(b) Suppose that the entries of $A$ are positive real numbers. Prove that there is an eigenvector in the first quadrant and also one in the second quadrant.

(a) 找出表达这一等式的关于 $s$ 的方程。
(b) 假设 $A$ 的元素是正实数。证明存在第一象限中的一个特征向量，也存在第二象限中的一个特征向量。

4.8. Let $T$ be a linear operator on a finite- dimensional vector space for which every nonzero vector is an eigenvector. Prove that $T$ is multiplication by a scalar.

4.8. 设 $T$ 是有限维向量空间上的一个线性算子，其中每个非零向量都是特征向量。证明 $T$ 是标量乘法。

## Section 5 The Characteristic Polynomial

## 第 5 节 特征多项式

5.1. Compute the characteristic polynomials and the complex eigenvalues and eigenvectors of

5.1. 计算下列矩阵的特征多项式、复特征值和特征向量：

equation[[144, 689, 627, 737]]

5.2. The characteristic polynomial of the matrix below is $t^{3} - 4t - 1$ . Determine the missing entries.

5.2. 下面矩阵的特征多项式是 $t^{3}-4t-1$。确定缺失的元素。

equation[[472, 794, 588, 856]]

5.3. What complex numbers might be eigenvalues of a linear operator $T$ such that

5.3. 线性算子 $T$ 满足以下条件时，哪些复数可能是其特征值？

$$T^{r} = I,\quad (b)T^{2} - 5T + 6I = 0?$$

===== Page 140 =====

5.4. Find a recursive relation for the characteristic polynomial of the $k \times k$ matrix

5.4. 找出 $k\times k$ 矩阵的特征多项式的递推关系：

equation[[408, 109, 654, 224]]

and compute the polynomial for $k \leq 5$ .

并计算 $k\le 5$ 时的多项式。

5.5. Which real $2 \times 2$ matrices have real eigenvalues? Prove that the eigenvalues are real if the off- diagonal entries have the same sign.

5.5. 哪些实 $2\times 2$ 矩阵有实特征值？证明如果非对角元素同号，则特征值是实数。

5.6. Let $V$ be a vector space with basis $(v_{0}, \ldots , v_{n})$ and let $a_{0}, \ldots , a_{n}$ be scalars. Define a linear operator $T$ on $V$ by the rules $T(v_{i}) = v_{i + 1}$ if $i < n$ and $T(v_{n}) = a_{0}v_{0} + a_{1}v_{1} + \dots + a_{n}v_{n}$ . Determine the matrix of $T$ with respect to the given basis, and the characteristic polynomial of $T$ .

5.6. 设 $V$ 是一个具有基 $(v_{0},\ldots,v_{n})$ 的向量空间，并设 $a_{0},\ldots,a_{n}$ 是标量。通过规则 $T(v_{i}) = v_{i+1}$（若 $i<n$）和 $T(v_{n}) = a_{0}v_{0}+a_{1}v_{1}+\cdots+a_{n}v_{n}$ 在 $V$ 上定义一个线性算子 $T$。确定 $T$ 关于给定基的矩阵，以及 $T$ 的特征多项式。

5.7. Do $A$ and $A^{1}$ have the same eigenvectors? the same eigenvalues?

5.7. $A$ 和 $A^{t}$ 有相同的特征向量吗？有相同的特征值吗？

5.8. Let $A = (a_{ij})$ be a $3 \times 3$ matrix. Prove that the coefficient of $t$ in the characteristic polynomial is the sum of the symmetric $2 \times 2$ minors

5.8. 设 $A = (a_{ij})$ 是一个 $3\times 3$ 矩阵。证明特征多项式中 $t$ 的系数是对称 $2\times 2$ 子式的和：

equation[[278, 432, 779, 478]]

5.9. Consider the linear operator of left multiplication by an $m \times m$ matrix $A$ on the space $F^{m \times m}$ of all $m \times m$ matrices. Determine the trace and the determinant of this operator.

5.9. 考虑在所有 $m\times m$ 矩阵空间 $F^{m\times m}$ 上左乘一个 $m\times m$ 矩阵 $A$ 的线性算子。确定这个算子的迹和行列式。

5.10. Let $A$ and $B$ be $n \times n$ matrices. Determine the trace and the determinant of the operator on the space $F^{n \times n}$ defined by $M \sim AMB$ .

5.10. 设 $A$ 和 $B$ 是 $n\times n$ 矩阵。确定空间 $F^{n\times n}$ 上由 $M \mapsto AMB$ 定义的算子的迹和行列式。

## Section 6 Triangular and Diagonal Forms

## 第 6 节 三角形式与对角形式

6.1. Let $A$ be an $n \times n$ matrix whose characteristic polynomial factors into linear factors: $p(t) = (t - \lambda_{1}) \dots (t - \lambda_{n})$ . Prove that $\operatorname{trace} A = \lambda_{1} + \dots + \lambda_{n}$ , that $\operatorname{det} A = \lambda_{1} \dots \lambda_{n}$ .

6.1. 设 $A$ 是一个 $n\times n$ 矩阵，其特征多项式分解为一次因式：$p(t) = (t-\lambda_{1})\cdots(t-\lambda_{n})$。证明 $\operatorname{trace}A = \lambda_{1}+\cdots+\lambda_{n}$，且 $\det A = \lambda_{1}\cdots\lambda_{n}$。

6.2. Suppose that a complex $n \times n$ matrix $A$ has distinct eigenvalues $\lambda_{1}, \ldots , \lambda_{n}$ , and let $v_{1}, \ldots , v_{n}$ be eigenvectors with these eigenvalues.

6.2. 假设一个 $n\times n$ 复矩阵 $A$ 有互异的特征值 $\lambda_{1},\ldots,\lambda_{n}$，并设 $v_{1},\ldots,v_{n}$ 是相应于这些特征值的特征向量。

(a) Show that every eigenvector is a multiple of one of the vectors $v_{i}$ .
(b) Show how one can recover the matrix from the eigenvalues and eigenvectors.

(a) 证明每个特征向量都是某个 $v_{i}$ 的倍数。
(b) 说明如何从特征值和特征向量恢复出矩阵。

6.3. Let $T$ be a linear operator that has two linearly independent eigenvectors with the same eigenvalue $\lambda$ . Prove that $\lambda$ is a multiple root of the characteristic polynomial of $T$ .

6.3. 设 $T$ 是一个线性算子，它有两个线性无关的特征向量具有相同的特征值 $\lambda$。证明 $\lambda$ 是 $T$ 的特征多项式的重根。

6.4. Let $A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$ . Find a matrix $P$ such that $P^{-1}AP$ is diagonal, and find a formula for the matrix $A^{30}$ .

6.4. 设 $A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$。找出一个矩阵 $P$ 使得 $P^{-1}AP$ 是对角矩阵，并找出矩阵 $A^{30}$ 的公式。

6.5. In each case, find a complex matrix $P$ such that $P^{-1}AP$ is diagonal.

6.5. 在每种情况下，找出一个复矩阵 $P$ 使得 $P^{-1}AP$ 是对角矩阵。

===== Page 141 =====

6.6. Suppose that $A$ is diagonalizable. Can the diagonalization be done with a matrix $P$ in the special linear group?

6.6. 假设 $A$ 是可对角化的。能否用特殊线性群中的矩阵 $P$ 完成对角化？

6.7. Prove that if $A$ and $B$ are $n \times n$ matrices and $A$ is nonsingular, then $AB$ is similar to $BA$ .

6.7. 证明如果 $A$ 和 $B$ 是 $n\times n$ 矩阵且 $A$ 非奇异，则 $AB$ 相似于 $BA$。

6.8. A linear operator $T$ is nilpotent if some positive power $T^k$ is zero. Prove that $T$ is nilpotent if and only if there is a basis of $V$ such that the matrix of $T$ is upper triangular, with diagonal entries zero.

6.8. 如果某个正整数次幂 $T^{k}$ 为零，则线性算子 $T$ 称为幂零的。证明 $T$ 是幂零的当且仅当存在 $V$ 的一组基，使得 $T$ 的矩阵是上三角的，且对角元为零。

6.9. Find all real $2 \times 2$ matrices such that $A^2 = I$ , and describe geometrically the way they operate by left multiplication on $\mathbb{R}^2$ .

6.9. 找出所有满足 $A^{2}=I$ 的实 $2\times 2$ 矩阵，并从几何上描述它们在 $\mathbb{R}^{2}$ 上通过左乘的作用方式。

6.10. Let $M$ be a matrix made up of two diagonal blocks: $M = \begin{bmatrix} A & 0 \\ 0 & D \end{bmatrix}$ . Prove that $M$ is diagonalizable if and only if $A$ and $D$ are diagonalizable.

6.10. 设 $M$ 是由两个对角块组成的矩阵：$M = \begin{bmatrix} A & 0 \\ 0 & D \end{bmatrix}$。证明 $M$ 可对角化当且仅当 $A$ 和 $D$ 可对角化。

6.11. Let $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ be a $2 \times 2$ matrix with eigenvalue $\lambda$ .

6.11. 设 $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ 是一个 $2\times 2$ 矩阵，具有特征值 $\lambda$。

(a) Show that unless it is zero, the vector $(b, \lambda - a)^t$ is an eigenvector.

(a) 证明除非为零，向量 $(b, \lambda-a)^{\mathrm{t}}$ 是一个特征向量。

(b) Find a matrix $P$ such that $P^{-1}AP$ is diagonal, assuming that $b \neq 0$ and that $A$ has distinct eigenvalues.

(b) 假设 $b\neq 0$ 且 $A$ 有互异的特征值，找出一个矩阵 $P$ 使得 $P^{-1}AP$ 是对角矩阵。

## Section 7 Jordan Form

## 第 7 节 若尔当标准形

7.1. Determine the Jordan form of the matrix $\begin{bmatrix} 1 & 1 & 0 \\ 0 & 1 & 0 \\ 0 & 1 & 1 \end{bmatrix}$ .

7.1. 确定矩阵 $\begin{bmatrix} 1 & 1 & 0 \\ 0 & 1 & 0 \\ 0 & 1 & 1 \end{bmatrix}$ 的若尔当标准形。

7.2. Prove that $A = \begin{bmatrix} 1 & 1 & 1 \\ -1 & -1 & -1 \\ 1 & 1 & 1 \end{bmatrix}$ is an idempotent matrix, i.e., that $A^2 = A$ , and find its Jordan form.

7.2. 证明 $A = \begin{bmatrix} 1 & 1 & 1 \\ -1 & -1 & -1 \\ 1 & 1 & 1 \end{bmatrix}$ 是一个幂等矩阵，即 $A^{2}=A$，并找出它的若尔当标准形。

7.3. Let $V$ be a complex vector space of dimension 5, and let $T$ be a linear operator on $V$ whose characteristic polynomial is $(t - \lambda)^5$ . Suppose that the rank of the operator $T - \lambda I$ is 2. What are the possible Jordan forms for $T$ ?

7.3. 设 $V$ 是一个 5 维复向量空间，$T$ 是 $V$ 上的一个线性算子，其特征多项式为 $(t-\lambda)^{5}$。假设算子 $T-\lambda I$ 的秩为 2。$T$ 可能的若尔当标准形有哪些？

7.4. (a) Determine all possible Jordan forms for a matrix whose characteristic polynomial is $(t + 2)^2 (t - 5)^3$ . (b) What are the possible Jordan forms for a matrix whose characteristic polynomial is $(t + 2)^2 (t - 5)^3$ , when space of eigenvectors with eigenvalue $-2$ is one- dimensional, and the space of eigenvectors with eigenvalue 5 is two- dimensional?

7.4. (a) 确定特征多项式为 $(t+2)^{2}(t-5)^{3}$ 的矩阵的所有可能的若尔当标准形。(b) 当特征值 $-2$ 的特征空间是一维的，而特征值 5 的特征空间是二维的时，特征多项式为 $(t+2)^{2}(t-5)^{3}$ 的矩阵的可能若尔当标准形有哪些？

7.5. What is the Jordan form of a matrix $A$ all of whose eigenvectors are multiples of a single vector?

7.5. 所有特征向量都是单个向量的倍数的矩阵 $A$ 的若尔当标准形是什么？

7.6. Determine all invariant subspaces of a linear operator whose Jordan form consists of one block.

7.6. 确定若尔当标准形由一个块组成的线性算子的所有不变子空间。

7.7. Is every complex square matrix $A$ such that $A^2 = A$ diagonalizable?

7.7. 每个满足 $A^{2}=A$ 的复方阵 $A$ 都是可对角化的吗？

7.8. Is every complex square matrix $A$ similar to its transpose?

7.8. 每个复方阵 $A$ 都相似于它的转置吗？

7.9. Find a $2 \times 2$ matrix with entries in $\mathbb{F}_p$ that has a power equal to the identity and an eigenvalue in $\mathbb{F}_p$ , but is not diagonalizable.

7.9. 找出一个元素在 $\mathbb{F}_{p}$ 中的 $2\times 2$ 矩阵，它有一个幂等于单位矩阵，且有一个特征值在 $\mathbb{F}_{p}$ 中，但不可对角化。

===== Page 142 =====

## Miscellaneous Problems

## 杂题

M.1. Let $\upsilon = (a_{1},\ldots ,a_{n})$ be a real row vector. We may form the $n!\times n$ matrix $M$ whose rows are obtained by permuting the entries of $\upsilon$ in all possible ways. The rows can be listed in an arbitrary order. Thus if $n = 3,M$ might be

M.1. 设 $\upsilon = (a_{1},\ldots,a_{n})$ 是一个实行向量。我们可以形成一个 $n!\times n$ 矩阵 $M$，其行是通过以所有可能的方式置换 $\upsilon$ 的条目得到的。行可以按任意顺序列出。因此，如果 $n=3$，$M$ 可能是：

equation[[451, 167, 609, 282]]

Determine the possible ranks that such a matrix could have.

确定这种矩阵可能具有的秩。

M.2. Let $A$ be a complex $n\times n$ matrix with $n$ distinct eigenvalues $\lambda_{1},\ldots ,\lambda_{n}$ . Assume that $\lambda_{1}$ is the largest eigenvalue, that is, that $|\lambda_{1}| > |\lambda_{i}|$ for all $i > 1$

M.2. 设 $A$ 是一个 $n\times n$ 复矩阵，有 $n$ 个互异的特征值 $\lambda_{1},\ldots,\lambda_{n}$。假设 $\lambda_{1}$ 是最大的特征值，即对所有 $i>1$ 有 $|\lambda_{1}| > |\lambda_{i}|$。

(a) Prove that for most vectors $X$ , the sequence $X_{k} = \lambda_{1}^{-k}A^{k}X$ converges to an eigenvector $Y$ with eigenvalue $\lambda_{1}$ , and describe precisely what the conditions on $X$ are for this to be true.
(b) Prove the same thing without assuming that the eigenvalues $\lambda_{1},\ldots ,\lambda_{n}$ are distinct.

(a) 证明对于大多数向量 $X$，序列 $X_{k} = \lambda_{1}^{-k}A^{k}X$ 收敛于一个具有特征值 $\lambda_{1}$ 的特征向量 $Y$，并精确描述 $X$ 需要满足什么条件才能使其成立。
(b) 在不假设特征值 $\lambda_{1},\ldots,\lambda_{n}$ 互异的情况下证明同样的结论。

M.3. Compute the largest eigenvalue of the matrix $\left[ \begin{array}{cc}3 & 1\\ 3 & 4 \end{array} \right]$ to three-place accuracy, using a method based on Exercise M.2.

M.3. 使用基于习题 M.2 的方法，将矩阵 $\begin{bmatrix} 3 & 1 \\ 3 & 4 \end{bmatrix}$ 的最大特征值计算到三位有效数字。

M.4. If $X = (x_{1},x_{2},\ldots)$ is an infinite real row vector and $A = (a_{ij}),0< i,j< \infty$ is an infinite real matrix, one may or may not be able to define the matrix product $XA$ . For which $A$ can one define right multiplication on the space $\mathbb{R}^{\infty}$ of all infinite row vectors (3.7.1)? on the space $Z(3.7.2)?$

M.4. 如果 $X = (x_{1},x_{2},\ldots)$ 是一个无限实行向量，且 $A = (a_{ij}), 0<i,j<\infty$ 是一个无限实矩阵，则可能定义矩阵乘积 $XA$，也可能不能。对于哪些 $A$，可以在所有无限行向量空间 $\mathbb{R}^{\infty}$ (3.7.1) 上定义右乘？在空间 $Z$ (3.7.2) 上呢？

\\*M.5. Let $\phi \colon F^{n}\to F^{m}$ be left multiplication by an $m\times n$ matrix $A$

\\*M.5. 设 $\phi: F^{n}\to F^{m}$ 是左乘一个 $m\times n$ 矩阵 $A$。

(a) Prove that the following are equivalent:

(a) 证明以下条件等价：

$A$ has a right inverse, a matrix $B$ such that $AB = I$ $\phi$ is surjective, the rank of $A$ is $m$

$A$ 有右逆，即存在矩阵 $B$ 使得 $AB = I$ $\iff$ $\phi$ 是满射 $\iff$ $A$ 的秩为 $m$

(b) Prove that the following are equivalent:

(b) 证明以下条件等价：

$A$ has a left inverse, a matrix $B$ such that $BA = I$

$\phi$ is injective,

the rank of $A$ is $n$

$A$ 有左逆，即存在矩阵 $B$ 使得 $BA = I$ $\iff$ $\phi$ 是单射 $\iff$ $A$ 的秩为 $n$

===== Page 143 =====

M.6. Without using the characteristic polynomial, prove that a linear operator on a vector space of dimension $n$ can have at most $n$ distinct eigenvalues.

M.6. 不使用特征多项式，证明 $n$ 维向量空间上的线性算子至多有 $n$ 个不同的特征值。

\*M.7. (powers of an operator) Let $T$ be a linear operator on a vector space $V$ . Let $K_{r}$ and $W_{r}$ denote the kernel and image, respectively, of $T^{r}$ .

\*M.7. (算子的幂) 设 $T$ 是向量空间 $V$ 上的一个线性算子。设 $K_{r}$ 和 $W_{r}$ 分别表示 $T^{r}$ 的核和像。

(a) Show that $K_{1} \subset K_{2} \subset \dots$ and that $W_{1} \supset W_{2} \supset \dots$ .

(a) 证明 $K_{1}\subset K_{2}\subset\cdots$ 且 $W_{1}\supset W_{2}\supset\cdots$。

(b) The following conditions might or might not hold for a particular value of $r$ :

(b) 对于某个特定的 $r$，以下条件可能成立也可能不成立：

(1) $K_{r} = K_{r + 1}$ (2) $W_{r} = W_{r + 1}$ (3) $W_{r} \cap K_{1} = \{0\}$ (4) $W_{1} + K_{r} = V$ .

Find all implications among the conditions (1)- (4) when $V$ is finite- dimensional.

找出当 $V$ 是有限维时，条件 (1)-(4) 之间的所有蕴含关系。

(c) Do the same thing when $V$ is infinite- dimensional.

(c) 当 $V$ 是无限维时，做同样的事情。

M.8. Let $T$ be a linear operator on a finite-dimensional complex vector space $V$ .

M.8. 设 $T$ 是有限维复向量空间 $V$ 上的一个线性算子。

(a) Let $\lambda$ be an eigenvalue of $T$ , and let $V_{\lambda}$ be the set of generalized eigenvectors, together with the zero vector. Prove that $V_{\lambda}$ is a $T$ -invariant subspace of $V$ . (This subspace is called a generalized eigenspace.)
(b) Prove that $V$ is the direct sum of its generalized eigenspaces.

(a) 设 $\lambda$ 是 $T$ 的一个特征值，并设 $V_{\lambda}$ 是广义特征向量与零向量组成的集合。证明 $V_{\lambda}$ 是 $V$ 的一个 $T$-不变子空间。（这个子空间被称为广义特征空间。）
(b) 证明 $V$ 是其所有广义特征空间的直和。

M.9. Let $V$ be a finite-dimensional vector space. A linear operator $T: V \to V$ is called a projection if $T^{2} = T$ (not necessarily an "orthogonal projection"). Let $K$ and $W$ be the kernel and image of a linear operator $T$ . Prove

M.9. 设 $V$ 是一个有限维向量空间。如果 $T^{2}=T$，则线性算子 $T: V\to V$ 称为投影（不一定是“正交投影”）。设 $K$ 和 $W$ 是线性算子 $T$ 的核和像。证明

(a) $T$ is a projection onto $W$ if and only if the restriction of $T$ to $W$ is the identity map.

(a) $T$ 是到 $W$ 的投影当且仅当 $T$ 在 $W$ 上的限制是恒等映射。

(b) If $T$ is a projection, then $V$ is the direct sum $W \oplus K$ .

(b) 如果 $T$ 是一个投影，则 $V$ 是直和 $W\oplus K$。

(c) The trace of a projection $T$ is equal to its rank.

(c) 投影 $T$ 的迹等于它的秩。

M.10. Let $A$ and $B$ be $m \times n$ and $n \times m$ real matrices.

M.10. 设 $A$ 和 $B$ 分别是 $m\times n$ 和 $n\times m$ 实矩阵。

(a) Prove that if $\lambda$ is a nonzero eigenvalue of the $m \times m$ matrix $A B$ then it is also an eigenvalue of the $n \times n$ matrix $B A$ . Show by example that this need not be true if $\lambda = 0$ .

(a) 证明如果 $\lambda$ 是 $m\times m$ 矩阵 $AB$ 的一个非零特征值，那么它也是 $n\times n$ 矩阵 $BA$ 的一个特征值。举例说明如果 $\lambda=0$，则不一定成立。

(b) Prove that $I_{m} - A B$ is invertible if and only if $I_{n} - B A$ is invertible.

(b) 证明 $I_{m} - AB$ 可逆当且仅当 $I_{n} - BA$ 可逆。

===== Page 144 =====