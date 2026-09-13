---
navigation:
  order: 30
---

# 3. मुख्य परिणाम

## 3.1 स्पेक्ट्रल गैप से प्राप्त ऊपरी सीमा

**प्रमेय 3.1.** किसी परिमित संबद्ध ग्राफ़ पर आलसी यादृच्छिक भ्रमण के लिए,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*प्रमाण.* आलस्य के कारण सभी आइगेनमान ऋणेतर होते हैं, अतः \(\lambda_\ast = \lambda_2 = 1 - \gamma\)। प्रमेयिका 2.3 तथा \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) से

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

दाहिना पक्ष \(\varepsilon\) से अधिक नहीं होता जब \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), और \(\sqrt{\pi_{\min}} \ge \pi_{\min}\) से दावा सिद्ध होता है। \(\square\)

## 3.2 चक्र ग्राफ़ और पूर्ण ग्राफ़

चक्र ग्राफ़ \(C_n\) पर आलसी भ्रमण के लिए \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\) होता है, अतः \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\)। प्रमेय 3.1 से \(t_{\mathrm{mix}} = O(n^2 \log n)\) प्राप्त होता है, जबकि वास्तविक मान \(\Theta(n^2)\) है — यह सीमा \(\log n\) गुणक जितनी ढीली है।

पूर्ण ग्राफ़ \(K_n\) पर \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\) है, अतः \(\gamma \ge \frac12\)। प्रमेय 3.1 से \(t_{\mathrm{mix}} = O(\log n)\) प्राप्त होता है, जो वास्तविक मान \(\Theta(\log n)\) से मेल खाता है।

तालिका 1 और चित्र 2 में \(\varepsilon = 1/4\) पर ऊपरी सीमा तथा संक्रमण आव्यूह की घातों से संख्यात्मक रूप से परिकलित मापित मान दिखाए गए हैं।

**तालिका 1.** मिश्रण समय \(t_{\mathrm{mix}}(1/4)\) की ऊपरी सीमा (प्रमेय 3.1) और मापित मान।

| ग्राफ़ | \(n\) | \(\gamma\) | सीमा | मापित |
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
  "description": "मिश्रण समय की ऊपरी सीमा और मापित मान",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "सीमा", "t": 39}, {"graph": "C_n", "n": 10, "kind": "मापित", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "सीमा", "t": 180}, {"graph": "C_n", "n": 20, "kind": "मापित", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "सीमा", "t": 831}, {"graph": "C_n", "n": 40, "kind": "मापित", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "सीमा", "t": 6}, {"graph": "K_n", "n": 10, "kind": "मापित", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "सीमा", "t": 8}, {"graph": "K_n", "n": 20, "kind": "मापित", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "सीमा", "t": 10}, {"graph": "K_n", "n": 40, "kind": "मापित", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "शीर्षों की संख्या n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (लघुगणकीय)"},
    "color": {"field": "graph", "type": "nominal", "title": "ग्राफ़"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**चित्र 2.** शीर्षों की संख्या \(n\) के सापेक्ष मिश्रण समय। चक्र ग्राफ़ में सीमा और मापित मान का अनुपात \(n\) के साथ बढ़ता जाता है, जबकि पूर्ण ग्राफ़ में यह एक अचर गुणक तक ही सीमित रहता है।
