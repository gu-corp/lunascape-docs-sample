---
navigation:
  order: 10
---

# 1. Wprowadzenie

Nieprzywiedlny i nieokresowy łańcuch Markowa na skończonej przestrzeni stanów zbiega z czasem do jedynego rozkładu stacjonarnego \(\pi\). Szybkość tej zbieżności mierzy **czas mieszania**. Oznaczając przez \(P\) macierz przejścia łańcucha, a przez \(P^t(x,\cdot)\) rozkład wychodzący ze stanu \(x\) w chwili \(t\), definiujemy

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

gdzie \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) jest odległością w wahaniu całkowitym.

W niniejszej pracy rozważamy **leniwe błądzenie losowe** na grafie \(G = (V, E)\) — w każdej chwili z prawdopodobieństwem \(1/2\) pozostajemy w miejscu, a z prawdopodobieństwem \(1/2\) przechodzimy do jednostajnie wybranego sąsiedniego wierzchołka. Lenistwo zapewnia nieokresowość, a macierz przejścia ma postać

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{w pozostałych przypadkach})
\end{cases}
$$

Rozkładem stacjonarnym jest \(\pi(x) = \deg(x) / 2|E|\).

W rozdziale 2 zebrano potrzebne dalej definicje i lematy, a w rozdziale 3 sformułowano i udowodniono górne ograniczenie czasu mieszania wynikające z przerwy spektralnej (twierdzenie 3.1) oraz sprawdzono numerycznie dokładność tego oszacowania na grafie cyklicznym i grafie pełnym.
