---
id: "005"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# CMMU device-side hotness tracking в Linux (CXL 3.2)

## Context and Problem Statement

Команда делает Linux RC для CMMU по спецификации CXL 3.2: устройство само мониторит горячие страницы и сообщает Linux, который решает миграцию. Проблема старого подхода — бинарная отчётность (страница «горячая»/нет), промоция срабатывала почти только по deadlock-ам; изменён подсчёт доступа со стороны CMMU.

**Из обсуждения на встрече:**

> «Проблема прежнего подхода: бинарная отчётность (страница «горячая»/нет), из-за чего промоция срабатывала почти только по deadlock-ам. Изменён подсчёт доступа со стороны CMMU — более точный трекинг» — Server - CMS _ Composable Memory System - workstream, 2026-09-04 — youtube.com/watch?v=SHcSemLj8T8
> «Это не универсальное решение: хорошо при большом числе реально горячих страниц внутри CXL-девайса; для задачи «какой CPU к какому NUMA-узлу» существующее поведение Linux разумнее» — Server - CMS _ Composable Memory System - workstream, 2026-09-04 — youtube.com/watch?v=SHcSemLj8T8

## Considered Options

* Только Linux-эвристики (NUMA)
* Только device-side CMMU
* Оба — под разные сценарии

## Decision Outcome

Hotness tracking device-side и поведение Linux — не конкуренты: CMMU для горячих страниц внутри CXL-девайса, Linux — для CPU↔NUMA-раскладки.

### Consequences

Бенчмарк CMMU для LLM — отдельный доклад; PR в Linux RC.

## Pros and Cons of the Options

### Только Linux-эвристики (NUMA)
* универсально
* бинарная горячесть → поздняя промоция
### Только device-side CMMU
* точный трекинг
* не решает NUMA-раскладку
### Оба — под разные сценарии
* принято
* двойная реализация
