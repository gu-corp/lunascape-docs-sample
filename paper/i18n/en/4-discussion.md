---
navigation:
  order: 40
---

# 4. Discussion

The bound in Theorem 3.1 is the relaxation time \(t_{\mathrm{rel}} = 1/\gamma\) multiplied by \(\log(1/\pi_{\min})\). The second factor is the price of starting from the worst possible point, and it disappears once the walk starts close to the stationary distribution. On the cycle graph this factor does not actually bite, because \(\pi\) is uniform regardless of the starting point, and the gap between the \(\ell^2\) distance and the total variation distance stays around \(\sqrt{n}\).

Conversely, combined with the lower bound \(t_{\mathrm{mix}}(\varepsilon) \ge (t_{\mathrm{rel}} - 1) \log \frac{1}{2\varepsilon}\) ([1, Theorem 12.5]), this places the mixing time somewhere between a constant multiple of the relaxation time and \(\log(1/\pi_{\min})\) times it. Closing that gap calls for a finer analysis, such as the cutoff phenomenon [2].

Directions for future work: (i) extending the analysis to non-reversible chains, (ii) bounding \(\pi_{\min}\) for graphs with weighted edges, and (iii) measuring the walk on graphs built from real data, such as road networks.
