---
navigation:
  order: 10
---

# 1. Einleitung

Eine irreduzible und aperiodische Markow-Kette auf einem endlichen Zustandsraum konvergiert mit der Zeit gegen eine eindeutige stationäre Verteilung \(\pi\). Wie schnell sie konvergiert, misst die **Mischzeit**. Bezeichnet man die Übergangsmatrix der Kette mit \(P\) und die Verteilung zum Zeitpunkt \(t\) ausgehend vom Zustand \(x\) mit \(P^t(x,\cdot)\), so setzt man

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Dabei ist \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) der Totalvariationsabstand.

In dieser Arbeit wird die **träge Irrfahrt** auf einem Graphen \(G = (V, E)\) behandelt (zu jedem Zeitpunkt bleibt sie mit Wahrscheinlichkeit \(1/2\) stehen und wechselt mit Wahrscheinlichkeit \(1/2\) gleichverteilt zu einem Nachbarknoten). Die Trägheit sichert die Aperiodizität, und die Übergangsmatrix lautet

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{sonst})
\end{cases}
$$

Die stationäre Verteilung ist \(\pi(x) = \deg(x) / 2|E|\).

Abschnitt 2 fasst die benötigten Definitionen und Lemmata zusammen; Abschnitt 3 formuliert und beweist eine obere Schranke für die Mischzeit anhand der Spektrallücke (Satz 3.1) und prüft die Genauigkeit der Abschätzung numerisch am Kreisgraphen und am vollständigen Graphen.
