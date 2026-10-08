---
id: "003"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# DDR5: счётчик ошибок общий на чип — локализацию не сделать

## Context and Problem Statement

Проблема DDR5: счёт общий на весь чип, нельзя отличить случайно распределённые ошибки (за ECC не опасны) от локализованной деградации (может дать uncorrectable). Цель — самый ранний сигнал для действия.

**Из обсуждения на встрече:**

> «Проблема DDR5: счёт общий на весь чип, нельзя отличить случайно распределённые ошибки (за ECC не опасны) от локализованной деградации (может дать uncorrectable). Цель — самый ранний сигнал для дейст…» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-07-14 — youtube.com/watch?v=mixYRaVFSGg
> «Итог: проблема сложная, спектр решений (полные error-логи, ECW-статистика); нужно продолжать искать оптимум» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-07-14 — youtube.com/watch?v=mixYRaVFSGg

## Considered Options

* Полные error-логи
* ECW-статистика
* Патентный scoreboard (Micron, DDR6)

## Decision Outcome

Открыто: спектр решений ищется; DDR6 scoreboard-предложение Micron — кандидат.

### Consequences

Без локализации — выбор между переплатой за логи и слепотой.

## Pros and Cons of the Options

### Полные error-логи
* полная картина
* объём логов на флоте
### ECW-статистика
* компактно
* частичная информация
### Патентный scoreboard (Micron, DDR6)
* адресная статистика по банкам
* новое железо DDR6
