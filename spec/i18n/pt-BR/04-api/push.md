---
navigation:
  order: 20
---

# 4.2 Requisição e resposta

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Compras\n- Leite\n- Ovos",
  "deviceId": "d_macbook"
}
```

Resposta (sucesso):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Resposta (conflito; retorna o resultado da resolução pelas [regras de 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Compras\n- Leite\n- Ovos\n>>> d_iphone\n- Pão" }
```
