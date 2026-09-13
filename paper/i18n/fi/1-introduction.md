---
navigation:
  order: 10
---

# 1. Johdanto

Äärellisessä tila-avaruudessa määritelty redusoitumaton ja jaksoton Markovin ketju suppenee ajan myötä kohti yksikäsitteistä stationaarista jakaumaa \(\pi\). Suppenemisen nopeutta mitataan **sekoittumisajalla**. Kun ketjun siirtymämatriisia merkitään \(P\):llä ja tilasta \(x\) hetkellä \(t\) saatua jakaumaa \(P^t(x,\cdot)\):llä, määritellään

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Tässä \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) on kokonaisvaihteluetäisyys.

Tässä työssä tarkastellaan **laiskaa satunnaiskulkua** graafilla \(G = (V, E)\): kullakin hetkellä kulkija pysyy paikallaan todennäköisyydellä \(1/2\) ja siirtyy todennäköisyydellä \(1/2\) tasaisesti valittuun naapurisolmuun. Laiskuus takaa jaksottomuuden, ja siirtymämatriisi on

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{muutoin})
\end{cases}
$$

Stationaarinen jakauma on \(\pi(x) = \deg(x) / 2|E|\).

Luvussa 2 kootaan yhteen tarvittavat määritelmät ja lemmat, ja luvussa 3 esitetään ja todistetaan spektriaukkoon perustuva sekoittumisajan yläraja (lause 3.1) sekä tarkistetaan arvion tarkkuus numeerisesti syklisellä graafilla ja täydellisellä graafilla.
