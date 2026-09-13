---
navigation:
  order: 20
---

# 4.2 Заявка и отговор

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Покупки\n- Мляко\n- Яйца",
  "deviceId": "d_macbook"
}
```

Отговор (успех):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Отговор (конфликт — връща се резултатът от разрешаването по [правилата в 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Покупки\n- Мляко\n- Яйца\n>>> d_iphone\n- Хляб" }
```
