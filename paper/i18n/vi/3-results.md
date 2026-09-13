---
navigation:
  order: 30
---

# 3. Kết quả chính

## 3.1 Chặn trên từ khoảng trống phổ

**Định lý 3.1.** Đối với bước ngẫu nhiên lười trên một đồ thị hữu hạn liên thông,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*Chứng minh.* Do tính lười nên mọi giá trị riêng đều không âm, vì vậy \(\lambda_\ast = \lambda_2 = 1 - \gamma\). Theo Bổ đề 2.3 và \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\),

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

Vế phải không vượt quá \(\varepsilon\) khi \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), và khẳng định được suy ra từ \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 Đồ thị vòng và đồ thị đầy đủ

Với bước đi lười trên đồ thị vòng \(C_n\), ta có \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), nên \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). Định lý 3.1 cho \(t_{\mathrm{mix}} = O(n^2 \log n)\), trong khi giá trị thực là \(\Theta(n^2)\); chặn trên lỏng hơn một thừa số \(\log n\).

Trên đồ thị đầy đủ \(K_n\), ta có \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), nên \(\gamma \ge \frac12\). Định lý 3.1 cho \(t_{\mathrm{mix}} = O(\log n)\), trùng với giá trị thực \(\Theta(\log n)\).

Bảng 1 và Hình 2 trình bày chặn trên tại \(\varepsilon = 1/4\) cùng với giá trị đo được, tính bằng số từ các lũy thừa của ma trận chuyển.

**Bảng 1.** Chặn trên của thời gian trộn \(t_{\mathrm{mix}}(1/4)\) (Định lý 3.1) so với giá trị đo được.

| Đồ thị | \(n\) | \(\gamma\) | Chặn trên | Đo được |
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
  "description": "Chặn trên và giá trị đo được của thời gian trộn",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "Chặn trên", "t": 39}, {"graph": "C_n", "n": 10, "kind": "Đo được", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "Chặn trên", "t": 180}, {"graph": "C_n", "n": 20, "kind": "Đo được", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "Chặn trên", "t": 831}, {"graph": "C_n", "n": 40, "kind": "Đo được", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "Chặn trên", "t": 6}, {"graph": "K_n", "n": 10, "kind": "Đo được", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "Chặn trên", "t": 8}, {"graph": "K_n", "n": 20, "kind": "Đo được", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "Chặn trên", "t": 10}, {"graph": "K_n", "n": 40, "kind": "Đo được", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "Số đỉnh n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (thang loga)"},
    "color": {"field": "graph", "type": "nominal", "title": "Đồ thị"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**Hình 2.** Thời gian trộn theo số đỉnh \(n\). Trên đồ thị vòng, tỉ số giữa chặn trên và giá trị đo được giãn rộng theo \(n\); trên đồ thị đầy đủ, tỉ số này chỉ nằm trong một thừa số hằng.
