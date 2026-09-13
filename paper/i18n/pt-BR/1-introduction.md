---
navigation:
  order: 10
---

# 1. Introdução

Uma cadeia de Markov irredutível e aperiódica em um espaço de estados finito converge, com o tempo, para uma única distribuição estacionária \(\pi\). A rapidez dessa convergência é medida pelo **tempo de mistura**. Escrevendo \(P\) para a matriz de transição da cadeia e \(P^t(x,\cdot)\) para a distribuição a partir do estado \(x\) no instante \(t\), define-se

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

onde \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) é a distância de variação total.

Este artigo trata do **passeio aleatório preguiçoso** em um grafo \(G = (V, E)\) — a cada instante, permanece no lugar com probabilidade \(1/2\) ou move-se para um vértice vizinho escolhido uniformemente com probabilidade \(1/2\). A preguiça garante a aperiodicidade, e a matriz de transição é

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{caso contrário})
\end{cases}
$$

A distribuição estacionária é \(\pi(x) = \deg(x) / 2|E|\).

A Seção 2 reúne as definições e os lemas necessários adiante; a Seção 3 enuncia e demonstra um limitante superior para o tempo de mistura a partir do intervalo espectral (Teorema 3.1) e verifica numericamente a precisão da estimativa no grafo ciclo e no grafo completo.
