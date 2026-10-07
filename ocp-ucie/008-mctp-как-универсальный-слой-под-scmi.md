---
id: "008"
status: accepted
type: decision
phase: 4
parent: "006"
cross_refs: []
created: 2026-10-05
---

# MCTP как универсальный слой под SCMI

## Context and Problem Statement

Альтернатива Rob — SCMI напрямую в UCIe минуя MCTP (сейчас нет способа попасть в UCIe через MCTP; есть неиспользованное соглашение UCIE–DMTF, Rob готов его «запустить», возможно волонтёрством). Обсуждение показало преимущество архитектуры «SCMI → всегда MCTP → биндинги ниже»: SCMI остаётся агностичен к транспорту (I3C, UCIe sideband/mainband), не нужны новые shim-слои и правки спеки. Bruno (автор альтернативы) согласен отозвать предложение, если оно усложняет.


**Из обсуждения в чате:**

> «Итог: направление — MCTP как универсальный слой, пока не встретим roadblock; Rob выяснит наличие реальных препятствий в UCIE-стандарте — youtube.com/watch?v=UNE6V8YvIf0» — Rob + Bruno, Chiplet Systems, 2026-07-29

## Considered Options

* SCMI → всегда MCTP → биндинги
* SCMI напрямую в UCIe

## Decision Outcome

Направление — MCTP как универсальный слой, пока не встретим roadblock; Rob выясняет наличие препятствий в UCIe-стандарте; отдельный документ маппинга MCTP over UCIe делать в UCIe-группе (шаблон есть).

### Consequences

Раздел UCIe в основном документе перерабатывается (в текущей версии нет MCTP); фундамент MCTP-over-UCIe нужен до финализации основного документа.

## Pros and Cons of the Options

### SCMI → всегда MCTP → биндинги

* единая архитектура, транспортная агностичность

### SCMI напрямую в UCIe

* отозвано Bruno/Rob: новые shim-слои, правки спеки UCIe

