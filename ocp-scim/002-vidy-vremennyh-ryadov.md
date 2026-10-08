---
id: "002"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Типы временных рядов: regular / stats / event; именование

## Context and Problem Statement

CISML-модель временных рядов: типизация (regular, stats…), конвертеры между типами. Именование — ключевая проблема: reference vs start timestamp, отказ от «interval time series», термин «stats time series» предложен как новый.

**Из обсуждения на встрече:**

> «Именование как ключевая проблема модели: reference timestamp vs start timestamp, отказ от «interval time series», термин «stats time series» предложен как новый; Джим открыт к предложениям» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-05-22 — youtube.com/watch?v=MDl6C73QgwA

## Considered Options

* Единый тип ряда
* Типизация + конвертеры

## Decision Outcome

Принято: типизация рядов с конвертерами; «stats time series» как отдельный тип.

### Consequences

Конвертеры boolean(level)/event(edge) — отдельная утилита.

## Pros and Cons of the Options

### Единый тип ряда
* просто
* теряется семантика источника
### Типизация + конвертеры
* принято: точность
* нужны конвертеры
