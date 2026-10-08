---
id: "002"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# HPCM-модуль: ребут концепции на Credo OmniConnect VSSR

## Context and Problem Statement

Ребут концепции HPCM-модуля на базе Credo OmniConnect VSSR: 25 модулей × 2 колонки = 50 съёмных memory-модулей; итого 10 ТБ памяти и 8 ТБ/с bandwidth на модуль. Модуль ~17 Вт (вся память+buffer), все 50 модулей ~300 Вт; full reticle XPU ~700–800 Вт; итого ~1 кВт, но термически распределённо.

**Из обсуждения на встрече:**

> «По бокам — 25 модулей × 2 колонки = 50 съёмных memory-модулей; итого 10 ТБ памяти и 8 ТБ/с bandwidth на модуль» — Server - HPC _ High Performance Computing - sub-project, 2026-05-26 — youtube.com/watch?v=3OoCQdvtXtk
> «Модуль ~17 Вт (вся память+buffer), все 50 модулей ~300 Вт; full reticle XPU ~700–800 Вт; итого ~1 кВт, но термически распределённо» — Server - HPC _ High Performance Computing - sub-project, 2026-05-26 — youtube.com/watch?v=3OoCQdvtXtk

## Considered Options

* Credo OmniConnect VSSR
* Собственная фабрика на Ethernet
* Другой D2D-вендор

## Decision Outcome

Принято: Credo VSSR как базис; 50 модулей/стойку-юнит конфигурация.

### Consequences

Зависимость от одного вендора PHY; Beachfront-спор (см. пр. 18).

## Pros and Cons of the Options

### Credo OmniConnect VSSR
* 8 ТБ/с на модуль, готовый silicon
* vendor lock
### Собственная фабрика на Ethernet
* открыто
* нет готового silicon
