---
navigation:
  order: 10
---

# 3.1 Bileşenler

| Öğe | Rol |
|---|---|
| İstemci | Notlardaki düzenlemeleri izler, değişiklikleri kuyruğa alır ve bağlantı kurulduğunda sunucuya gönderir |
| Eşitleme API'si | Değişiklikleri kabul eder, sürüm numaralarını verir ve diğer aygıtlara dağıtır |
| Depolama | Her notun geçerli içeriğini ve son 30 günlük geçmişini tutar |
| Bildirimler | Bir değişiklik olduğunda, aygıtı çekmeye yönlendiren hafif bir sinyal gönderir |

```mermaid
flowchart TB
  subgraph A[Aygıt A]
    EA[Düzenleyici] --> QA[Kuyruk]
  end
  subgraph B[Aygıt B]
    EB[Düzenleyici] --> QB[Kuyruk]
  end
  QA -- push --> API[Eşitleme API'si]
  QB -- push --> API
  API --> STORE[(Depolama)]
  API --> NOTIFY[Bildirimler]
  NOTIFY -. çekmeye yönlendirir .-> QA
  NOTIFY -. çekmeye yönlendirir .-> QB
```
