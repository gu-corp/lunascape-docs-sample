---
navigation:
  order: 20
---

# 1.2 Kapsam ve varsayımlar

## Kapsam

| No. | Kapsam içinde | Kapsam dışında |
|---|---|---|
| 1 | Not oluşturma, güncelleme ve silme işlemlerinin eşitlenmesi | Notların ortak düzenlenmesi (eşzamanlı düzenlemede imleç paylaşımı) |
| 2 | Cihazlar arasındaki çakışmaların saptanması ve çözülmesi | Cihazdaki düzenleyici |
| 3 | Eşitleme API'si (HTTP) | Ücretlendirme, hesap yönetimi |

## Varsayımlar

- Cihazlar yalnızca aralıklı olarak bağlanır. Çevrimdışı düzenleme olağan durumdur.
- Bir notun gövdesi en çok 1 MB'tır.
- Sıra, cihazın saatine bağlı değildir; sunucunun sürüm numaraları belirler.
