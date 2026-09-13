---
navigation:
  order: 30
---

# 4.3 Hatalar

| Durum | Anlamı | Cihazın yapacağı |
|---|---|---|
| 400 | İstek biçimi hatalı | Göndermeyi durdurun, günlüğe kaydedin |
| 401 | Belirteç geçersiz | Yeniden kimlik doğrulayın |
| 409 | Sürüm uyuşmazlığı (çakışma) | Yanıttaki `body` ile değiştirin, çakışma olduğunu gösterin |
| 413 | Gövde 1 MB'ı aşıyor | Kullanıcıya bildirin, göndermeyin |
| 429 | İstek sayısı çok fazla | `Retry-After` içinde belirtilen saniye kadar bekleyip yeniden gönderin |
| 5xx | Sunucu arızası | Üstel geri çekilmeyle yeniden gönderin (en fazla 5 kez) |
