---
id: "004"
status: accepted
type: decision
phase: 3
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Отчётность: периодическая база + event-driven поверх

## Context and Problem Statement

Обсуждение суммаризации ошибок для JEDEC (SK hynix, LPDDR5): event-driven vs периодическая отчётность — решение: периодический режим сохраняется, event-driven добавляется поверх.

**Из обсуждения на встрече:**

> «Event-driven vs периодическая отчётность: решение — периодический режим сохраняется, event-driven добавляется поверх» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-05-05 — youtube.com/watch?v=VobTBNeRo9c

## Considered Options

* Только периодическая
* Только event-driven
* Периодическая база + event-driven надстройка

## Decision Outcome

Принято: гибрид — периодический базис не ломается, события добавляются.

### Consequences

Модель для JEDEC-предложений SK hynix; согласуется с pull-моделью HFM.

## Pros and Cons of the Options

### Только периодическая
* просто
* поздние сигналы
### Только event-driven
* быстро
* потеря базовой статистики
### Периодическая база + event-driven надстройка
* принято
* две модели потребления
