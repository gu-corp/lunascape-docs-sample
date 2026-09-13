# שירות סנכרון פתקים Orbit — מפרט תפקודי

| פריט | תוכן |
|---|---|
| מזהה מסמך | ORB-SPEC-001 |
| גרסה | 1.3 |
| תאריך עדכון | 2026-09-06 |
| מצב | מאושר |
| אחראי המסמך | צוות Orbit (בדיוני) |
| קשור | ORB-REQ-001 (רשימת הדרישות), ORB-ADR-0001 (בחירת שיטת הסנכרון) |

## היסטוריית גרסאות

| גרסה | תאריך | תוכן העדכון | מעדכן |
|---|---|---|---|
| 1.0 | 2026-07-01 | מהדורה ראשונה | צוות Orbit |
| 1.1 | 2026-08-10 | נוספו כללים ליישוב התנגשויות (3.4) | צוות Orbit |
| 1.2 | 2026-09-06 | נוספה טבלת השגיאות של ה-API (4.3) | צוות Orbit |
| 1.3 | 2026-09-06 | ארגון מחדש לתיקייה אחת לכל פרק | צוות Orbit |

## מבנה

1. [סקירה כללית](01-overview/README.md) — מטרה, [היקף והנחות יסוד](01-overview/scope.md), [מונחים](01-overview/terms.md)
2. [דרישות](02-requirements/README.md) — [דרישות תפקודיות](02-requirements/functional.md), [דרישות לא-תפקודיות](02-requirements/non-functional.md), [מעקב אחר דרישות](02-requirements/traceability.md)
3. [מבנה המערכת](03-architecture/README.md) — [רכיבים](03-architecture/components.md), [מהלך הסנכרון](03-architecture/sync-flow.md), [מספור גרסאות](03-architecture/versioning.md), [יישוב התנגשויות](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [נקודות קצה](04-api/endpoints.md), [בקשה ותשובה](04-api/push.md), [שגיאות](04-api/errors.md)
5. [החלטות תכן](05-decisions/README.md) — [ORB-ADR-0001 בחירת שיטת הסנכרון](05-decisions/0001-sync-method.md)

> **על המסמך הזה**
> זהו מפרט בדיוני שנכתב כדוגמה לאופן הכתיבה ב-Lunascape Docs. המוצר והחברה אינם קיימים במציאות. הוא נועד להראות שימוש בתיקייה לכל פרק, בטבלאות, בתרשימים (Mermaid), בקוד ובתרגום.
