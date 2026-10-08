---
id: "002"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Улучшенный ECS / host-driven scrub для DDR6

## Context and Problem Statement

Adam (Micron, при поддержке Drew): улучшенный ECS / host-driven scrub для DDR6; интеграция с RAS API / анализаторами FMFM. Roy (LPDDR/HBM перспектива) запросил данные ECS из флота (ETC, EPRC по SKU) для поиска «golden number» порогов.

**Из обсуждения на встрече:**

> «Запросил у Adam данные ECS из fleet (ETC, EPRC по некоторым SKU) для поиска «golden number» порогов и лучшей логики мониторинга; договорились продолжить по email» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-08-11 — youtube.com/watch?v=iqiCb2u4fa0

## Considered Options

* Фиксированные пороги вендора
* Пороги из fleet-данных (golden number)

## Decision Outcome

Пороги калибруются fleet-данными (ETC/EPRC); мониторинг-логика уточняется итеративно.

### Consequences

Зависимость от SKU-специфичной статистики; результаты через RAS API.

## Pros and Cons of the Options

### Фиксированные пороги вендора
* просто
* промахи на реальных флота-х
### Пороги из fleet-данных (golden number)
* принято: точность
* нужен доступ к fleet-телеметрии
