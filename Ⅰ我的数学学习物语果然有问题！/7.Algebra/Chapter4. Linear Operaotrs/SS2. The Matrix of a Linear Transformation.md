---
tags:
  - Algebra
  - Linear_Algebra
  - Matrix
---
任一个列向量空间线性变化为另一个列向量空间是某一个矩阵的左乘变化

> [!Success] Lemma
> 令 $T:F^n\to F^m$ 是一个列向量间的线性变化。将设 $T(e_{j})$ 中的坐标向量记为 $A_{j}=(a_{1j},a_{2j},\cdots,a_{mj})$ 令 $A$ 为 $A_{1},A_{2},\cdots,A_{n}$ 为一个 $m\times n$ 矩阵。那么 $T$ 对 $F^n$ 中的向量的变化即左乘矩阵 $A$ 
>$$T(X) = T(\sum_{j}e_{j}x_{j}) = \sum_{j}T(e_{j})x_{j} = \sum_{j}A_{j}x_{j} = AX$$

我们可以直接举一个例子，矩阵 $R$ 表示将一个将 $\mathbb{R}^{2}$ 上的向量绕着原点逆时针旋转 $\theta$ 的映射  $\rho :\mathbb{R}^{2}\to \mathbb{R}^{2}$ ，其中 
$$R=\begin{bmatrix}
\cos\theta & -\sin \theta \\
\sin\theta & \cos\theta
\end{bmatrix}$$
我们令 $\mathbb{R}$ 上向量为 $X=r\begin{bmatrix}\cos\alpha \\ \sin\alpha\end{bmatrix}$ 于是我们就有 
$$RX=r\begin{bmatrix}
\cos\theta & -\sin \theta \\
\sin\theta & \cos\theta
\end{bmatrix}\begin{bmatrix}\cos\alpha \\ \sin\alpha\end{bmatrix}=r\begin{bmatrix}
\cos\theta \cos \alpha-\sin\theta \sin\alpha \\
\sin\theta \cos\alpha+\cos\theta \sin\alpha
\end{bmatrix}=r\begin{bmatrix}
\cos(\theta+\alpha) \\
\sin(\theta+\alpha)
\end{bmatrix}$$
确实 $RX$ 就是 $X$ 逆时针旋转 $\theta$ 得到的

当我们选定了两个空间的基，我们可以对任意的线性变化 $T:V\to W$ 进行类似引理的计算，如果 $\mathbf{B}=(v_{1},\cdots,v_{n})$ 是 $V$ 空间的一组基，我们使用记号 $T(\mathbf{B})$ 来表示 **Hypervector** 