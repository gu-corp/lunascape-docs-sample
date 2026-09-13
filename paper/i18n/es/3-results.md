---
navigation:
  order: 30
---

# 3. Resultados principales

## 3.1 Una cota superior a partir de la brecha espectral

**Teorema 3.1.** Para el paseo aleatorio perezoso sobre un grafo finito y conexo,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Demostración.* La pereza hace que todos los valores propios sean no negativos, de modo que \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Por el lema 2.3 y \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Para que el lado derecho sea menor o igual que \(\varepsilon\) basta con \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), y la afirmación se sigue de \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 El grafo ciclo y el grafo completo

En el paseo perezoso sobre el grafo ciclo \(C_n\) se tiene \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), de modo que \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). El teorema 3.1 da \(t_{\mathrm{mix}} = O(n^2 \log n)\), pero el valor real es \(\Theta(n^2)\): la cota es holgada en un factor \(\log n\).

En el grafo completo \(K_n\), \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) y \(\gamma \ge \frac12\). El teorema 3.1 da \(t_{\mathrm{mix}} = O(\log n)\), que coincide con el valor real \(\Theta(\log n)\).

La tabla 1 y la figura 2 muestran la cota superior en \(\varepsilon = 1/4\) junto con el valor medido, calculado numéricamente a partir de las potencias de la matriz de transición.

**Tabla 1.** Cota superior del tiempo de mezcla \(t_{\mathrm{mix}}(1/4)\) (teorema 3.1) frente al valor medido.

| Grafo | \(n\) | \(\gamma\) | Cota | Medido |
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
  "description": "Cota superior y valor medido del tiempo de mezcla",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Cota", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Medido", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Cota", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Medido", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Cota", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Medido", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Cota", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Medido", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Cota", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Medido", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Cota", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Medido", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Número de vértices n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (escala logarítmica)"},
    "color": {"field": "graph", "type": "nominal", "title": "Grafo"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figura 2.** Tiempo de mezcla frente al número de vértices \(n\). En el grafo ciclo, la razón entre la cota y el valor medido se ensancha a medida que crece \(n\); en el grafo completo se mantiene dentro de un factor constante.
