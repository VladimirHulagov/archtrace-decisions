---
id: "004"
title: "SCMI → UMAP → MTP (UCIe)"
status: accepted
type: decision
phase: 4
parent: "003"
cross_refs: []
created: 2026-10-05
---

## Контекст

Маппинг на UCIe: SCMI делится на protocol/command, инкапсулируется в UMAP (memory access wrapper: адрес, byte enables), затем в MTP (маршрутизация: destination address, traffic classes). Есть варианты MTP-инкапсуляции для sideband и mainband — SCMI-уровню неважно, каким путём доставлено. Иерархия пакета: заголовок MTP → UMAP (заголовок) → SCMI payload. Маршрутизация: адреса per endpoint, глобальны только source/destination ID (единственные глобальные определения UCIe на весь SiP); транзитные пакеты проходят без терминирования.


**Из обсуждения в чате:**

> «SCMI делится на protocol и command; они инкапсулируются в UCIe UMAP, затем в UCIe MTP. Есть отдельные варианты для sideband и mainband — youtube.com/watch?v=g0zTysNyd2k» — Rob (AMD), Chiplet Systems, 2026-04-15
> «типичный SCMI-памят ~128 байт; заголовки — 5 double words (2 MTP + 3 UMAP) = 40 байт; итого 168 байт ≈ ~10% оверхеда — youtube.com/watch?v=NH4Z99vPkGc» — Gil + Bruno, Chiplet Systems, 2026-04-22


## Решение

Инкапсуляция SCMI в UMAP/MTP; структура пакета агностична к интерфейсу; заголовки пока не оптимизируются.

## Последствия

Оверхед заголовков ~40 байт (5 double words: 2 MTP + 3 UMAP) на типичный SCMI-мессадж 128 байт (~10% по оценке Bruno); control plane агностичен к внутренним шинам чиплета (AXI/CHI/custom), data plane требует бриджей.

