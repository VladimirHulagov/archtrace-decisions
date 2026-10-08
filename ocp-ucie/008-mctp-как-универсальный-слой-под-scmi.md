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


**Кросс-упоминания из других воркстримов:**

> «Сценарии: inband log export to USB, PLDM inband, log into the host, outband. - Открытый вопрос: какой сторонний список vendor ID использовать. Ранее расходились в обсуждении; кандидат — **IANA Private Enterprise Number (PEN)**, он используется в MCTP и в IPMI FRU data; альтернатива — PCI vendor ID. - Решение по духу MCTP base spec: в vendor-defined message types MCTP есть 8-битный идентификатор me…» — HM - DDD _ Datacenter Diagnostics and Debug - workstrea, 2026-05-07 — youtube.com/watch?v=XnZCKWrW0EU
> «**3. Дискуссия: определения in-band / out-of-band (Остин):** - Текущее определение in-band в спеке привязано к сетевому доступу, но в DMTF (MCTP) in-band — это код, исполняющийся в host OS и обращающийся к устройству напрямую (например, по PCI-шве), без host-сети Ethernet; при этом MCTP и Redfish определяют термины по-разному. - Уточнение: в спеке термины используются 14 раз, в основном в информат…» — HM - DDD _ Datacenter Diagnostics and Debug - workstrea, 2026-09-24 — youtube.com/watch?v=2eEv_dEECZc


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

