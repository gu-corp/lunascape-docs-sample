---
navigation:
  order: 30
---

# 3. Résultats principaux

## 3.1 Une borne supérieure issue du trou spectral

**Théorème 3.1.** Pour la marche aléatoire paresseuse sur un graphe fini connexe,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Démonstration.* La paresse rend toutes les valeurs propres positives ou nulles, donc \(\lambda_\ast = \lambda_2 = 1 - \gamma\). D'après le lemme 2.3 et \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Le membre de droite est inférieur ou égal à \(\varepsilon\) dès que \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), et l'affirmation découle de \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Le graphe cyclique et le graphe complet

Pour la marche paresseuse sur le graphe cyclique \(C_n\), \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), donc \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Le théorème 3.1 donne alors \(t_{\mathrm{mix}} = O(n^2 \log n)\), alors que la valeur exacte est \(\Theta(n^2)\) : la borne est trop lâche d'un facteur \(\log n\).

Sur le graphe complet \(K_n\), \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), donc \(\gamma \ge \frac12\). Le théorème 3.1 donne \(t_{\mathrm{mix}} = O(\log n)\), ce qui coïncide avec la valeur exacte \(\Theta(\log n)\).

Le tableau 1 et la figure 2 présentent la borne supérieure pour \(\varepsilon = 1/4\) ainsi que la valeur mesurée, calculée numériquement à partir des puissances de la matrice de transition.

**Tableau 1.** Borne supérieure du temps de mélange \(t_{\mathrm{mix}}(1/4)\) (théorème 3.1) et valeur mesurée.

| Graphe | \(n\) | \(\gamma\) | Borne | Mesure |
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
  "description": "Borne supérieure et valeur mesurée du temps de mélange",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Borne", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Mesure", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Borne", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Mesure", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Borne", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Mesure", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Borne", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Mesure", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Borne", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Mesure", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Borne", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Mesure", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Nombre de sommets n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (échelle logarithmique)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graphe"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Figure 2.** Temps de mélange en fonction du nombre de sommets \(n\). Sur le graphe cyclique, l'écart entre la borne et la mesure se creuse à mesure que \(n\) augmente ; sur le graphe complet, il reste borné par un facteur constant.
