---
navigation:
  order: 30
---

# 3. 主要結果

## 3.1 由譜隙導出的上界

**定理 3.1.** 對於有限連通圖上的惰性隨機漫步，

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*證明.* 由於惰性使得所有特徵值皆為非負，故 \(\lambda_\ast = \lambda_2 = 1 - \gamma\)。由引理 2.3 與 \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) 可得

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

只要 \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\)，右邊即不超過 \(\varepsilon\)；再由 \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) 即得所述主張。 \(\square\)

## 3.2 環圖與完全圖

在環圖 \(C_n\) 上的惰性漫步中，\(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\)，因此 \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\)。定理 3.1 給出 \(t_{\mathrm{mix}} = O(n^2 \log n)\)，但真值為 \(\Theta(n^2)\)，該上界鬆了 \(\log n\) 這個倍數。

在完全圖 \(K_n\) 上，\(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\)，因此 \(\gamma \ge \frac12\)。定理 3.1 給出 \(t_{\mathrm{mix}} = O(\log n)\)，與真值 \(\Theta(\log n)\) 一致。

表 1 與圖 2 列出 \(\varepsilon = 1/4\) 時的上界，以及由轉移矩陣的冪次數值計算所得的實測值。

**表 1.** 混合時間 \(t_{\mathrm{mix}}(1/4)\) 的上界（定理 3.1）與實測值。

| 圖 | \(n\) | \(\gamma\) | 上界 | 實測 |
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
  "description": "混合時間的上界與實測值",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "上界", "t": 39}, {"graph": "C_n", "n": 10, "kind": "實測", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "上界", "t": 180}, {"graph": "C_n", "n": 20, "kind": "實測", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "上界", "t": 831}, {"graph": "C_n", "n": 40, "kind": "實測", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "上界", "t": 6}, {"graph": "K_n", "n": 10, "kind": "實測", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "上界", "t": 8}, {"graph": "K_n", "n": 20, "kind": "實測", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "上界", "t": 10}, {"graph": "K_n", "n": 40, "kind": "實測", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "頂點數 n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4)（對數）"},
    "color": {"field": "graph", "type": "nominal", "title": "圖"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**圖 2.** 混合時間對頂點數 \(n\) 的關係。在環圖上，上界與實測值的比值隨 \(n\) 增大而擴大；在完全圖上則維持在常數倍以內。
