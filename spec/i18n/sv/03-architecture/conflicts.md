---
navigation:
  order: 40
---

# 3.4 Konfliktlösning

| Fall | Regel |
|---|---|
| Samma rad har ändrats var för sig | Båda ändringarna behålls: den som kom senare läggs till sist, avskild med `>>>`. Användaren får se att det finns en konflikt (REQ-006) |
| Olika rader har ändrats | Slås samman automatiskt med en trevägssammanslagning; användaren informeras inte |
| Den ena sidan har tagit bort | Borttagningen gäller, och den andra sidans innehåll hamnar i papperskorgen (REQ-005) |

I samtliga fall går inget innehåll förlorat (REQ-004).
