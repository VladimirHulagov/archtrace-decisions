---
id: "008"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Posted writes vs flow control: гарантия от переполнения буфера

## Context and Problem Statement

Основной технический спор: как гарантировать отсутствие переполнения буфера при произвольном числе posted writes, особенно на широком интерфейсе.

**Из обсуждения на встрече:**

> «Posted writes vs flow control — основной технический спор: как гарантировать отсутствие переполнения буфера при произвольном числе posted writes, особенно на широком интерфейсе» — Server - OCE - BOW 82347332118 - 87373664893 - sub-project, 2026-06-10 — youtube.com/watch?v=fuFN7vSIHsg

## Considered Options

* Кредитная модель (credits)
* Ограничение числа posted writes
* Сторожевые таймеры + retry

## Decision Outcome

Открыто: спор не закрыт в дайджесте; требует моделирования на широких конфигурациях.

### Consequences

Блокирует финализацию link-layer раздела главы 7.

## Pros and Cons of the Options

### Кредитная модель (credits)
* строгая гарантия
* накладные расходы на широких интерфейсах
### Ограничение числа posted writes
* просто
* снижает полезную пропускную
### Сторожевые таймеры + retry
* восстановление
* латентность восстановления
