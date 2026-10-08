---
id: "004"
status: accepted
type: problem
phase: 2
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Roll-up вложенных подкомпонентов «превращается в кашу»

## Context and Problem Statement

Пример status dump вскрыл: GPU как subcomponent of subcomponent, который сам содержит подкомпоненты — вложенность subcomponent-in-subcomponent при чтении JSON «превращается в кашу». Дискуссия о конечных vs групповых устройствах: проблема признана, решения нет.

**Из обсуждения на встрече:**

> «Ключевая проблема, подсвеченная примером: roll-up при вложенных подкомпонентах (GPU как subcomponent of subcomponent, который сам содержит подкомпоненты)» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-06-18 — youtube.com/watch?v=Y4R-dapN8uY
> «Признано проблемой; решения пока нет — вложенность subcomponent-in-subcomponent «превращается в кашу» при чтении JSON» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-06-18 — youtube.com/watch?v=Y4R-dapN8uY

## Considered Options

* Плоский список с parent-ссылками
* Глубокая вложенность как есть

## Decision Outcome

Открыто: ищется формат, читаемый и человеком, и машиной; иерархия — физическая (см. 005).

### Consequences

Блокирует финализацию required-полей для уровней иерархии.

## Pros and Cons of the Options

### Плоский список с parent-ссылками
* легко парсить
* теряет наглядность дерева
### Глубокая вложенность как есть
* наглядно
* «каша» при чтении — отвергнуто как есть
