---
navigation:
  order: 10
---

# 2.1 Funktionelle krav

| ID | Krav | Prioritet | Verifikation |
|---|---|---|---|
| REQ-001 | En note oprettet på én enhed når frem til andre enheder inden for 10 sekunder efter tilslutning | Påkrævet | Integrationstest |
| REQ-002 | En note, der er redigeret offline, sendes automatisk ved gentilslutning | Påkrævet | Integrationstest |
| REQ-003 | To opdateringer af samme version registreres som en konflikt | Påkrævet | Enhedstest |
| REQ-004 | En konflikt løses automatisk efter [reglerne i 3.4](../03-architecture/conflicts.md), uden at indholdet fra nogen af siderne går tabt | Påkrævet | Enhedstest |
| REQ-005 | En sletning slår igennem på de andre enheder og kan gendannes fra papirkurven i 30 dage | Anbefalet | Integrationstest |
| REQ-006 | En enhed kan vise synkroniseringsstatus (synkroniseret, sender, konflikt) | Anbefalet | Visuel kontrol |
