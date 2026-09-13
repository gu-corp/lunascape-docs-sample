---
navigation:
  order: 30
---

# 3. Rezultate principale

## 3.1 O margine superioară dată de intervalul spectral

**Teorema 3.1.** Pentru mersul aleator leneș pe un graf finit conex,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Demonstrație.* Lenea face ca toate valorile proprii să fie nenegative, deci \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Din Lema 2.3 și din \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) rezultă

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Pentru ca membrul drept să fie cel mult \(\varepsilon\) este suficient ca \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), iar afirmația decurge din \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Graful ciclu și graful complet

Pentru mersul leneș pe graful ciclu \(C_n\) avem \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), deci \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Teorema 3.1 dă \(t_{\mathrm{mix}} = O(n^2 \log n)\), în timp ce valoarea adevărată este \(\Theta(n^2)\): marginea este slabă cu un factor \(\log n\).

Pe graful complet \(K_n\) avem \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), deci \(\gamma \ge \frac12\). Teorema 3.1 dă \(t_{\mathrm{mix}} = O(\log n)\), ceea ce coincide cu valoarea adevărată \(\Theta(\log n)\).

Tabelul 1 și Figura 2 prezintă marginea superioară la \(\varepsilon = 1/4\) alături de valoarea măsurată, calculată numeric din puterile matricei de tranziție.

**Tabelul 1.** Marginea superioară a timpului de amestecare \(t_{\mathrm{mix}}(1/4)\) (Teorema 3.1) față de valoarea măsurată.

| Graf | \(n\) | \(\gamma\) | Margine | Măsurat |
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
  "description": "Marginea superioară și valoarea măsurată a timpului de amestecare",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Margine", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Măsurat", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Margine", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Măsurat", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Margine", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Măsurat", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Margine", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Măsurat", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Margine", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Măsurat", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Margine", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Măsurat", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Numărul de vârfuri n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (scară logaritmică)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figura 2.** Timpul de amestecare în funcție de numărul de vârfuri \(n\). Pe graful ciclu, raportul dintre margine și valoarea măsurată crește odată cu \(n\); pe graful complet, el rămâne în limitele unui factor constant.
