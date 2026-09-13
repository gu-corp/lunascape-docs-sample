---
navigation:
  order: 40
---

# 3.4 Çakışmaların çözümü

| Durum | Kural |
|---|---|
| Aynı satır birbirinden bağımsız değiştirildi | İki değişiklik de saklanır: sonra gelen, `>>>` ile ayrılarak sona eklenir. Cihaz çakışma olduğunu gösterir (REQ-006) |
| Farklı satırlar değiştirildi | Üç yönlü birleştirmeyle otomatik olarak birleştirilir; kullanıcıya bildirilmez |
| Taraflardan biri notu sildi | Silme önceliklidir, diğer tarafın içeriği çöp kutusuna gider (REQ-005) |

Her durumda hiçbir içerik kaybolmaz (REQ-004).
