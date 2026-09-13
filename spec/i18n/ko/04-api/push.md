---
navigation:
  order: 20
---

# 4.2 요청과 응답

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "장보기\n- 우유\n- 달걀",
  "deviceId": "d_macbook"
}
```

응답(성공):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

응답(충돌. [3.4의 규칙](../03-architecture/conflicts.md)으로 해결한 결과를 반환한다):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "장보기\n- 우유\n- 달걀\n>>> d_iphone\n- 빵" }
```
