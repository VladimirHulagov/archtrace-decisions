---
id: "007"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# MIPI debug over PLDM: Type 7 (FIFO) для данных, Type 2 для control

## Context and Problem Statement

Интеграция MIPI debug-спеков в PLDM/Redfish: рабочее предложение — данные через PLDM Type 7 (FIFO), control plane моделировать в Type 2. MIPI: детали (numeric/state/structured attribute) — на их технических обсуждениях. Ключевой концепт MIPI — «network adapter» между инфраструктурами (peek/poke, trace) и транспортами; security-слой между адаптерами и транспортом.

**Из обсуждения на встрече:**

> «Итог: рекомендация MIPI — данные через Type 7 (FIFO), control plane моделировать в Type 2; детали (numeric/state/structured attribute) — на их технических обсуждениях» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-06-11 — youtube.com/watch?v=I_ot8ICybQw
> «Рабочее предложение: использовать PLDM Type 7 для передачи данных и Type 2 для управления/контролов. Цель — к следующей встрече выработать направление для MIPP, чтобы те заложили его в требования» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-06-04 — youtube.com/watch?v=J4L-xJQ-F1o

## Considered Options

* PLDM Type 7 (FIFO) + Type 2
* Специфичный транспортный маппинг MIPI
* Физический порт/USB-мост

## Decision Outcome

Type 7 + Type 2 — рабочее направление, передано MIPI Alliance для требований.

### Consequences

Транспорт Redfish→PLDM стандартизован и предпочтителен; USB-мост требует нового firmware.

## Pros and Cons of the Options

### PLDM Type 7 (FIFO) + Type 2
* принято: reuses существующий стек
* FIFO-семантика накладывает ограничения
### Специфичный транспортный маппинг MIPI
* заточено под debug
* свой стек — дорого
### Физический порт/USB-мост
* работает без сети
* новый firmware, «camel humps» иерархий
