---
navigation:
  order: 20
---

# 4.2 Запрос и ответ

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Покупки\n- Молоко\n- Яйца",
  "deviceId": "d_macbook"
}
```

Ответ (успех):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Ответ (конфликт; возвращается результат разрешения по [правилам из 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Покупки\n- Молоко\n- Яйца\n>>> d_iphone\n- Хлеб" }
```
