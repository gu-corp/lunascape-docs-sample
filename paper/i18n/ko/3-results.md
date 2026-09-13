---
navigation:
  order: 30
---

# 3. 주요 결과

## 3.1 스펙트럼 간격에 의한 상계

**정리 3.1.** 유한 연결 그래프 위의 지연 확률 보행에 대하여,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*증명.* 지연에 의해 고윳값은 음이 아니므로 \(\lambda_\ast = \lambda_2 = 1 - \gamma\)이다. 보조정리 2.3과 \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\)로부터

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

우변이 \(\varepsilon\) 이하가 되는 \(t\)로는 \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\)이면 충분하며, \(\sqrt{\pi_{\min}} \ge \pi_{\min}\)로부터 주장이 따라 나온다. \(\square\)

## 3.2 순환 그래프와 완전 그래프

순환 그래프 \(C_n\)의 지연 보행에서는 \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\)이므로, \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\)이다. 정리 3.1은 \(t_{\mathrm{mix}} = O(n^2 \log n)\)을 주지만, 참값은 \(\Theta(n^2)\)이며 \(\log n\)만큼 느슨하다.

완전 그래프 \(K_n\)에서는 \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\)이고 \(\gamma \ge \frac12\)이다. 정리 3.1은 \(t_{\mathrm{mix}} = O(\log n)\)을 주며, 참값 \(\Theta(\log n)\)과 일치한다.

표 1과 그림 2에 \(\varepsilon = 1/4\)에서의 상계와, 전이 행렬의 거듭제곱으로부터 수치 계산한 실측값을 나타낸다.

**표 1.** 혼합 시간 \(t_{\mathrm{mix}}(1/4)\)의 상계(정리 3.1)와 실측값.

| 그래프 | \(n\) | \(\gamma\) | 상계 | 실측 |
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
  "description": "혼합 시간의 상계와 실측값",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "상계", "t": 39}, {"graph": "C_n", "n": 10, "kind": "실측", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "상계", "t": 180}, {"graph": "C_n", "n": 20, "kind": "실측", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "상계", "t": 831}, {"graph": "C_n", "n": 40, "kind": "실측", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "상계", "t": 6}, {"graph": "K_n", "n": 10, "kind": "실측", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "상계", "t": 8}, {"graph": "K_n", "n": 20, "kind": "실측", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "상계", "t": 10}, {"graph": "K_n", "n": 40, "kind": "실측", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "정점 수 n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4)(로그)"},
    "color": {"field": "graph", "type": "nominal", "title": "그래프"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**그림 2.** 정점 수 \(n\)에 대한 혼합 시간. 순환 그래프에서는 상계와 실측의 비가 \(n\)과 함께 벌어지고, 완전 그래프에서는 상수배에 머문다.
