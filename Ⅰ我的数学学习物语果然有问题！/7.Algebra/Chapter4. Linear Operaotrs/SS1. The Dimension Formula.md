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