---
id: "005"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# LPDDR7: цель — приблизиться к chipkill

## Context and Problem Statement

Обновление по комитету данных JEDEC (LPDDR RAS, Anil/Meta): LPDDR7 — цель приблизиться к chipkill (в LPDDR6 chipkill уровня ×4 DIMM недостижим). Проблема — сформулировать problem statement от имени server fleet operators, сохранив economies of scale.

**Из обсуждения на встрече:**

> «Итог: LPDDR7 — цель приблизиться к chipkill (в LPDDR6 chipkill уровня ×4 DIMM недостижим). Проблема — сформулировать problem statement от имени server fleet operators, сохранив economies of scale» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-06-16 — youtube.com/watch?v=eNKvkrOxsYM

## Considered Options

* Считать, что LPDDR не для серверов
* Problem statement JEDEC + RAS-фичи LPDDR7

## Decision Outcome

Осиный путь: LPDDR7 приближается к server-grade RAS через JEDEC-канал.

### Consequences

Компромисс с economies of scale (LPDDR — массовый мобильный продукт).

## Pros and Cons of the Options

### Считать, что LPDDR не для серверов
* нет работы
* теряем рынок LPDDR-серверов
### Problem statement JEDEC + RAS-фичи LPDDR7
* принято: системный голос
* долгий JEDEC-цикл
