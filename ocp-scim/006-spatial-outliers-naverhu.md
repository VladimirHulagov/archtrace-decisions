---
id: "006"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Spatial outlier-детекция ценнее на верхних уровнях агрегации

## Context and Problem Statement

Стратегия outlier-детекции (Panos): централизация vs распределённость. Итог обсуждения с Jim: spatial outlier-детекция (сравнение узлов между собой) ценнее на верхних уровнях агрегации — индустрия не дала хорошего решения; temporal-режим (ряд сам по себе) — на leaf.

**Из обсуждения на встрече:**

> «Итог обсуждения с Jim: spatial outlier-детекция (сравнение узлов между собой) ценнее на верхних уровнях агрегации — индустрия не дала хорошего решения, и этому стоит уделить внимание; temporal-режим…» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-07-17 — youtube.com/watch?v=sx1kw9XurK0

## Considered Options

* Temporal на всех уровнях
* Temporal на leaf, spatial на верхних уровнях

## Decision Outcome

Принято: разделение ролей по уровням.

### Consequences

Copy — модельная операция или множество потребителей: реализация свободна (zero-copy, ссылки).

## Pros and Cons of the Options

### Temporal на всех уровнях
* единообразно
* пропуск межузловых аномалий
### Temporal на leaf, spatial на верхних уровнях
* принято: адресует пробел
* две реализации
