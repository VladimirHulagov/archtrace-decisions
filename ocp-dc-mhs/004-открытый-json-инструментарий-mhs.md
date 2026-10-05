---
id: "004"
title: "Открытый JSON-инструментарий MHS"
status: accepted
type: decision
phase: 4
parent: "002"
cross_refs: []
created: 2026-10-05
---

## Контекст

Инструменты для снижения барьера внедрения: FRU Packaging Tool (DSP0220 DMTF, место под подпись; выпущен) и JSON Validator (схема + кросс-ссылки секций, вклад Intel; выпущен) — оба на wiki; FPGA JSON File Creation Tool (двухфазный, обкатан с Xilinx/Lattice/Alter внутри HPE) — к Global Summit; Netlist-to-JSON (Cadence/Allegro → JSON; ключ к конвенциям именования netlist и нумерации шин I2C_0/I2C_1) — в разработке; JSON-to-Linux Device Tree — в планах, низкий приоритет. Lattice подписала MHS CLA; контрибуция их interpreter-инструмента — решение Lattice (IP), возможно просто демо на Summit.


**Из обсуждения в чате:**

> «Инструменты: два выпущены на wiki (FRU image packaging tool для HPM; JSON validator для схем), один в прогрессе, два в разработке — youtube.com/watch?v=9YcQS9tiPeY» — Brian (MHS), Server project, 2026-07-22
> «Критичны конвенция именования netlist и консистентная нумерация шин (I2C_1/I2C_0, единый префикс у относящихся к шине цепей) — youtube.com/watch?v=TDWUsWESO2U» — Phil Leech (HPE), DC-MHS Public, 2026-07-15


## Решение

Открытый toolchain из 5 инструментов под self-describing JSON; форки и PR приветствуются, мейнтейнеры HPE/Intel.

## Последствия

Функциональность JSON Validator может быть частично влита в другие инструменты; device tree tool может не успеть к Global Summit.

