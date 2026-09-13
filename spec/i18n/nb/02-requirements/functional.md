---
navigation:
  order: 10
---

# 2.1 Funksjonelle krav

| ID | Krav | Prioritet | Verifisering |
|---|---|---|---|
| REQ-001 | Et notat som opprettes på én enhet, når andre enheter innen 10 sekunder etter tilkobling | Påkrevd | Integrasjonstest |
| REQ-002 | Et notat som redigeres frakoblet, sendes automatisk ved gjenoppkobling | Påkrevd | Integrasjonstest |
| REQ-003 | To oppdateringer av samme versjon oppdages som en konflikt | Påkrevd | Enhetstest |
| REQ-004 | En konflikt løses automatisk etter [reglene i 3.4](../03-architecture/conflicts.md), uten at innholdet fra noen av sidene går tapt | Påkrevd | Enhetstest |
| REQ-005 | En sletting gjenspeiles på andre enheter, og kan gjenopprettes fra papirkurven i 30 dager | Anbefalt | Integrasjonstest |
| REQ-006 | En enhet kan vise synkroniseringsstatusen (synkronisert, sender, konflikt) | Anbefalt | Visuell kontroll |
