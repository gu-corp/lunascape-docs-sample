---
navigation:
  order: 40
---

# 3.4 Rješavanje sukoba

| Slučaj | Pravilo |
|---|---|
| Isti redak promijenjen je neovisno | Zadržavaju se obje promjene: ona koja je stigla kasnije dodaje se na kraj, odvojena znakom `>>>`. Korisniku se prikazuje sukob (REQ-006) |
| Promijenjeni su različiti redci | Automatsko objedinjavanje trosmjernim spajanjem; korisnika se o tome ne obavještava |
| Jedna je strana izbrisala zapis | Brisanje ima prednost, a sadržaj druge strane odlazi u koš za smeće (REQ-005) |

Ni u jednom slučaju sadržaj se ne gubi (REQ-004).
