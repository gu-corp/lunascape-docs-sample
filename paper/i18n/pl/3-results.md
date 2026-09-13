---
navigation:
  order: 30
---

# 3. Główne wyniki

## 3.1 Ograniczenie górne wynikające z przerwy spektralnej

**Twierdzenie 3.1.** Dla leniwego błądzenia losowego na skończonym grafie spójnym zachodzi

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Dowód.* Leniwość sprawia, że wszystkie wartości własne są nieujemne, zatem \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Z lematu 2.3 oraz z nierówności \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) otrzymujemy

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Prawa strona jest nie większa niż \(\varepsilon\), gdy \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), a teza wynika z nierówności \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Graf cykliczny i graf pełny

Dla leniwego błądzenia na grafie cyklicznym \(C_n\) mamy \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), zatem \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Twierdzenie 3.1 daje \(t_{\mathrm{mix}} = O(n^2 \log n)\), podczas gdy wartość rzeczywista wynosi \(\Theta(n^2)\) — ograniczenie jest zbyt słabe o czynnik \(\log n\).

Na grafie pełnym \(K_n\) mamy \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), a więc \(\gamma \ge \frac12\). Twierdzenie 3.1 daje \(t_{\mathrm{mix}} = O(\log n)\), co pokrywa się z wartością rzeczywistą \(\Theta(\log n)\).

Tabela 1 i rysunek 2 przedstawiają ograniczenie górne dla \(\varepsilon = 1/4\) oraz wartość zmierzoną, obliczoną numerycznie z potęg macierzy przejścia.

**Tabela 1.** Ograniczenie górne czasu mieszania \(t_{\mathrm{mix}}(1/4)\) (twierdzenie 3.1) w zestawieniu z wartością zmierzoną.

| Graf | \(n\) | \(\gamma\) | Ograniczenie | Pomiar |
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
  "description": "Ograniczenie górne i zmierzony czas mieszania",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Ograniczenie", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Pomiar", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Ograniczenie", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Pomiar", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Ograniczenie", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Pomiar", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Ograniczenie", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Pomiar", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Ograniczenie", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Pomiar", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Ograniczenie", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Pomiar", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Liczba wierzchołków n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4), skala logarytmiczna"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Rysunek 2.** Czas mieszania w zależności od liczby wierzchołków \(n\). Na grafie cyklicznym stosunek ograniczenia do wartości zmierzonej rośnie wraz z \(n\); na grafie pełnym pozostaje w granicach stałego czynnika.
