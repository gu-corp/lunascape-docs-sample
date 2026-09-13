---
navigation:
  order: 30
---

# 3. Hasil utama

## 3.1 Batas atas daripada jurang spektrum

**Teorem 3.1.** Bagi jalan rawak malas pada graf terhingga yang berhubung,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bukti.* Sifat malas menjadikan setiap nilai eigen tak negatif, jadi \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Menurut Lema 2.3 dan \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Ruas kanan tidak melebihi \(\varepsilon\) apabila \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), dan dakwaan itu menyusul daripada \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Graf kitaran dan graf lengkap

Bagi jalan rawak malas pada graf kitaran \(C_n\), \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), maka \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Teorem 3.1 memberikan \(t_{\mathrm{mix}} = O(n^2 \log n)\), sedangkan nilai sebenarnya ialah \(\Theta(n^2)\) — batas itu longgar sebanyak faktor \(\log n\).

Pada graf lengkap \(K_n\), \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), maka \(\gamma \ge \frac12\). Teorem 3.1 memberikan \(t_{\mathrm{mix}} = O(\log n)\), sepadan dengan nilai sebenar \(\Theta(\log n)\).

Jadual 1 dan Rajah 2 menunjukkan batas atas pada \(\varepsilon = 1/4\) berserta nilai ukur yang dikira secara berangka daripada kuasa matriks peralihan.

**Jadual 1.** Batas atas bagi masa pencampuran \(t_{\mathrm{mix}}(1/4)\) (Teorem 3.1) berbanding nilai ukur.

| Graf | \(n\) | \(\gamma\) | Batas atas | Nilai ukur |
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
  "description": "Batas atas dan nilai ukur masa pencampuran",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Batas atas", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Nilai ukur", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Batas atas", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Nilai ukur", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Batas atas", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Nilai ukur", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Batas atas", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Nilai ukur", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Batas atas", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Nilai ukur", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Batas atas", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Nilai ukur", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Bilangan bucu n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (skala logaritma)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Rajah 2.** Masa pencampuran berbanding bilangan bucu \(n\). Pada graf kitaran, nisbah antara batas atas dan nilai ukur melebar bersama \(n\); pada graf lengkap ia kekal dalam lingkungan faktor malar.
