---
navigation:
  order: 10
---

# 2.1 Funktionella krav

| ID | Krav | Prioritet | Verifieringsmetod |
|---|---|---|---|
| REQ-001 | En anteckning som skapas på en enhet når övriga enheter inom 10 sekunder efter anslutning | Obligatoriskt | Integrationstest |
| REQ-002 | En anteckning som redigerats offline skickas automatiskt vid återanslutning | Obligatoriskt | Integrationstest |
| REQ-003 | Två uppdateringar av samma version upptäcks som en konflikt | Obligatoriskt | Enhetstest |
| REQ-004 | Konflikter löses automatiskt enligt [reglerna i 3.4](../03-architecture/conflicts.md), utan att innehållet från någondera sidan går förlorat | Obligatoriskt | Enhetstest |
| REQ-005 | En borttagning återspeglas på övriga enheter och kan återställas från papperskorgen i 30 dagar | Rekommenderat | Integrationstest |
| REQ-006 | En enhet kan visa synkroniseringens status (synkroniserad, skickar, konflikt) | Rekommenderat | Okulär kontroll |
