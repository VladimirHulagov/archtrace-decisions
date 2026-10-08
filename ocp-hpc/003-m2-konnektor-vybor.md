---
id: "003"
status: accepted
type: decision
phase: 2
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Коннектор: остаться на M.2 с новой распиновкой

## Context and Problem Statement

Дискуссия с Z (Amphenol) и Raymond (TE) о разъёме и Gen7: M.2 (0.5 мм, 0.8 мм substrate) vs EDSFF/MCIO (6 мм, 1.57 мм) — компромисс плотности против готовности к Gen7; итог: остаться на M.2 с новой распиновкой, Z проверит доработку вертикального коннектора.

**Из обсуждения на встрече:**

> «M.2 (0.5 мм, 0.8 мм substrate) vs EDSFF/MCIO (6 мм, 1.57 мм) — компромисс плотности против готовности к Gen7; итог: остаться на M.2 с новой распиновкой, Z проверит доработку вертикального коннектора» — Server - HPC _ High Performance Computing - sub-project, 2026-06-09 — youtube.com/watch?v=JM8RADZ20Aw

## Considered Options

* EDSFF/MCIO
* M.2 с новой распиновкой

## Decision Outcome

Принято: M.2-дериватив (плотность), доработка под Gen7 сигналинг.

### Consequences

Итерации коннектора с Amphenol (tabs, alignment pips); SI-симуляция OCD-DIMM.

## Pros and Cons of the Options

### EDSFF/MCIO
* готов к Gen7
* 6 мм профиль — потеря плотности
### M.2 с новой распиновкой
* принято: 0.5 мм плотность
* риск SI на Gen7
