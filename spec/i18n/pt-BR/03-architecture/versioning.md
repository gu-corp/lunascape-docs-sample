---
navigation:
  order: 30
---

# 3.3 Números de versão

O número de versão é um inteiro monotonicamente crescente que o servidor atribui a cada nota. O dispositivo envia a última versão que recebeu como `baseVersion`. Quando a versão atual do servidor não coincide com `baseVersion`, há um conflito (REQ-003). O relógio do dispositivo não é usado para determinar a ordem ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
