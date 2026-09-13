---
navigation:
  order: 30
---

# 3.3 版本編號

版本編號是伺服器為每則筆記採用的單調遞增整數。裝置會將最後收到的版本作為 `baseVersion` 送出。當伺服器目前的版本與 `baseVersion` 不一致時，即視為衝突（REQ-003）。裝置的時鐘不用於決定順序（[ORB-ADR-0001](../05-decisions/0001-sync-method.md)）。
