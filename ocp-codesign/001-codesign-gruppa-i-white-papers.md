---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# AI HW/SW CoDesign: какие white papers ведёт группа

## Context and Problem Statement

Группа ведёт два главных документа 2026: «AI fabric specialization for agentic AI» (транзакционность агентных нагрузок end-to-end: compute+network+storage) и «Neuromorphic computing from co-design perspective». Scope-спор: «fabric» — только сеть или вся экосистема; итог: для конкретного стандарта критична сеть, но co-design-группа покрывает всё.

**Из обсуждения на встрече:**

> «Объём понятия «fabric»: только сеть или вся экосистема? Итог: для конкретного стандарта критична сеть, но co-design-группа покрывает всё (пример — chiplet WG, где рядом обсуждают CXL)» — Server - AI HW SW CoDesign - sub-project, 2026-08-21 — youtube.com/watch?v=274ePJUWHjQ

## Considered Options

* Фокус только на сети
* Compute + networking + storage end-to-end

## Decision Outcome

Scope расширен: всё, что решает транзакционную проблему агентного AI.

### Consequences

Два white paper параллельно; внешний collaboration-трек (UEC, ESUN, IETF, LF).

## Pros and Cons of the Options

### Фокус только на сети
* узко и глубоко
* теряем system-картину
### Compute + networking + storage end-to-end
* принято
* широкий scope размывает фокус
