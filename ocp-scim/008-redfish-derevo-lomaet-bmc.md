---
id: "008"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Сбор всего Redfish-дерева может «положить» BMC

## Context and Problem Statement

Bis: попытка собрать все данные из Redfish-дерева может «положить» BMC у ряда крупных вендоров — cost of collecting каждого бита суммируется в операционные накладные расходы.

**Из обсуждения на встрече:**

> «Bis: попытка собрать все данные из Redfish-дерева может «положить» BMC у ряда крупных вендоров — cost of collecting каждого бита суммируется в операционные накладные расходы» — HM - SCIM _ Scalable Cloud Infrastructure Management - sub-project, 2026-06-19 — youtube.com/watch?v=Gs3iWEcRWqo

## Considered Options

* Собирать всё Redfish-дерево
* Избирательный сбор по модели детекторов

## Decision Outcome

Аргумент за SCIM-модель: избирательный сбор, детекторы на leaf.

### Consequences

Мотивирует протоко-агностичность (не только Redfish).

## Pros and Cons of the Options

### Собирать всё Redfish-дерево
* полнота
* кладёт BMC — отвергнуто
### Избирательный сбор по модели детекторов
* принято: живые BMC
* нужна модель что собирать
