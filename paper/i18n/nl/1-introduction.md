---
navigation:
  order: 10
---

# 1. Inleiding

Een irreducibele, aperiodieke markovketen op een eindige toestandsruimte convergeert in de loop van de tijd naar een unieke stationaire verdeling \(\pi\). Hoe snel die convergeert, wordt gemeten door de **mengtijd**. Schrijven we \(P\) voor de overgangsmatrix van de keten en \(P^t(x,\cdot)\) voor de verdeling vanuit toestand \(x\) op tijdstip \(t\), dan definiëren we

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Hierin is \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) de totale-variatieafstand.

In dit artikel behandelen we de **luie aselecte wandeling** op een graaf \(G = (V, E)\): op elk tijdstip blijft de wandeling met kans \(1/2\) staan en gaat ze met kans \(1/2\) uniform naar een aangrenzend knooppunt. De luiheid garandeert aperiodiciteit, en de overgangsmatrix is

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{anders})
\end{cases}
$$

De stationaire verdeling is \(\pi(x) = \deg(x) / 2|E|\).

Paragraaf 2 verzamelt de definities en lemma's die verderop nodig zijn; paragraaf 3 formuleert en bewijst een bovengrens voor de mengtijd op basis van de spectrale kloof (stelling 3.1) en toetst de scherpte daarvan numeriek aan de cykelgraaf en de volledige graaf.
