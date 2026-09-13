---
navigation:
  order: 20
---

# 4.2 Żądanie i odpowiedź

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Zakupy\n- Mleko\n- Jajka",
  "deviceId": "d_macbook"
}
```

Odpowiedź (powodzenie):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Odpowiedź (konflikt — zwracana jest treść będąca wynikiem [reguł z 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Zakupy\n- Mleko\n- Jajka\n>>> d_iphone\n- Chleb" }
```
