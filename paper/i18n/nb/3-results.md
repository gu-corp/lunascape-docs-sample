---
navigation:
  order: 30
---

# 3. Hovedresultater

## 3.1 En øvre grense fra spektralgapet

**Teorem 3.1.** For den late tilfeldige gangen på en endelig sammenhengende graf gjelder

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bevis.* Latheten gjør alle egenverdiene ikke-negative, så \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Av lemma 2.3 og \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) følger

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Høyresiden er høyst \(\varepsilon\) så snart \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), og påstanden følger av \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Syklusgrafen og den komplette grafen

For den late gangen på syklusgrafen \(C_n\) er \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), altså \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Teorem 3.1 gir da \(t_{\mathrm{mix}} = O(n^2 \log n)\), mens den sanne verdien er \(\Theta(n^2)\) — grensen er slakk med en faktor \(\log n\).

På den komplette grafen \(K_n\) er \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), altså \(\gamma \ge \frac12\). Teorem 3.1 gir \(t_{\mathrm{mix}} = O(\log n)\), som stemmer med den sanne verdien \(\Theta(\log n)\).

Tabell 1 og figur 2 viser den øvre grensen ved \(\varepsilon = 1/4\) sammen med den målte verdien, beregnet numerisk fra potenser av overgangsmatrisen.

**Tabell 1.** Den øvre grensen for blandingstiden \(t_{\mathrm{mix}}(1/4)\) (teorem 3.1) mot den målte verdien.

| Graf | \(n\) | \(\gamma\) | Grense | Målt |
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
  "description": "Øvre grense og målt blandingstid",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Grense", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Målt", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Grense", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Målt", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Grense", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Målt", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Grense", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Målt", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Grense", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Målt", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Grense", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Målt", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Antall noder n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logaritmisk)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figur 2.** Blandingstid mot antall noder \(n\). På syklusgrafen øker forholdet mellom grensen og den målte verdien med \(n\); på den komplette grafen holder det seg innenfor en konstant faktor.
