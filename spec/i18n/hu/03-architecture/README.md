---
navigation:
  order: 30
---

# 3. Felépítés

A szinkronizálás négy elemből áll: a kliensből, a szinkronizálási API-ból, a tárolóból és az értesítésekből ([összetevők](components.md)). A [szinkronizálás folyamata](sync-flow.md) azt a sorrendet mutatja be, amelyben egy változás eljut a készülékről a kiszolgálóra, majd a kiszolgálóról a többi készülékre. Ez a sorrend a [verziószámokon](versioning.md) alapul; azt pedig, hogy a rendszer miként kezeli az ugyanarra a verzióra érkező két frissítést, az [ütközések feloldása](conflicts.md) határozza meg.
