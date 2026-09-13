---
navigation:
  order: 30
---

# 3. Resultados principais

## 3.1 Limite superior a partir do intervalo espectral

**Teorema 3.1.** Para o passeio aleatório preguiçoso em um grafo finito conexo,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Demonstração.* A preguiça torna os autovalores não negativos, portanto \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Pelo Lema 2.3 e por \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

O lado direito é no máximo \(\varepsilon\) desde que \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), e a afirmação decorre de \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 O grafo ciclo e o grafo completo

No passeio preguiçoso sobre o grafo ciclo \(C_n\), tem-se \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), portanto \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). O Teorema 3.1 fornece \(t_{\mathrm{mix}} = O(n^2 \log n)\), mas o valor verdadeiro é \(\Theta(n^2)\): o limite é frouxo por um fator de \(\log n\).

No grafo completo \(K_n\), \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) e \(\gamma \ge \frac12\). O Teorema 3.1 fornece \(t_{\mathrm{mix}} = O(\log n)\), coincidindo com o valor verdadeiro \(\Theta(\log n)\).

A Tabela 1 e a Figura 2 mostram o limite superior em \(\varepsilon = 1/4\) e o valor medido, calculado numericamente a partir das potências da matriz de transição.

**Tabela 1.** Limite superior do tempo de mistura \(t_{\mathrm{mix}}(1/4)\) (Teorema 3.1) e valor medido.

| Grafo | \(n\) | \(\gamma\) | Limite | Medido |
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
  "description": "Limite superior e valor medido do tempo de mistura",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Limite", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Medido", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Limite", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Medido", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Limite", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Medido", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Limite", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Medido", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Limite", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Medido", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Limite", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Medido", "t": 4}
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

**Figura 2.** Tempo de mistura em função do número de vértices \(n\). No grafo ciclo, a razão entre o limite e o valor medido aumenta com \(n\); no grafo completo, ela permanece dentro de um fator constante.
