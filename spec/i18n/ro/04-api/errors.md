---
navigation:
  order: 30
---

# 4.3 Erori

| Stare | Semnificație | Ce face dispozitivul |
|---|---|---|
| 400 | Cerere cu format incorect | Oprește trimiterea și o consemnează în jurnal |
| 401 | Token invalid | Se autentifică din nou |
| 409 | Nepotrivire de versiune (conflict) | Înlocuiește cu `body` din răspuns și afișează un conflict |
| 413 | Corpul depășește 1 MB | Anunță utilizatorul și nu trimite |
| 429 | Prea multe cereri | Așteaptă numărul de secunde indicat în `Retry-After`, apoi retrimite |
| 5xx | Defecțiune a serverului | Retrimite cu întârziere exponențială (de cel mult 5 ori) |
