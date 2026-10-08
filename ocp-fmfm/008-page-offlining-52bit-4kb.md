---
id: "008"
status: accepted
type: decision
phase: 3
parent: "007"
cross_refs: []
created: 2026-10-08
---

# Page offlining: допущение 52-битного физадреса, страницы 4 КБ

## Context and Problem Statement

Для page offlining в RAS API endpoint принято допущение: 52-битное физическое адресное пространство (типично для ARM/AMD/Intel) и страницы 4 КБ для простоты; huge pages можно закодировать отдельно.

**Из обсуждения на встрече:**

> «Для page offlining принято допущение: 52-битное физическое адресное пространство (типично для ARM/AMD/Intel) и страницы 4 КБ для простоты; huge pages можно закодировать отдельно» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-09-22 — youtube.com/watch?v=dun8_t0NiIk

## Considered Options

* Поддержка всех размеров страниц сразу
* 4 КБ базис + отдельное кодирование huge

## Decision Outcome

Принято: 4 КБ базис, huge pages отдельно.

### Consequences

Упрощает первый релиз endpoint; huge-страницы — расширение.

## Pros and Cons of the Options

### Поддержка всех размеров страниц сразу
* универсально
* сложно и долго
### 4 КБ базис + отдельное кодирование huge
* принято: быстро
* требует later-расширения
