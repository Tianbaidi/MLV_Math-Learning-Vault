---
tags:
  - Fourier_Analysis
---

> [!Question] Main Question  
> 在给定的 $t_0\in[0,2\pi]$ 处，总存在一个连续函数，使得它的 Fourier series 在该点发散。

## Proof

我们先证明在点 $0$ 处存在连续函数，其 Fourier 级数发散。之后再通过平移推广到任意给定的 $t_0$。
记 Fourier 部分和为
$$S_N(f)(\theta)=\sum_{|n|\leq N}\widehat f(n)e^{in\theta}.  $$
我们从锯齿函数的 Fourier 级数出发：
$$  \sum_{n\neq 0}\frac{e^{in\theta}}{n}.  $$
这个级数在正频率 $e^{in\theta}$ 与负频率 $e^{-in\theta}$ 之间具有对称性。为了制造发散，我们将打破这种对称性。
对每个 $N\geq 1$，定义
$$f_N(\theta)=\sum_{1\leq |n|\leq N}\frac{e^{in\theta}}{n},  $$
以及只包含负频率部分的函数
$$\widetilde f_N(\theta)=\sum_{-N\leq n\leq -1}\frac{e^{in\theta}}{n}.  $$
注意在 $\theta=0$ 处，
$$  \widetilde f_N(0)=\sum_{n=-N}^{-1}\frac{1}{n}  =-\sum_{n=1}^N\frac{1}{n}. $$
因此
 $$  |\widetilde f_N(0)|\sum_{n=1}^N\frac{1}{n}  \geq \log N.  $$
所以负频率部分在 $0$ 处可以产生大约 $\log N$ 级别的增长。
另一方面，$f_N$ 是完整的对称部分和。由锯齿函数 Fourier 级数的 Abel 平均有界性，以及相应的 Tauber 型估计，可知存在常数 $C>0$，使得对一切 $N$ 与 $\theta$ 都有
$$|f_N(\theta)|\leq C.  $$
也就是说，$f_N$ 关于 $N$ 与 $\theta$ 一致有界。
接下来进行频率平移。定义
$$  P_N(\theta)=e^{i2N\theta}f_N(\theta),  $$
以及
$$  \widetilde P_N(\theta)=e^{i2N\theta}\widetilde f_N(\theta).  $$
由于乘上 $e^{i2N\theta}$ 会把所有 Fourier 频率整体向右平移 $2N$ 个单位，所以 $P_N$ 的非零频率集中在区间
$$  N\leq n\leq 3N  $$
之中，而其对称中心从原来的 $0$ 被移动到了 $2N$。
于是 Fourier 部分和算子 $S_M$ 对 $P_N$ 有如下作用：
$$  S_M(P_N)(\theta)=  \begin{cases}  P_N(\theta), & M\geq 3N,\\\widetilde P_N(\theta), & M=2N,\\  0, & M<N.  \end{cases}  $$
其中最关键的是 $M=2N$ 的情况。此时 $S_{2N}$ 正好截取到平移后的左半部分频率，因此把原本对称的频率块截成了不对称的一半。这就是所谓的“对称破缺”。
现在选择一列增长很快的正整数 $N_k$，以及一个正项可和数列 $\alpha_k$，使得
$$  N_{k+1}>3N_k  $$
并且
$$  \alpha_k\log N_k\to\infty.  $$
例如可以取
$$  \alpha_k=\frac{1}{k^2},  \qquad  N_k=3^{2^k}.  $$
此时
$$  \sum_{k=1}^{\infty}\alpha_k<\infty,  $$
并且
 $$  \alpha_k\log N_k\frac{1}{k^2}\cdot 2^k\log 3  \to\infty.  $$
现在定义函数
$$  
F(\theta)=\sum_{k=1}^{\infty}\alpha_k P_{N_k}(\theta).  
$$

由于 $|P_N(\theta)|=|f_N(\theta)|$，而 $f_N$ 一致有界，所以存在常数 $C>0$，使得
$$  |P_{N_k}(\theta)|\leq C.  $$
又因为
$$  \sum_{k=1}^{\infty}\alpha_k<\infty,  $$
所以由 Weierstrass 判别法，级数
$$  \sum_{k=1}^{\infty}\alpha_k P_{N_k}(\theta)  $$
一致收敛。因此 $F$ 是一个连续的 $2\pi$-周期函数。
下面证明 $F$ 的 Fourier 级数在 $0$ 处发散。
取部分和指标
$$  M=2N_m.  $$
由于 $N_{k+1}>3N_k$，不同的频率块彼此分离。因此当计算 $S_{2N_m}(F)(0)$ 时：
- 对于 $k<m$ 的频率块，已经被完整包含进来；
    
- 对于 $k=m$ 的频率块，正好被截成不对称的一半；
    
- 对于 $k>m$ 的频率块，还完全没有被截到。
    
因此

$$  S_{2N_m}(F)(0)\sum_{k<m}\alpha_k P_{N_k}(0)  +  \alpha_m \widetilde P_{N_m}(0).  $$
前一项由于 $P_{N_k}$ 一致有界且 $\sum \alpha_k$ 收敛，所以整体是有界的，即
$$  \left|\sum_{k<m}\alpha_k P_{N_k}(0)\right|=O(1).  $$
而第二项满足
$$  |\widetilde P_{N_m}(0)||\widetilde f_{N_m}(0)|  \geq \log N_m.  $$
于是
$$  |S_{2N_m}(F)(0)|  \geq  \alpha_m|\widetilde P_{N_m}(0)|-O(1).  $$
因此
$$  |S_{2N_m}(F)(0)|  \geq  \alpha_m\log N_m-O(1).  $$
由于我们已经选择了 $\alpha_m\log N_m\to\infty$，所以
$$  |S_{2N_m}(F)(0)|\to\infty.  $$
这说明 $F$ 的 Fourier 部分和在 $0$ 处无界，因此 Fourier 级数在 $0$ 处发散。
最后，将结论推广到任意给定点 $t_0\in[0,2\pi]$。
定义
$$  G(\theta)=F(\theta-t_0).  $$
则 $G$ 仍然是连续的 $2\pi$-周期函数。并且由 Fourier 系数的平移性质可知，
$$  S_N(G)(\theta)=S_N(F)(\theta-t_0).  $$
令 $\theta=t_0$，得到
$$  S_N(G)(t_0)=S_N(F)(0).  $$
由于 $S_N(F)(0)$ 发散，所以 $S_N(G)(t_0)$ 也发散。
因此，对于任意给定的 $t_0\in[0,2\pi]$，都存在连续函数 $G$，使得它的 Fourier series 在 $t_0$ 处发散。
**证毕。**