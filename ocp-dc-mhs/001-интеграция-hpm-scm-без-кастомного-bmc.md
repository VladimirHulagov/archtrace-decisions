---
id: "001"
title: "Интеграция HPM/SCM без кастомного BMC"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-05
---

## Контекст

Спеки MHS покрывают электро-механику («подключишь — не сгорит»), но программная интеграция модулей от разных вендоров требует априорного знания BMC о каждой плате: шины, устройства, регистры, FPGA-логика. Каждая комбинация HPM+SCM = ручная интеграция («plug and code»). Цель workstream Modular Plug-and-Play (лид Phil Leech, HPE, с 2024) — смешивание HPM и SCM от разных поставщиков.


**Из обсуждения в чате:**

> «Цель PnP — смешивание HPM и SCM от разных поставщиков; спеки MHS — электро-механические («подключишь — не сгорит»), но всё остальное — plug and code — youtube.com/watch?v=TDWUsWESO2U» — Phil Leech (HPE), DC-MHS Public, 2026-07-15


