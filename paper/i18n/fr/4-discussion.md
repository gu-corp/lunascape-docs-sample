---
navigation:
  order: 40
---

# 4. Discussion

La borne du théorème 3.1 est le temps de relaxation \(t_{\mathrm{rel}} = 1/\gamma\) multiplié par \(\log(1/\pi_{\min})\). Ce second facteur est le prix à payer lorsque l'on part du pire point de départ possible, et il disparaît dès que la marche commence près de la distribution stationnaire. Sur le graphe cyclique, ce facteur ne pèse en réalité pas, car \(\pi\) est uniforme quel que soit le point de départ, et l'écart entre la distance \(\ell^2\) et la distance en variation totale reste de l'ordre de \(\sqrt{n}\).

À l'inverse, combinée avec la borne inférieure \(t_{\mathrm{mix}}(\varepsilon) \ge (t_{\mathrm{rel}} - 1) \log \frac{1}{2\varepsilon}\) ([1, théorème 12.5]), cette borne situe le temps de mélange entre un multiple constant du temps de relaxation et \(\log(1/\pi_{\min})\) fois celui-ci. Combler cet intervalle demande une analyse plus fine, comme celle du phénomène de cutoff [2].

Pistes de travail futures : (i) l'extension aux chaînes non réversibles, (ii) l'évaluation de \(\pi_{\min}\) pour les graphes à arêtes pondérées, et (iii) la mesure sur des graphes issus de données réelles, par exemple des réseaux routiers.
