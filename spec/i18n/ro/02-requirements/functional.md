---
navigation:
  order: 10
---

# 2.1 Cerințe funcționale

| ID | Cerință | Prioritate | Metodă de verificare |
|---|---|---|---|
| REQ-001 | O notiță creată pe un dispozitiv ajunge la celelalte dispozitive în cel mult 10 secunde de la conectare | Obligatoriu | Test de integrare |
| REQ-002 | O notiță editată offline este trimisă automat la reconectare | Obligatoriu | Test de integrare |
| REQ-003 | Două actualizări asupra aceleiași versiuni sunt detectate drept conflict | Obligatoriu | Test unitar |
| REQ-004 | Conflictul se rezolvă automat conform [regulilor din 3.4](../03-architecture/conflicts.md), fără a pierde conținutul niciuneia dintre părți | Obligatoriu | Test unitar |
| REQ-005 | Ștergerea se propagă și pe celelalte dispozitive, iar timp de 30 de zile poate fi restaurată din coșul de gunoi | Recomandat | Test de integrare |
| REQ-006 | Dispozitivul poate afișa starea sincronizării (sincronizat, în curs de trimitere, conflict) | Recomandat | Inspecție vizuală |
