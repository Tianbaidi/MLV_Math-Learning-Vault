---
tags:
  - Algebraic_Topology
  - Fundamental_Group
---
# Reparametrization 重新参数化

在研究路径时，一条路径不仅包含“经过哪些点”，还包含了“在什么时间经过这些点”。设$f:I\to X,\qquad I=[0,1]$ 是一条路径。如果存在连续映射 $\varphi:I\to I$ 满足 $\varphi(0)=0,\qquad \varphi(1)=1,$ 那么复合映射
$$
f\circ\varphi:I\to X
$$
称为路径 $f$ 的一个 **reparametrization（重新参数化）**。也可以简写为 $f\varphi.$


重新参数化的核心思想是：
$$
\boxed{\text{改变路径的“时间安排”，而不改变路径的几何内容}}
$$

原路径在时刻 $s$ 位于 $f(s),$ 重新参数化之后，在时刻 $s$ 位于

$$
f(\varphi(s)).
$$

也就是说，$\varphi$ 告诉我们：
> 新时间 $s$ 应当对应原路径的哪个时间 $\varphi(s)$。

例如，如果 $\varphi(s)=s^2,$ 那么重新参数化后的路径为
$$
f(s^2).
$$
由于当 $0<s<1$ 时有 $s^2<s,$ 所以路径前半段走得更慢，后半段走得更快。但仍然有
$$
f(\varphi(0))=f(0),
$$
以及

$$
f(\varphi(1))=f(1),
$$
因此起点和终点没有发生变化。

我们并没有要求 $\varphi$ 单调递增。因此重新参数化不一定只是“改变速度”。 $\varphi$ 可以先增加、再减少、最后再增加，此时 $f\circ\varphi$ 可能表现为：
$$
\text{沿 }f\text{ 前进}
\longrightarrow
\text{倒退一段}
\longrightarrow
\text{继续前进}.
$$

只要 $\varphi(0)=0,\qquad \varphi(1)=1$ 并且 $\varphi$ 连续，仍然是 Hatcher 意义下的重新参数化。


重新参数化最重要的性质是
$$
\boxed{f\circ\varphi\simeq f.}
$$
也就是说：

> 重新参数化不会改变路径的同伦类。

把 $\varphi$ 连续地变成恒等映射 $\operatorname{id}_I(s)=s.$ 定义
$$
\varphi_t(s)
=
(1-t)\varphi(s)+ts.
$$

- 当 $t=0$ 时， $\varphi_0(s)=\varphi(s)$ ;
	
- 而当 $t=1$ 时，$\varphi_1(s)=s.$ ;

因此 $f\circ\varphi_t$ , 给出了一个同伦
$$
f\circ\varphi\simeq f.
$$

这里 $\varphi_t(s)$ 始终属于 $I$，因为 $\varphi_t(s)=(1-t)\varphi(s)+ts$ 是 $\varphi(s)$ 与 $s$ 的凸组合。且
$$
\varphi_t(0)=0,
\qquad
\varphi_t(1)=1,
$$
所以这个同伦始终保持路径的两个端点不动。

---

## 在基本群这里引入重新参数化？

路径乘法定义为
$$
fg(s)=
\begin{cases}
f(2s), & 0\le s\le \frac12,\\
g(2s-1), & \frac12\le s\le1.
\end{cases}
$$

因此每拼接一次路径，就会重新分配各段路径所占的时间。

例如比较 $(fg)h$ 和 $f(gh).$

- 对于 $(fg)h$：
$$
f:\left[0,\frac14\right],
\qquad
g:\left[\frac14,\frac12\right],
\qquad
h:\left[\frac12,1\right].
$$
	
- 而对于 $f(gh)$：
$$
f:\left[0,\frac12\right],
\qquad
g:\left[\frac12,\frac34\right],
\qquad
h:\left[\frac34,1\right].
$$

因此作为具体的映射，一般有 $(fg)h\neq f(gh).$ 但两条路径实际经过的顺序都是
$$
f\longrightarrow g\longrightarrow h.
$$
区别只是各段路径所占的时间不同。所以存在一个分段线性的重新参数化
$$
\varphi:I\to I
$$
使得 $f(gh)=((fg)h)\circ\varphi.$ 由于重新参数化保持同伦类，
$$
((fg)h)\circ\varphi\simeq(fg)h,
$$
于是 $f(gh)\simeq(fg)h.$ 因此在同伦类上有
$$
[f(gh)]=[(fg)h].
$$
也就是
$$
[f]([g][h])=([f][g])[h].
$$

这证明了 $\pi_1(X,x_0)$ 中乘法的结合律。所以这里重新参数化的作用可以概括成：
$$
\boxed{
\text{把“只是时间安排不同”的路径识别为同一个同伦类}
}
$$

---

重新参数化还可以用来理解单位元。设 $c$ 是常值路径。路径
$$
fc
$$
表示：

- 前一半时间把 $f$ 走完；
- 后一半时间停在终点。

它和原来的 $f$ 只是在时间安排上不同，因此
$$
fc\simeq f.
$$
同理，

$$
cf\simeq f.
$$
因此常值路径的同伦类就是基本群中的单位元。

---

## 更一般的理解

重新参数化体现了一个非常普遍的数学思想：

$$
\boxed{
\text{区分一个几何对象本身，与描述这个对象所使用的参数}
}
$$

路径

$$
f:I\to X
$$

其实同时包含两部分信息：

1. 路径在空间 $X$ 中经过哪些点；
2. 在什么时间经过这些点。

但在很多拓扑问题中，我们真正关心的是第一部分，而第二部分只是描述方式。

因此可以通过重新参数化改变“时间表”，而保留真正重要的拓扑信息。

类似的思想以后还会出现在：

- 曲线的弧长参数化；
- 曲线积分的参数无关性；
- 微分几何中的单位速度曲线；
- 测地线的参数选择；
- 变分法中的参数规范化。

所以重新参数化不只是 Proposition 1.3 中为了证明结合律临时使用的小技巧，它体现的是：

$$
\boxed{
\text{去掉不重要的参数自由度，只保留真正的几何信息}
}
$$

---

## 一句话总结

> **Reparametrization 是通过复合 $f\circ\varphi$ 改变路径的时间安排；只要 $\varphi(0)=0,\varphi(1)=1$，重新参数化后的路径与原路径保持端点固定同伦。**

因此它特别适合处理：
$$
\boxed{\text{几何路径相同，但速度或时间分配不同}}
$$

的情况。

❤️来自*Chatgpt*。