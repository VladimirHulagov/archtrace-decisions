---
id: "006"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# CXL+SSD гибрид «Infinite Memory» (MX1)

## Context and Problem Statement

Разрыв DRAM↔NAND по ёмкости/стоимости/латентности: DRAM дорогая и в дефиците; CXL — байт-адресуемая, NAND — блочная, нужен мост. Решение Xina (Harry Kim): устройство MX1 — CXL memory expander с 4 каналами DDR5 (CXL 3.x), тысячи RISC-V ядер на контроллере как вычислительный ресурс гибрида.

**Из обсуждения на встрече:**

> «Проблема: большой разрыв между DRAM и NAND flash по ёмкости, стоимости и латентности; DRAM дорогая и в дефиците. CXL — байт-адресуемая память, NAND — блочное устройство, нужен мост между медиа» — Server - CMS _ Composable Memory System - workstream, 2026-09-11 — youtube.com/watch?v=cBBhinFRL0g

## Considered Options

* Только DRAM+CXL (без NAND-тира)
* Гибрид CXL-контроллер + NAND с compute на борту

## Decision Outcome

Гибридный мост принят как кандидат «меню опций»: байт-адресуемая шапка над блочным NAND.

### Consequences

Латентность моста — ключевой вопрос для KV; сравнение с CMX (GPU→NAND напрямую).

## Pros and Cons of the Options

### Только DRAM+CXL (без NAND-тира)
* проще
* дорогая ёмкость
### Гибрид CXL-контроллер + NAND с compute на борту
* тысячи RISC-V ядер делают мост прозрачным
* новое железо — риск зрелости
