---
navigation:
  order: 20
---

# 4.2 Запит і відповідь

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Покупки\n- Молоко\n- Яйця",
  "deviceId": "d_macbook"
}
```

Відповідь (успіх):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Відповідь (конфлікт — повертається результат, розв'язаний за [правилами з 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Покупки\n- Молоко\n- Яйця\n>>> d_iphone\n- Хліб" }
```
