---
navigation:
  order: 10
---

# 1. Giới thiệu

Một xích Markov bất khả quy và không tuần hoàn trên không gian trạng thái hữu hạn hội tụ theo thời gian về một phân phối dừng duy nhất \(\pi\). Đại lượng đo tốc độ hội tụ đó là **thời gian trộn**. Ký hiệu \(P\) là ma trận chuyển của xích và \(P^t(x,\cdot)\) là phân phối xuất phát từ trạng thái \(x\) tại thời điểm \(t\), ta định nghĩa

$$
d(t) = \max_{x \in \Omega} \bigl\| P^t(x,\cdot) - \pi \bigr\|_{\mathrm{TV}}, \qquad
t_{\mathrm{mix}}(\varepsilon) = \min\{\, t \ge 0 : d(t) \le \varepsilon \,\}
$$

Ở đây \(\|\mu - \nu\|_{\mathrm{TV}} = \frac12 \sum_{y} |\mu(y) - \nu(y)|\) là khoảng cách biến phân toàn phần.

Bài viết này xét **bước ngẫu nhiên trễ** trên đồ thị \(G = (V, E)\) (tại mỗi thời điểm, đứng yên với xác suất \(1/2\), hoặc chuyển sang một đỉnh kề được chọn đều với xác suất \(1/2\)). Tính trễ bảo đảm tính không tuần hoàn, và ma trận chuyển là

$$
P(x, y) = \begin{cases}
\dfrac{1}{2} & (y = x) \\[6pt]
\dfrac{1}{2\deg(x)} & (\{x, y\} \in E) \\[6pt]
0 & (\text{khác})
\end{cases}
$$

Phân phối dừng là \(\pi(x) = \deg(x) / 2|E|\).

Mục 2 tập hợp các định nghĩa và bổ đề cần thiết; Mục 3 phát biểu và chứng minh chặn trên của thời gian trộn theo khe phổ (Định lý 3.1), rồi kiểm tra bằng số độ chính xác của đánh giá này trên đồ thị vòng và đồ thị đầy đủ.
