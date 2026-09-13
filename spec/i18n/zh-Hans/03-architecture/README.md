---
navigation:
  order: 30
---

# 3. 架构

同步由客户端、同步 API、存储和通知这四个要素构成（[构成要素](components.md)）。变更从终端传到服务器、再从服务器传到其他终端的顺序，见[同步流程](sync-flow.md)。该顺序的依据是[版本号](versioning.md)，对同一版本的更新发生重叠时的处理方式，则由[冲突解决](conflicts.md)规定。
