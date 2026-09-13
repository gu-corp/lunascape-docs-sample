---
navigation:
  order: 10
---

# 1. Introducere

Un lanț Markov ireductibil și aperiodic pe un spațiu de stări finit converge în timp către o unică distribuție staționară \(\pi\). Viteza cu care are loc această convergență se măsoară prin **timpul de amestecare**. Notând cu \(P\) matricea de tranziție a lanțului și cu \(P^t(x,\cdot)\) distribuția pornită din starea \(x\) la momentul \(t\), definim

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

unde \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) este distanța în variație totală.

În această lucrare se studiază **mersul aleator leneș** pe un graf \(G = (V, E)\): la fiecare moment de timp, se rămâne pe loc cu probabilitatea \(1/2\) sau se trece cu probabilitatea \(1/2\) la un vârf vecin ales uniform. Lenea garantează aperiodicitatea, iar matricea de tranziție este

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{în rest})
\end{cases}
$$

Distribuția staționară este \(\pi(x) = \deg(x) / 2|E|\).

Secțiunea 2 adună definițiile și lemele necesare mai departe; secțiunea 3 enunță și demonstrează o margine superioară a timpului de amestecare obținută din intervalul spectral (teorema 3.1) și verifică numeric precizia estimării pe graful ciclu și pe graful complet.
