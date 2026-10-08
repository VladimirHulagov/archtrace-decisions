---
id: "012"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# PIM/computational memory: стандартизация партиционирования — в SNIA

## Context and Problem Statement

Дискуссия о стандартизации PIM-интерфейсов (Pankaj, Anil, Randy): разрыв между потребностью в disaggregated memory (Google/Dell) и отсутствием CXL-решений в презентациях индустрии. Направление: SNIA SDC — стандартизация партиционирования для computational memory.

**Из обсуждения на встрече:**

> «Разрыв между потребностью в disaggregated memory (Google/Dell) и отсутствием CXL-решений в презентациях индустрии» — Server - CMS _ Composable Memory System - workstream, 2026-05-15 — youtube.com/watch?v=oEG1cNQsGuc
> «Pankaj — SNIA SDC: стандартизация партиционирования для computational memory» — Server - CMS _ Composable Memory System - workstream, 2026-09-04 — youtube.com/watch?v=SHcSemLj8T8

## Considered Options

* Стандартизовать PIM в OCP
* Партиционирование — в SNIA, OCP — системный уровень

## Decision Outcome

Партиционирование computational memory уходит в SNIA SDC; OCP держит системную оркестрацию.

### Consequences

Зависимость от сроков SNIA; программный стек (PyTorch-команда) ждёт интерфейс.

## Pros and Cons of the Options

### Стандартизовать PIM в OCP
* контроль
* дублирование SNIA
### Партиционирование — в SNIA, OCP — системный уровень
* принято: без конфликта с SDO
* внешние сроки
