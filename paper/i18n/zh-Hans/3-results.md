---
navigation:
  order: 30
---

# 3. 主要结果

## 3.1 由谱隙给出的上界

**定理 3.1.** 对于有限连通图上的懒惰随机游走，

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*证明.* 由于懒惰性使得所有特征值非负，故 \(\lambda_\ast = \lambda_2 = 1 - \gamma\)。由引理 2.3 及 \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) 可得

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

要使右端不超过 \(\varepsilon\)，只需 \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\)，再由 \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) 即得所述结论。 \(\square\)

## 3.2 圈图与完全图

对圈图 \(C_n\) 上的懒惰游走，\(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\)，因此 \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\)。定理 3.1 给出 \(t_{\mathrm{mix}} = O(n^2 \log n)\)，而真实值为 \(\Theta(n^2)\)，即该界松了 \(\log n\) 这一因子。

对完全图 \(K_n\)，\(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\)，故 \(\gamma \ge \frac12\)。定理 3.1 给出 \(t_{\mathrm{mix}} = O(\log n)\)，与真实值 \(\Theta(\log n)\) 一致。

表 1 与图 2 给出了 \(\varepsilon = 1/4\) 时的上界，以及由转移矩阵的幂数值计算得到的实测值。

**表 1.** 混合时间 \(t_{\mathrm{mix}}(1/4)\) 的上界（定理 3.1）与实测值。

| 图 | \(n\) | \(\gamma\) | 上界 | 实测 |
|---|---:|---:|---:|---:|
| \(C_n\) | 10 | 0.0955 | 39 | 13 |
| \(C_n\) | 20 | 0.0245 | 180 | 49 |
| \(C_n\) | 40 | 0.0062 | 831 | 195 |
| \(K_n\) | 10 | 0.5556 | 6 | 3 |
| \(K_n\) | 20 | 0.5263 | 8 | 4 |
| \(K_n\) | 40 | 0.5128 | 10 | 4 |

```vega-lite
{
  "$schema": "https://vega.github.io/schema/vega-lite/v6.json",
  "description": "混合时间的上界与实测值",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "上界", "t": 39}, {"graph": "C_n", "n": 10, "kind": "实测", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "上界", "t": 180}, {"graph": "C_n", "n": 20, "kind": "实测", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "上界", "t": 831}, {"graph": "C_n", "n": 40, "kind": "实测", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "上界", "t": 6}, {"graph": "K_n", "n": 10, "kind": "实测", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "上界", "t": 8}, {"graph": "K_n", "n": 20, "kind": "实测", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "上界", "t": 10}, {"graph": "K_n", "n": 40, "kind": "实测", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "顶点数 n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4)（对数）"},
    "color": {"field": "graph", "type": "nominal", "title": "图"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**图 2.** 混合时间随顶点数 \(n\) 的变化。在圈图上，上界与实测值之比随 \(n\) 增大而扩大；在完全图上则保持在常数倍之内。
