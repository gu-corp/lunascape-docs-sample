---
navigation:
  order: 20
---

# 1.2 Escopo e premissas

## Escopo

| Nº | Dentro do escopo | Fora do escopo |
|---|---|---|
| 1 | Sincronização da criação, atualização e exclusão de notas | Edição colaborativa de notas (cursores compartilhados na edição simultânea) |
| 2 | Detecção e resolução de conflitos entre dispositivos | O editor dentro do dispositivo |
| 3 | API de sincronização (HTTP) | Cobrança e gerenciamento de contas |

## Premissas

- Os dispositivos se conectam apenas de forma intermitente. A edição off-line é a premissa.
- O corpo de uma nota tem 1 MB como limite máximo.
- A ordem não depende do relógio do dispositivo: quem a determina é o número de versão do servidor.
