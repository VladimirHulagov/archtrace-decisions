---
id: "005"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Нотация aggregation pipeline: BNF vs SQL-подобная vs Prometheus AST

## Context and Problem Statement

Ведущий (Broadcom): «Как выражать aggregation pipeline» (черновые слайды). Выбор нотации не решён: BNF (ведущий) vs SQL-подобная функциональная нотация, язык Prometheus и AST (Panos); договорились о нескольких «неглубоких» проработках с примерами и сравнении результатов.

**Из обсуждения на встрече:**

> «Выбор нотации не решён: BNF (ведущий) vs SQL-подобная функциональная нотация, язык PromQL и AST (Panos); договорились о нескольких «неглубоких» проработках с примерами и сравнении результатов» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-09-25 — youtube.com/watch?v=TqzSio5rm8k

## Considered Options

* BNF-грамматика
* SQL-подобная нотация
* PromQL
* AST

## Decision Outcome

Открыто: несколько shallow-проработок с примерами → сравнение.

### Consequences

Определяет DX (developer experience) всей телеметрии.

## Pros and Cons of the Options

### BNF-грамматика
* строгость
* громоздко
### SQL-подобная нотация
* знакомо
* не вся семантика выражается
### PromQL
* готовый язык
* привязка к стеку Prometheus
### AST
* машинно-точно
* не человекочитаемо
