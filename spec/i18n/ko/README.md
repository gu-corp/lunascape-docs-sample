# Orbit 노트 동기화 서비스 기능 사양서

| 항목 | 내용 |
|---|---|
| 문서 ID | ORB-SPEC-001 |
| 판 | 1.3 |
| 갱신일 | 2026-09-06 |
| 상태 | 승인됨 |
| 문서 책임자 | Orbit 개발팀(가상) |
| 관련 | ORB-REQ-001(요건 목록), ORB-ADR-0001(동기화 방식 선정) |

## 개정 이력

| 판 | 날짜 | 개정 내용 | 개정자 |
|---|---|---|---|
| 1.0 | 2026-07-01 | 초판 | Orbit 개발팀 |
| 1.1 | 2026-08-10 | 충돌 해결 규칙 추가(3.4) | Orbit 개발팀 |
| 1.2 | 2026-09-06 | API 오류 표 추가(4.3) | Orbit 개발팀 |
| 1.3 | 2026-09-06 | 장별 폴더 구성으로 변경 | Orbit 개발팀 |

## 구성

1. [개요](01-overview/README.md) — 목적, [범위와 전제](01-overview/scope.md), [용어](01-overview/terms.md)
2. [요건](02-requirements/README.md) — [기능 요건](02-requirements/functional.md), [비기능 요건](02-requirements/non-functional.md), [요건 추적](02-requirements/traceability.md)
3. [구성](03-architecture/README.md) — [구성 요소](03-architecture/components.md), [동기화 흐름](03-architecture/sync-flow.md), [판 번호](03-architecture/versioning.md), [충돌 해결](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [엔드포인트](04-api/endpoints.md), [요청과 응답](04-api/push.md), [오류](04-api/errors.md)
5. [설계 판단](05-decisions/README.md) — [ORB-ADR-0001 동기화 방식 선정](05-decisions/0001-sync-method.md)

> **이 문서에 대하여**
> Lunascape Docs의 작성 방법을 보여 주는 예로 만든 가상의 사양서입니다. 제품과 회사는 실재하지 않습니다. 장별 폴더, 표, 다이어그램(Mermaid), 코드, 번역의 사용법을 보기 위한 것입니다.
