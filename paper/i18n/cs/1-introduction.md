---
navigation:
  order: 10
---

# 1. Úvod

Ireducibilní a aperiodický Markovův řetězec na konečném stavovém prostoru konverguje v čase k jedinému stacionárnímu rozdělení \(\pi\). To, jak rychle konverguje, měří **čas promíchání**. Označíme-li \(P\) přechodovou matici řetězce a \(P^t(x,\cdot)\) rozdělení v čase \(t\) vycházející ze stavu \(x\), definujeme

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

kde \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) je vzdálenost v totální variaci.

Tato práce se zabývá **líným náhodným procházením** na grafu \(G = (V, E)\) (v každém kroku zůstane s pravděpodobností \(1/2\) na místě a s pravděpodobností \(1/2\) přejde do rovnoměrně zvoleného sousedního vrcholu). Lenost zaručuje aperiodicitu a přechodová matice má tvar

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{jinak})
\end{cases}
$$

Stacionární rozdělení je \(\pi(x) = \deg(x) / 2|E|\).

Oddíl 2 shrnuje potřebné definice a lemmata, oddíl 3 uvádí a dokazuje horní odhad času promíchání pomocí spektrální mezery (věta 3.1) a numericky ověřuje přesnost tohoto odhadu na kružnicovém grafu a na úplném grafu.
