---
navigation:
  order: 10
---

# 1. Bevezetés

Egy véges állapotteren értelmezett irreducibilis és aperiodikus Markov-lánc az idő múlásával egyetlen stacionárius eloszláshoz, \(\pi\)-hez konvergál. Azt, hogy milyen gyorsan konvergál, a **keveredési idő** méri. Jelölje \(P\) a lánc átmenetmátrixát, és \(P^t(x,\cdot)\) az \(x\) állapotból induló eloszlást a \(t\) időpontban; ekkor legyen

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Itt \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) a teljes variációs távolság.

Ez a dolgozat a \(G = (V, E)\) gráfon vett **lusta véletlen bolyongást** tárgyalja: minden lépésben \(1/2\) valószínűséggel helyben marad, és \(1/2\) valószínűséggel egyenletes eloszlás szerint választott szomszédos csúcsba lép. A lustaság biztosítja az aperiodikusságot, az átmenetmátrix pedig

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{egyébként})
\end{cases}
$$

A stacionárius eloszlás \(\pi(x) = \deg(x) / 2|E|\).

A 2. szakasz összefoglalja a szükséges definíciókat és lemmákat; a 3. szakasz kimondja és bizonyítja a keveredési idő spektrálréssel adott felső korlátját (3.1. tétel), majd a körgráfon és a teljes gráfon numerikusan ellenőrzi a becslés élességét.
