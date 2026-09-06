---
navigation:
  order: 30
---

# 3.3 版番号

版番号はノートごとにサーバーが採番する単調増加の整数である。端末は最後に受け取った版を `baseVersion` として送る。サーバーの現在の版と `baseVersion` が一致しないとき、競合とする（REQ-003）。端末の時計は順序の決定に用いない（[ORB-ADR-0001](../05-decisions/0001-sync-method.md)）。
