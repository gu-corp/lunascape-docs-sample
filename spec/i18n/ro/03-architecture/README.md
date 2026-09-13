---
navigation:
  order: 30
---

# 3. Arhitectura

Sincronizarea este alcătuită din patru elemente: clientul, API-ul de sincronizare, depozitul de date și notificările ([componente](components.md)). [Fluxul de sincronizare](sync-flow.md) arată ordinea în care o modificare ajunge de la un dispozitiv la server și de la server la celelalte dispozitive. Această ordine se întemeiază pe [numerele de versiune](versioning.md), iar modul de tratare a două actualizări care ajung pe aceeași versiune este stabilit în [rezolvarea conflictelor](conflicts.md).
