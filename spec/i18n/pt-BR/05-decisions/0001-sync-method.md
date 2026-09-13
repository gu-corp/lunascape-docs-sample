---
navigation:
  order: 10
---

# ORB-ADR-0001: Adotar "versões atribuídas pelo servidor com mesclagem de três vias" como método de sincronização

| Item | Conteúdo |
|---|---|
| ID do documento | ORB-ADR-0001 |
| Versão | 1.0 |
| Data de atualização | 2026-07-01 |
| Estado | Aprovado |

## 1. Contexto

É preciso fazer convergir notas editadas offline em vários dispositivos. Havia três candidatos: (a) prevalece a última atualização pelo horário, (b) um CRDT, (c) números de versão atribuídos pelo servidor com mesclagem de três vias.

## 2. Decisão

| N.º | Decisão |
|---|---|
| 1 | A ordem é determinada pelos números de versão atribuídos pelo servidor. Não se confia no relógio dos dispositivos |
| 2 | Os conflitos são resolvidos por mesclagem de três vias; a linha que não puder ser resolvida mantém os dois lados. A prioridade é não perder conteúdo |
| 3 | O CRDT não foi adotado. As notas são curtas, não há exigência de edição simultânea e isso não compensa o custo de dobrar ou mais o tamanho do corpo do texto |

## 3. Consequências

| N.º | Consequência |
|---|---|
| 1 | O dispositivo mantém `baseVersion` e o anexa a cada envio |
| 2 | A exibição do conflito (REQ-006) passa a ser um recurso obrigatório do dispositivo |
| 3 | O servidor guarda o histórico dos últimos 30 dias (para a lixeira e como base da mesclagem de três vias) |
