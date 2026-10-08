---
id: "007"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Жидкостное охлаждение: тип решения нужен в boot-time

## Context and Problem Statement

Точка решения — boot-time execution, передача от host firmware: «правильная группа для этого». Предложение: если бы OpenSFI/BIOS сообщал «single-phase / two-phase / air cooling», это сняло бы пробле…

**Из обсуждения на встрече:**

> «Точка решения — boot-time execution, передача от host firmware: «правильная группа для этого». Предложение: если бы OpenSFI/BIOS сообщал «single-phase / two-phase / air cooling», это сняло бы пробле…» — OPF - Open Platform Firmware - project, 2026-06-04 — youtube.com/watch?v=1zooRC-rWcA

## Considered Options

* Определять охлаждение рантаймом
* Декларация типа охлаждения в firmware

## Decision Outcome

Направление: декларация в firmware (single-phase/two-phase/air).

### Consequences

Прямая связь с HPC-группой (двухфазное охлаждение модулей) и liquid cooling трендом.

## Pros and Cons of the Options

### Определять охлаждение рантаймом
* гибко
* поздно для thermal budget
### Декларация типа охлаждения в firmware
* принято: рано и точно
* ещё одно поле конфигурации
