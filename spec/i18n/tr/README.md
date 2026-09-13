# Orbit Not Eşitleme Hizmeti — İşlevsel Şartname

| Öğe | İçerik |
|---|---|
| Belge kimliği | ORB-SPEC-001 |
| Sürüm | 1.3 |
| Güncelleme tarihi | 2026-09-06 |
| Durum | Onaylandı |
| Belge sorumlusu | Orbit geliştirme ekibi (kurgusal) |
| İlgili | ORB-REQ-001 (gereksinim listesi), ORB-ADR-0001 (eşitleme yönteminin seçimi) |

## Düzeltme geçmişi

| Sürüm | Tarih | Düzeltme içeriği | Düzelten |
|---|---|---|---|
| 1.0 | 2026-07-01 | İlk sürüm | Orbit geliştirme ekibi |
| 1.1 | 2026-08-10 | Çakışma çözümü kuralları eklendi (3.4) | Orbit geliştirme ekibi |
| 1.2 | 2026-09-06 | API hata tablosu eklendi (4.3) | Orbit geliştirme ekibi |
| 1.3 | 2026-09-06 | Her bölüm için bir klasör olacak biçimde yeniden düzenlendi | Orbit geliştirme ekibi |

## Yapı

1. [Genel bakış](01-overview/README.md) — amaç, [kapsam ve varsayımlar](01-overview/scope.md), [terimler](01-overview/terms.md)
2. [Gereksinimler](02-requirements/README.md) — [işlevsel gereksinimler](02-requirements/functional.md), [işlevsel olmayan gereksinimler](02-requirements/non-functional.md), [gereksinimlerin izlenmesi](02-requirements/traceability.md)
3. [Mimari](03-architecture/README.md) — [bileşenler](03-architecture/components.md), [eşitleme akışı](03-architecture/sync-flow.md), [sürüm numaraları](03-architecture/versioning.md), [çakışmaların çözümü](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [uç noktalar](04-api/endpoints.md), [istek ve yanıt](04-api/push.md), [hatalar](04-api/errors.md)
5. [Tasarım kararları](05-decisions/README.md) — [ORB-ADR-0001, eşitleme yönteminin seçimi](05-decisions/0001-sync-method.md)

> **Bu belge hakkında**
> Lunascape Docs ile yazmanın bir örneği olarak hazırlanmış kurgusal bir şartnamedir. Böyle bir ürün veya şirket gerçekte yoktur. Her bölüm için bir klasörün, tabloların, diyagramların (Mermaid), kodun ve çevirinin nasıl kullanıldığını göstermek içindir.
