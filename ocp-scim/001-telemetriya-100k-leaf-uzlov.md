---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# Телеметрия до 100 000+ leaf-узлов big AI ЦОД

## Context and Problem Statement

Ключевая цель SCIM — решения, масштабируемые до hyperscaler-ЦОД уровня big AI: порядка 100 000+ leaf-узлов, генерирующих телеметрию. Протоко-агностичная архитектура телеметрии с типами узлов; модель состояния leaf-узла; SysML-моделирование агрегации.

**Из обсуждения на встрече:**

> «Ключевая цель — решения, масштабируемые до hyperscaler-ЦОД уровня big AI: порядка 100 000+ leaf-узлов, генерирующих телеметрию» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-04-10 — youtube.com/watch?v=CmltCzenw7U

## Considered Options

* Тянуть всё в центр
* Протоко-агностичная модель с агрегацией по уровням

## Decision Outcome

Направление: иерархическая агрегация (metrics → bundles → super bundles), portable-блоки без привязки к месту выполнения.

### Consequences

Рождает темы: типы рядов, детекторы, нотация pipeline, spatial outliers.

## Pros and Cons of the Options

### Тянуть всё в центр
* просто
* 100k листов кладут центр
### Протоко-агностичная модель с агрегацией по уровням
* принято: масштаб
* сложная модель
