---
id: "007"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# PCIe poison: трассировка HBM→хост ломается на IOVA

## Context and Problem Statement

Доклад о page offlining в Linux: проблема трассировки poison от HBM на PCIe-устройстве до физического адреса хоста — в TLP-заголовке только IOVA; трансляцию знает kernel, но она не экспонируется — зафиксировано как issue «PCIe → host».

**Из обсуждения на встрече:**

> «Проблема трассировки poison от HBM на PCIe-устройстве до физического адреса хоста: в TLP-заголовке только IOVA; трансляцию знает kernel, но она не экспонируется — зафиксировано как issue «PCIe → hos…» — HM - FMFM _ Fleetscale Memory Fault Management - workstream, 2026-09-22 — youtube.com/watch?v=dun8_t0NiIk

## Considered Options

* Экспонировать трансляцию kernel
* Отдельный канал отчёта устройства

## Decision Outcome

Зафиксировано как issue; решение открыто.

### Consequences

Блокирует автоматический page offlining для device-памяти (HBM).

## Pros and Cons of the Options

### Экспонировать трансляцию kernel
* полная трассировка
* интерфейс kernel↔RAS
### Отдельный канал отчёта устройства
* не трогает kernel
* вендор-специфика
