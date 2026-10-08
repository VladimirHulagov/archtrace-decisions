---
id: "003"
status: accepted
type: decision
phase: 3
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Типы: number + поле unit; единицы по DSP0248

## Context and Problem Statement

Ревью JSON-схемы, сгенерированной ИИ по примеру: числовые значения (напряжения, токи) должны быть number, а не string — все «string или number» меняются на number. Для нестандартных единиц (data rate) — два поля: unit + value (integer); компьютеры поле unit могут пропускать. Latency/error rate: DSP0248 задаёт базовые единицы (seconds) + модификатор степени 10.

**Из обсуждения на встрече:**

> «Ключевое решение: числовые значения (напряжения, токи) должны быть типом number, а не string — все «string или number» меняются на number» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-07-30 — youtube.com/watch?v=xB-SvJTXCkc
> «Latency и error rate: как измерять — обсуждение перенесено; DSP0248 задаёт базовые единицы (seconds) + модификатор степени 10 (−3 для миллисекунд) — решение по этому вопросу на следующую встречу» — HM - DDD _ Datacenter Diagnostics and Debug - workstream, 2026-07-30 — youtube.com/watch?v=xB-SvJTXCkc

## Considered Options

* String-значения «как есть»
* number + unit-поле, единицы DSP0248

## Decision Outcome

Принято: number везде, unit-поле для нестандартных единиц, степени десяти по DSP0248.

### Consequences

ИИ-генерация схем допустима только с человеческим ревью типов.

## Pros and Cons of the Options

### String-значения «как есть»
* ничего не менять
* нельзя сравнивать/агрегировать
### number + unit-поле, единицы DSP0248
* принято: машинная обработка
* ревью всех полей схемы
