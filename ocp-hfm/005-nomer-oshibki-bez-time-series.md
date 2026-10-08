---
id: "005"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# Индустрия трактует «номер ошибки» без time-series анализа

## Context and Problem Statement

Критика подходов в индустрии: компании сообщают «номер ошибки» и делают выводы без time-series анализа; для SRAM/DRAM это «threshold approach» к radiation strikes — неточный. Drew строит time-series-поток CPER в RAS API.

**Из обсуждения на встрече:**

> «Критика подходов в индустрии: компании сообщают «номер ошибки» и делают выводы без time-series анализа; для SRAM/DRAM это «threshold approach» к radiation strikes — неточный» — HM - Hardware Fault Management - sub-project, 2026-07-24 — youtube.com/watch?v=Ev4dgeaNB6E

## Considered Options

* Threshold-подход (счётчик → порог)
* Time-series анализ потока ошибок

## Decision Outcome

Направление: time-series CPER → анализаторы → RAS API.

### Consequences

Базис для демо RAS API (shim → vendor-анализатор CER по памяти) и интеграции FMFM.

## Pros and Cons of the Options

### Threshold-подход (счётчик → порог)
* дёшево
* неточный — отвергнуто как базис
### Time-series анализ потока ошибок
* ранние признаки деградации
* нужен пайплайн и хранение
