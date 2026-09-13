---
navigation:
  order: 30
---

# 4.3 Pogreške

| Stanje | Značenje | Postupak uređaja |
|---|---|---|
| 400 | Neispravan oblik zahtjeva | Prekinuti slanje i zabilježiti u zapisnik |
| 401 | Token nije valjan | Ponovno se autentificirati |
| 409 | Neslaganje verzija (sukob) | Zamijeniti sadržajem `body` iz odgovora i prikazati sukob |
| 413 | Tijelo veće od 1 MB | Obavijestiti korisnika i ne slati |
| 429 | Previše zahtjeva | Pričekati broj sekundi naveden u `Retry-After` pa ponovno poslati |
| 5xx | Kvar poslužitelja | Ponovno slati s eksponencijalnim odmakom (najviše 5 puta) |
