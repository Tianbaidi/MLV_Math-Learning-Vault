---
tags:
  - Fourier_Analysis
  - Exercises
---
1. If $z=x+iy$ is a complex number with $x,y\in \mathbb{R}$ , we define 
$$|z|=(x^{2}+y^{2})^{1/2}$$
and we call this quantity the moudulus(模) or absolute value of $z$ .

(a) What is the geometric interpretation of $|z|$ 
   Answer: The length in the complex plane
(b) Show that if $|z|=0$ ,then $z=0$ 
   if $|z|=0$ , $x^{2}+y^{2}=0$ 
   Accroding to $x,y \in \mathbb{R}$ , $x=0$ and so $y$
   $z=0$ 
(c) Show that if $\lambda\in \mathbb{R}$ , then $|\lambda z|=|\lambda||z|$ ,where  $\lambda$ donates the standard absolute value of a real number
   $\lambda z=\lambda x+i\lambda y$  and the moudulus of $\lambda z$ is $(\lambda^{2}x^{2}+\lambda^{2}y^{2})^{1/2}=\lambda(x^{2}+y^{2})^{1/2}=|\lambda||z|$ 
(d) If $z_{1}$ and $z_{2}$ are two complex number, prove that 
$$|z_{1}z_{2}|=|z_{1}||z_{2}|\quad and \quad |z_{1}+z_{2}|=|z_{1}|+|z_{2}|$$
make $z_{1}=x_{1}+iy_{1}$ , $z_{2}=x_{2}+iy_{2}$ . $z_{1}z_{2}=x_{1}x_{2}+iy_{2}x_{1}+iy_{1}x_{2}-y_{1}y_{2}=[x_{1}x_{2}-y_{1}y_{2}]+i[y_{2}x_{1}-y_{1}x_{2}]$ , then we calculate the moudulus of this niw complex number ...
but the next question is much harder! However we can use the Geometric interpretation of $|z|$ and then ,we can see a triangle...
(e) Show that if $z \not=0$ , then $|\frac{1}{z}|=\frac{1}{|z|}$

---

 复数的柯西收敛准则证明

设 $\{z_n\}$ 是一个复数序列，其中 $z_n = x_n + i y_n$，$x_n, y_n \in \mathbb{R}$。  
**定理**：$\{z_n\}$ 收敛当且仅当它是柯西序列，即  
$\forall \varepsilon > 0,\ \exists N \in \mathbb{N},\ \forall m,n > N:\ |z_n - z_m| < \varepsilon.$

Let $\{z_n\}$ be a sequence of complex numbers, where $z_n = x_n + i y_n$, $x_n, y_n \in \mathbb{R}$.  
**Theorem**: $\{z_n\}$ converges if and only if it is a Cauchy sequence, i.e.,  
$\forall \varepsilon > 0,\ \exists N \in \mathbb{N},\ \forall m,n > N:\ |z_n - z_m| < \varepsilon.$

---

 1. 必要性（收敛 $\Rightarrow$ 柯西序列）

**证明**：  
假设 $z_n \to z$。对任意 $\varepsilon > 0$，存在 $N$ 使 $n > N$ 时 $|z_n - z| < \frac{\varepsilon}{2}$。  
取 $m,n > N$，由三角不等式：
$$
|z_n - z_m| \le |z_n - z| + |z - z_m| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.
$$
因此 $\{z_n\}$ 是柯西序列。 $\square$
**Proof**:  
Assume $z_n \to z$. For any $\varepsilon > 0$, there exists $N$ such that $|z_n - z| < \frac{\varepsilon}{2}$ whenever $n > N$.  
Take $m,n > N$. By the triangle inequality:
$$
|z_n - z_m| \le |z_n - z| + |z - z_m| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.
$$
Hence $\{z_n\}$ is a Cauchy sequence. $\square$

---

 2. 充分性（柯西序列 $\Rightarrow$ 收敛）

**证明**：  
已知 $\{z_n\}$ 是柯西序列，即对任意 $\varepsilon > 0$，存在 $N$ 使 $m,n > N$ 时 $|z_n - z_m| < \varepsilon$。
**Proof**:  
Assume $\{z_n\}$ is a Cauchy sequence, i.e., for any $\varepsilon > 0$, there exists $N$ such that $|z_n - z_m| < \varepsilon$ whenever $m,n > N$.
 2.1 转化为实部与虚部序列
利用不等式：
$$
|x_n - x_m| \le |z_n - z_m|,\quad |y_n - y_m| \le |z_n - z_m|.
$$
于是对同样的 $N$，当 $m,n > N$ 时有
$$
|x_n - x_m| < \varepsilon,\qquad |y_n - y_m| < \varepsilon.
$$
所以 $\{x_n\}$ 和 $\{y_n\}$ 都是实数域中的柯西序列。
Using the inequalities:
$$
|x_n - x_m| \le |z_n - z_m|,\quad |y_n - y_m| \le |z_n - z_m|.
$$
Then for the same $N$, whenever $m,n > N$, we have
$$
|x_n - x_m| < \varepsilon,\qquad |y_n - y_m| < \varepsilon.
$$
Thus $\{x_n\}$ and $\{y_n\}$ are Cauchy sequences in the real numbers.
 2.2 利用实数完备性
实数域 $\mathbb{R}$ 是完备的，因此实柯西序列必收敛：
$$
x_n \to x \in \mathbb{R},\quad y_n \to y \in \mathbb{R}.
$$
The real field $\mathbb{R}$ is complete; therefore every real Cauchy sequence converges:
$$
x_n \to x \in \mathbb{R},\quad y_n \to y \in \mathbb{R}.
$$

 2.3 构造复数极限并验证
令 $z = x + iy$。估计：
$$
|z_n - z| = |(x_n - x) + i(y_n - y)| \le |x_n - x| + |y_n - y|.
$$
由 $x_n \to x,\ y_n \to y$，对任意 $\varepsilon > 0$，存在 $N_1,N_2$：
- 当 $n > N_1$ 时，$|x_n - x| < \frac{\varepsilon}{2}$；
- 当 $n > N_2$ 时，$|y_n - y| < \frac{\varepsilon}{2}$。
取 $N = \max(N_1,N_2)$，则当 $n > N$ 时：
$$
|z_n - z| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.
$$
即 $z_n \to z$。 $\square$
Let $z = x + iy$. Estimate:
$$
|z_n - z| = |(x_n - x) + i(y_n - y)| \le |x_n - x| + |y_n - y|.
$$
Since $x_n \to x$ and $y_n \to y$, for any $\varepsilon > 0$, there exist $N_1, N_2$ such that:
- $|x_n - x| < \frac{\varepsilon}{2}$ for $n > N_1$;
- $|y_n - y| < \frac{\varepsilon}{2}$ for $n > N_2$.
Take $N = \max(N_1, N_2)$. Then for all $n > N$:
$$
|z_n - z| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.
$$
That is, $z_n \to z$. $\square$