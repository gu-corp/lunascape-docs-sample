---
navigation:
  order: 30
---

# 3. Hlavní výsledky

## 3.1 Horní mez daná spektrální mezerou

**Věta 3.1.** Pro líné náhodné procházky na konečném souvislém grafu platí

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Důkaz.* Vlivem lenosti jsou všechna vlastní čísla nezáporná, takže \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Z lemmatu 2.3 a z nerovnosti \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) plyne

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Pravá strana je nejvýše \(\varepsilon\), jakmile \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), a tvrzení plyne z \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Kružnicový graf a úplný graf

Pro línou procházku na kružnicovém grafu \(C_n\) je \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), takže \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Věta 3.1 pak dává \(t_{\mathrm{mix}} = O(n^2 \log n)\), zatímco skutečná hodnota je \(\Theta(n^2)\) — mez je volnější o činitel \(\log n\).

Na úplném grafu \(K_n\) je \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), a tedy \(\gamma \ge \frac12\). Věta 3.1 dává \(t_{\mathrm{mix}} = O(\log n)\), což odpovídá skutečné hodnotě \(\Theta(\log n)\).

Tabulka 1 a obrázek 2 uvádějí horní mez při \(\varepsilon = 1/4\) spolu s naměřenou hodnotou, vypočtenou numericky z mocnin přechodové matice.

**Tabulka 1.** Horní mez doby míchání \(t_{\mathrm{mix}}(1/4)\) (věta 3.1) proti naměřené hodnotě.

| Graf | \(n\) | \(\gamma\) | Mez | Naměřeno |
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
  "description": "Horní mez a naměřená doba míchání",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Mez", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Naměřeno", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Mez", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Naměřeno", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Mez", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Naměřeno", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Mez", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Naměřeno", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Mez", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Naměřeno", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Mez", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Naměřeno", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Počet vrcholů n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4), logaritmická škála"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Obrázek 2.** Doba míchání v závislosti na počtu vrcholů \(n\). U kružnicového grafu se poměr mezi mezí a naměřenou hodnotou s rostoucím \(n\) rozevírá; u úplného grafu zůstává v mezích konstantního násobku.
