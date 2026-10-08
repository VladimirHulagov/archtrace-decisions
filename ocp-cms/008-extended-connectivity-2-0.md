---
id: "008"
status: accepted
type: decision
phase: 2
parent: "007"
cross_refs: []
created: 2026-10-08
---

# Extended Connectivity 2.0: protocol-agnostic, массовый socket

## Context and Problem Statement

Кабельное решение для вывода PCIe из сервера: опираться на самый массовый shipping socket и коннекторы (QSFP-DD / OSFP-XD), чтобы не получить нишевую кастомную кабельную систему. Draft «extended connectivity» договорились версионировать как 2.0 на базе released-версии и начать правки.

**Из обсуждения на встрече:**

> «Решение должно быть protocol-agnostic: опираться на самый массовый shipping socket и коннекторы, чтобы не получилась нишевая/кастомная кабельная система» — Server - CMS _ Composable Memory System - workstream, 2026-07-24 — youtube.com/watch?v=RatgqQYHuxQ
> «Версионирование draft «extended connectivity» — договорились назвать его 2.0 на базе текущей released-версии и начать правки, привлекая Amphenol (если возьмутся за кабели)» — Server - CMS _ Composable Memory System - workstream, 2026-06-22 — youtube.com/watch?v=rpwgZJVDL6s

## Considered Options

* Кастомный коннектор под задачу
* QSFP-DD/OSFP-XD + protocol-agnostic overlay

## Decision Outcome

Принято: spec 2.0 поверх массовых коннекторов, правки с привлечением Amphenol.

### Consequences

Демо на OCP Global через Innovation Village (без аренды стенда); нужны QSFP-DD кабели.

## Pros and Cons of the Options

### Кастомный коннектор под задачу
* оптимален электрически
* нишевая система — отвергнуто
### QSFP-DD/OSFP-XD + protocol-agnostic overlay
* принято: массовый socket = цена/доступность
* бюджет потерь требует redriver
