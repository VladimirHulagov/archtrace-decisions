---
id: "004"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# MCP + A2A: композируются, а не конкурируют

## Context and Problem Statement

A2A — открытый протокол поверх HTTP с JSON-RPC 2.0 (тот же транспорт, что MCP), поддерживает стриминг (SSE). Соотношение MCP и A2A: вертикаль vs горизонталь, общий транспорт JSON-RPC/HTTP, композируются, а не заменяют друг друга.

**Из обсуждения на встрече:**

> «Соотношение MCP и A2A: вертикаль vs горизонталь, общий транспорт JSON-RPC/HTTP, композируются, а не заменяют друг друга» — Server - AI HW SW CoDesign - sub-project, 2026-05-29 — youtube.com/watch?v=eXS9BBAKO8A
> «A2A — открытый протокол: открытая публикация и управление, работает поверх HTTP с JSON-RPC 2.0 (тот же транспорт, что MCP), поддерживает стриминг (server-sent events)» — Server - AI HW SW CoDesign - sub-project, 2026-05-29 — youtube.com/watch?v=eXS9BBAKO8A

## Considered Options

* Один протокол на всё
* MCP (вертикаль) + A2A (горизонталь)

## Decision Outcome

Принято: композируемая пара — MCP для инструментария, A2A для межагентных связей.

### Consequences

Вопрос: умеет ли MCP dynamic discovery и capability matching вместо фиксированного графа оркестрации — зависит от протокольного слоя.

## Pros and Cons of the Options

### Один протокол на всё
* просто
* не покрывает обе оси
### MCP (вертикаль) + A2A (горизонталь)
* принято: полнота
* два стека для агентов
