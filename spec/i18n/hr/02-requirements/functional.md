---
navigation:
  order: 10
---

# 2.1 Funkcionalni zahtjevi

| ID | Zahtjev | Prioritet | Način provjere |
|---|---|---|---|
| REQ-001 | Bilješka stvorena na jednom uređaju stiže na druge uređaje unutar 10 sekundi od povezivanja | Obavezno | Integracijski test |
| REQ-002 | Bilješka uređena izvan mreže šalje se automatski pri ponovnom povezivanju | Obavezno | Integracijski test |
| REQ-003 | Dvije izmjene iste verzije otkrivaju se kao sukob | Obavezno | Jedinični test |
| REQ-004 | Sukob se automatski rješava prema [pravilima iz 3.4](../03-architecture/conflicts.md), bez gubitka sadržaja bilo koje strane | Obavezno | Jedinični test |
| REQ-005 | Brisanje se prenosi na druge uređaje, a sadržaj se 30 dana može vratiti iz Koša za smeće | Preporučeno | Integracijski test |
| REQ-006 | Uređaj može prikazati stanje sinkronizacije (sinkronizirano, slanje u tijeku, sukob) | Preporučeno | Vizualna provjera |
