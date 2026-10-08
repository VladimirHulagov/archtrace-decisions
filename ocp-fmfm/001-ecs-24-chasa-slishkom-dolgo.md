---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# ECS раз в 24 часа слишком редко для RCA памяти

## Context and Problem Statement

Ключевая проблема: интервал ECS раз в 24 часа слишком велик, информации о состоянии DRAM через ECS недостаточно; цель — эффективный RCA памяти, митигация отказов в рантайме и оценка качества флота. Дрю ранее продвигал 24-часовой patrol scrub — период корректен для soft errors, но для деградации нужен более ранний сигнал.

**Из обсуждения на встрече:**

> «Ключевая проблема: интервал ECS раз в 24 часа слишком велик и информации о состоянии DRAM через ECS недостаточно; цель — эффективный RCA памяти, митигация отказов в рантайме и оценка качества флота» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-05-19 — youtube.com/watch?v=l5fp3jXl72w
> «Сам Drew ранее (в Intel/HP) продвигал 24-часовой patrol scrub — период скраббинга корректен и достаточен, чтобы вычищать soft errors и не влиять на производительность» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-05-08 — youtube.com/watch?v=NXq7Of3EOv0

## Considered Options

* Оставить 24-часовой ECS
* Адаптивное сканирование областей по указанию хоста
* Host-driven scrub

## Decision Outcome

Направление: адаптивный host-driven scrub (Adam/Micron DDR6) поверх периодического ECS.

### Consequences

Рождает линейку: DDR5 общий счётчик, LPDDR7 chipkill, golden number порогов.

## Pros and Cons of the Options

### Оставить 24-часовой ECS
* нулевые усилия
* поздний сигнал деградации
### Адаптивное сканирование областей по указанию хоста
* ранний сигнал
* нагрузка на контроллер
### Host-driven scrub
* принято: хост знает workload
* требует ECS-данных из флота
