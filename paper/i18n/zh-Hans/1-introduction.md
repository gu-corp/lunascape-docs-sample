---
navigation:
  order: 10
---

# 1. 引言

有限状态空间上不可约且非周期的马尔可夫链，随时间收敛到唯一的平稳分布 \(\pi\)。衡量收敛快慢的量是**混合时间**。记链的转移矩阵为 \(P\)，时刻 \(t\) 从状态 \(x\) 出发的分布为 \(P^t(x,\cdot)\)，定义

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

其中 \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) 为全变差距离。

本文讨论图 \(G = (V, E)\) 上的**懒惰随机游走**（每一时刻以概率 \(1/2\) 停留在原处，以概率 \(1/2\) 均匀地移动到相邻顶点）。懒惰性保证了非周期性，转移矩阵为

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{其他})
\end{cases}
$$

平稳分布为 \(\pi(x) = \deg(x) / 2|E|\)。

第 2 节汇总后文所需的定义与引理，第 3 节叙述并证明由谱隙给出的混合时间上界（定理 3.1），并在环图与完全图上用数值方法验证该估计的精度。
