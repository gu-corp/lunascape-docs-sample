---
navigation:
  order: 30
---

# 3.3 版本号

版本号是服务器为每条笔记分配的单调递增整数。设备将最后收到的版本作为 `baseVersion` 发送。当服务器的当前版本与 `baseVersion` 不一致时，即为冲突（REQ-003）。设备时钟不参与顺序的判定（[ORB-ADR-0001](../05-decisions/0001-sync-method.md)）。
