---
id: "002"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Путь данных KV-тиринга — задача tiering-софта, не стандарта

## Context and Problem Statement

Выбор пути KV cache между тирами (host DRAM / CXL / NAND) делают существующие инструменты: LMCache, Mooncake, vLLM KV connector, NVIDIA Dynamo (NIXL). CXL-память «прятана» в блоке DRAM и может пулиться; решений pooled-памяти в host-части в проде не видно (Meta, Nilesh).

**Из обсуждения на встрече:**

> «Выбор пути — задача tiering-софта (LMCache, Mooncake, vLLM KV connector, Nvidia Dynamo); CXL-память «спрятана» в блоке DRAM и может быть pooled. Пулед-память в host — пока не видел решений» — Server - CMS _ Composable Memory System - workstream, 2026-08-19 — youtube.com/watch?v=lyw048uUPwg

## Considered Options

* Фиксировать путь в спеке CMS
* Оставить выбор tiering-софту

## Decision Outcome

Путь данных не стандартизуется: CMS даёт пул, маршрутизацию делают LMCache/Mooncake/Dynamo.

### Consequences

Критичны бенчмарки и «авторитетные» рецепты интеграции (запрос Grant).

## Pros and Cons of the Options

### Фиксировать путь в спеке CMS
* единообразие
* ломает существующие стеки
### Оставить выбор tiering-софту
* принято: не ломает экосистему
* запрошены бенчмарки/рецепты
