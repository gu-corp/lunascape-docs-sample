---
navigation:
  order: 30
---

# 3. Huvudresultat

## 3.1 En övre gräns från spektralgapet

**Sats 3.1.** För den lata slumpvandringen på en ändlig sammanhängande graf gäller

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Bevis.* Latheten gör alla egenvärden icke-negativa, så \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Av lemma 2.3 och \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) följer

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Högerledet är högst \(\varepsilon\) så snart \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), och påståendet följer av \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Cykelgrafen och den fullständiga grafen

För den lata vandringen på cykelgrafen \(C_n\) är \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), så \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Sats 3.1 ger \(t_{\mathrm{mix}} = O(n^2 \log n)\), medan det sanna värdet är \(\Theta(n^2)\) — gränsen är alltså lös med en faktor \(\log n\).

På den fullständiga grafen \(K_n\) är \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) och \(\gamma \ge \frac12\). Sats 3.1 ger \(t_{\mathrm{mix}} = O(\log n\)), vilket stämmer med det sanna värdet \(\Theta(\log n)\).

Tabell 1 och figur 2 visar den övre gränsen vid \(\varepsilon = 1/4\) tillsammans med det uppmätta värdet, beräknat numeriskt ur potenser av övergångsmatrisen.

**Tabell 1.** Den övre gränsen för blandningstiden \(t_{\mathrm{mix}}(1/4)\) (sats 3.1) jämförd med det uppmätta värdet.

| Graf | \(n\) | \(\gamma\) | Övre gräns | Uppmätt |
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
  "description": "Övre gräns och uppmätt blandningstid",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Övre gräns", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Uppmätt", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Övre gräns", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Uppmätt", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Övre gräns", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Uppmätt", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Övre gräns", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Uppmätt", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Övre gräns", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Uppmätt", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Övre gräns", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Uppmätt", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Antal hörn n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logaritmisk)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figur 2.** Blandningstiden som funktion av antalet hörn \(n\). På cykelgrafen växer förhållandet mellan den övre gränsen och det uppmätta värdet med \(n\); på den fullständiga grafen håller det sig inom en konstant faktor.
