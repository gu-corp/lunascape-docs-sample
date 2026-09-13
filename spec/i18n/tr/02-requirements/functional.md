---
navigation:
  order: 10
---

# 2.1 İşlevsel gereksinimler

| ID | Gereksinim | Öncelik | Doğrulama yöntemi |
|---|---|---|---|
| REQ-001 | Bir cihazda oluşturulan not, bağlantı kurulduktan sonra 10 saniye içinde diğer cihazlara ulaşır | Zorunlu | Entegrasyon testi |
| REQ-002 | Çevrimdışıyken düzenlenen not, yeniden bağlanıldığında otomatik olarak gönderilir | Zorunlu | Entegrasyon testi |
| REQ-003 | Aynı sürüm üzerindeki iki güncelleme çakışma olarak algılanır | Zorunlu | Birim testi |
| REQ-004 | Çakışma, [3.4'teki kurallarla](../03-architecture/conflicts.md) otomatik olarak çözülür ve iki tarafın içeriği de kaybolmaz | Zorunlu | Birim testi |
| REQ-005 | Silme işlemi diğer cihazlara da yansır ve 30 gün boyunca çöp kutusundan geri alınabilir | Önerilen | Entegrasyon testi |
| REQ-006 | Cihaz, eşitleme durumunu (eşitlendi, gönderiliyor, çakışma var) gösterebilir | Önerilen | Gözle inceleme |
