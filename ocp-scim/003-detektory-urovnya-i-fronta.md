---
id: "003"
status: accepted
type: decision
phase: 3
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Детекторы: level (boolean) vs edge (event) + паттерн-детекторы

## Context and Problem Statement

Модель детекторов: boolean (level) vs event (edge) выходы — договорились о конвертирующей утилите; новая категория — детекторы паттернов. Threshold crossing alerts и threshold aggregation.

**Из обсуждения на встрече:**

> «boolean (level) vs event (edge) выходы детекторов — договорились о конвертирующей утилите» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-06-19 — youtube.com/watch?v=Gs3iWEcRWqo

## Considered Options

* Только threshold
* Палитра детекторов + конвертеры типов

## Decision Outcome

Принято: палитра детекторов, конвертация level↔edge утилитой.

### Consequences

Паттерн-детекторы — расширяемая категория модели.

## Pros and Cons of the Options

### Только threshold
* просто
* бедная семантика
### Палитра детекторов + конвертеры типов
* принято
* больше кода
