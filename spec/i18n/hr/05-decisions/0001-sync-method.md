---
navigation:
  order: 10
---

# ORB-ADR-0001: Kao način sinkronizacije odabrati „poslužiteljem dodijeljene verzije uz trosmjerno spajanje”

| Stavka | Sadržaj |
|---|---|
| ID dokumenta | ORB-ADR-0001 |
| Verzija | 1.0 |
| Datum ažuriranja | 2026-07-01 |
| Status | Odobreno |

## 1. Pozadina

Bilješke koje se uređuju izvan mreže na više uređaja moraju se uskladiti. Razmatrale su se tri mogućnosti: (a) pobjeđuje zadnje vrijeme izmjene, (b) CRDT, (c) brojevi verzija koje dodjeljuje poslužitelj uz trosmjerno spajanje.

## 2. Odluka

| Br. | Odluka |
|---|---|
| 1 | Redoslijed se određuje brojevima verzija koje dodjeljuje poslužitelj. Satovima uređaja se ne vjeruje |
| 2 | Sukobi se rješavaju trosmjernim spajanjem, a redak koji se ne može razriješiti zadržava obje strane. Prednost ima to da se sadržaj ne izgubi |
| 3 | CRDT se ne uvodi. Bilješke su kratke, nema zahtjeva za istodobnim uređivanjem, pa se cijena udvostručenja veličine sadržaja ili više od toga ne isplati |

## 3. Posljedice

| Br. | Posljedica |
|---|---|
| 1 | Uređaj čuva `baseVersion` i prilaže ga uz svako slanje |
| 2 | Prikaz sukoba (REQ-006) postaje obavezna značajka uređaja |
| 3 | Poslužitelj čuva povijest zadnjih 30 dana (za Koš za smeće i kao osnovu za trosmjerno spajanje) |
