---
navigation:
  order: 30
---

# 3. Hasil utama

## 3.1 Batas atas dari celah spektral

**Teorema 3.1.** Untuk jalan acak malas pada graf terhubung berhingga,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bukti.* Karena kemalasan membuat setiap nilai eigen tak negatif, maka \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Dari Lema 2.3 dan \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Agar ruas kanan tidak melebihi \(\varepsilon\), cukup diambil \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), dan pernyataan tersebut mengikuti dari \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Graf siklus dan graf lengkap

Pada jalan malas di graf siklus \(C_n\) berlaku \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), sehingga \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Teorema 3.1 memberikan \(t_{\mathrm{mix}} = O(n^2 \log n)\), sedangkan nilai sebenarnya adalah \(\Theta(n^2)\); batas itu longgar sebesar faktor \(\log n\).

Pada graf lengkap \(K_n\) berlaku \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), sehingga \(\gamma \ge \frac12\). Teorema 3.1 memberikan \(t_{\mathrm{mix}} = O(\log n)\), yang sesuai dengan nilai sebenarnya \(\Theta(\log n)\).

Tabel 1 dan Gambar 2 menunjukkan batas atas pada \(\varepsilon = 1/4\) beserta nilai terukur yang dihitung secara numerik dari perpangkatan matriks transisi.

**Tabel 1.** Batas atas waktu pencampuran \(t_{\mathrm{mix}}(1/4)\) (Teorema 3.1) dibandingkan dengan nilai terukur.

| Graf | \(n\) | \(\gamma\) | Batas atas | Terukur |
|---|---:|---:|---:|---:|
| \(C_n\) | 10 | 0,0955 | 39 | 13 |
| \(C_n\) | 20 | 0,0245 | 180 | 49 |
| \(C_n\) | 40 | 0,0062 | 831 | 195 |
| \(K_n\) | 10 | 0,5556 | 6 | 3 |
| \(K_n\) | 20 | 0,5263 | 8 | 4 |
| \(K_n\) | 40 | 0,5128 | 10 | 4 |

```vega-lite
{
  "$schema": "https://vega.github.io/schema/vega-lite/v6.json",
  "description": "Batas atas dan nilai terukur waktu pencampuran",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Batas atas", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Terukur", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Batas atas", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Terukur", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Batas atas", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Terukur", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Batas atas", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Terukur", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Batas atas", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Terukur", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Batas atas", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Terukur", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Jumlah simpul n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (skala logaritmik)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Gambar 2.** Waktu pencampuran terhadap jumlah simpul \(n\). Pada graf siklus, rasio antara batas atas dan nilai terukur melebar seiring bertambahnya \(n\); pada graf lengkap, rasio itu tetap dalam kelipatan konstanta.
