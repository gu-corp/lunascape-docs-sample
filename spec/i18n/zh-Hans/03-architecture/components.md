---
navigation:
  order: 10
---

# 3.1 组成部分

| 要素 | 作用 |
|---|---|
| 客户端 | 监视笔记的编辑，将变更放入队列，并在连接时发送到服务器 |
| 同步 API | 接收变更、分配版本号，并分发到其他设备 |
| 存储 | 保存每条笔记的当前内容，以及最近 30 天的历史记录 |
| 通知 | 发生变更时，向设备发送轻量信号，提示其拉取 |

```mermaid
flowchart TB
  subgraph A[设备 A]
    EA[编辑器] --> QA[队列]
  end
  subgraph B[设备 B]
    EB[编辑器] --> QB[队列]
  end
  QA -- push --> API[同步 API]
  QB -- push --> API
  API --> STORE[(存储)]
  API --> NOTIFY[通知]
  NOTIFY -. 提示拉取 .-> QA
  NOTIFY -. 提示拉取 .-> QB
```
