---
navigation:
  order: 10
---

# 1. Indledning

En irreducibel, aperiodisk Markov-kæde på et endeligt tilstandsrum konvergerer med tiden mod en entydig stationær fordeling \(\pi\). Hvor hurtigt den konvergerer, måles ved **blandingstiden**. Skriver vi \(P\) for kædens overgangsmatrix og \(P^t(x,\cdot)\) for fordelingen fra tilstanden \(x\) til tiden \(t\), definerer vi

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

hvor \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) er totalvariationsafstanden.

I denne artikel behandles den **dovne tilfældige vandring** på en graf \(G = (V, E)\) (ved hvert tidsskridt bliver vandringen med sandsynlighed \(1/2\) stående og flytter med sandsynlighed \(1/2\) til en ensartet valgt nabo). Dovenskaben sikrer aperiodicitet, og overgangsmatricen bliver

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{ellers})
\end{cases}
$$

Den stationære fordeling er \(\pi(x) = \deg(x) / 2|E|\).

Afsnit 2 samler de definitioner og lemmaer, der er brug for senere; afsnit 3 formulerer og beviser en øvre grænse for blandingstiden ud fra spektralgabet (sætning 3.1) og efterprøver numerisk vurderingens skarphed på cykelgrafen og den fuldstændige graf.
