---
navigation:
  order: 10
---

# ORB-ADR-0001: Alegerea metodei de sincronizare „versiuni atribuite de server și îmbinare în trei direcții”

| Element | Conținut |
|---|---|
| ID document | ORB-ADR-0001 |
| Versiune | 1.0 |
| Data actualizării | 2026-07-01 |
| Stare | Aprobat |

## 1. Context

Notele editate offline pe mai multe dispozitive trebuie să conveargă. Au fost luate în considerare trei variante: (a) câștigă ultima modificare după marcajul de timp, (b) un CRDT, (c) numere de versiune atribuite de server și îmbinare în trei direcții.

## 2. Decizie

| Nr. | Decizie |
|---|---|
| 1 | Ordinea este stabilită de numerele de versiune atribuite de server. Ceasul dispozitivului nu este considerat de încredere |
| 2 | Conflictele se rezolvă prin îmbinare în trei direcții, iar liniile care nu pot fi rezolvate păstrează ambele variante. Prioritatea este să nu se piardă conținut |
| 3 | CRDT nu se adoptă: notele sunt scurte, nu există cerința de editare simultană, iar dublarea sau mai mult a dimensiunii textului nu justifică acest cost |

## 3. Consecințe

| Nr. | Consecință |
|---|---|
| 1 | Dispozitivul păstrează `baseVersion` și îl atașează la fiecare trimitere |
| 2 | Afișarea conflictelor (REQ-006) devine o funcție obligatorie a dispozitivului |
| 3 | Serverul păstrează istoricul ultimelor 30 de zile (pentru coșul de gunoi și ca bază pentru îmbinarea în trei direcții) |
