---
navigation:
  order: 10
---

# 1. Introduction

Une chaîne de Markov irréductible et apériodique sur un espace d'états fini converge au cours du temps vers une unique distribution stationnaire \(\pi\). La vitesse de cette convergence se mesure par le **temps de mélange**. En notant \(P\) la matrice de transition de la chaîne et \(P^t(x,\cdot)\) la distribution issue de l'état \(x\) à l'instant \(t\), on pose

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

où \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) est la distance en variation totale.

Cet article traite de la **marche aléatoire paresseuse** sur un graphe \(G = (V, E)\) : à chaque instant, on reste sur place avec probabilité \(1/2\), ou l'on se déplace vers un sommet voisin choisi uniformément avec probabilité \(1/2\). La paresse garantit l'apériodicité, et la matrice de transition s'écrit

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{sinon})
\end{cases}
$$

La distribution stationnaire est \(\pi(x) = \deg(x) / 2|E|\).

La section 2 rassemble les définitions et les lemmes nécessaires ; la section 3 énonce et démontre une borne supérieure du temps de mélange à partir du trou spectral (théorème 3.1), puis vérifie numériquement la précision de cette estimation sur le graphe cycle et le graphe complet.
