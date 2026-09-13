---
navigation:
  order: 30
---

# 3.3 버전 번호

버전 번호는 노트마다 서버가 부여하는 단조 증가 정수이다. 단말은 마지막으로 받은 버전을 `baseVersion`으로 보낸다. 서버의 현재 버전과 `baseVersion`이 일치하지 않을 때 충돌로 본다(REQ-003). 단말의 시계는 순서를 정하는 데 사용하지 않는다([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
