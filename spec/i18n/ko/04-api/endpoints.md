---
navigation:
  order: 10
---

# 4.1 엔드포인트

| 메서드 | 경로 | 목적 | 요구사항 |
|---|---|---|---|
| POST | `/notes/push` | 노트의 변경을 보낸다 | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | 지정한 버전 이후의 변경을 받는다 | REQ-001 |
| DELETE | `/notes/{id}` | 노트를 삭제한다(휴지통으로) | REQ-005 |
| POST | `/notes/{id}/restore` | 휴지통에서 되돌린다 | REQ-005 |
