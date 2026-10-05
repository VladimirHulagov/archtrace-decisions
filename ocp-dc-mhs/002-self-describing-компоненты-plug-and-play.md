---
id: "002"
title: "Self-describing компоненты (Plug-and-Play)"
status: accepted
type: decision
phase: 4
parent: "001"
cross_refs: []
created: 2026-10-05
---

## Контекст

Решение — self-describing компоненты: детальный discovery process (FRU Discovery spec), компоненты сами сообщают шины, устройства, регистры и JSON программной логики, чтобы BMC не знал всё a priori. Roadmap спек: 0.7 (FRU Discovery Boot + FPGA, feature complete) — конец сентября 2026; 0.9 — структурные правки и чистка языка; 1.0 — Q1/начало Q2 2027. POC: technology demonstration на APAC Summit (HP+Intel+Jabil), более полный POC на innovation village Global Summit.


**Из обсуждения в чате:**

> «Решение — self-describing компоненты: детальный discovery process (FRU Discovery spec), компоненты сами сообщают свои шины, устройства, регистры и JSON программной логики, так что BMC не должен знать всё a priori — youtube.com/watch?v=TDWUsWESO2U» — Phil Leech (HPE), DC-MHS Public, 2026-07-15


## Опции

### Option A: Self-describing + discovery

FRU Discovery spec, компоненты сообщают шины/устройства/регистры/JSON сами

### Option B: Априорные конфиги BMC

статус-кво «plug and code» — отклонено: не масштабируется на mix-and-match вендоров

## Решение

Базовый уровень plug-and-play через self-describing компоненты; BMC собирает дерево шин из JSON-описаний плат.

## Последствия

Инструмент описывает только свою плату; соединение сегментов на границе HPM/SCM — задача BMC (какие пины — I2C_0 и т.д.); пример интерпретации дадут в спеке или reference example.

