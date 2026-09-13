---
navigation:
  order: 10
---

# 4.1 נקודות קצה

| מתודה | נתיב | מטרה | דרישה |
|---|---|---|---|
| POST | `/notes/push` | שליחת שינוי בפתק | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | קבלת שינויים שאחרי הגרסה שצוינה | REQ-001 |
| DELETE | `/notes/{id}` | מחיקת פתק (לאשפה) | REQ-005 |
| POST | `/notes/{id}/restore` | שחזור פתק מהאשפה | REQ-005 |
