---
navigation:
  order: 40
---

# 4. Discusión

La cota del teorema 3.1 tiene la forma del tiempo de relajación \(t_{\mathrm{rel}} = 1/\gamma\) multiplicado por \(\log(1/\pi_{\min})\). Este segundo factor es el precio de partir del peor punto posible y desaparece cuando se parte de una distribución cercana a la distribución estacionaria. En el grafo ciclo este factor no influye en la práctica, porque \(\pi\) es uniforme con independencia del punto de partida y la diferencia entre la distancia \(\ell^2\) y la distancia de variación total se mantiene del orden de \(\sqrt{n}\).

En sentido contrario, al combinarla con la cota inferior \(t_{\mathrm{mix}}(\varepsilon) \ge (t_{\mathrm{rel}} - 1) \log \frac{1}{2\varepsilon}\) ([1, teorema 12.5]), se obtiene que el tiempo de mezcla se sitúa entre un múltiplo constante del tiempo de relajación y \(\log(1/\pi_{\min})\) veces este. Cerrar esa distancia exige un análisis más fino, como el del fenómeno de corte (cutoff) [2].

Como trabajo futuro se señalan: (i) la extensión a cadenas no reversibles, (ii) la estimación de \(\pi_{\min}\) en grafos con aristas ponderadas y (iii) la medición sobre grafos de datos reales, por ejemplo redes de carreteras.
