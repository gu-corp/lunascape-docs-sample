---
navigation:
  order: 40
---

# 3.4 Konfliktløsning

| Tilfelle | Regel |
|---|---|
| Samme linje er endret hver for seg | Begge endringene beholdes: den som kom sist, legges til slutt, skilt ut med `>>>`. Brukeren får beskjed om at det foreligger en konflikt (REQ-006) |
| Ulike linjer er endret | Slås sammen automatisk med en treveis fletting; brukeren får ikke beskjed |
| Den ene siden har slettet | Slettingen går foran, og innholdet fra den andre siden legges i papirkurven (REQ-005) |

I alle tilfeller går ikke noe innhold tapt (REQ-004).
