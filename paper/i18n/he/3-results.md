---
navigation:
  order: 30
---

# 3. תוצאות עיקריות

## 3.1 חסם עליון מתוך הפער הספקטרלי

**משפט 3.1.** עבור הילוך מקרי עצל על גרף סופי וקשיר,

$$
t_{\mathrm{mix}}(\varepsilon) \;\le\; \frac{1}{\gamma}\,\log\!\left(\frac{1}{\varepsilon\,\pi_{\min}}\right), \qquad \pi_{\min} = \min_x \pi(x).
$$

*הוכחה.* העצלות הופכת את כל הערכים העצמיים לאי-שליליים, ולכן \(\lambda_\ast = \lambda_2 = 1 - \gamma\). מלמה 2.3 ומן \(\frac{1-\pi(x)}{\pi(x)} \le \frac{1}{\pi_{\min}}\) נובע

$$
d(t) \le \frac{1}{2\sqrt{\pi_{\min}}} (1 - \gamma)^t \le \frac{1}{\sqrt{\pi_{\min}}} e^{-\gamma t}.
$$

האגף הימני קטן מ-\(\varepsilon\) או שווה לו כאשר \(t \ge \frac{1}{\gamma} \log \frac{1}{\varepsilon \sqrt{\pi_{\min}}}\), והטענה נובעת מן \(\sqrt{\pi_{\min}} \ge \pi_{\min}\). \(\square\)

## 3.2 גרף המעגל וגרף השלם

עבור ההילוך העצל על גרף המעגל \(C_n\) מתקיים \(\lambda_2 = \frac12\bigl(1 + \cos\frac{2\pi}{n}\bigr)\), ולכן \(\gamma = \frac12\bigl(1 - \cos\frac{2\pi}{n}\bigr) \approx \frac{\pi^2}{n^2}\). משפט 3.1 נותן \(t_{\mathrm{mix}} = O(n^2 \log n)\), אך הערך האמיתי הוא \(\Theta(n^2)\) — החסם רופף בפי \(\log n\).

בגרף השלם \(K_n\) מתקיים \(\lambda_2 = \frac12\bigl(1 - \frac{1}{n-1}\bigr)\), ולכן \(\gamma \ge \frac12\). משפט 3.1 נותן \(t_{\mathrm{mix}} = O(\log n)\), בהתאמה לערך האמיתי \(\Theta(\log n)\).

טבלה 1 ואיור 2 מציגים את החסם עבור \(\varepsilon = 1/4\) לצד הערך הנמדד, שחושב נומרית מחזקות של מטריצת המעברים.

**טבלה 1.** החסם העליון על זמן הערבוב \(t_{\mathrm{mix}}(1/4)\) (משפט 3.1) מול הערך הנמדד.

| גרף | \(n\) | \(\gamma\) | חסם | נמדד |
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
  "description": "החסם העליון וזמן הערבוב הנמדד",
  "width": 420,
  "height": 240,
  "data": {
    "values": [
      {"graph": "C_n", "n": 10, "kind": "חסם", "t": 39}, {"graph": "C_n", "n": 10, "kind": "נמדד", "t": 13},
      {"graph": "C_n", "n": 20, "kind": "חסם", "t": 180}, {"graph": "C_n", "n": 20, "kind": "נמדד", "t": 49},
      {"graph": "C_n", "n": 40, "kind": "חסם", "t": 831}, {"graph": "C_n", "n": 40, "kind": "נמדד", "t": 195},
      {"graph": "K_n", "n": 10, "kind": "חסם", "t": 6}, {"graph": "K_n", "n": 10, "kind": "נמדד", "t": 3},
      {"graph": "K_n", "n": 20, "kind": "חסם", "t": 8}, {"graph": "K_n", "n": 20, "kind": "נמדד", "t": 4},
      {"graph": "K_n", "n": 40, "kind": "חסם", "t": 10}, {"graph": "K_n", "n": 40, "kind": "נמדד", "t": 4}
    ]
  },
  "mark": {"type": "line", "point": true},
  "encoding": {
    "x": {"field": "n", "type": "quantitative", "title": "מספר הצמתים n"},
    "y": {"field": "t", "type": "quantitative", "scale": {"type": "log"}, "title": "t_mix(1/4) (סולם לוגריתמי)"},
    "color": {"field": "graph", "type": "nominal", "title": "גרף"},
    "strokeDash": {"field": "kind", "type": "nominal", "title": ""}
  }
}
```

**איור 2.** זמן הערבוב כפונקציה של מספר הצמתים \(n\). בגרף המעגל היחס בין החסם לערך הנמדד מתרחב עם \(n\); בגרף השלם הוא נשאר בגדר מכפלה קבועה.
