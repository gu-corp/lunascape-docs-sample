---
navigation:
  order: 40
---

# 4. Discussão

O limite superior do Teorema 3.1 tem a forma do tempo de relaxação \(t_{\mathrm{rel}} = 1/\gamma\) multiplicado por \(\log(1/\pi_{\min})\). Esse segundo fator é o preço de partir do pior ponto inicial possível e deixa de ser necessário quando se parte de uma distribuição próxima da distribuição estacionária. No grafo ciclo, esse fator não pesa de fato, porque \(\pi\) é uniforme independentemente do ponto de partida e a diferença entre a distância \(\ell^2\) e a distância de variação total permanece da ordem de \(\sqrt{n}\).

Em sentido contrário, combinando com o limite inferior \(t_{\mathrm{mix}}(\varepsilon) \ge (t_{\mathrm{rel}} - 1) \log \frac{1}{2\varepsilon}\) ([1, Teorema 12.5]), conclui-se que o tempo de mistura está entre um múltiplo constante do tempo de relaxação e \(\log(1/\pi_{\min})\) vezes esse tempo. Para fechar essa lacuna é preciso uma análise mais fina, como a do fenômeno de cutoff [2].

Como trabalhos futuros, apontam-se: (i) a extensão para cadeias não reversíveis, (ii) a estimativa de \(\pi_{\min}\) em grafos com arestas ponderadas e (iii) a medição em grafos de dados reais (por exemplo, redes rodoviárias).
