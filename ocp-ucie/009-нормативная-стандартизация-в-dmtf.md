---
id: "009"
status: accepted
type: decision
phase: 4
parent: "008"
cross_refs: []
created: 2026-10-05
---

# Нормативная стандартизация в DMTF

## Context and Problem Statement

Куда положить SCMI-to-MCTP биндинг: (1) OCP определяет собственный vendor ID и формат — риск пересечений (прецедент: vendor ID для GPU firmware updates пересёкся с DMTF), долгосрочная поддержка на OCP; (2) OCP владеет спекой, DMTF подписывает — юридически крайне тяжело; (3) опубликовать публичную версию OCP (~0.9), подать запрос в DMTF, DMTF выпускает нормативную версию, OCP-версия становится информативной. Выбран (3). Без message type кода SCMI остаётся vendor-defined, что сужает применимость. Целевая группа — PMCI; процесс ~12-16 недель; представитель AMD в DMTF (Justin) согласился поддержать.


**Из обсуждения в чате:**

> «Опубликовать публичную версию спеки OCP (~0.9), подать в DMTF запрос, DMTF выпускает нормативную версию, а OCP-версия становится информативной — выбран этот путь — youtube.com/watch?v=UNE6V8YvIf0» — Souvik (ARM) + Dominic, Chiplet Systems, 2026-07-29
> «представитель группы в DMTF должен связаться с организацией, чтобы получить официальный message type code для протокола SCMI — youtube.com/watch?v=892Y_qEiXZM» — Dominic (Arm), Chiplet Systems, 2026-08-12

## Considered Options

* DMTF нормативно, OCP информативно
* Собственный vendor ID OCP
* Совместное владение OCP+DMTF

## Decision Outcome

Путь «OCP 0.9 → DMTF normative»; Dominic с коллегой из ARM инициируют процесс; для DMTF достаточно use case + обоснование биндинга + ссылка на OCP-спеку.

### Consequences

Биндинги на физические уровни живут у владельцев PHY: MCTP over UCIe — в UCIe-группе (у UCIe есть соглашение с DMTF, ранее не было потребности).

## Pros and Cons of the Options

### DMTF нормативно, OCP информативно

* выбрано: легитимность, отсутствие vendor-ID конфликтов

### Собственный vendor ID OCP

* отклонено: пересечения с DMTF, поддержка навсегда на OCP

### Совместное владение OCP+DMTF

* отклонено: formal collaborative agreement, legals

