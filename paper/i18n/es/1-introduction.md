---
navigation:
  order: 10
---

# 1. Introducción

Una cadena de Markov irreducible y aperiódica sobre un espacio de estados finito converge con el tiempo a una única distribución estacionaria \(\pi\). La rapidez de esa convergencia se mide mediante el **tiempo de mezcla**. Si escribimos \(P\) para la matriz de transición de la cadena y \(P^t(x,\cdot)\) para la distribución a partir del estado \(x\) en el instante \(t\), definimos

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

donde \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) es la distancia de variación total.

En este artículo se estudia el **paseo aleatorio perezoso** sobre un grafo \(G = (V, E)\): en cada instante, permanece en el mismo vértice con probabilidad \(1/2\) o se desplaza con probabilidad \(1/2\) a un vértice vecino elegido de manera uniforme. La pereza garantiza la aperiodicidad, y la matriz de transición es

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{en los demás casos})
\end{cases}
$$

La distribución estacionaria es \(\pi(x) = \deg(x) / 2|E|\).

En la sección 2 se reúnen las definiciones y los lemas necesarios; en la sección 3 se enuncia y se demuestra una cota superior del tiempo de mezcla a partir del hueco espectral (teorema 3.1) y se comprueba numéricamente la precisión de la estimación en el grafo ciclo y en el grafo completo.
