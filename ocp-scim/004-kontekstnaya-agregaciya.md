---
id: "004"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Контекстная агрегация: динамизм входов — главное отличие

## Context and Problem Statement

Panos: концепция контекстной агрегации и use cases. Спор spatial vs contextual агрегации сведён к тому, что главное отличие — динамизм входов.

**Из обсуждения на встрече:**

> «Spatial vs contextual агрегация — спор сведён к тому, что главное отличие — динамизм входов» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-04-24 — youtube.com/watch?v=m5ocAlst2kQ

## Considered Options

* Только статическая spatial
* Spatial + contextual (динамические входы)

## Decision Outcome

Принято: оба вида; динамизм входов — критерий различения.

### Consequences

Контекст задаёт окно агрегации (например, трейнинг-джоб) поверх пространственной.

## Pros and Cons of the Options

### Только статическая spatial
* просто
* не ловит джобы
### Spatial + contextual (динамические входы)
* принято
* дороже вычисления
