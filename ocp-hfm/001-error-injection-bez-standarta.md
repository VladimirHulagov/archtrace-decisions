---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# Error injection: у каждого вендора свой ad-hoc механизм

## Context and Problem Statement

Проверка RAS-логики требует контролируемого внесения ошибок, но стандарта нет — вендоры делают по-своему, гипертскалеры не могут единообразно тестировать флот. Группа HFM пишет документ по error injection: таксономия, behavior, security, outcomes.

**Из обсуждения на встрече:**

> «Основной спор: точность флага injected-ошибок (только инжектированные) vs простота глобального флага режима — разрешён компромиссом «нормативно просто, информативно точно, поэтапно»» — HM - Hardware Fault Management - sub-project, 2026-04-24 — youtube.com/watch?v=ejManGe_-RY

## Considered Options

* Вендорские механизмы как есть
* Стандартизованная таксономия и API инжекции

## Decision Outcome

Направление: единый документ error injection с таксономией, behavior-разделом, security и outcomes.

### Consequences

Тянет security-раздел (аутентификация, распознаваемость), мультитенантность и аудит.

## Pros and Cons of the Options

### Вендорские механизмы как есть
* нулевые усилия
* флот-тестирование невозможно
### Стандартизованная таксономия и API инжекции
* единые тесты флота
* долгий консенсус
