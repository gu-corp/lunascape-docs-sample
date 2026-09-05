---
navigation:
  order: 30
---

# 3. 主結果

## 3.1 スペクトルギャップによる上界

**定理 3.1.** 有限連結グラフ上の遅延ランダムウォークについて、

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*証明.* 遅延により固有値は非負なので \(\lambda_\ast = \lambda_2 = 1 - \gamma\) である。補題 2.3 と \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) より

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

右辺が \(\varepsilon\) 以下となる \(t\) は \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\) で十分であり、\(\sqrt{\pi_{\min}} \ge \pi_{\min}\) から主張が従う。 \(\square\)

## 3.2 円グラフと完全グラフ

円グラフ \(C_n\) の遅延ウォークでは \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\) なので、\(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\) である。定理 3.1 は \(t_{\mathrm{mix}} = O(n^2 \log n)\) を与えるが、真の値は \(\Theta(n^2)\) であり、\(\log n\) の分だけ緩い。

完全グラフ \(K_n\) では \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) であり \(\gamma \ge \frac12\)。定理 3.1 は \(t_{\mathrm{mix}} = O(\log n)\) を与え、真の値 \(\Theta(\log n)\) と一致する。

表 1 と図 2 に、\(\varepsilon = 1/4\) における上界と、遷移行列の累乗から数値計算した実測値を示す。

**表 1.** 混合時間 \(t_{\mathrm{mix}}(1/4)\) の上界（定理 3.1）と実測値。

| グラフ | \(n\) | \(\gamma\) | 上界 | 実測 |
|---|---:|---:|---:|---:|
| \(C_n\) | 10 | 0.0955 | 39 | 13 |
| \(C_n\) | 20 | 0.0245 | 180 | 49 |
| \(C_n\) | 40 | 0.0062 | 831 | 195 |
| \(K_n\) | 10 | 0.5556 | 6 | 3 |
| \(K_n\) | 20 | 0.5263 | 8 | 4 |
| \(K_n\) | 40 | 0.5128 | 10 | 4 |

```vega-lite
{
  "$schema": "https://vega.github.io/schema/vega-lite/v5.json",
  "description": "混合時間の上界と実測値",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "上界", "t": 39}, {"graph": "C_n", "n": 10, "kind": "実測", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "上界", "t": 180}, {"graph": "C_n", "n": 20, "kind": "実測", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "上界", "t": 831}, {"graph": "C_n", "n": 40, "kind": "実測", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "上界", "t": 6}, {"graph": "K_n", "n": 10, "kind": "実測", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "上界", "t": 8}, {"graph": "K_n", "n": 20, "kind": "実測", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "上界", "t": 10}, {"graph": "K_n", "n": 40, "kind": "実測", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "頂点数 n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4)（対数）"},
    "color": {"field": "graph", "type": "nominal", "title": "グラフ"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**図 2.** 頂点数 \(n\) に対する混合時間。円グラフでは上界と実測の比が \(n\) とともに広がり、完全グラフでは定数倍に留まる。
