---
navigation:
  order: 30
---

# 3. Glavni rezultati

## 3.1 Gornja ograda iz spektralnog procjepa

**Teorem 3.1.** Za lijenu slučajnu šetnju na konačnom povezanom grafu vrijedi

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Dokaz.* Zbog lijenosti su sve svojstvene vrijednosti nenegativne, pa je \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Iz leme 2.3 i \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) slijedi

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Desna strana je najviše \(\varepsilon\) čim je \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), a tvrdnja slijedi iz \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Ciklički graf i potpuni graf

Za lijenu šetnju na cikličkom grafu \(C_n\) je \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), pa je \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Teorem 3.1 tada daje \(t_{\mathrm{mix}} = O(n^2 \log n)\), dok je prava vrijednost \(\Theta(n^2)\) — ograda je labava za faktor \(\log n\).

Na potpunom grafu \(K_n\) je \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), pa je \(\gamma \ge \frac12\). Teorem 3.1 daje \(t_{\mathrm{mix}} = O(\log n)\), što se podudara s pravom vrijednošću \(\Theta(\log n)\).

Tablica 1 i slika 2 prikazuju gornju ogradu pri \(\varepsilon = 1/4\) uz izmjerenu vrijednost, izračunatu numerički iz potencija matrice prijelaza.

**Tablica 1.** Gornja ograda vremena miješanja \(t_{\mathrm{mix}}(1/4)\) (teorem 3.1) i izmjerena vrijednost.

| Graf | \(n\) | \(\gamma\) | Ograda | Izmjereno |
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
  "description": "Gornja ograda i izmjereno vrijeme miješanja",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Ograda", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Izmjereno", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Ograda", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Izmjereno", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Ograda", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Izmjereno", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Ograda", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Izmjereno", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Ograda", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Izmjereno", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Ograda", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Izmjereno", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Broj vrhova n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4), logaritamska skala"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Slika 2.** Vrijeme miješanja u ovisnosti o broju vrhova \(n\). Na cikličkom grafu omjer ograde i izmjerene vrijednosti raste s \(n\); na potpunom grafu ostaje unutar konstantnog faktora.
