# Orbit Note Sync — Especificação funcional

| Item | Valor |
|---|---|
| ID do documento | ORB-SPEC-001 |
| Versão | 1.3 |
| Data de atualização | 2026-09-06 |
| Situação | Aprovado |
| Responsável pelo documento | Equipe Orbit (fictícia) |
| Relacionados | ORB-REQ-001 (lista de requisitos), ORB-ADR-0001 (escolha do método de sincronização) |

## Histórico de revisões

| Versão | Data | Descrição da revisão | Autor |
|---|---|---|---|
| 1.0 | 2026-07-01 | Versão inicial | Equipe Orbit |
| 1.1 | 2026-08-10 | Regras de resolução de conflitos adicionadas (3.4) | Equipe Orbit |
| 1.2 | 2026-09-06 | Tabela de erros da API adicionada (4.3) | Equipe Orbit |
| 1.3 | 2026-09-06 | Reorganização em uma pasta por capítulo | Equipe Orbit |

## Estrutura

1. [Visão geral](01-overview/README.md) — objetivo, [escopo e premissas](01-overview/scope.md), [termos](01-overview/terms.md)
2. [Requisitos](02-requirements/README.md) — [requisitos funcionais](02-requirements/functional.md), [requisitos não funcionais](02-requirements/non-functional.md), [rastreabilidade dos requisitos](02-requirements/traceability.md)
3. [Arquitetura](03-architecture/README.md) — [componentes](03-architecture/components.md), [fluxo de sincronização](03-architecture/sync-flow.md), [numeração de versões](03-architecture/versioning.md), [resolução de conflitos](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [endpoints](04-api/endpoints.md), [requisição e resposta](04-api/push.md), [erros](04-api/errors.md)
5. [Decisões de projeto](05-decisions/README.md) — [ORB-ADR-0001 Escolha do método de sincronização](05-decisions/0001-sync-method.md)

> **Sobre este documento**
> Especificação fictícia criada como exemplo de escrita para o Lunascape Docs. O produto e a empresa não existem. Serve para mostrar o uso de uma pasta por capítulo, tabelas, diagramas (Mermaid), código e traduções.
