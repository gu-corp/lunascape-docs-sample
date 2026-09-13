---
navigation:
  order: 30
---

# 3. Päätulokset

## 3.1 Spektriraon antama yläraja

**Lause 3.1.** Äärellisen yhtenäisen graafin laiskalle satunnaiskululle pätee

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Todistus.* Laiskuuden vuoksi ominaisarvot ovat epänegatiivisia, joten \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Lemman 2.3 ja epäyhtälön \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) nojalla

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Oikea puoli on korkeintaan \(\varepsilon\), kun \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), ja väite seuraa epäyhtälöstä \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Syklinen graafi ja täydellinen graafi

Syklisen graafin \(C_n\) laiskalle kululle \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), joten \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Lause 3.1 antaa tuloksen \(t_{\mathrm{mix}} = O(n^2 \log n)\), mutta todellinen arvo on \(\Theta(n^2)\), eli raja on löysä tekijän \(\log n\) verran.

Täydellisessä graafissa \(K_n\) on \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), joten \(\gamma \ge \frac12\). Lause 3.1 antaa tuloksen \(t_{\mathrm{mix}} = O(\log n)\), joka vastaa todellista arvoa \(\Theta(\log n)\).

Taulukossa 1 ja kuvassa 2 esitetään yläraja arvolla \(\varepsilon = 1/4\) sekä siirtymämatriisin potensseista numeerisesti laskettu mitattu arvo.

**Taulukko 1.** Sekoittumisajan \(t_{\mathrm{mix}}(1/4)\) yläraja (lause 3.1) ja mitattu arvo.

| Graafi | \(n\) | \(\gamma\) | Yläraja | Mitattu |
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
  "description": "Sekoittumisajan yläraja ja mitattu arvo",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Yläraja", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Mitattu", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Yläraja", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Mitattu", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Yläraja", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Mitattu", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Yläraja", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Mitattu", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Yläraja", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Mitattu", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Yläraja", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Mitattu", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Kärkien lukumäärä n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logaritminen)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graafi"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Kuva 2.** Sekoittumisaika kärkien lukumäärän \(n\) suhteen. Syklisessä graafissa ylärajan ja mitatun arvon suhde kasvaa \(n\):n myötä, kun taas täydellisessä graafissa se pysyy vakiokertoimen sisällä.
