---
navigation:
  order: 10
---

# 1. Uvod

Ireducibilan i aperiodičan Markovljev lanac na konačnom prostoru stanja s vremenom konvergira jedinstvenoj stacionarnoj distribuciji \(\pi\). Brzinu te konvergencije mjeri **vrijeme miješanja**. Ako s \(P\) označimo matricu prijelaza lanca, a s \(P^t(x,\cdot)\) distribuciju iz stanja \(x\) u trenutku \(t\), definiramo

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

pri čemu je \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) udaljenost u totalnoj varijaciji.

U ovom se radu razmatra **lijeni slučajni hod** na grafu \(G = (V, E)\) (u svakom trenutku s vjerojatnošću \(1/2\) ostaje na mjestu, a s vjerojatnošću \(1/2\) prelazi na jednoliko odabran susjedni vrh). Lijenost jamči aperiodičnost, a matrica prijelaza glasi

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{inače})
\end{cases}
$$

Stacionarna distribucija je \(\pi(x) = \deg(x) / 2|E|\).

U 2. poglavlju sabrane su potrebne definicije i leme, a u 3. poglavlju iskazana je i dokazana gornja ograda vremena miješanja preko spektralnog procjepa (Teorem 3.1) te je točnost procjene numerički provjerena na cikličkom i potpunom grafu.
