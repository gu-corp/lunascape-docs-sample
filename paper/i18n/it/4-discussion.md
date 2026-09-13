---
navigation:
  order: 40
---

# 4. Discussione

Il limite superiore del teorema 3.1 ha la forma del tempo di rilassamento \(t_{\mathrm{rel}} = 1/\gamma\) moltiplicato per \(\log(1/\pi_{\min})\). Quest'ultimo fattore è il prezzo da pagare per partire dal punto di partenza peggiore e diventa superfluo se si parte da una distribuzione vicina a quella stazionaria. Nel grafo ciclico questo fattore non incide realmente, perché \(\pi\) è uniforme indipendentemente dal punto di partenza e lo scarto tra la distanza \(\ell^2\) e la distanza in variazione totale resta dell'ordine di \(\sqrt{n}\).

Al contrario, combinando con il limite inferiore \(t_{\mathrm{mix}}(\varepsilon) \ge (t_{\mathrm{rel}} - 1) \log \frac{1}{2\varepsilon}\) ([1, teorema 12.5]), si ricava che il tempo di mescolamento è compreso tra un multiplo costante del tempo di rilassamento e \(\log(1/\pi_{\min})\) volte tale tempo. Per colmare questo divario serve un'analisi più fine, come quella del fenomeno di cutoff [2].

Come sviluppi futuri si indicano: (i) l'estensione alle catene non reversibili, (ii) la stima di \(\pi_{\min}\) per grafi con archi pesati, (iii) la misurazione su grafi costruiti da dati reali (per esempio reti stradali).
