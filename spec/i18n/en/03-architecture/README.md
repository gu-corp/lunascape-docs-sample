---
navigation:
  order: 30
---

# 3. Architecture

Sync is built from four elements: the client, the sync API, the store and notifications ([components](components.md)). [The sync flow](sync-flow.md) shows the order in which a change travels from a device to the server, and from the server to other devices. That order rests on [version numbers](versioning.md); how the system handles two updates that land on the same version is defined in [conflict resolution](conflicts.md).
