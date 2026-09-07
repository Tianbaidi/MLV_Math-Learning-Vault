---
title: Chern's Conjecture with Constant Cubic Trace
authors: [Huixin Tan, Zizhou Tang, Yuquan Xie, Wenjiao Yan]
tags: [Geometry, Differential_Geometry, Minimal_Hypersurface, Chern_Conjecture]
source: [[2609.03711v1.pdf]]
---


> [!ABSTRACT] Abstract
> We prove that the values set of $S=|A|^{2}$ attained by closed embedded minimal hypersurfaces in $S^{n+1}(1)$ with constant $S$ and constant $f_{3}=\mathrm{tr}(A^{3})$ is locally finite, where $A$ denotes the shape operator. Neither the topology of the hypersurface nor the value of $f_{3}$ is fixed.

*2020 Mathematics Subject Classification.* Primary 53C42; Secondary 53C24, 58J60.

*Key words and phrases.* Chern conjecture, minimal hypersurface, constant scalar curvature, cubic trace, rolling radius, real analytic set.

*The project is partially supported by the NSFC (No.12271038, 12371048, 12526205), Nankai Zhide Foundation, and by the Open Project of the Key Laboratory of Mathematics and Complex Systems, Beijing Normal University (No. K202503).*

## 1. Introduction

Let $F:M^{n}\to S^{n+1}(1)$ be a closed minimal hypersurface, let $A$ be its shape operator, and put $S=\mathrm{tr}(A^{2})$. The Gauss equation gives the scalar curvature identity
$$R=n(n-1)-S,$$
so the constant scalar curvature condition is equivalent to the constancy of $S$.

S. S. Chern's conjecture asks, with the dimension $n$ fixed but with the closed source manifold and the immersion otherwise arbitrary, whether the possible constant values of $S$ form a discrete set $^{[6,\,7]}$. The same formulation appears as Problem 105 in Yau's problem list [30, p. 693].

Simons' rigidity inequality implies that a closed minimal hypersurface satisfying $0\le S\le n$ has $S=0$ or $S=n$ $^{[23]}$. The equality case $S=n$ was identified independently by Chern, do Carmo, and Kobayashi and by Lawson as a Clifford minimal hypersurface $^{[7,\,15]}$. Peng and Terng derived higher-order integral inequalities and used them to prove the next pinching gap above $n$: if the constant $S$ is greater than $n$, then $S>n+\frac{1}{12n}$ $^{[20,\,21]}$. Their work initiated a long sequence of pinching results. Among later improvements are the estimates of Ding and Xin and of Xu and his students $^{[9,\,17,\,29]}$. Building on Peng and Terng's three-dimensional estimates, Chang completed the proof of Chern's conjecture for $n=3$ $^{[4]}$. Much of the subsequent work has concentrated on the first and second gap problems, which exclude new constant values of $S$ near the known models. Such pinching results isolate the first few admissible values but do not control the full value set. Apart from Chang's work $^{[4]}$ in dimension three and classification results under additional hypotheses, the discreteness problem remains open.


A connected hypersurface in the sphere is called isoparametric if all of its principal curvatures are constant. Isoparametric minimal hypersurfaces supply the principal model family for Chern's conjecture. If $g$ denotes the number of distinct principal curvatures, Cartan's work and Münzner's structure theorems show that $g$ is restricted to $1,2,3,4,$ or $6$, and a minimal member has $S=(g-1)n$ $^{[3,\,18,\,19]}$. These examples therefore yield the familiar values $0$, $n$, $2n$, $3n$, and $5n$ whenever the corresponding multiplicities exist. The stronger classification expectation that every closed minimal hypersurface with constant scalar curvature is isoparametric remains open in general. The surveys of Ge and Tang and of Scherfner, Weiss, and Yau give broader accounts of the conjecture and its relation to isoparametric geometry $^{[11,\,22]}$.

Although Chern's conjecture is formulated for immersed hypersurfaces, the embedded subclass is natural. It contains all of the standard isoparametric models, excludes covering multiplicities, and gives a global separation of the sphere. Historically, however, imposing embeddedness has led to little additional progress: the principal gap and rigidity results recalled above already hold for immersions, and the conjecture remains open in general even in the embedded category.

Additional symmetric functions of the principal curvatures have proved useful in attacking this classification problem. De Almeida and Brito proved that a closed hypersurface in $S^{4}$ with constant mean curvature and constant nonnegative scalar curvature is isoparametric $^{[1]}$. Tang, Wei, and Yan extended this result to $n>3$ under $g=n$ everywhere and $\int_{M}R\,d\mu\ge 0$: constancy of $f_{k}=\mathrm{tr}(A^{k})$ for $1\le k\le n-1$ implies isoparametricity $^{[24]}$. Tang and Yan removed the condition $g=n$, proving the same conclusion for $n\ge 4$ under $R\ge 0$ and constant $f_{k}$, $1\le k\le n-1$ $^{[25]}$. For constant $f_{3}$, Cheng, Wei, and Yamashiro obtained a dimension-independent pinching theorem $^{[5]}$. In dimension four, Deng, Gu, and Wei proved isoparametricity for closed minimal hypersurfaces with constant scalar curvature satisfying the Willmore condition $^{[8]}$. These results are classification or gap theorems, whereas the conclusion below concerns local finiteness of the value set in every dimension.

We now formulate the class precisely. For $n\ge 2$, let $E_{n}^{(3)}$ be the set of numbers $s\ge 0$ for which there exist a closed connected smooth $n$-manifold $M$ and a smooth embedding $F:M\hookrightarrow S^{n+1}(1)$ such that, with respect to a global unit normal,
$$H=0,\qquad S\equiv s,\qquad f_{3}\equiv q$$
for some real number $q$.

**Theorem 1.1.** For every integer $n\ge 2$ and every finite $\Lambda\ge 0$, the set
$$E_{n}^{(3)}\cap[0,\Lambda]$$
is finite.

Theorem 1.1 establishes the discreteness predicted by Chern's conjecture in the stronger form of local finiteness for embedded hypersurfaces with constant $f_{3}$. Here the hypersurface is not fixed: its diffeomorphism type, its embedding, and the constant value of $f_{3}$ may all vary.

**Remark 1.2.** Chern's original conjecture concerns closed minimal submanifolds with arbitrary codimension: for fixed $n,m\ge 1$, the possible constant values of $S$ realized by closed minimally immersed $n$-submanifolds of $S^{n+m}(1)$ are conjectured to form a discrete set. Most subsequent work has focused on its hypersurface case $m=1$. Quite recently, Firester and Tsiamis disproved the conjecture in higher codimension by constructing, for $n\ge 3$ and $m\ge 4$, and also for even $n\ge 4$ and $m\ge 3$, countable families of closed embedded minimal $n$-submanifolds whose constant $S$-values are dense in a bounded interval $^{[10]}$. Thus embeddedness alone does not enforce discreteness in higher codimension. In codimension one, however, embeddedness together with a uniform bound on $S$ yields the two-sided tubular control needed for compactness. Together with the constancy of $f_{3}$, this leads to Theorem 1.1 and provides further evidence for the hypersurface conjecture.

The proof of the main theorem consists of a local part and a global part. For the local part, consider a $C^{1}$ family $F_{t}$ with values in $C^{3}(M,S^{n+1}(1))$, such that every $F_{t}$ is minimal and both $S_{t}$ and $f_{3,t}$ are spatially constant. If $\phi$ is the normal speed, the linearized mean curvature equation and the variation of $S$ give
$$0=H'=\Delta\phi+(n+S)\phi,\qquad \frac{1}{2}S'=\langle A,\nabla^{2}\phi\rangle+f_{3}\phi.$$
Integration, the Codazzi equation, and the constancy of $f_{3}$ imply $S'=0$. This path rigidity does not by itself control a possibly singular moduli space, so we reduce the mean-curvature equation to a finite-dimensional real analytic zero set and impose constancy of $S$ and $f_{3}$ by analytic variance functionals. The real analytic curve-selection lemma then converts any hypothetical local accumulation of $S$-values into an analytic path, contradicting path rigidity.

For the global part, a uniform bound for $S$ gives a uniform bound for the principal curvatures but does not by itself give an area bound or multiplicity-one compactness. Embeddedness supplies the missing global control. Each hypersurface separates the sphere into two domains, and Howard's rigidity form of the rolling theorem, together with the strict positivity of the Ricci tensor, yields equality of the rolling and focal radii on each side $^{[14]}$. The focal formula in the sphere then yields a uniform two-sided normal injectivity radius. Integrating the normal Jacobian over a shorter tube gives a uniform area bound, after which Hausdorff compactness, the uniform reach bound, varifold compactness, and elliptic regularity give smooth embedded multiplicity-one compactness. The local result at a smooth limit then completes the proof of Theorem 1.1.

Section 2 fixes the geometric conventions and derives the variation formulas used later. Section 3 proves a smooth path rigidity. Section 4 proves local constancy of the $S$-value on the finite-dimensional analytic set defined by the minimality and constancy conditions. Section 5 proves the uniform tube, area, and compactness statements. Section 6 proves Theorem 1.1 and discusses its precise scope.

## 2. Conventions and variation formulas

Throughout the paper, $M^{n}$ is closed and connected, the ambient sphere has sectional curvature one, and $F:M\to S^{n+1}(1)$ is a two-sided hypersurface, meaning that its normal line bundle is trivial. We fix a global unit normal $\nu$. Since $S^{n+1}(1)$ is orientable, two-sidedness is equivalent here to the orientability of $M$. For the closed embedded hypersurfaces considered in the main theorem, two-sidedness is automatic because they separate the sphere. Let $\bar g$ and $\bar\nabla$ denote the round metric on $S^{n+1}(1)$ and its Levi-Civita connection, respectively. The induced metric on $M$ is $g=F^{*}\bar g$, and its Levi-Civita connection is denoted by $\nabla$. We use the shape-operator convention
$$A(X)=-\left(\nabla_{X}\nu\right)^{\top},$$
where $(\cdot)^{\top}$ denotes orthogonal projection onto $TM$. We write $h(X,Y)=\langle AX,Y\rangle$, $H=\mathrm{tr}\,A$, $S=\mathrm{tr}(A^{2})$, and $f_{3}=\mathrm{tr}(A^{3})$. The Laplacian is $\Delta=\mathrm{tr}\,\nabla^{2}$, so its spectrum on a closed manifold is nonpositive.

Since the unit sphere is Einstein, its ambient Ricci tensor satisfies $\mathrm{Ric}=ng$, and hence $\mathrm{Ric}(\nu,X)=0$ for every $X\in TM$. Thus the contracted Codazzi equation reduces to
$$\mathrm{div}\,A=\nabla H. \tag{1}$$
In particular, $\mathrm{div}\,A=0$ on a minimal hypersurface. The Gauss equation gives
$$R=n(n-1)+H^{2}-S,$$
and hence $R=n(n-1)-S$ when $H=0$.

**Lemma 2.1 (Normal variation formulas).** Let $I\subset\mathbb{R}$ be an interval containing $0$, and let $t\mapsto F_{t}$ be a $C^{1}$ map from $I$ into $C^{3}(M,S^{n+1}(1))$. Assume that each $F_{t}$ is a two-sided immersion and that $F_{0}=F$. Choose the global unit normals $\nu_{t}$ to depend $C^{1}$ on $t$, with $\nu_{0}=\nu$, and suppose that $\partial_{t}F_{t}|_{t=0}=\phi\nu$. Let $g_{t}$ and $A_{t}$ denote the induced metric and shape operator. Then
$$g'=-2\phi h, \tag{2}$$
$$A'=\nabla^{2}\phi+\phi(A^{2}+I), \tag{3}$$
where the Hessian in (3) is viewed as a self-adjoint endomorphism. If $F$ is minimal, then
$$H'=\Delta\phi+(n+S)\phi, \tag{4}$$
$$S'=2\left(\langle A,\nabla^{2}\phi\rangle+f_{3}\phi\right), \tag{5}$$
where, in a local $g$-orthonormal frame $\{e_{i}\}$, $h_{ij}=h(e_{i},e_{j})$, $\phi_{ij}=\nabla^{2}\phi(e_{i},e_{j})$, and $\langle A,\nabla^{2}\phi\rangle=\sum_{i,j}h_{ij}\phi_{ij}$. Here primes denote derivatives at $t=0$.

*Proof.* Let $X,Y$ be vector fields on $M$, extended independently of $t$, and identify $dF_{0}(X)$ and $dF_{0}(Y)$ with $X$ and $Y$. For a vector field $Z_{t}$ along $F_{t}$, write $D_{t}Z_{t}=\nabla_{\partial_{t}F_{t}}Z_{t}$. All quantities below are evaluated at $t=0$.

Put $V=\partial_{t}F_{t}|_{t=0}=\phi\nu$. Since $[\partial_{t},X]=0$, the torsion-free property of the ambient connection gives
$$\left.D_{t}\,dF_{t}(X)\right|_{t=0}=\nabla_{X}V=X(\phi)\nu-\phi AX.$$
Differentiating $g_{t}(X,Y)=\langle dF_{t}(X),dF_{t}(Y)\rangle$ and using the preceding identity, we obtain
$$g'(X,Y)=\langle X(\phi)\nu-\phi AX,Y\rangle+\langle X,Y(\phi)\nu-\phi AY\rangle=-2\phi h(X,Y).$$
This proves (2).

We next determine the variation of the unit normal. Differentiating $\langle\nu_{t},\nu_{t}\rangle=1$ shows that $D_{t}\nu_{t}|_{t=0}$ is orthogonal to $\nu$. Differentiating $\langle\nu_{t},dF_{t}(X)\rangle=0$ gives
$$\langle D_{t}\nu_{t}|_{t=0},X\rangle=-\left\langle\nu,\left.D_{t}dF_{t}(X)\right|_{t=0}\right\rangle=-X(\phi).$$
The vector $D_{t}\nu_{t}|_{t=0}$ is tangent to the ambient sphere and, by the preceding normalization identity, is orthogonal to $\nu$. Since $T_{F(x)}S^{n+1}(1)=dF(T_{x}M)\oplus\mathbb{R}\nu$, it therefore belongs to $dF(T_{x}M)$. The preceding identity then determines it uniquely as
$$D_{t}\nu_{t}|_{t=0}=-\nabla\phi.$$

Consider now the covariant second fundamental form $h_{t}(X,Y)=\langle\nabla_{dF_{t}(X)}dF_{t}(Y),\nu_{t}\rangle$. Differentiation yields
$$h'(X,Y)=\left\langle D_{t}\nabla_{dF_{t}(X)}dF_{t}(Y)\big|_{t=0},\nu\right\rangle+\langle\nabla_{X}Y,D_{t}\nu_{t}|_{t=0}\rangle.$$
The curvature commutation formula and $[\partial_{t},X]=0$ give
$$\left.D_{t}\nabla_{dF_{t}(X)}dF_{t}(Y)\right|_{t=0}=\nabla_{X}\big(Y(\phi)\nu-\phi AY\big)+R(\phi\nu,X)Y.$$
The normal component of the first term on the right is $X(Y(\phi))-\phi h(X,AY)$. For the unit sphere, $R(U,V)W=\langle V,W\rangle U-\langle U,W\rangle V$, and therefore $\langle R(\phi\nu,X)Y,\nu\rangle=\phi g(X,Y)$. The variation of the normal contributes
$$\langle\nabla_{X}Y,D_{t}\nu_{t}|_{t=0}\rangle=-\langle\nabla_{X}Y,\nabla\phi\rangle.$$
Combining these identities and using $\nabla^{2}\phi(X,Y)=X(Y(\phi))-\langle\nabla_{X}Y,\nabla\phi\rangle$, we find
$$h'(X,Y)=\nabla^{2}\phi(X,Y)+\phi g(X,Y)-\phi h(X,AY).$$
Equivalently,
$$h'=\nabla^{2}\phi+\phi g-\phi h\circ A,\qquad (h\circ A)(X,Y)=h(X,AY)=\langle A^{2}X,Y\rangle.$$

It remains to pass from the covariant tensor $h$ to the shape operator $A$. Differentiating $h_{t}(X,Y)=g_{t}(A_{t}X,Y)$ gives $h'(X,Y)=g'(AX,Y)+g(A'X,Y)$. Hence, by (2) and the formula for $h'$,
$$g(A'X,Y)=h'(X,Y)-g'(AX,Y)=\nabla^{2}\phi(X,Y)+\phi g(X,Y)-\phi\langle A^{2}X,Y\rangle+2\phi\langle A^{2}X,Y\rangle=\nabla^{2}\phi(X,Y)+\phi g(X,Y)+\phi\langle A^{2}X,Y\rangle.$$
Viewing the Hessian as a self-adjoint endomorphism therefore gives
$$A'=\nabla^{2}\phi+\phi(A^{2}+I),$$
which proves (3). Notice that the term $2\phi A^{2}$ arising from the variation of the metric is precisely what changes the term $-\phi A^{2}$ in $h'$ into $+\phi A^{2}$ in $A'$.

Finally, since $H=\mathrm{tr}\,A$, taking the trace of (3) gives
$$H'=\Delta\phi+(n+S)\phi.$$
This identity does not require minimality. Similarly, regarding $A_{t}$ as a family of endomorphisms of $TM$, we obtain
$$\begin{aligned}S'=\mathrm{tr}(A^{2})'&=2\,\mathrm{tr}(AA')\\&=2\langle A,\nabla^{2}\phi\rangle+2\phi\,\mathrm{tr}(A^{3})+2\phi\,\mathrm{tr}\,A\\&=2\langle A,\nabla^{2}\phi\rangle+2\phi f_{3}+2\phi H.\end{aligned}$$
When $F$ is minimal, $H=0$, and the last identity reduces to
$$S'=2\left(\langle A,\nabla^{2}\phi\rangle+f_{3}\phi\right).$$
This proves (4) and (5). $\square$

**Remark 2.2.** For a general variation field $W+\phi\nu$, the right-hand sides of the scalar variation formulas acquire the transport terms $W(H)$ and $W(S)$. These terms vanish along a family on which $H$ is zero and $S$ is spatially constant. Equivalently, a time-dependent reparametrization removes $W$, so Lemma 2.1 applies to the geometric family without changing its images.

## 3. Rigidity along differentiable families

The first ingredient is an exact no-drift statement for the constant $S$-value along a constrained family. To specify the regularity of such a family, we regard $C^{3}(M,S^{n+1}(1))$ as the Banach manifold of $C^{3}$ maps from $M$ into $S^{n+1}(1)$, with the topology induced by $C^{3}(M,\mathbb{R}^{n+2})$. A path $t\mapsto F_{t}$ is $C^{1}$ in this space if, after viewing $F_{t}$ as an $\mathbb{R}^{n+2}$-valued map, the derivative $\partial_{t}F_{t}$ exists in $C^{3}(M,\mathbb{R}^{n+2})$ and depends continuously on $t$ in the $C^{3}$ norm. The resulting rigidity statement does not require the maps $F_{t}$ to be embeddings.

**Proposition 3.1.** Let $I\subset\mathbb{R}$ be an interval, and let $t\mapsto F_{t}$ be a $C^{1}$ map from $I$ into $C^{3}(M,S^{n+1}(1))$. Assume that every $F_{t}$ is a two-sided minimal immersion and that both $S_{t}$ and $f_{3,t}$ are spatially constant on $M$. Then the function $t\mapsto S_{t}$ is constant on $I$.

*Proof.* Fix $t\in I$. On a parameter neighborhood of $t$, choose the global unit normals to depend $C^{1}$-smoothly on the parameter. Write
$$\partial_{t}F_{t}=dF_{t}(V)+\phi\nu=:W+\phi\nu,$$
where $V\in\Gamma(TM)$, $W=dF_{t}(V)$ is the tangential component, and $\phi=\langle\partial_{t}F_{t},\nu\rangle$ is the normal speed. The tangential component changes only the parametrization, so Remark 2.2 allows us to discard its transport terms. In the calculation below, all geometric quantities and the measure $d\mu$ are those of the fixed member $F_{t}$; the subscript $t$ is suppressed.

Because the family is minimal, Equation (4) gives
$$\Delta\phi+(n+S)\phi=0. \tag{6}$$
Integrating (6) over the closed hypersurface yields
$$\int_{M}\phi\,d\mu=0, \tag{7}$$
since $S$ is spatially constant, $S\ge 0$, and hence $n+S$ is a positive constant that may be taken outside the integral. Since $S_{t}$ is spatially constant, its derivative is a real number, and Equation (5) may be written as
$$\frac{1}{2}\frac{dS_{t}}{dt}=\langle A,\nabla^{2}\phi\rangle+f_{3}\phi=:c(t). \tag{8}$$
The contracted Codazzi identity (1) and minimality give
$$\int_{M}\langle A,\nabla^{2}\phi\rangle\,d\mu=-\int_{M}\langle\mathrm{div}\,A,\nabla\phi\rangle\,d\mu=0. \tag{9}$$
Integrating (8), using (9), the spatial constancy of $f_{3}$, and (7) gives
$$c(t)\,\mathrm{Vol}(M)=f_{3}\int_{M}\phi\,d\mu=0.$$
Thus $c(t)=0$ at every $t$, and hence $S_{t}$ is constant on $I$. $\square$

**Remark 3.2.** Without the spatial constancy of $f_{3}$, the same calculation gives
$$\frac{1}{2}S'\,\mathrm{Vol}(M)=\int_{M}\phi f_{3}\,d\mu,$$
and neither the Jacobi equation nor $\int_{M}\phi\,d\mu=0$ forces the right-hand side to vanish. This is the precise point at which the constant-$f_{3}$ hypothesis enters the local argument.

**Remark 3.3.** The preceding observation has a natural Fredholm formulation. Fix $t\in I$, and let $L_{t}=\Delta_{t}+n+S_{t}$ be the Jacobi operator of $F_{t}$. By (6), the normal speed $\phi$ belongs to $\ker L_{t}$. Since $L_{t}$ is self-adjoint and Fredholm on the closed manifold $M$, the Fredholm alternative gives
$$f_{3,t}\perp_{L^{2}(M,g_{t})}\ker L_{t}\quad\Longleftrightarrow\quad f_{3,t}\in\mathrm{Ran}\,L_{t}=\mathrm{Ran}(\Delta_{t}+n+S_{t}).$$
Thus the weaker range condition already forces the integral in Remark 3.2 to vanish and yields $\frac{dS_{t}}{dt}=0$. If $f_{3,t}$ is spatially constant, then $f_{3,t}=\frac{L_{t}f_{3,t}}{n+S_{t}}$, so the hypothesis of Proposition 3.1 implies the range condition. Consequently, the constant-$f_{3}$ assumption in Theorem 1.1 is a convenient sufficient condition for path rigidity, whereas the range condition above provides a weaker sufficient condition expressed in spectral terms. Extending Theorem 1.1 to the range condition requires showing, through the finite-dimensional reduction of Section 4, that this condition defines a semianalytic constrained set. The local rigidity statement must then be formulated relative to this set, so that the global compactness argument imposes the range condition on the approximating hypersurfaces without requiring it to pass to the limiting hypersurface.

## 4. Analytic local rigidity

We next pass from Proposition 3.1, which concerns differentiable paths, to a neighborhood statement without assuming that the local zero set of the mean curvature operator is a manifold. The finite-dimensional reduction used below is the standard Lyapunov–Schmidt construction for the mean-curvature operator, consistent with the general Fredholm description of minimal submanifolds in [27].

Fix a smooth closed embedded minimal hypersurface $F:M\hookrightarrow S^{n+1}(1)$, choose a global unit normal $\nu$, and fix $k\ge 4$ and $0<\alpha<1$. Here $C^{k,\alpha}(M)$ denotes the usual Hölder space of real-valued functions on $M$, defined with respect to the induced metric $g$. For $u\in C^{k,\alpha}(M)$ sufficiently small, the corresponding spherical normal graph is
$$F_{u}(x)=\cos(u(x))F(x)+\sin(u(x))\nu(x). \tag{10}$$
For $u$ sufficiently small, $F_{u}$ is an embedding. Up to reparametrization, every nearby embedding is uniquely represented as such a normal graph. Let $\pi_{F}$ be the nearest-point projection from a tubular neighborhood of $F(M)$ onto $F(M)$. If an embedding $G:M\to S^{n+1}(1)$ is sufficiently close to $F$ in $C^{k,\alpha}$, then
$$p_{G}=F^{-1}\circ\pi_{F}\circ G:M\to M$$
is a $C^{k,\alpha}$ diffeomorphism. The reparametrized embedding $G\circ p_{G}^{-1}$ meets each normal fiber of $F(M)$ once and hence has a unique representation $F_{u}$ of the form (10). Writing $\mathrm{Emb}^{k,\alpha}(M,S^{n+1}(1))$ for the space of $C^{k,\alpha}$ embeddings and $\mathrm{Diff}^{k,\alpha}(M)$ for the group of $C^{k,\alpha}$ diffeomorphisms of $M$, acting on embeddings by precomposition, the small normal graphs form a local slice for $\mathrm{Emb}^{k,\alpha}(M,S^{n+1}(1))\,/\,\mathrm{Diff}^{k,\alpha}(M)$.

Let $U\subset C^{k,\alpha}(M)$ be a sufficiently small open neighborhood of the origin. For $u\in U$, set
$$P_{u}=\cos u\,I-\sin u\,A,\qquad Q_{u}=\sin u\,I+\cos u\,A,\qquad \eta_{u}=-\sin u\,F+\cos u\,\nu.$$
Since $P_{0}=I$, $P_{u}$ is invertible for $u$ sufficiently small. Taking $U$ smaller if necessary, we may also assume that $F_{u}$ is an embedding for every $u\in U$. Differentiating (10) and using $d\nu(X)=-AX$ give
$$dF_{u}(X)=P_{u}X+du(X)\eta_{u}$$
for every $X\in T_{x}M$. All gradients and norms below are taken with respect to $g$. Set $\xi_{u}=P_{u}^{-1}\nabla u$. Since $\xi_{u}$ is orthogonal to both $F$ and $\nu$, the vectors $\eta_{u}$ and $\xi_{u}$ are tangent to $S^{n+1}(1)$ at $F_{u}(x)$. Moreover, since $P_{u}$ is self-adjoint, we have
$$\langle\eta_{u}-\xi_{u},dF_{u}(X)\rangle=du(X)-\langle P_{u}\xi_{u},X\rangle=du(X)-\langle\nabla u,X\rangle=0.$$
Since $\eta_{u}\perp\xi_{u}$ and $|\eta_{u}|=1$, we have $|\eta_{u}-\xi_{u}|^{2}=1+|\xi_{u}|^{2}$. Thus a unit normal to $F_{u}$ is
$$\nu_{u}=\frac{\eta_{u}-P_{u}^{-1}\nabla u}{\sqrt{1+|P_{u}^{-1}\nabla u|^{2}}}.$$
We choose the sign so that $\nu_{0}=\nu$. Let $g_{u}$, $h_{u}$, and $d\mu_{u}$ be the induced metric, scalar second fundamental form, and volume measure, respectively, pulled back to $M$, so that
$$g_{u}(X,Y)=\langle P_{u}X,P_{u}Y\rangle+du(X)du(Y),\qquad h_{u}(X,Y)=\langle\nabla_{dF_{u}(X)}dF_{u}(Y),\nu_{u}\rangle.$$
Let $A_{u}$ be the shape operator determined by $g_{u}(A_{u}X,Y)=h_{u}(X,Y)$, or equivalently $A_{u}=g_{u}^{-1}h_{u}$. Set $S_{u}=\mathrm{tr}(A_{u}^{2})$ and $f_{3,u}=\mathrm{tr}(A_{u}^{3})$. If $\hat{H}_{u}:F_{u}(M)\to\mathbb{R}$ denotes the mean curvature with respect to $\nu_{u}$, define
$$\mathcal{H}:U\to C^{k-2,\alpha}(M),\qquad \mathcal{H}(u)=\hat{H}_{u}\circ F_{u}=\mathrm{tr}_{g_{u}}h_{u}.$$
Thus $\mathcal{H}(u)=0$ if and only if $F_{u}$ is minimal, and the minimality of $F$ gives $\mathcal{H}(0)=0$. For the computation below, set $v_{u}=\sqrt{1+|P_{u}^{-1}\nabla u|^{2}}$. Let $e_{1},\dots,e_{n}$ be a local $g$-orthonormal frame and write $u_{i}=\nabla_{e_{i}}u$ and $u_{ij}=\nabla^{2}u(e_{i},e_{j})$. Let $D$ denote the Euclidean connection of $\mathbb{R}^{n+2}$. Since $\nu_{u}\perp F_{u}$, the second fundamental form may be computed with $D$ in place of the spherical connection. The Gauss formula for $F$, together with the definitions of $P_{u}$, $Q_{u}$, and $\eta_{u}$, gives
$$D_{X}\eta_{u}=-Q_{u}X-du(X)F_{u},$$
$$D_{X}(P_{u}Y)=P_{u}\nabla_{X}Y-du(X)Q_{u}Y-\sin u\,(\nabla_{X}A)Y+h(X,P_{u}Y)\nu-\langle X,P_{u}Y\rangle F.$$
Since $h_{u}$ is tensorial, we may compute at a point where $\nabla_{e_{i}}e_{j}=0$. Using $dF_{u}(e_{i})=P_{u}e_{i}+u_{i}\eta_{u}$ and the formula for $\nu_{u}$ in the definition of $h_{u}$, together with the identities above, we obtain
$$(h_{u})_{ij}=\frac{1}{v_{u}}u_{ij}+\frac{1}{v_{u}}\left[\langle Q_{u}e_{i},P_{u}e_{j}\rangle+u_{i}\langle Q_{u}e_{j},\xi_{u}\rangle+u_{j}\langle Q_{u}e_{i},\xi_{u}\rangle+\sin u\,\langle(\nabla_{e_{i}}A)e_{j},\xi_{u}\rangle\right].$$
When $u$ is constant, this formula reduces to the parallel hypersurface identity $A_{u}=P_{u}^{-1}Q_{u}$, which also fixes the sign convention. On the other hand, $(g_{u})_{ij}=\langle P_{u}e_{i},P_{u}e_{j}\rangle+u_{i}u_{j}$, so both $(g_{u})_{ij}$ and its inverse $(g_{u})^{ij}$ depend only on $x,u,\nabla u$. Consequently
$$\mathcal{H}(u)=\frac{1}{v_{u}}(g_{u})^{ij}u_{ij}+\frac{1}{v_{u}}(g_{u})^{ij}\left[\langle Q_{u}e_{i},P_{u}e_{j}\rangle+u_{i}\langle Q_{u}e_{j},\xi_{u}\rangle+u_{j}\langle Q_{u}e_{i},\xi_{u}\rangle+\sin u\,\langle(\nabla_{e_{i}}A)e_{j},\xi_{u}\rangle\right].$$
Thus $\mathcal{H}$ is a quasilinear second-order operator. The formulas above show that $g_{u}$ and $\frac{d\mu_{u}}{d\mu}$ depend only on $u$ and $\nabla u$, while $h_{u}$, and hence $A_{u}$, $S_{u}$, and $f_{3,u}$, also involve $\nabla^{2}u$. Thus $g_{u},\frac{d\mu_{u}}{d\mu}\in C^{k-1,\alpha}$ and $h_{u},A_{u},S_{u},f_{3,u}\in C^{k-2,\alpha}$. On $U$, both $P_{u}$ and $g_{u}$ remain uniformly invertible. Matrix inversion and the positive square root are analytic on their respective domains, while Hölder spaces are Banach algebras under pointwise multiplication. The formulas above therefore show that all these quantities depend real analytically on $u$, with values in the stated Hölder spaces. For analytic composition operators in Schauder spaces, see [26, Ch. II]. In particular, $\mathcal{H}:U\to C^{k-2,\alpha}(M)$ is real analytic near the origin. Lemma 2.1 gives its derivative
$$D\mathcal{H}(0)=L:=\Delta+n+S. \tag{11}$$

For smooth real-valued functions $u,v$ on $M$, integration by parts, together with the fact that $M$ has no boundary and $n+S$ is real-valued, gives
$$\int_{M}vLu\,d\mu=-\int_{M}\langle\nabla v,\nabla u\rangle\,d\mu+\int_{M}(n+S)uv\,d\mu=\int_{M}uLv\,d\mu.$$
Thus $L$ is formally self-adjoint. Since its principal part is $\Delta$, it is also elliptic. Standard elliptic Schauder theory on the closed manifold $M$ shows that $L:C^{k,\alpha}(M)\to C^{k-2,\alpha}(M)$ is Fredholm: its kernel is finite-dimensional, its range is closed, and the range has finite codimension in the codomain. We write $\mathrm{Ran}\,L$ for this range.

The Fredholm alternative, formal self-adjointness, and elliptic regularity imply that $f\in C^{k-2,\alpha}(M)$ belongs to $\mathrm{Ran}\,L$ if and only if $\int_{M}f\varphi\,d\mu=0$ for every $\varphi\in\ker L$. It follows that $\mathrm{codim}\,\mathrm{Ran}\,L=\dim\ker L$. Hence the Fredholm index of $L$, defined by
$$\mathrm{ind}\,L:=\dim\ker L-\mathrm{codim}\,\mathrm{Ran}\,L,$$
is zero.

Put $K=\ker L$. Elliptic regularity shows that every element of the finite-dimensional space $K$ is smooth. Let $K^{\perp_{L^{2}}}$ denote its orthogonal complement with respect to the $L^{2}(M,g)$ inner product, and set
$$X=C^{k,\alpha}(M)\cap K^{\perp_{L^{2}}},\qquad Y=C^{k-2,\alpha}(M)\cap K^{\perp_{L^{2}}}.$$
Then $C^{k,\alpha}(M)=K\oplus X$ and $C^{k-2,\alpha}(M)=K\oplus Y$. Since $L$ vanishes on $K$, the preceding characterization of its range shows that $L:X\to Y$ is bijective. The Schauder estimate then gives a bounded inverse $L^{-1}:Y\to X$.

Let $P$ be the $L^{2}$-orthogonal projection onto $K$, and put $Q=I-P$. Choosing an $L^{2}$-orthonormal basis of the smooth finite-dimensional space $K$ shows that $P$ is bounded on both $C^{k,\alpha}(M)$ and $C^{k-2,\alpha}(M)$. The analytic implicit function theorem therefore supplies neighborhoods $U_{K}\subset K$ and $U_{X}\subset X$ of zero and a real analytic map
$$\Psi:U_{K}\to U_{X},\qquad \Psi(0)=0,\qquad D\Psi(0)=0,$$
such that
$$Q\mathcal{H}(z+w)=0\quad\Longleftrightarrow\quad w=\Psi(z) \tag{12}$$
whenever $z+w$ is sufficiently small. Define the finite-dimensional obstruction map
$$\kappa:U_{K}\to K,\qquad \kappa(z)=P\mathcal{H}\big(z+\Psi(z)\big). \tag{13}$$
It follows from (12) and (13) that the small minimal graphs are exactly those represented by $z\in U_{K}$ with $\kappa(z)=0$.

For $u\in U$, denote the $d\mu_{u}$-averages of $S_{u}$ and $f_{3,u}$ by
$$\bar{S}(u)=\frac{\int_{M}S_{u}\,d\mu_{u}}{\int_{M}d\mu_{u}},\qquad \bar{f}_{3}(u)=\frac{\int_{M}f_{3,u}\,d\mu_{u}}{\int_{M}d\mu_{u}}. \tag{14}$$
Their deviations from these averages are measured by
$$V_{S}(u)=\int_{M}\left(S_{u}-\bar{S}(u)\right)^{2}d\mu_{u}, \tag{15}$$
$$V_{3}(u)=\int_{M}\left(f_{3,u}-\bar{f}_{3}(u)\right)^{2}d\mu_{u}. \tag{16}$$
The preceding formulas show that $\bar{S}(u)$, $\bar{f}_{3}(u)$, $V_{S}(u)$, and $V_{3}(u)$ depend real analytically on $u$ near the origin. Here we use the Banach-algebra property of Hölder spaces and the fact that $\int_{M}d\mu_{u}>0$. Since the integrands in (15) and (16) are continuous and nonnegative, $V_{S}(u)=0$ exactly when $S_{u}$ is spatially constant, and $V_{3}(u)=0$ exactly when $f_{3,u}$ is spatially constant.

**Theorem 4.1.** Let $F:M\hookrightarrow S^{n+1}(1)$ be a closed connected embedded minimal hypersurface with $S\equiv s_{0}$ and constant $f_{3}$. Then there exists $\varepsilon>0$ such that, for every $u\in C^{k,\alpha}(M)$ with $\|u\|_{C^{k,\alpha}}<\varepsilon$, if $F_{u}$ is minimal and both $S_{u}$ and $f_{3,u}$ are spatially constant, then $S_{u}\equiv s_{0}$. Equivalently, the same conclusion holds in the local normal slice described above, and hence in a neighborhood of $[F]$ in $\mathrm{Emb}^{k,\alpha}(M,S^{n+1}(1))\,/\,\mathrm{Diff}^{k,\alpha}(M)$.

*Proof.* Choose linear coordinates on the finite-dimensional space $K$, and define
$$u(z)=z+\Psi(z),\qquad s(z)=\bar{S}(u(z)),$$
and consider the real analytic set
$$Z=\{z\in U_{K}:\kappa(z)=0,\;V_{S}(u(z))=0,\;V_{3}(u(z))=0\}.$$
By construction, $z\in Z$ if and only if $F_{u(z)}$ is minimal and both $S_{u(z)}$ and $f_{3,u(z)}$ are spatially constant. Assume otherwise. Then there is a sequence $z_{j}\in Z$ converging to $0$ such that $s(z_{j})\neq s(0)=s_{0}$. After passing to a subsequence, either $s(z_{j})>s_{0}$ for every $j$ or $s(z_{j})<s_{0}$ for every $j$. We consider the first case; the second is handled in the same way. The origin then lies in the closure of the semianalytic set
$$Z_{+}=Z\cap\{z:s(z)>s_{0}\}.$$
The set $Z_{+}$ is semianalytic, hence subanalytic, so Hironaka's curve selection lemma [13, Proposition 3.9, p. 482] gives $\varepsilon>0$ and a real analytic curve $\gamma:(-\varepsilon,\varepsilon)\to U_{K}$ such that $\gamma(0)=0$ and $\gamma((0,\varepsilon))\subset Z_{+}$. For $0<t<\varepsilon$, the graphs $F_{u(\gamma(t))}$ form a real analytic family of minimal embeddings with spatially constant $S$ and $f_{3}$. Since $k\ge 4$ was fixed above, this family is $C^{1}$ with values in $C^{3}(M,S^{n+1}(1))$. Proposition 3.1 therefore applies on $(0,\varepsilon)$. Proposition 3.1 shows that $s(\gamma(t))$ has zero derivative for every $0<t<\varepsilon$, and hence is constant on that interval. Since $\gamma(t)\to 0$ as $t\to 0$, continuity of $s$ gives $s(\gamma(t))=s_{0}$ for $0<t<\varepsilon$. This contradicts $\gamma(t)\in Z_{+}$, where $s(\gamma(t))>s_{0}$. Hence every sufficiently small normal graph that is minimal and has spatially constant $S$ and $f_{3}$ satisfies $S\equiv s_{0}$. The local normal-graph representation then gives the same conclusion for embeddings sufficiently close to $F$, modulo reparametrization. $\square$

**Remark 4.2.** The Lyapunov–Schmidt reduction allows for a nontrivial Jacobi kernel $K=\ker L$. Curve selection handles possible singularities of the finite-dimensional constrained analytic set $Z$. Nontriviality of $K$ alone does not imply that the corresponding point of the minimal moduli space is singular. Vanishing of the derivative along smooth paths alone does not exclude the accumulation of different $S$-values along singular branches.

## 5. Uniform tubes and smooth embedded compactness

We now prove the global compactness statement needed to allow the source manifold and its topology to vary. For a closed embedded hypersurface $F:M\hookrightarrow S^{n+1}(1)$, define its spherical normal injectivity radius to be the supremum of the numbers $r>0$ for which
$$E:M\times(-r,r)\to S^{n+1}(1),\qquad E(x,t)=\cos t\,F(x)+\sin t\,\nu(x),$$
is injective and nonsingular.

**Lemma 5.1.** Let $F:M^{n}\hookrightarrow S^{n+1}(1)$ be a closed connected embedded minimal hypersurface satisfying $|A|\le K$. Define
$$r_{K}=\begin{cases}\arctan(K^{-1}), & K>0,\\ \pi/2, & K=0.\end{cases} \tag{17}$$
Then the spherical normal injectivity radius of $F(M)$ is at least $r_{K}$.

*Proof.* The embedded connected hypersurface separates the sphere into two connected open domains $\Omega_{+}$ and $\Omega_{-}$, whose closures are compact manifolds with common boundary $F(M)$. Give each closure the metric induced from the sphere and choose the inward unit normal along its boundary. With the induced metric, $\Omega_{\pm}$ has Ricci tensor $ng>0$, while its boundary $F(M)$ has zero mean curvature. Fix either sign. For the compact manifold $\Omega_{\pm}$, let $\mathrm{Roll}$ be the infimum of the inward boundary cut distances and let $\mathrm{Foc}$ be the infimum of the first inward focal distances. By these definitions, the inward normal exponential map is a diffeomorphism from $\partial\Omega_{\pm}\times[0,r)$ onto its image whenever $r<\mathrm{Roll}$, and one always has $\mathrm{Roll}\le\mathrm{Foc}$. Howard's rigidity form of the rolling theorem states that, for a complete connected manifold with smooth non-empty compact boundary, nonnegative Ricci curvature, and nonnegative inward mean curvature, the strict inequality $\mathrm{Roll}<\mathrm{Foc}$ can occur only for a Riemannian cylinder or a generalized Möbius band [14, Theorem 3]. Each exceptional space has a local product interval direction with zero Ricci curvature, so neither can be isometric to $\Omega_{+}$ or $\Omega_{-}$. Consequently the rolling radius of each side equals its focal radius.

Along a normal geodesic in the unit sphere, the tangential normal Jacobi map is
$$J_{t}=\cos t\,I-\sin t\,A \tag{18}$$
for the corresponding inward shape operator. If $\lambda$ is a principal curvature and $K>0$, the first positive zero of $\cos t-\lambda\sin t$, when it occurs before $\pi/2$, is $\arctan(1/\lambda)$ with $0<\lambda\le K$. If $\lambda\le 0$, no positive zero occurs before $\pi/2$. Thus the first focal distance on either side is at least $\arctan(K^{-1})$. When $K=0$, Equation (18) is $\cos t\,I$, and the first focal distance is $\pi/2$. The equality of rolling and focal radii shows that each one-sided normal exponential map is injective and nonsingular before $r_{K}$. For these parameter values, the normal segments are the unique minimizing geodesics to the boundary and remain in the interior of the corresponding domain. Hence normal geodesics directed into opposite sides cannot meet, because the two one-sided images lie in disjoint domains. The two one-sided estimates therefore give the required two-sided normal injectivity bound. $\square$

**Proposition 5.2.** Under the hypotheses of Lemma 5.1, let $r_{K}$ be defined by (17), and put $\delta_{K}=r_{K}/2$ and $b_{K}=\cos\delta_{K}-K\sin\delta_{K}$. Then $b_{K}>0$ and
$$\mathrm{Vol}(M)\le\frac{\mathrm{Vol}(S^{n+1}(1))}{2\delta_{K}b_{K}^{n}}. \tag{19}$$

*Proof.* The normal Jacobian at $(x,t)$ is
$$J(x,t)=\det\left(\cos t\,I-\sin t\,A_{x}\right)=\prod_{i=1}^{n}\left(\cos t-\lambda_{i}(x)\sin t\right). \tag{20}$$
For $|t|\le\delta_{K}$ and $|\lambda_{i}|\le K$, every factor in (20) is at least $b_{K}$. The choice $\delta_{K}<r_{K}$ implies $b_{K}>0$. Lemma 5.1 shows that the normal exponential map is injective on $M\times[-\delta_{K},\delta_{K}]$. The change-of-variables formula and (20) therefore give
$$\mathrm{Vol}(S^{n+1}(1))\ge\int_{-\delta_{K}}^{\delta_{K}}\int_{M}J(x,t)\,d\mu(x)dt\ge 2\delta_{K}b_{K}^{n}\,\mathrm{Vol}(M),$$
which is (19). $\square$

For $x\in S^{n+1}(1)$ and $\rho>0$, let $B_{\rho}(x)$ denote the open geodesic ball of radius $\rho$ centered at $x$. If $P\subset T_{x}S^{n+1}(1)$ is a linear subspace, set
$$B_{\rho}^{P}(0)=\{v\in P:|v|<\rho\},$$
where the norm is induced by the spherical metric at $x$.

**Lemma 5.3.** For fixed $n\ge 2$, $K\ge 0$, and $0<\theta<1$, there are constants $r>0$ and $C<\infty$. If $\Sigma^{n}\subset S^{n+1}(1)$ is a closed connected embedded minimal hypersurface satisfying $|A|\le K$, then, for every $x\in\Sigma$, the entire set $\Sigma\cap B_{r}(x)$ is a single spherical graph over $T_{x}\Sigma$. More precisely, after choosing a unit normal $\nu(x)$, there is a smooth function
$$u_{x}:B_{2r}^{T_{x}\Sigma}(0)\to(-r,r)$$
such that $u_{x}(0)=0$, $Du_{x}(0)=0$,
$$\|u_{x}\|_{C^{1,1}(B_{2r}^{T_{x}\Sigma}(0))}\le C,\qquad \|Du_{x}\|_{C^{0}(B_{2r}^{T_{x}\Sigma}(0))}\le\theta,$$
and
$$\Sigma\cap B_{r}(x)=\left\{\exp_{x}\left(v+u_{x}(v)\nu(x)\right):v\in B_{2r}^{T_{x}\Sigma}(0)\cap B_{r}(x)\right\}. \tag{21}$$

*Proof.* Let $r_{K}$ be defined by (17), put $\rho=\frac{r_{K}}{2}$, $b_{K}=\cos\rho-K\sin\rho>0$, and choose a unit normal field $\nu$ along $\Sigma$. By Lemma 5.1, the normal exponential map
$$E:\Sigma\times(-\rho,\rho)\to S^{n+1}(1),\qquad E(x,t)=\cos t\,x+\sin t\,\nu(x),$$
is a diffeomorphism onto its image $U$. The image $U$ is exactly the open metric $\rho$-neighborhood of $\Sigma$. Indeed, a minimizing geodesic from a point at distance less than $\rho$ to $\Sigma$ is normal at its endpoint. Conversely, if $E(x,t)$ had distance less than $|t|$ from $\Sigma$, a minimizing normal geodesic would give a second representation under $E$, contradicting injectivity. Thus $s(E(x,t))=t$ is the smooth signed-distance function on $U$.

In a principal frame at $x$, the tangential eigenvalues of $\nabla^{2}s$ at $E(x,t)$ are
$$-\frac{\sin t+\lambda_{i}(x)\cos t}{\cos t-\lambda_{i}(x)\sin t},\qquad 1\le i\le n,$$
and the eigenvalue in the normal geodesic direction is zero. Since
$$\cos t-\lambda_{i}(x)\sin t\ge\cos\rho-K\sin\rho=b_{K}>0$$
for $|t|<\rho$, we have the uniform estimates
$$|\nabla s|=1,\qquad |\nabla^{2}s|\le C_{0}:=\frac{\sqrt{n}(1+K)}{b_{K}}\ \ \text{on}\ U. \tag{22}$$

Choose $r>0$, depending only on $n$ and $K$, so small that $4r<\rho$, $16C_{0}r<1$, and the spherical exponential charts on balls of radius $4r$ have uniformly controlled $C^{2}$ norms and distortion. For $x\in\Sigma$, define
$$\Phi_{x}(v,\tau)=\exp_{x}\left(v+\tau\nu(x)\right),\qquad v\in B_{2r}^{T_{x}\Sigma}(0),\ |\tau|\le r.$$
The coordinate cylinder lies in $B_{4r}(x)\subset U$. At $(0,0)$, one has $\partial_{\tau}(s\circ\Phi_{x})|_{(0,0)}=1$. The Hessian bound (22) and the uniform $C^{2}$ control of $\Phi_{x}$ imply a uniform Lipschitz bound for $d(s\circ\Phi_{x})$. After decreasing $r$, uniformly in $x$ and $\Sigma$, it follows that
$$\partial_{\tau}(s\circ\Phi_{x})(v,\tau)\ge\frac{1}{4} \tag{23}$$
throughout the cylinder. Moreover, since $s(x)=0$ and $ds_{x}(v)=0$ for $v\in T_{x}\Sigma$, Taylor's formula along the radial geodesic and (22) give $s(\Phi_{x}(v,0))\le\frac{1}{2}C_{0}|v|^{2}<\frac{r}{8}$. Integrating (23) in the $\tau$-direction yields
$$s(\Phi_{x}(v,-r))<0<s(\Phi_{x}(v,r)).$$
Every vertical coordinate line therefore contains exactly one zero of $s\circ\Phi_{x}$.

The quantitative implicit-function theorem produces a smooth function $u_{x}$ whose graph is precisely the zero set in the coordinate cylinder. Since $s(\Phi_{x}(0,0))=s(x)=0$, uniqueness of the zero on the vertical line gives $u_{x}(0)=0$. Differentiating $(s\circ\Phi_{x})(v,u_{x}(v))=0$ at $v=0$, and using $ds_{x}|_{T_{x}\Sigma}=0$ and $\partial_{\tau}(s\circ\Phi_{x})(0,0)=1$, gives $Du_{x}(0)=0$. The functions $s\circ\Phi_{x}$ have a uniform $C^{1,1}$ bound and their $\tau$-derivatives have the uniform positive lower bound (23). Differentiating $(s\circ\Phi_{x})(v,u_{x}(v))=0$ once and twice, the second time almost everywhere, gives a uniform $C^{1,1}$ bound for $u_{x}$. Let $C_{1}$ be a uniform Lipschitz bound for $Du_{x}$ furnished by the preceding $C^{1,1}$ estimate. Since $Du_{x}(0)=0$, for every $v\in B_{2r}^{T_{x}\Sigma}(0)$, we have $|Du_{x}(v)|\le C_{1}|v|\le 2C_{1}r$. After decreasing $r$ further, depending also on $\theta$, we may assume that $2C_{1}r\le\theta$. Hence
$$\|Du_{x}\|_{C^{0}(B_{2r}^{T_{x}\Sigma}(0))}\le\theta.$$

If $y\in\Sigma\cap B_{r}(x)$, its unique spherical exponential coordinate at $x$ has the form $v+\tau\nu(x)$, with $|v|,|\tau|<r$. Since $s(y)=0$, uniqueness of the zero on the corresponding vertical line gives $\tau=u_{x}(v)$. The converse inclusion is immediate because the graph is contained in $s^{-1}(0)=\Sigma$. This proves (21), as we hoped. $\square$

**Proposition 5.4.** Let $F_{j}:M_{j}^{n}\hookrightarrow S^{n+1}(1)$ be a sequence of closed connected embedded minimal hypersurfaces satisfying
$$\sup_{M_{j}}|A_{j}|\le K.$$
After passage to a subsequence, there are a closed connected smooth manifold $M_{\infty}$, a smooth minimal embedding $F_{\infty}:M_{\infty}\hookrightarrow S^{n+1}(1)$, and diffeomorphisms $\psi_{j}:M_{\infty}\to M_{j}$ such that $F_{j}\circ\psi_{j}\to F_{\infty}$ smoothly. Moreover, the images $F_{j}(M_{j})$ are single-valued spherical normal graphs over $F_{\infty}(M_{\infty})$ for all sufficiently large $j$.

*Proof.* Set $\Sigma_{j}=F_{j}(M_{j})$. Apply Lemma 5.3 with $\theta=1/10$, and let $r$ be the resulting radius. The Blaschke selection theorem [2, Theorem 7.3.8, p. 253] gives, after passage to a subsequence, Hausdorff convergence
$$\Sigma_{j}\to\Sigma_{\infty}$$
for a nonempty compact set $\Sigma_{\infty}\subset S^{n+1}(1)$. Choose points $x_{\infty}^{1},\dots,x_{\infty}^{N}\in\Sigma_{\infty}$ such that the balls $B_{r/8}(x_{\infty}^{a})$ cover $\Sigma_{\infty}$, and choose $x_{j}^{a}\in\Sigma_{j}$ with $x_{j}^{a}\to x_{\infty}^{a}$. Using parallel transport, identify the tangent spaces with $T_{x_{\infty}^{a}}S^{n+1}(1)$. After passing to a further subsequence, we may assume, for all $1\le a\le N$, that
$$T_{x_{j}^{a}}\Sigma_{j}\to P_{\infty}^{a}\subset T_{x_{\infty}^{a}}S^{n+1}(1).$$

The local graphs supplied by Lemma 5.3 have uniformly small gradients and uniform $C^{1,1}$ bounds. Using parallel transport, identify the domains of the local graphs with fixed balls in $P_{\infty}^{a}$, and regraph over $P_{\infty}^{a}$ when necessary. The Arzelà–Ascoli theorem then gives, for every $\alpha\in(0,1)$,
$$u_{j}^{a}\to u_{\infty}^{a}\ \ \text{in}\ C^{1,\alpha},$$
where $u_{\infty}^{a}$ is $C^{1,1}$ with the same uniform bound. The limit graph is exactly $\Sigma_{\infty}$ in $B_{r/2}(x_{\infty}^{a})$. For one inclusion, every point on the limit graph is a limit of points of $\Sigma_{j}$. For the reverse inclusion, let $y\in\Sigma_{\infty}\cap B_{r/2}(x_{\infty}^{a})$ and choose $y_{j}\in\Sigma_{j}$ with $y_{j}\to y$. For large $j$, (21) shows that $y_{j}$ lies on the graph centered at $x_{j}^{a}$. Hence there is no additional component or sheet in the smaller ball.

For large $j$, the balls $B_{r/4}(x_{j}^{a})$ cover $\Sigma_{j}$, by Hausdorff convergence and the choice of the points $x_{\infty}^{a}$. On overlaps, the limiting graphs agree, since they describe the same Hausdorff limit. They therefore define an embedded $C^{1,1}$ atlas on $\Sigma_{\infty}$, and the convergence $\Sigma_{j}\to\Sigma_{\infty}$ is locally one-sheeted in $C^{1,\alpha}$. Since a Hausdorff limit of connected compact sets is connected, $\Sigma_{\infty}$ is connected.

Proposition 5.2 gives a uniform mass bound. The multiplicity-one conclusion, however, comes from the finite one-sheet graph cover rather than from the mass bound alone. Regard each associated varifold as a Radon measure on the compact Grassmann bundle $G_{n}(TS^{n+1})$. On each one-sheet graph chart, the graph parametrizations, area densities, and tangent planes converge uniformly. Using a partition of unity subordinate to the smaller balls, we may test this convergence against any continuous function on the Grassmann bundle. It follows that $\Sigma_{j}\to\Sigma_{\infty}$ as varifolds with multiplicity one. For every smooth vector field $X$ on the sphere, the function $(x,P)\mapsto\mathrm{div}_{P}X(x)$ is continuous on the Grassmann bundle. Minimality and the preceding varifold convergence therefore imply
$$0=\lim_{j\to\infty}\int_{\Sigma_{j}}\mathrm{div}_{T\Sigma_{j}}X\,d\mu_{j}=\int_{\Sigma_{\infty}}\mathrm{div}_{T\Sigma_{\infty}}X\,d\mu_{\infty}.$$
Hence $\Sigma_{\infty}$ is stationary.

In a $C^{1,1}$ graph chart, stationarity implies that the graph function $u$ is a weak solution of the Euler–Lagrange equation for the area functional
$$\partial_{\beta}A^{\beta}(x,u,\nabla u)=B(x,u,\nabla u), \tag{24}$$
where the equation is understood in the sense of distributions. Here $A^{\beta}$ and $B$ are smooth. Under the uniform gradient bound, the matrix $\left(\frac{\partial A^{\beta}}{\partial p_{\gamma}}\right)_{\beta,\gamma=1}^{n}$ is uniformly positive definite.

Since $u\in C^{1,1}\subset W^{2,\infty}$, the Sobolev chain rule expands (24) almost everywhere into the nondivergence equation
$$a^{\beta\gamma}(x)u_{\beta\gamma}=f(x),$$
where
$$a^{\beta\gamma}(x)=\frac{\partial A^{\beta}}{\partial p_{\gamma}}\left(x,u(x),\nabla u(x)\right)$$
and
$$f(x)=B(x,u,\nabla u)-\frac{\partial A^{\beta}}{\partial x_{\beta}}(x,u,\nabla u)-\frac{\partial A^{\beta}}{\partial z}(x,u,\nabla u)u_{\beta}.$$
Thus $a^{\beta\gamma}$ and $f$ are Lipschitz, and the equation is uniformly elliptic. In particular, on every relatively compact subchart and for each $\alpha\in(0,1)$, they belong to $C^{0,\alpha}$. Since $u\in W^{2,\infty}$ is a strong solution of the equation almost everywhere, the interior strong-solution regularity theorem for uniformly elliptic nondivergence equations gives $u\in C^{2,\alpha}$ [12, Theorem 9.19]. Once this regularity is available, differentiating the equation and applying Schauder estimates iteratively gives $u\in C^{\infty}$. Therefore $\Sigma_{\infty}$ is a closed connected smooth embedded minimal hypersurface.

Let $\pi_{\infty}$ be the nearest-point projection from a fixed tubular neighborhood of the smooth compact hypersurface $\Sigma_{\infty}$ onto $\Sigma_{\infty}$. Hausdorff and local $C^{1}$ convergence imply that $\Sigma_{j}$ lies in this tube and is transverse to its normal fibers for all sufficiently large $j$. Thus
$$\pi_{\infty}|_{\Sigma_{j}}:\Sigma_{j}\to\Sigma_{\infty}$$
is a local diffeomorphism. Its image is open and closed in the connected hypersurface $\Sigma_{\infty}$, so the map is surjective. Since $\Sigma_{j}$ is compact, it is therefore a finite covering.

We now verify that this covering has degree one. Fix $y\in\Sigma_{\infty}$ and choose one of the smaller one-sheet convergence balls containing $y$. After shrinking that ball once, both $\Sigma_{\infty}$ and the entire portion of $\Sigma_{j}$ in the twice larger ball are graphs over a fixed convex ball in $T_{y}\Sigma_{\infty}$, and their graph functions converge in $C^{1}$. In these coordinates, $\pi_{\infty}|_{\Sigma_{j}}$ is represented by a map $\Pi_{j}$ satisfying
$$\|D\Pi_{j}-I\|_{C^{0}}<\frac{1}{2}$$
for all sufficiently large $j$. For points $v,w$ in the smaller convex coordinate ball, integration along the segment from $w$ to $v$ gives
$$|\Pi_{j}(v)-\Pi_{j}(w)|\ge\frac{1}{2}|v-w|.$$
Hence $\Pi_{j}$ is injective there. If $z\in\Sigma_{j}$ lies in the fiber over $y$, then $y=\pi_{\infty}(z)$ and hence
$$d(z,y)=d(z,\Sigma_{\infty})\le d_{H}(\Sigma_{j},\Sigma_{\infty})\to 0.$$
Thus every point of the fiber lies in this coordinate ball when $j$ is large. The fiber therefore contains at most one point, and surjectivity shows that it contains exactly one. Since $y$ was arbitrary, the covering has degree one and $\pi_{\infty}|_{\Sigma_{j}}$ is a diffeomorphism.

Set $M_{\infty}=\Sigma_{\infty}$, let $F_{\infty}$ be the inclusion, and define
$$G_{j}=\left(\pi_{\infty}|_{\Sigma_{j}}\right)^{-1},\qquad \psi_{j}=F_{j}^{-1}\circ G_{j}.$$
Then $\psi_{j}:M_{\infty}\to M_{j}$ is a diffeomorphism and $F_{j}\circ\psi_{j}=G_{j}$. After choosing a unit normal $\nu_{\infty}$, there is a unique smooth function $v_{j}:M_{\infty}\to\mathbb{R}$, with $\|v_{j}\|_{C^{0}}\to 0$, such that
$$F_{j}\circ\psi_{j}(x)=\cos v_{j}(x)\,F_{\infty}(x)+\sin v_{j}(x)\,\nu_{\infty}(x). \tag{25}$$
The local $C^{1,\alpha}$ convergence gives $v_{j}\to 0$ in $C^{1,\alpha}$. On the finite atlas above, the passage from the tangent-plane graphs in Lemma 5.3 to the normal graph (25) is given by a fixed smooth coordinate change. Uniform transversality bounds its inverse derivatives, so the uniform local $C^{1,1}$ estimates transfer to a uniform $C^{1,1}$ bound for $v_{j}$.

In a fixed finite atlas of $M_{\infty}$, the minimal graph equation takes the form
$$a_{\infty}^{\beta\gamma}(x,v_{j},\nabla v_{j})\nabla_{\beta}\nabla_{\gamma}v_{j}=f_{\infty}(x,v_{j},\nabla v_{j}),$$
where the coefficients $a_{\infty}^{\beta\gamma}$ and $f_{\infty}$ depend smoothly on $x$, $v_{j}$, and $\nabla v_{j}$. The equation is uniformly elliptic. The uniform $C^{1,1}$ bound makes the coefficients and the right-hand side uniformly bounded in $C^{0,\alpha}$. Applying the interior strong-solution estimate on a finite collection of slightly smaller charts yields a uniform $C^{2,\alpha}$ bound. Schauder bootstrapping then yields uniform $C^{m,\alpha}$ bounds for every $m$. Thus the sequence $\{v_{j}\}$ is precompact in $C^{\infty}(M_{\infty})$. Since $v_{j}\to 0$ in $C^{1}$, every smooth subsequential limit is zero, and hence $v_{j}\to 0$ smoothly. By (25), $F_{j}\circ\psi_{j}\to F_{\infty}$ smoothly, and the images are single-valued spherical normal graphs over $F_{\infty}(M_{\infty})$ for all sufficiently large $j$. $\square$

**Remark 5.5.** A uniform bound for $|A|$ gives local graphical control. The global argument also uses minimality and embeddedness through Howard's rolling theorem. This gives a uniform tubular neighborhood, which in turn yields the area bound and rules out multiple sheets in the limit.

Both assumptions are needed. Wiygul constructed embedded minimal surfaces by stacking Clifford tori that converge to the Clifford torus with any prescribed fixed multiplicity [28]. In these examples the catenoidal necks shrink, so no uniform bound for $|A|$ can hold. On the other hand, if immersions are allowed, one may precompose a standard Clifford embedding with an $S^{1}$-factor by a degree-$d$ covering of that factor. The resulting immersions have the same $|A|$, $S$, and $f_{3}$, while their area and covering multiplicity increase with $d$. Thus the curvature bound excludes the first behavior, while embeddedness excludes the second.

**Corollary 5.6.** For fixed $n\ge 2$ and $\Lambda\ge 0$, only finitely many diffeomorphism types occur among closed connected manifolds $M^{n}$ admitting a minimal embedding $F:M\hookrightarrow S^{n+1}(1)$ with $\sup_{M}|A|^{2}\le\Lambda$.

*Proof.* Suppose otherwise, choose minimal embeddings $F_{j}:M_{j}\hookrightarrow S^{n+1}(1)$ such that no two of the manifolds $M_{j}$ are diffeomorphic and $\sup_{M_{j}}|A_{j}|\le\sqrt{\Lambda}$. Proposition 5.4 gives, after passing to a subsequence, a smooth manifold $M_{\infty}$ and diffeomorphisms $\psi_{j}:M_{\infty}\to M_{j}$. This contradicts the choice of the $M_{j}$. $\square$

**Remark 5.7.** The uniformity of the curvature bound in the preceding corollary is essential. Lawson constructed closed embedded minimal surfaces $\Sigma_{g}\subset S^{3}$ of arbitrarily large genus $g$ [16]. Writing $S_{g}=|A_{g}|^{2}$, the preceding corollary implies that
$$\max_{\Sigma_{g}}S_{g}\to\infty\quad\text{as}\quad g\to\infty.$$
Indeed, otherwise a subsequence would have a uniform upper bound for $S_{g}$ while representing infinitely many diffeomorphism types. This observation concerns the larger compactness class and does not assert that the Lawson surfaces have spatially constant $S$ or $f_{3}$.

## 6. Proof of the global theorem

*Proof of Theorem 1.1.* Assume for contradiction that $E_{n}^{(3)}\cap[0,\Lambda]$ contains infinitely many distinct values $s_{j}$. For every $j$, choose a closed connected manifold $M_{j}$ and a minimal embedding $F_{j}:M_{j}\hookrightarrow S^{n+1}(1)$ such that $S_{j}\equiv s_{j}$ and $f_{3,j}$ is spatially constant. The bound $s_{j}\le\Lambda$ gives $|A_{j}|\le\sqrt{\Lambda}$. Using Proposition 5.4, we obtain a smoothly convergent subsequence with an embedded minimal limit $F_{\infty}:M_{\infty}\hookrightarrow S^{n+1}(1)$, and the members of the subsequence are eventually single normal graphs over the limit.

After passing to a further subsequence, compactness of $[0,\Lambda]$ gives $s_{j}\to s_{\infty}$. Smooth convergence of the second fundamental forms yields $S_{\infty}=s_{\infty}$. Choose the normals of the eventual graphs compatibly with a fixed normal of the limit. Each corresponding $f_{3,j}$ is still spatially constant, and smooth convergence gives a spatially constant limit $f_{3,\infty}$. Thus the limiting hypersurface satisfies all hypotheses of Theorem 4.1. That theorem implies that for every sufficiently large $j$, $F_{j}(M_{j})$ has constant squared norm equal to $s_{\infty}$. Hence $s_{j}=s_{\infty}$ for all sufficiently large $j$, contradicting the choice of pairwise distinct values. The contradiction proves finiteness on $[0,\Lambda]$. $\square$

**Corollary 6.1.** For each fixed $n\ge 2$, the set $E_{n}^{(3)}$ is a closed locally finite subset of $[0,\infty)$, and in particular it has no finite accumulation point.

*Proof.* Local finiteness is exactly the conclusion of Theorem 1.1 on arbitrary compact intervals. Every locally finite subset of $[0,\infty)$ is closed because a point in its closure lies in a compact interval containing only finitely many points of the subset. $\square$

**Remark 6.2.** The set $E_{n}^{(3)}$ is a union over all closed connected source manifolds, not a spectrum attached to one fixed $M$. If disconnected sources are allowed while $S$ and $f_{3}$ are required to have one global constant value, selecting any connected component shows that the value set is unchanged. Theorem 1.1 is therefore the weak Chern conclusion for the subclass defined by embeddedness and constant $f_{3}$, but it does not settle the original immersed problem.

**AI disclosure.** During the preparatory phase, we used ChatGPT 5.6 Sol to interpret relevant literature and mathematical tools, including the Blaschke selection theorem and the real analytic curve selection lemma. All mathematical arguments and proofs were independently developed and verified by the authors, who prepared the final manuscript and take full responsibility for its content.

## References

[1] S. C. de Almeida and F. G. B. Brito, *Closed 3-dimensional hypersurfaces with constant mean curvature and constant scalar curvature*, Duke Math. J. **61** (1990), no. 1, 195–206.

[2] D. Burago, Y. Burago, and S. Ivanov, *A Course in Metric Geometry*, Graduate Studies in Mathematics, vol. 33, American Mathematical Society, Providence, RI, 2001.

[3] É. Cartan, *Sur des familles remarquables d'hypersurfaces isoparamétriques dans les espaces sphériques*, Math. Z. **45** (1939), 335–367.

[4] S. P. Chang, *On minimal hypersurfaces with constant scalar curvatures in $S^{4}$*, J. Differential Geom. **37** (1993), 523–534.

[5] Q.-M. Cheng, G. X. Wei, and T. Yamashiro, *The second gap of the scalar curvature of complete minimal hypersurfaces*, Comm. Anal. Geom. **33** (2025), no. 3, 623–636.

[6] S. S. Chern, *Minimal Submanifolds in a Riemannian Manifold*, Technical Report No. 19, Department of Mathematics, University of Kansas, Lawrence, 1968.

[7] S. S. Chern, M. do Carmo, and S. Kobayashi, *Minimal submanifolds of a sphere with second fundamental form of constant length*, in Functional Analysis and Related Fields, Springer, New York, 1970, pp. 59–75.

[8] Q. T. Deng, H. L. Gu, and Q. Y. Wei, *Closed Willmore minimal hypersurfaces with constant scalar curvature in $S^{5}(1)$ are isoparametric*, Adv. Math. **314** (2017), 278–305.

[9] Q. Ding and Y. L. Xin, *On Chern's problem for rigidity of minimal hypersurfaces in the spheres*, Adv. Math. **227** (2011), 131–145.

[10] B. Firester and R. Tsiamis, *On Chern's conjecture for minimal submanifolds of the sphere*, arXiv:2608.18074 (2026).

[11] J. Q. Ge and Z. Z. Tang, *Chern conjecture and isoparametric hypersurfaces*, in Differential Geometry, Adv. Lect. Math. (ALM), vol. 22, International Press, Somerville, MA, 2012, pp. 49–60.

[12] D. Gilbarg and N. S. Trudinger, *Elliptic Partial Differential Equations of Second Order*, 2nd ed., Classics in Mathematics, Springer-Verlag, Berlin, 2001.

[13] H. Hironaka, *Subanalytic sets*, in Number Theory, Algebraic Geometry and Commutative Algebra: In Honor of Yasuo Akizuki, Kinokuniya, Tokyo, 1973, pp. 453–493.

[14] R. Howard, *Blaschke's rolling theorem for manifolds with boundary*, Manuscripta Math. **99** (1999), no. 4, 471–483.

[15] H. B. Lawson, Jr., *Local rigidity theorems for minimal hypersurfaces*, Ann. of Math. (2) **89** (1969), 187–197.

[16] H. B. Lawson, Jr., *Complete minimal surfaces in $S^{3}$*, Ann. of Math. (2) **92** (1970), no. 3, 335–374.

[17] L. Lei, H. W. Xu, and Z. Y. Xu, *On the generalized Chern conjecture for hypersurfaces with constant mean curvature in a sphere*, Sci. China Math. **64** (2021), no. 7, 1493–1504.

[18] H. F. Münzner, *Isoparametrische Hyperflächen in Sphären*, Math. Ann. **251** (1980), 57–71.

[19] H. F. Münzner, *Isoparametrische Hyperflächen in Sphären. II*, Math. Ann. **256** (1981), 215–232.

[20] C. K. Peng and C. L. Terng, *Minimal hypersurfaces of spheres with constant scalar curvature*, in Seminar on Minimal Submanifolds, Ann. of Math. Stud., vol. 103, Princeton University Press, Princeton, NJ, 1983, pp. 177–198.

[21] C. K. Peng and C. L. Terng, *The scalar curvature of minimal hypersurfaces in spheres*, Math. Ann. **266** (1983), 105–113.

[22] M. Scherfner, S. Weiss, and S.-T. Yau, *A review of the Chern conjecture for isoparametric hypersurfaces in spheres*, in Advances in Geometric Analysis, Adv. Lect. Math. (ALM), vol. 21, International Press, Somerville, MA, 2012, pp. 175–187.

[23] J. Simons, *Minimal varieties in Riemannian manifolds*, Ann. of Math. (2) **88** (1968), 62–105.

[24] Z. Z. Tang, D. Y. Wei, and W. J. Yan, *A sufficient condition for a hypersurface to be isoparametric*, Tohoku Math. J. (2) **72** (2020), no. 4, 493–505.

[25] Z. Z. Tang and W. J. Yan, *On the Chern conjecture for isoparametric hypersurfaces*, Sci. China Math. **66** (2023), 143–162.

[26] T. Valent, *Boundary Value Problems of Finite Elasticity: Local Theorems on Existence, Uniqueness, and Analytic Dependence on Data*, Springer Tracts in Natural Philosophy, vol. 31, Springer-Verlag, New York, 1988.

[27] B. White, *The space of minimal submanifolds for varying Riemannian metrics*, Indiana Univ. Math. J. **40** (1991), no. 1, 161–200.

[28] D. Wiygul, *Minimal surfaces in the 3-sphere by stacking Clifford tori*, J. Differential Geom. **114** (2020), no. 3, 467–549.

[29] H. W. Xu and Z. Y. Xu, *On Chern's conjecture for minimal hypersurfaces and rigidity of self-shrinkers*, J. Funct. Anal. **273** (2017), no. 11, 3406–3425.

[30] S.-T. Yau, *Problem section*, in Seminar on Differential Geometry, Ann. of Math. Stud., vol. 102, Princeton University Press, Princeton, NJ, 1982, pp. 669–706.

---

*School of Mathematical Sciences, Laboratory of Mathematics and Complex Systems, Beijing Normal University, Beijing 100875, P. R. China*
*Email address: hxtan@mail.bnu.edu.cn*

*Chern Institute of Mathematics & LPMC, Nankai University, Tianjin 300071, P. R. China*
*Email address: zztang@nankai.edu.cn*

*School of Mathematics, Hangzhou Normal University, Hangzhou 311121, P. R. China*
*Email address: yuqxie@hznu.edu.cn*

*School of Mathematical Sciences, Laboratory of Mathematics and Complex Systems, Beijing Normal University, Beijing 100875, P. R. China*
*Email address: wjyan@bnu.edu.cn*
