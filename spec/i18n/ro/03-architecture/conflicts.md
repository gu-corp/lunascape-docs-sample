---
navigation:
  order: 40
---

# 3.4 Rezolvarea conflictelor

| Caz | Regulă |
|---|---|
| Aceeași linie a fost modificată separat | Ambele modificări se păstrează: cea sosită mai târziu se adaugă la sfârșit, separată prin `>>>`. Aparatul îi semnalează utilizatorului conflictul (REQ-006) |
| Au fost modificate linii diferite | Se integrează automat printr-o îmbinare în trei direcții; utilizatorul nu este înștiințat |
| Una dintre părți a șters notița | Ștergerea are prioritate, iar conținutul celeilalte părți ajunge în coșul de gunoi (REQ-005) |

În toate cazurile, niciun conținut nu se pierde (REQ-004).
