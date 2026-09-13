---
navigation:
  order: 10
---

# 4.1 Päätepisteet

| Metodi | Polku | Tarkoitus | Vaatimus |
|---|---|---|---|
| POST | `/notes/push` | Lähetä muistiinpanon muutos | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Vastaanota annettua versiota uudemmat muutokset | REQ-001 |
| DELETE | `/notes/{id}` | Poista muistiinpano (roskakoriin) | REQ-005 |
| POST | `/notes/{id}/restore` | Palauta muistiinpano roskakorista | REQ-005 |
