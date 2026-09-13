---
navigation:
  order: 10
---

# 1. 緒論

有限狀態空間上不可約且非週期的馬可夫鏈，會隨時間收斂到唯一的平穩分布 \(\pi\)。衡量收斂速度的量就是**混合時間**。將此鏈的轉移矩陣記為 \(P\)，時刻 \(t\) 時從狀態 \(x\) 出發的分布記為 \(P^t(x,\cdot)\)，則定義

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

其中 \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) 為全變差距離。

本文處理圖 \(G = (V, E)\) 上的**懶惰隨機漫步**（每一時刻以機率 \(1/2\) 停留原處，以機率 \(1/2\) 均勻地移動到相鄰頂點）。懶惰性保證了非週期性，而轉移矩陣為

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{其他})
\end{cases}
$$

平穩分布為 \(\pi(x) = \deg(x) / 2|E|\)。

第 2 節整理後續所需的定義與引理，第 3 節敘述並證明由譜隙導出的混合時間上界（定理 3.1），並以環圖與完全圖數值驗證該估計的精確度。
