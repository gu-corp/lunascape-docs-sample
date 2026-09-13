---
navigation:
  order: 30
---

# 3. Belangrijkste resultaten

## 3.1 Een bovengrens uit de spectrale kloof

**Stelling 3.1.** Voor de luie stochastische wandeling op een eindige samenhangende graaf geldt

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bewijs.* Door de luiheid zijn alle eigenwaarden niet-negatief, dus \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Uit Lemma 2.3 en \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) volgt

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Voor \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\) is de rechterkant hoogstens \(\varepsilon\), en uit \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) volgt de bewering. \(\square\)

## 3.2 De cyclusgraaf en de volledige graaf

Bij de luie wandeling op de cyclusgraaf \(C_n\) is \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), dus \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Stelling 3.1 geeft \(t_{\mathrm{mix}} = O(n^2 \log n)\), terwijl de werkelijke waarde \(\Theta(n^2)\) is: de grens is een factor \(\log n\) te ruim.

Op de volledige graaf \(K_n\) is \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), dus \(\gamma \ge \frac12\). Stelling 3.1 geeft \(t_{\mathrm{mix}} = O(\log n)\), wat overeenkomt met de werkelijke waarde \(\Theta(\log n)\).

Tabel 1 en figuur 2 tonen de bovengrens bij \(\varepsilon = 1/4\) naast de gemeten waarde, numeriek berekend uit de machten van de overgangsmatrix.

**Tabel 1.** De bovengrens op de mengtijd \(t_{\mathrm{mix}}(1/4)\) (Stelling 3.1) naast de gemeten waarde.

| Graaf | \(n\) | \(\gamma\) | Bovengrens | Gemeten |
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
  "description": "Bovengrens en gemeten mengtijd",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Bovengrens", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Gemeten", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Bovengrens", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Gemeten", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Bovengrens", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Gemeten", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Bovengrens", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Gemeten", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Bovengrens", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Gemeten", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Bovengrens", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Gemeten", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Aantal knopen n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logschaal)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graaf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figuur 2.** Mengtijd ten opzichte van het aantal knopen \(n\). Bij de cyclusgraaf loopt de verhouding tussen bovengrens en meting op met \(n\); bij de volledige graaf blijft die binnen een constante factor.
