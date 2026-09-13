---
navigation:
  order: 10
---

# 2.1 Requisitos funcionais

| ID | Requisito | Prioridade | Verificação |
|---|---|---|---|
| REQ-001 | Uma nota criada em um dispositivo chega aos outros dispositivos em até 10 segundos após a conexão | Obrigatório | Teste de integração |
| REQ-002 | Uma nota editada offline é enviada automaticamente na reconexão | Obrigatório | Teste de integração |
| REQ-003 | Duas atualizações da mesma versão são detectadas como conflito | Obrigatório | Teste unitário |
| REQ-004 | Um conflito é resolvido automaticamente pelas [regras da seção 3.4](../03-architecture/conflicts.md), sem perder o conteúdo de nenhum dos lados | Obrigatório | Teste unitário |
| REQ-005 | Uma exclusão é propagada aos outros dispositivos e pode ser restaurada da lixeira por 30 dias | Recomendado | Teste de integração |
| REQ-006 | O dispositivo pode exibir o estado da sincronização (sincronizado, enviando, com conflito) | Recomendado | Inspeção visual |
