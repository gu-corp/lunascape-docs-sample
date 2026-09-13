---
navigation:
  order: 40
---

# 3.4 Resolução de conflitos

| Caso | Regra |
|---|---|
| A mesma linha foi alterada separadamente | As duas alterações são mantidas: a que chegou depois é acrescentada ao final, separada por `>>>`. O usuário vê a indicação de conflito (REQ-006) |
| Linhas diferentes foram alteradas | São integradas automaticamente por uma mesclagem de três vias. O usuário não é avisado |
| Um dos lados excluiu | A exclusão tem prioridade, e o conteúdo do outro lado vai para a lixeira (REQ-005) |

Em todos os casos, nenhum conteúdo é perdido (REQ-004).
