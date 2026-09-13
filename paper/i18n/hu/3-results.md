---
navigation:
  order: 30
---

# 3. Fő eredmények

## 3.1. Felső korlát a spektrális résből

**3.1. tétel.** Véges összefüggő gráfon vett lusta véletlen sétára

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bizonyítás.* A lustaság miatt minden sajátérték nemnegatív, így \(\lambda_\ast = \lambda_2 = 1 - \gamma\). A 2.3. lemma és a \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) egyenlőtlenség alapján

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

A jobb oldal legfeljebb \(\varepsilon\), ha \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), az állítás pedig a \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) egyenlőtlenségből következik. \(\square\)

## 3.2. A körgráf és a teljes gráf

A \(C_n\) körgráfon vett lusta sétára \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), így \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). A 3.1. tétel ekkor \(t_{\mathrm{mix}} = O(n^2 \log n)\) értéket ad, szemben a valódi \(\Theta(n^2)\) értékkel – a korlát éppen \(\log n\) szorzóval laza.

A \(K_n\) teljes gráfon \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), tehát \(\gamma \ge \frac12\). A 3.1. tétel \(t_{\mathrm{mix}} = O(\log n)\) értéket ad, ami megegyezik a valódi \(\Theta(\log n)\) értékkel.

Az 1. táblázat és a 2. ábra az \(\varepsilon = 1/4\) melletti felső korlátot, valamint az átmenetmátrix hatványaiból numerikusan számított mért értéket mutatja.

**1. táblázat.** A \(t_{\mathrm{mix}}(1/4)\) keveredési idő felső korlátja (3.1. tétel) és mért értéke.

| Gráf | \(n\) | \(\gamma\) | Korlát | Mért |
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
  "description": "A keveredési idő felső korlátja és mért értéke",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Korlát", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Mért", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Korlát", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Mért", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Korlát", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Mért", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Korlát", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Mért", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Korlát", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Mért", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Korlát", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Mért", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Csúcsok száma n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logaritmikus)"},
    "color": {"field": "graph", "type": "nominal", "title": "Gráf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**2. ábra.** A keveredési idő az \(n\) csúcsszám függvényében. A körgráfon a korlát és a mért érték aránya \(n\) növekedésével egyre nagyobb, a teljes gráfon viszont konstans szorzón belül marad.
