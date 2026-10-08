---
id: "003"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# UCPI: development-time (человекочитаемый) и execution-time (бинарный)

## Context and Problem Statement

Два аспекта UPCI: development time (человекочитаемый формат) и execution time (бинарный формат). Входной формат: JSON и/или YAML (конверсия тривиальна; при конверсии теряются только комментарии); решение можно отложить до экспериментов с PCS. Бинарный формат: поддержка нескольких бинарных представлений из разных сценариев.

**Из обсуждения на встрече:**

> «Требования собраны по итогам face-to-face встреч; два аспекта UPCI: development time (человекочитаемый формат) и execution time (бинарный формат)» — OPF - Open Platform Firmware - project, 2026-04-23 — youtube.com/watch?v=USHWGxPcOHc
> «Входной формат: JSON и/или YAML (конверсия тривиальна, YAML — надмножество; при конверсии теряются только комментарии). Решение по конкретному выбору можно отложить до экспериментов с PCS» — OPF - Open Platform Firmware - project, 2026-04-23 — youtube.com/watch?v=USHWGxPcOHc

## Considered Options

* Только бинарный
* JSON/YAML dev + бинарный runtime

## Decision Outcome

Принято: два представления; выбор конкретного входного формата отложен до PCS-экспериментов.

### Consequences

Формат отдельным документом (не внутри UPCI-спеки) — тенденция, финальное слово за Felix.

## Pros and Cons of the Options

### Только бинарный
* компактно
* неудобно человеку
### JSON/YAML dev + бинарный runtime
* принято: оба мира
* конверсия в пайплайне
