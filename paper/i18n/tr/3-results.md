---
navigation:
  order: 30
---

# 3. Ana sonuçlar

## 3.1 Spektral aralıktan gelen üst sınır

**Teorem 3.1.** Sonlu bağlantılı bir graf üzerindeki tembel rastgele yürüyüş için,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Kanıt.* Tembellik nedeniyle özdeğerler negatif olmadığından \(\lambda_\ast = \lambda_2 = 1 - \gamma\) olur. Lemma 2.3 ve \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) eşitsizliğinden

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Sağ tarafın \(\varepsilon\) değerini aşmaması için \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\) olması yeterlidir; iddia da \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) eşitsizliğinden çıkar. \(\square\)

## 3.2 Çevrim grafı ve tam graf

Çevrim grafı \(C_n\) üzerindeki tembel yürüyüşte \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\) olduğundan \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\) olur. Teorem 3.1 buradan \(t_{\mathrm{mix}} = O(n^2 \log n)\) verir; oysa gerçek değer \(\Theta(n^2)\)'dir, yani sınır \(\log n\) çarpanı kadar gevşektir.

Tam graf \(K_n\) üzerinde \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) ve dolayısıyla \(\gamma \ge \frac12\)'dir. Teorem 3.1 buradan \(t_{\mathrm{mix}} = O(\log n)\) verir ve bu, gerçek değer \(\Theta(\log n)\) ile örtüşür.

Tablo 1 ve Şekil 2, \(\varepsilon = 1/4\) için üst sınırı ve geçiş matrisinin kuvvetlerinden sayısal olarak hesaplanan ölçülen değeri gösterir.

**Tablo 1.** Karışma zamanı \(t_{\mathrm{mix}}(1/4)\) için üst sınır (Teorem 3.1) ve ölçülen değer.

| Graf | \(n\) | \(\gamma\) | Üst sınır | Ölçülen |
|---|---:|---:|---:|---:|
| \(C_n\) | 10 | 0.0955 | 39 | 13 |
| \(C_n\) | 20 | 0.0245 | 180 | 49 |
| \(C_n\) | 40 | 0.0062 | 831 | 195 |
| \(K_n\) | 10 | 0.5556 | 6 | 3 |
| \(K_n\) | 20 | 0.5263 | 8 | 4 |
| \(K_n\) | 40 | 0.5128 | 10 | 4 |

```vega-lite
{
  "$schema": "https://vega.github.io/schema/vega-lite/v6.json",
  "description": "Karışma zamanının üst sınırı ve ölçülen değeri",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Üst sınır", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Ölçülen", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Üst sınır", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Ölçülen", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Üst sınır", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Ölçülen", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Üst sınır", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Ölçülen", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Üst sınır", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Ölçülen", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Üst sınır", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Ölçülen", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Köşe sayısı n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (logaritmik)"},
    "color": {"field": "graph", "type": "nominal", "title": "Graf"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Şekil 2.** Köşe sayısı \(n\) karşısında karışma zamanı. Çevrim grafında üst sınırın ölçülen değere oranı \(n\) büyüdükçe açılır; tam grafta ise sabit bir çarpan içinde kalır.
