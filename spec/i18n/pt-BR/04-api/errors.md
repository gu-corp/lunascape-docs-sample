---
navigation:
  order: 30
---

# 4.3 Erros

| Status | Significado | O que o dispositivo faz |
|---|---|---|
| 400 | Formato da requisição inválido | Interromper o envio e registrar em log |
| 401 | Token inválido | Autenticar novamente |
| 409 | Divergência de versão (conflito) | Substituir pelo `body` da resposta e indicar o conflito |
| 413 | Corpo acima de 1 MB | Avisar o usuário e não enviar |
| 429 | Requisições em excesso | Aguardar os segundos indicados em `Retry-After` e reenviar |
| 5xx | Falha do servidor | Reenviar com espera exponencial (até 5 vezes) |
