---
navigation:
  order: 40
---

# 3.4 Løsning af konflikter

| Tilfælde | Regel |
|---|---|
| Den samme linje er ændret hvert sted for sig | Begge ændringer bevares: den, der kom sidst, føjes til til sidst, adskilt med `>>>`. Brugeren får vist, at der er en konflikt (REQ-006) |
| Forskellige linjer er ændret | Flettes automatisk med en trevejsfletning; brugeren får ikke besked |
| Den ene side har slettet | Sletningen vinder, og den anden sides indhold lægges i papirkurven (REQ-005) |

I alle tilfælde går intet indhold tabt (REQ-004).
