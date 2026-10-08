---
id: "005"
status: accepted
type: decision
phase: 2
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Охлаждение: гибридное одно-/двухфазное, negative pressure

## Context and Problem Statement

Michael Wei (Creain): cold plate с гибридным одно-/двухфазным водяным охлаждением (WIP); концепт жидкостного охлаждения модуля (двухфазное, отрицательное давление). Разводка: вход с одной стороны, вывод пара с другой, вертикальный манифольд. Bob (Mainstream) — controlled superheat direct refrigerant.

**Из обсуждения на встрече:**

> «Michael Wei, cold plate с гибридным одно-/двухфазным водяным охлаждением (WIP)» — Server - HPC _ High Performance Computing - sub-project, 2026-09-29 — youtube.com/watch?v=1xGXDqk6A5k
> «Спор о терминологии: substrate vs module vs package; «near silicon» vs NPO/NPC; предложение отказаться от имени «M.2»» — Server - HPC _ High Performance Computing - sub-project, 2026-07-21 — youtube.com/watch?v=TUqAN9j1MCQ

## Considered Options

* Однофазная вода
* Гибрид однофазной и двухфазной (negative pressure)

## Decision Outcome

Направление: гибрид; терминология substrate/module/package унифицируется.

### Consequences

Термин «M.2» предложено убрать из названия концепта.

## Pros and Cons of the Options

### Однофазная вода
* отработано
* предел плотности тепла
### Гибрид однофазной и двухфазной (negative pressure)
* высокая плотность
* сложность и безопасность
