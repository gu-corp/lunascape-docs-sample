---
navigation:
  order: 30
---

# 3. Hauptergebnisse

## 3.1 Eine obere Schranke aus der Spektrallücke

**Satz 3.1.** Für die verzögerte Irrfahrt auf einem endlichen zusammenhängenden Graphen gilt

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Beweis.* Durch die Verzögerung sind alle Eigenwerte nichtnegativ, also ist \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Aus Lemma 2.3 und \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) folgt

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Damit die rechte Seite höchstens \(\varepsilon\) beträgt, genügt \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), und aus \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) folgt die Behauptung. \(\square\)

## 3.2 Kreisgraph und vollständiger Graph

Für die verzögerte Irrfahrt auf dem Kreisgraphen \(C_n\) ist \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), also \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Satz 3.1 liefert \(t_{\mathrm{mix}} = O(n^2 \log n)\), der wahre Wert ist jedoch \(\Theta(n^2)\); die Schranke ist um den Faktor \(\log n\) zu grob.

Auf dem vollständigen Graphen \(K_n\) ist \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) und damit \(\gamma \ge \frac12\). Satz 3.1 liefert \(t_{\mathrm{mix}} = O(\log n)\) und stimmt mit dem wahren Wert \(\Theta(\log n)\) überein.

Tabelle 1 und Abbildung 2 zeigen die obere Schranke für \(\varepsilon = 1/4\) zusammen mit den aus Potenzen der Übergangsmatrix numerisch berechneten Messwerten.

**Tabelle 1.** Obere Schranke der Mischzeit \(t_{\mathrm{mix}}(1/4)\) (Satz 3.1) und Messwert.

| Graph | \(n\) | \(\gamma\) | Schranke | Messwert |
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
  "description": "Obere Schranke und gemessene Mischzeit",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Schranke", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Messwert", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Schranke", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Messwert", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Schranke", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Messwert", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Schranke", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Messwert", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Schranke", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Messwert", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Schranke", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Messwert", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Knotenzahl n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logarithmisch)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graph"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Abbildung 2.** Mischzeit in Abhängigkeit von der Knotenzahl \(n\). Beim Kreisgraphen wächst das Verhältnis von Schranke zu Messwert mit \(n\), beim vollständigen Graphen bleibt es bei einem konstanten Faktor.
