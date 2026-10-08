---
id: "002"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# JSON-схема status dump v1: required минимум, агрегаты опционально

## Context and Problem Statement

Схема v1 (Donald + Marco): power и temperature на уровне system убраны из required — агрегаты есть не у всех систем; проблемы температуры проявятся через healthy, детали — на уровне компонентов. Спор required vs optional для малых/дешёвых компонентов (FPGA без датчиков) решён гибкостью через описание в спеке, а не через схему.

**Из обсуждения на встрече:**

> «Power и temperature на уровне system убраны из required — агрегаты есть не у всех систем; проблемы температуры всё равно проявятся через healthy, а детали — на уровне компонентов» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-08-06 — youtube.com/watch?v=rliqOfbFK5o
> «Спор о required vs optional для power/temperature на разных уровнях иерархии: малые/дешёвые компоненты (FPGA и пр.) могут не иметь датчиков; итог — гибкость через описание в спеке, а не через схему» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-08-06 — youtube.com/watch?v=rliqOfbFK5o

## Considered Options

* Жёсткий required на всех уровнях
* Минимум required + гибкость текстом спеки

## Decision Outcome

Принято: минимум required, гибкость — текстом спецификации.

### Consequences

Генерация примеров ИИ требует ревью человеком; теги TODO и фиксация решений в документе.

## Pros and Cons of the Options

### Жёсткий required на всех уровнях
* машинная валидация
* ломает компоненты без датчиков
### Минимум required + гибкость текстом спеки
* принято
* валидация слабее
