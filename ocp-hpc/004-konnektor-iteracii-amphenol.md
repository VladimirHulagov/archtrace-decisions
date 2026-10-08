---
id: "004"
status: accepted
type: decision
phase: 3
parent: "003"
cross_refs: []
created: 2026-10-08
---

# Итерации коннектора: механические tabs вместо сквозных pips

## Context and Problem Statement

Обновление M.2 коннектора от Amphenol (Z): по итогам прошлого обсуждения убраны сквозные alignment pips, вставлены mechanical tabs, поджаты «ноги». Термический анализ коннектора от Foxconn (Tim); ко-пакетированный медный коннектор Titan (Amphenol) как альтернатива — для CPC-применения нужно 112 дифпаров.

**Из обсуждения на встрече:**

> «Z не смог присутствовать, прислал слайды и 3D-модель; Alan презентовал от его имени. Правки по итогам прошлого обсуждения: убраны сквозные alignment pips, вставлены mechanical tabs, поджаты «ноги»» — Server - HPC _ High Performance Computing - sub-project, 2026-07-07 — youtube.com/watch?v=oOIkq8Jvdes
> «Продуктовая линейка Titan — высокоскоростной коннектор для mezz/cable-решений; для CPC-применения нужно 112 дифпаров» — Server - HPC _ High Performance Computing - sub-project, 2026-09-01 — youtube.com/watch?v=OEL620Fn9h4

## Considered Options

* Сквозные alignment pips
* Mechanical tabs + поджатые ноги

## Decision Outcome

Принято: tabs-конструкция; Titan (112 дифпаров) — кандидат на CPC.

### Consequences

Термоконцепт: water jacket + two-phase chamber; разводка вход/выход жидкости.

## Pros and Cons of the Options

### Сквозные alignment pips
* точно
* SI-паразиты — отвергнуто
### Mechanical tabs + поджатые ноги
* принято
* новые механические допуски
