---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# KV cache инференса — главный драйвер composability памяти

## Context and Problem Statement

Сквозной вывод встреч CMS 2026: KV cache для LLM-инференса — основной потребитель памяти и главный аргумент за пулинг/шаринг CXL-памяти. Ключевой спор: CMX (GPU читает NAND напрямую, задача планирования) vs CPU-managed tiering (узкое место CPU↔GPU) и латентность NAND при промахе DRAM-cache. Развилка: одно «правильное» решение или меню опций.

**Из обсуждения на встрече:**

> «KV cache для инференса — главный драйвер памяти; спор о сравнении CMX (GPU→NAND напрямую, задача планирования) vs CPU-managed tiering (узкое место CPU↔GPU) и о латентности NAND при промахе DRAM-cach…» — Server - CMS _ Composable Memory System - workstream, 2026-06-26 — youtube.com/watch?v=7EP6YDfr3OY
> «Идея Manoj: свести в одно место все pooled/shared memory решения (XCON, Xena, Samsung, Micron — у Chandra был доклад по disaggregated NAND storage, не pooled memory) как «меню опций» для KV cache» — Server - CMS _ Composable Memory System - workstream, 2026-09-04 — youtube.com/watch?v=SHcSemLj8T8

## Considered Options

* Одно универсальное решение (CMX-подход)
* CPU-managed tiering-стек
* «Меню опций» pooled/shared решений

## Decision Outcome

Группа структурировала направление как «меню опций» для KV cache: решения разной латентности/стоимости не конкурируют, а покрывают разные trade-offs. Панель «CMS solutions for KV cache» готовится к OCP Global.

### Consequences

Бенчмарки KV cache — отдельный трек; сравнение CMX vs tiering требует white paper с топологией.

## Pros and Cons of the Options

### Одно универсальное решение (CMX-подход)
* проще стандартизовать
* латентность NAND при промахе — риск
### CPU-managed tiering-стек
* готовый софт (LMCache/Mooncake)
* узкое место CPU↔GPU
### «Меню опций» pooled/shared решений
* принято: покрывает весь спектр deployment
* нужен оркестратор выбора
