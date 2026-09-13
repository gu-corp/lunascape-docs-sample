---
navigation:
  order: 10
---

# 1. Giriş

Sonlu bir durum uzayı üzerindeki indirgenemez ve periyodik olmayan bir Markov zinciri, zamanla tek bir durağan dağılım \(\pi\) değerine yakınsar. Ne kadar hızlı yakınsadığını ölçen büyüklük **karışma zamanı**dır. Zincirin geçiş matrisi \(P\) ve \(t\) anında \(x\) durumundan başlayan dağılım \(P^t(x,\cdot)\) olarak yazıldığında,

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

olarak tanımlanır. Burada \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) toplam değişim uzaklığıdır.

Bu çalışmada, \(G = (V, E)\) grafı üzerindeki **tembel rastgele yürüyüş** ele alınmaktadır (her adımda \(1/2\) olasılıkla yerinde kalınır, \(1/2\) olasılıkla komşu köşelerden biri düzgün dağılımla seçilerek oraya geçilir). Tembellik periyodik olmamayı güvence altına alır ve geçiş matrisi

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{diğer durumlarda})
\end{cases}
$$

biçimini alır. Durağan dağılım \(\pi(x) = \deg(x) / 2|E|\) şeklindedir.

2. bölümde gerekli tanımlar ve yardımcı önermeler bir araya getirilir; 3. bölümde spektral aralıktan elde edilen karışma zamanı üst sınırı (Teorem 3.1) ifade edilip kanıtlanır ve kestirimin keskinliği çevrim grafı ile tam graf üzerinde sayısal olarak sınanır.
