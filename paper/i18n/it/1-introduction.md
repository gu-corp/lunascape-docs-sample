---
navigation:
  order: 10
---

# 1. Introduzione

Una catena di Markov irriducibile e aperiodica su uno spazio degli stati finito converge nel tempo a un'unica distribuzione stazionaria \(\pi\). La velocità di questa convergenza si misura con il **tempo di mescolamento**. Indicando con \(P\) la matrice di transizione della catena e con \(P^t(x,\cdot)\) la distribuzione al tempo \(t\) a partire dallo stato \(x\), si pone

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

dove \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) è la distanza in variazione totale.

In questo lavoro si considera la **passeggiata aleatoria pigra** su un grafo \(G = (V, E)\): a ogni passo si resta fermi con probabilità \(1/2\) oppure ci si sposta con probabilità \(1/2\) verso un vertice adiacente scelto uniformemente. La pigrizia garantisce l'aperiodicità e la matrice di transizione risulta

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{altrimenti})
\end{cases}
$$

La distribuzione stazionaria è \(\pi(x) = \deg(x) / 2|E|\).

Nella sezione 2 si raccolgono le definizioni e i lemmi necessari; nella sezione 3 si enuncia e si dimostra un limite superiore per il tempo di mescolamento ottenuto dal gap spettrale (teorema 3.1) e se ne verifica numericamente la precisione sul grafo ciclo e sul grafo completo.
