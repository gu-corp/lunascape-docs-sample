---
navigation:
  order: 10
---

# 1. Introduction

An irreducible, aperiodic Markov chain on a finite state space converges over time to a unique stationary distribution \(\pi\). How fast it converges is measured by the **mixing time**. Writing \(P\) for the chain's transition matrix and \(P^t(x,\cdot)\) for the distribution starting from state \(x\) at time \(t\), define

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

where \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) is the total variation distance.

This paper studies the **lazy random walk** on a graph \(G = (V, E)\) — at each step, stay in place with probability \(1/2\), or move to a uniformly chosen neighbor with probability \(1/2\). The laziness guarantees aperiodicity, and the transition matrix is

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{otherwise})
\end{cases}
$$

The stationary distribution is \(\pi(x) = \deg(x) / 2|E|\).

Section 2 collects the definitions and lemmas needed later; Section 3 states and proves an upper bound on the mixing time from the spectral gap (Theorem 3.1), and checks its sharpness numerically on the cycle graph and the complete graph.
