---
id: "006"
status: accepted
type: decision
phase: 4
parent: "001"
cross_refs: []
created: 2026-10-05
---

# SCMI over MCTP over I3C

## Context and Problem Statement

Для I3C-пути принят стек SCMI → MCTP → I3C: SCMI инкапсулируется в MCTP-пакеты по DMTF-спецификации MCTP transport binding over I3C. Структура кадра: I3C-адрес + 8-битный PEC, внутри MCTP (4-байтный заголовок + payload), внутри — SCMI без перестановки полей. Эффективность инкапсуляции ~70% (оценка Arm) — приемлемо. Опирается на MIPI I3C Basic (royalty-free) — этой версии достаточно. MCTP для UCIe отвергнут ранее как избыточный (там есть собственный MTP). Инициация: IBI (In-Band Interrupt) — target уведомляет контроллер без отдельного провода.


**Из обсуждения в чате:**

> «SCMI инкапсулируется «как есть» по стандарту SCMI, без перестановки полей — «всё просто». Оценка эффективности инкапсуляции ~70% — youtube.com/watch?v=w4eTeVuy26s» — Bruno, Chiplet Systems, 2026-06-17
> «Изначально Роб предполагал использовать MCTP и для UCIe, и для I3C, но отказались: для UCIe MCTP избыточен — есть собственный MTP — youtube.com/watch?v=IXifDBAGtys» — Bruno, Chiplet Systems, 2026-06-24

## Considered Options

* SCMI → MCTP → I3C
* SCMI напрямую в I3C
* Поддержать и I²C legacy

## Decision Outcome

SCMI over MCTP over I3C; спецификация Бруно дошла до v0.7, презентована FCSA и на общем OCP-звонке («very coherent»).

SCMI over MCTP over I3C; спецификация Бруно дошла до v0.7, презентована FCSA и на общем OCP-звонке («very coherent»).

### Consequences

Все коммуникации по I3C принуждаются к MCTP (замечание Gilberto; контраргумент — future-proof, отдельные спеки для других протоколов); несколько MCTP endpoints на одном I3C-адресе должны объявлять себя MCTP-бриджем; discovery опирается на I3C enumeration + MCTP discovery.

**Из проблемы 001 (S3):** два несогласованных маппинга SCMI (Rob→UCIe, Bruno→I3C) → I3C-путь требует собственного решения (S3).

Все коммуникации по I3C принуждаются к MCTP (замечание Gilberto; контраргумент — future-proof, отдельные спеки для других протоколов); несколько MCTP endpoints на одном I3C-адресе должны объявлять себя MCTP-бриджем; discovery опирается на I3C enumeration + MCTP discovery.

## Pros and Cons of the Options

### SCMI → MCTP → I3C

* DMTF binding, ~70% эффективности, MCTP транспортно-агностичен

### SCMI напрямую в I3C

* отклонено: теряется транспортная агностичность, дублирование DMTF

### Поддержать и I²C legacy

* отклонено: MCTP over I²C опирается на SMBus ARP и polling, без IBI — «burden»
* SCMI over MCTP over I3C; спецификация Бруно дошла до v0.7, презентована FCSA и на общем OCP-звонке («very coherent»).
* Все коммуникации по I3C принуждаются к MCTP (замечание Gilberto; контраргумент — future-proof, отдельные спеки для других протоколов); несколько MCTP endpoints на одном I3C-адресе должны объявлять себя MCTP-бриджем; discovery опирается на I3C enumeration + MCTP discovery.
* **Из проблемы 001 (S3):** два несогласованных маппинга SCMI (Rob→UCIe, Bruno→I3C) → I3C-путь требует собственного решения (S3).
* ### Option A: SCMI → MCTP → I3C
* ### Option B: SCMI напрямую в I3C
* ### Option C: Поддержать и I²C legacy
* SCMI over MCTP over I3C; спецификация Бруно дошла до v0.7, презентована FCSA и на общем OCP-звонке («very coherent»).
* Все коммуникации по I3C принуждаются к MCTP (замечание Gilberto; контраргумент — future-proof, отдельные спеки для других протоколов); несколько MCTP endpoints на одном I3C-адресе должны объявлять себя MCTP-бриджем; discovery опирается на I3C enumeration + MCTP discovery.

