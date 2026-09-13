---
navigation:
  order: 30
---

# 3. Hovedresultater

## 3.1 Øvre grænse ud fra spektralgabet

**Sætning 3.1.** For den dovne tilfældige vandring på en endelig sammenhængende graf gælder

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bevis.* Dovenheden gør alle egenværdier ikke-negative, så \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Af lemma 2.3 og \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) følger

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Højresiden er højst \(\varepsilon\), når \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), og påstanden følger af \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Cykelgrafen og den komplette graf

For den dovne vandring på cykelgrafen \(C_n\) er \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), altså \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Sætning 3.1 giver \(t_{\mathrm{mix}} = O(n^2 \log n)\), men den sande værdi er \(\Theta(n^2)\) — grænsen er løs med en faktor \(\log n\).

På den komplette graf \(K_n\) er \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), altså \(\gamma \ge \frac12\). Sætning 3.1 giver \(t_{\mathrm{mix}} = O(\log n)\), hvilket stemmer med den sande værdi \(\Theta(\log n)\).

Tabel 1 og figur 2 viser den øvre grænse ved \(\varepsilon = 1/4\) sammen med den målte værdi, der er beregnet numerisk ud fra potenser af overgangsmatricen.

**Tabel 1.** Øvre grænse for blandingstiden \(t_{\mathrm{mix}}(1/4)\) (sætning 3.1) og den målte værdi.

| Graf | \(n\) | \(\gamma\) | Grænse | Målt |
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
  "description": "Øvre grænse og målt blandingstid",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Grænse", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Målt", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Grænse", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Målt", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Grænse", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Målt", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Grænse", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Målt", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Grænse", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Målt", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Grænse", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Målt", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Antal knuder n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logaritmisk)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figur 2.** Blandingstiden som funktion af antallet af knuder \(n\). På cykelgrafen vokser forholdet mellem grænsen og den målte værdi med \(n\), mens det på den komplette graf holder sig inden for en konstant faktor.
