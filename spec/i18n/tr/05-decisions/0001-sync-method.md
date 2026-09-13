---
navigation:
  order: 10
---

# ORB-ADR-0001: Eşitleme yöntemi olarak "sunucunun numaraladığı sürümler ve üç yönlü birleştirme" seçimi

| Öğe | İçerik |
|---|---|
| Belge kimliği | ORB-ADR-0001 |
| Sürüm | 1.0 |
| Güncelleme tarihi | 2026-07-01 |
| Durum | Onaylandı |

## 1. Arka plan

Birden çok cihazda çevrimdışı düzenlenen notların birbirine yakınsaması gerekiyor. Üç aday vardı: (a) en son güncelleme zamanının kazanması, (b) CRDT, (c) sunucunun numaraladığı sürüm numaraları ve üç yönlü birleştirme.

## 2. Karar

| No. | Karar |
|---|---|
| 1 | Sıra, sunucunun numaraladığı sürüm numaralarıyla belirlenir. Cihazın saatine güvenilmez |
| 2 | Çakışmalar üç yönlü birleştirmeyle çözülür; çözülemeyen satırda her iki taraf da korunur. İçeriği yitirmemek önceliklidir |
| 3 | CRDT benimsenmez. Notlar kısadır, eşzamanlı düzenleme gereksinimi yoktur ve metin boyutunun iki katına ya da daha fazlasına çıkması bu bedele değmez |

## 3. Etkiler

| No. | Etki |
|---|---|
| 1 | Cihaz `baseVersion` değerini tutar ve her göndermede buna ekler |
| 2 | Çakışmanın gösterilmesi (REQ-006) cihazın zorunlu bir işlevi olur |
| 3 | Sunucu son 30 günün geçmişini tutar (çöp kutusu ve üç yönlü birleştirmenin temeli için) |
