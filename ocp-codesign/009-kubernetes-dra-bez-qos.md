---
id: "009"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Kubernetes DRA: нет QoS-характеристик при выборе устройств

## Context and Problem Statement

Google (John): Kubernetes Dynamic Resource Allocation (DRA) для AI/ML — нет QoS-характеристик при альтернативном выборе устройств (2×40GB vs 1×80GB — латентность 4×L4 сильно выше) — решение остаётся за автором workload.

**Из обсуждения на встрече:**

> «Нет QoS-характеристик при альтернативном выборе устройств (2×40GB vs 1×80GB — латентность 4×L4 сильно выше) — решение остаётся за автором workload» — Server - AI HW SW CoDesign - sub-project, 2026-04-17 — youtube.com/watch?v=MkzUyuQLHpk

## Considered Options

* Оставить выбор автору workload
* QoS-дескрипторы устройств в DRA

## Decision Outcome

Зафиксирован пробел; кандидат в требования white paper.

### Consequences

Пересечение с CMS (оркестрация pooled ресурсов в K8s).

## Pros and Cons of the Options

### Оставить выбор автору workload
* как есть
* субоптимальные выборы
### QoS-дескрипторы устройств в DRA
* осознанный выбор
* требует upstream K8s
