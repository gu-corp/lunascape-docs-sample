---
navigation:
  order: 40
---

# 3.4 Ütközések feloldása

| Eset | Szabály |
|---|---|
| Ugyanazt a sort egymástól függetlenül módosították | Mindkét módosítás megmarad: a később érkezett a végére kerül, `>>>` jellel elválasztva. A készülék ütközést jelez (REQ-006) |
| Különböző sorokat módosítottak | Háromutas egyesítéssel automatikusan összevonja; a felhasználó nem kap értesítést |
| Az egyik fél törölte a jegyzetet | A törlés az erősebb, a másik fél tartalma a kukába kerül (REQ-005) |

Egyik esetben sem vész el tartalom (REQ-004).
