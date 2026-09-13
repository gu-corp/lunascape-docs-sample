---
navigation:
  order: 10
---

# 1. Pendahuluan

Rantai Markov yang tak terturunkan dan aperiodik pada ruang keadaan terhingga menumpu dari masa ke masa kepada satu taburan pegun \(\pi\) yang unik. Kepantasan penumpuan itu diukur oleh **masa pencampuran**. Dengan menulis \(P\) bagi matriks peralihan rantai tersebut dan \(P^t(x,\cdot)\) bagi taburan bermula dari keadaan \(x\) pada masa \(t\), kita takrifkan

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

dengan \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) ialah jarak variasi total.

Kertas ini membincangkan **perjalanan rawak malas** pada graf \(G = (V, E)\) (pada setiap masa, kekal di tempat dengan kebarangkalian \(1/2\), atau berpindah secara seragam ke jiran dengan kebarangkalian \(1/2\)). Sifat malas itu menjamin keaperiodikan, dan matriks peralihannya ialah

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{lain-lain})
\end{cases}
$$

Taburan pegunnya ialah \(\pi(x) = \deg(x) / 2|E|\).

Bahagian 2 menghimpunkan takrif dan lema yang diperlukan, manakala Bahagian 3 menyatakan dan membuktikan batas atas masa pencampuran daripada jurang spektrum (Teorem 3.1), serta mengesahkan ketepatan anggaran itu secara berangka pada graf kitaran dan graf lengkap.
