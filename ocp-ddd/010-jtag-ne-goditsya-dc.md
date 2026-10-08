---
id: "010"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# JTAG не годится для production-диагностики ЦОД

## Context and Problem Statement

JTAG vs system-level debug: разные уровни (разработка чипа vs эксплуатация в датацентре); JTAG не годится для production DC — запреты, отсутствие security, проблема daisy chain. Вместо этого — network adapter-подход MIPI поверх стандартных транспортов.

**Из обсуждения на встрече:**

> «JTAG vs system-level debug: разные уровни (разработка чипа vs эксплуатация в датацентре); JTAG не годится для production DC (запреты, отсутствие security, проблема daisy chain)» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-04-16 — youtube.com/watch?v=fzbh2Yv8mss

## Considered Options

* JTAG-инфраструктура в проде
* MIPI debug поверх PLDM/Redfish

## Decision Outcome

Принято: production-диагностика — через MIPI/PLDM-стек; JTAG остаётся для чиповой отладки.

### Consequences

Определяет спрос на мосты (I3C/USB, PCIe) со security-слоем.

## Pros and Cons of the Options

### JTAG-инфраструктура в проде
* знакомый инструмент
* запреты, security, daisy chain — отвергнуто
### MIPI debug поверх PLDM/Redfish
* принято: управляемый и безопасный
* требует интеграции с MIPI Alliance
