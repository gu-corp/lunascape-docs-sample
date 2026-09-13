---
navigation:
  order: 20
---

# 1.2 Opseg i pretpostavke

## Opseg

| Br. | Uključeno u opseg | Izvan opsega |
|---|---|---|
| 1 | Sinkronizacija stvaranja, ažuriranja i brisanja bilješki | Zajedničko uređivanje bilješki (dijeljenje pokazivača pri istodobnom uređivanju) |
| 2 | Otkrivanje i rješavanje sukoba među uređajima | Uređivač na uređaju |
| 3 | API za sinkronizaciju (HTTP) | Naplata, upravljanje računima |

## Pretpostavke

- Uređaji se povezuju samo povremeno. Uređivanje izvan mreže uzima se kao uobičajeno.
- Tijelo bilješke ograničeno je na najviše 1 MB.
- Redoslijed ne ovisi o satu uređaja; određuju ga brojevi verzija s poslužitelja.
