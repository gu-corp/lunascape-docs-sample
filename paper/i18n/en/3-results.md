---
navigation:
  order: 30
---

# 3. Main results

## 3.1 An upper bound from the spectral gap

**Theorem 3.1.** For the lazy random walk on a finite connected graph,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Proof.* Laziness makes every eigenvalue non-negative, so \(\lambda_\ast = \lambda_2 = 1 - \gamma\). By Lemma 2.3 and \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

The right-hand side is at most \(\varepsilon\) once \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), and the claim follows from \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 The cycle graph and the complete graph

For the lazy walk on the cycle graph \(C_n\), \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), so \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Theorem 3.1 then gives \(t_{\mathrm{mix}} = O(n^2 \log n)\), against a true value of \(\Theta(n^2)\) — the bound is loose by a factor of \(\log n\).

On the complete graph \(K_n\), \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), so \(\gamma \ge \frac12\). Theorem 3.1 gives \(t_{\mathrm{mix}} = O(\log n)\), matching the true value \(\Theta(\log n)\).

Table 1 and Figure 2 show the bound at \(\varepsilon = 1/4\) alongside the measured value, computed numerically from powers of the transition matrix.

**Table 1.** The upper bound on the mixing time \(t_{\mathrm{mix}}(1/4)\) (Theorem 3.1) against the measured value.

| Graph | \(n\) | \(\gamma\) | Bound | Measured |
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
  "description": "Upper bound and measured mixing time",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Bound", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Measured", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Bound", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Measured", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Bound", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Measured", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Bound", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Measured", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Bound", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Measured", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Bound", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Measured", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Vertices n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4), log scale"},
    "color": {"field": "graph", "type": "nominal", "title": "Graph"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figure 2.** Mixing time against the number of vertices \(n\). On the cycle graph, the ratio between the bound and the measured value widens with \(n\); on the complete graph it stays within a constant factor.
