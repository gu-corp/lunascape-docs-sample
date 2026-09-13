---
navigation:
  order: 30
---

# 3. Risultati principali

## 3.1 Un limite superiore dalla lacuna spettrale

**Teorema 3.1.** Per la passeggiata aleatoria pigra su un grafo finito connesso,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Dimostrazione.* La pigrizia rende non negativi tutti gli autovalori, quindi \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Dal lemma 2.3 e da \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) segue

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Il membro destro è minore o uguale a \(\varepsilon\) non appena \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), e l'asserto segue da \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Il grafo ciclo e il grafo completo

Per la passeggiata pigra sul grafo ciclo \(C_n\) si ha \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), quindi \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Il teorema 3.1 dà allora \(t_{\mathrm{mix}} = O(n^2 \log n)\), mentre il valore vero è \(\Theta(n^2)\): il limite è lasco di un fattore \(\log n\).

Sul grafo completo \(K_n\) si ha \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), quindi \(\gamma \ge \frac12\). Il teorema 3.1 dà \(t_{\mathrm{mix}} = O(\log n)\), che coincide con il valore vero \(\Theta(\log n)\).

La tabella 1 e la figura 2 mostrano il limite superiore per \(\varepsilon = 1/4\) insieme al valore misurato, calcolato numericamente dalle potenze della matrice di transizione.

**Tabella 1.** Limite superiore del tempo di mescolamento \(t_{\mathrm{mix}}(1/4)\) (teorema 3.1) e valore misurato.

| Grafo | \(n\) | \(\gamma\) | Limite | Misurato |
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
  "description": "Limite superiore e valore misurato del tempo di mescolamento",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Limite", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Misurato", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Limite", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Misurato", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Limite", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Misurato", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Limite", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Misurato", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Limite", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Misurato", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Limite", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Misurato", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Numero di vertici n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (scala logaritmica)"},
    "color": {"field": "graph", "type": "nominal", "title": "Grafo"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figura 2.** Tempo di mescolamento in funzione del numero di vertici \(n\). Sul grafo ciclo il rapporto tra il limite e il valore misurato si allarga al crescere di \(n\); sul grafo completo resta entro un fattore costante.
