---
id: "010"
status: accepted
type: decision
phase: 3
parent: "008"
cross_refs: []
created: 2026-10-08
---

# Redriver-решение: QSFP-DD x8, 4 редрайвера, претюненный буст

## Context and Problem Statement

Конфигурация: QSFP-DD — x8, 4 редрайвера (один редрайвер = 4 дифпары), два на направление. Вопрос «кабель 0 дБ или с активным усилением» привёл к выводу: текущий редрайвер претюнится под фиксированный буст до отгрузки, без ПО-перенастройки. Терминологический спор dynamic retrain vs link trainable vs intelligent.

**Из обсуждения на встрече:**

> «Вопрос команды Raymond к Lotes: кабель должен быть «0 дБ» или с активным усилением — отсюда вывод, что текущий редрайвер претюнится под фиксированный буст до отгрузки, без ПО-перенастройки» — Server - CMS _ Composable Memory System - workstream, 2026-09-28 — youtube.com/watch?v=gSh3YD5iIvs
> «Конфигурация: QSFP-DD — x8 (by eight); 4 редрайвера, так как один редрайвер обрабатывает 4 дифпары: два на одно направление, два на обратное» — Server - CMS _ Composable Memory System - workstream, 2026-07-20 — youtube.com/watch?v=sXT22DQQwR0

## Considered Options

* Retimer (полный повторитель)
* Pretuned redriver без ПО-конфигурации
* Программируемый redriver

## Decision Outcome

Pretuned redriver: буст фиксируется до отгрузки; терминология «intelligent» уходит из спеки.

### Consequences

«Чёрный ящик» как альтернатива редрайверу запрошен у Raymond; риск — потеря гибкости под разные каналы.

## Pros and Cons of the Options

### Retimer (полный повторитель)
* гибкость, компенсация канала
* потребление/цена/латентность
### Pretuned redriver без ПО-конфигурации
* принято: дёшево и ship-ready
* канал должен быть предсказуемым
### Программируемый redriver
* универсально
* нет стандарта управления — deferred
