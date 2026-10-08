---
id: "008"
status: accepted
type: problem
phase: 2
parent: "006"
cross_refs: []
created: 2026-10-08
---

# Чиплеты: fault management не определён

## Context and Problem Statement

White paper по chiplet fault management (Drew + Savvita): рисунки, таблица use cases, артефакты инжектирования. Гость ARM (Hashim) спросил, покрывает ли фреймворк чиплеты; его white paper по RAS просмотрен Drew без замечаний — предложено опубликовать.

**Из обсуждения на встрече:**

> «Гость-спикер (ARM, Hashim) спросил, покрывает ли фреймворк chiplet'ы; упомянул свой white paper по RAS — Drew его просмотрел, проблем не нашёл, предложил опубликовать» — HM - Hardware Fault Management - sub-project, 2026-06-12 — youtube.com/watch?v=SjHYwJfsSfE

## Considered Options

* Каждый чиплет — «компонент» с полным FM
* Модель границ пакета (package boundary)

## Decision Outcome

Открыто: white paper фиксирует use cases; интерфейс FM чиплета — на проработке.

### Consequences

Связь с FCSA-экосистемой (границы ответственности вендоров чиплетов).

## Pros and Cons of the Options

### Каждый чиплет — «компонент» с полным FM
* гранулярно
* взрыв сложности
### Модель границ пакета (package boundary)
* соответствует FCSA
* внутренности чиплета невидимы
