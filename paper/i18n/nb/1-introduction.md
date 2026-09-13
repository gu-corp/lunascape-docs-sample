---
navigation:
  order: 10
---

# 1. Innledning

En irredusibel og aperiodisk Markov-kjede på et endelig tilstandsrom konvergerer med tiden mot en entydig stasjonær fordeling \(\pi\). Hvor raskt den konvergerer, måles ved **miksetiden**. Skriver vi \(P\) for kjedens overgangsmatrise og \(P^t(x,\cdot)\) for fordelingen fra tilstanden \(x\) ved tiden \(t\), definerer vi

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Her er \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) totalvariasjonsavstanden.

Denne artikkelen behandler **den late tilfeldige vandringen** på en graf \(G = (V, E)\) (ved hvert tidssteg blir den stående med sannsynlighet \(1/2\), eller flytter seg til en uniformt valgt nabo med sannsynlighet \(1/2\)). Latheten sikrer aperiodisitet, og overgangsmatrisen blir

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{ellers})
\end{cases}
$$

Den stasjonære fordelingen er \(\pi(x) = \deg(x) / 2|E|\).

Avsnitt 2 samler de definisjonene og lemmaene som trengs senere; avsnitt 3 formulerer og beviser en øvre grense for miksetiden ut fra spektralgapet (teorem 3.1), og kontrollerer numerisk hvor skarpt anslaget er på sykelgrafen og den komplette grafen.
