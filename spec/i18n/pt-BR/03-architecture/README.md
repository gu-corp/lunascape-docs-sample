---
navigation:
  order: 30
---

# 3. Arquitetura

A sincronização é composta por quatro elementos: o cliente, a API de sincronização, o armazenamento e as notificações ([componentes](components.md)). [O fluxo de sincronização](sync-flow.md) mostra a ordem em que uma alteração vai do dispositivo ao servidor e do servidor aos demais dispositivos. Essa ordem se apoia nos [números de versão](versioning.md); o tratamento de duas atualizações que incidem sobre a mesma versão está definido em [resolução de conflitos](conflicts.md).
