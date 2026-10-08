---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# Статус-дампы компонентов разрознены — единого формата нет

## Context and Problem Statement

Диагностика ЦОД требует снимать статус-дампы с гетерогенных компонентов (NIC, NVMe, GPU, BMC), но у каждого вендора свой формат и механизм доступа. Группа DDD строит единую JSON-схему status dump и параллельный стек code currency (какие версии кода где стоят). KPI для дампов: размер, объём конфигурации, время снятия — в hyperscale-спеках уже есть.

**Из обсуждения на встрече:**

> «Контекст: в публичных hyperscale-спеках для других дампов KPI уже есть (размер, объём конфигурации, время снятия). Спорные моменты: KPI формулировать для компонента или иерархии; это shall / should…» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-09-24 — youtube.com/watch?v=2eEv_dEECZc

## Considered Options

* Остаться на вендорских форматах
* Единая JSON-схема status dump + KPI

## Decision Outcome

Направление: единая схема v1 + KPI-рекомендации (max file size, transfer time, guidance) — PR Энрико после мержа текущего.

### Consequences

Тянет за собой вопросы roll-up, единиц измерения, механизма доступа (in-band).

## Pros and Cons of the Options

### Остаться на вендорских форматах
* нулевые усилия
* невозможно коррелировать
### Единая JSON-схема status dump + KPI
* принято
* нужна дисциплина ревью (issues, PR)
