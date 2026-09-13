---
navigation:
  order: 10
---

# 1. Inledning

En irreducibel och aperiodisk Markovkedja på ett ändligt tillståndsrum konvergerar med tiden mot en entydig stationär fördelning \(\pi\). Hur snabbt den konvergerar mäts av **blandningstiden**. Om vi skriver \(P\) för kedjans övergångsmatris och \(P^t(x,\cdot)\) för fördelningen från tillståndet \(x\) vid tiden \(t\), definierar vi

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Här är \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) totalvariationsavståndet.

I den här uppsatsen behandlas **den lata slumpvandringen** på en graf \(G = (V, E)\) (vid varje tidssteg stannar den kvar med sannolikhet \(1/2\) och går med sannolikhet \(1/2\) till en likformigt vald grannnod). Lattheten garanterar aperiodicitet, och övergångsmatrisen blir

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{för övrigt})
\end{cases}
$$

Den stationära fördelningen är \(\pi(x) = \deg(x) / 2|E|\).

Avsnitt 2 samlar de definitioner och lemman som behövs; avsnitt 3 formulerar och bevisar en övre gräns för blandningstiden utifrån spektralgapet (sats 3.1) och kontrollerar numeriskt hur skarp uppskattningen är för cykelgrafen och den fullständiga grafen.
