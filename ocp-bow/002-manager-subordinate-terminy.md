---
id: "002"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Терминология: manager/subordinate вместо master/slave

## Context and Problem Statement

OCP запрещает исторические «master/slave» — нужна замена для консистентности документов. Проблема: ARM до сих пор использует master/slave повсеместно (шина APB и др.), исторические документы на этой терминологии. Пары-кандидаты: manager/subordinate vs requester/responder (ARM APB).

**Из обсуждения на встрече:**

> «Какую пару терминов принять взамен master/slave: manager/subordinate (выбрано Морганом, поддержано) vs requester/responder (ARM APB)» — Server - OCE - BOW 82347332118 - 87373664893 - sub-project, 2026-04-01 — youtube.com/watch?v=M1vsCBXlGcM

## Considered Options

* manager/subordinate
* requester/responder (ARM)

## Decision Outcome

Принято: manager/subordinate.

### Consequences

Расхождение с ARM-миром фиксируется в глоссарии; старые документы остаются как есть.

## Pros and Cons of the Options

### manager/subordinate
* принято: нейтрально и ясно
* расходится с ARM-терминологией
### requester/responder (ARM)
* совместимо с ARM
* слышится как роль протокола, не стороны
