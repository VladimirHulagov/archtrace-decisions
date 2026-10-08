---
id: "009"
status: accepted
type: decision
phase: 2
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Метрики → бандлы → супербандлы: иерархия экспорта

## Context and Problem Statement

Data pipelining: time series, bundle, super bundle; source ranking и «putting it together» — три вида агрегации (temporal, spatial, contextual) в одной рамке.

**Из обсуждения на встрече:**

> «Джим, метрики → бандлы → супербандлы: иерархия экспорта» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-08-14 — youtube.com/watch?v=ZRRRgy_faic

## Considered Options

* Плоский экспорт метрик
* Иерархия bundles/super bundles

## Decision Outcome

Принято: иерархическая упаковка для масштаба 100k+.

### Consequences

Требует конвертеров типов рядов и детекторов (см. 002–003).

## Pros and Cons of the Options

### Плоский экспорт метрик
* просто
* шторм на верхнем уровне
### Иерархия bundles/super bundles
* принято: масштаб
* слои упаковки
