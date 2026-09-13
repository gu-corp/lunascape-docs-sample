---
navigation:
  order: 10
---

# 1. Pendahuluan

Rantai Markov yang tak tereduksi dan aperiodik pada ruang keadaan berhingga konvergen seiring waktu ke sebuah distribusi stasioner tunggal \(\pi\). Seberapa cepat konvergensi itu terjadi diukur oleh **waktu pencampuran**. Dengan menuliskan \(P\) sebagai matriks transisi rantai tersebut dan \(P^t(x,\cdot)\) sebagai distribusi dari keadaan \(x\) pada waktu \(t\), definisikan

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Di sini \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) adalah jarak variasi total.

Makalah ini membahas **jalan acak malas** pada graf \(G = (V, E)\) (pada setiap waktu, tetap di tempat dengan peluang \(1/2\), atau berpindah ke salah satu simpul tetangga secara seragam dengan peluang \(1/2\)). Sifat malas tersebut menjamin aperiodisitas, dan matriks transisinya menjadi

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{lainnya})
\end{cases}
$$

Distribusi stasionernya adalah \(\pi(x) = \deg(x) / 2|E|\).

Bagian 2 merangkum definisi dan lema yang diperlukan; Bagian 3 menyatakan dan membuktikan batas atas waktu pencampuran berdasarkan celah spektral (Teorema 3.1), serta memeriksa ketajaman taksiran itu secara numerik pada graf siklus dan graf lengkap.
