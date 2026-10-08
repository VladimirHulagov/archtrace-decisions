---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# Memory capacity/bandwidth trade-off для GenAI инференса

## Context and Problem Statement

Алан (ведущий): «Breaking the memory capacity/bandwidth trade-off for GenAI inference» — подготовка к OCP Summit. Разрыв между ёмкостью и полосой памяти: AI-инференс memory-bound, HBM дорог и ограничен. Обзор трендов: OpenAI Jalapeno, Nvidia Rubin Ultra, Groq, SemiAnalysis о сети как узком месте.

**Из обсуждения на встрече:**

> «Alan, «Breaking the memory capacity/bandwidth trade-off for agentic inference» (подготовка к OCP Summit, слайд…» — Server - HPC _ High Performance Computing - sub-project, 2026-09-01 — youtube.com/watch?v=OEL620Fn9h4

## Considered Options

* Больше HBM в пакете
* Вынести память из пакета модулями

## Decision Outcome

Направление: съёмные memory-модули (HPCM) с дешёвой памятью + скоростная фабрика.

### Consequences

Рождает линию: коннектор, охлаждение, питание шасси, 3D-стекинг прогноз.

## Pros and Cons of the Options

### Больше HBM в пакете
* максимальная полоса
* цена/тепло/reticle лимит
### Вынести память из пакета модулями
* принято: масштаб ёмкости
* нужна фабрика и коннекторы
