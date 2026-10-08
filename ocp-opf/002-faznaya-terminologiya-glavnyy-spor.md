---
id: "002"
status: accepted
type: problem
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Терминология фаз (config/reconfig, ESP/SIP/SiP) — источник споров

## Context and Problem Statement

Дискуссия о наименовании стадий (reconfig vs config): терминология фаз (ESP/SIP/SiP, config/reconfig) — главный источник споров. Итог по S3 resume: добавить текст/приложение «вне scope OpenSFI» (resume, error handling — SFI только возвращает ошибку, обработка — на хосте).

**Из обсуждения на встрече:**

> «Терминология фаз (ESP/SIP/SiP, config/reconfig) — главный источник споров» — OPF - Open Platform Firmware - project, 2026-04-09 — youtube.com/watch?v=9F5XmZZVcRk
> «Итог: добавить текст/приложение «вне scope OpenSFI» (resume, error handling — SFI только возвращает ошибку, обработка — на хосте)» — OPF - Open Platform Firmware - project, 2026-04-09 — youtube.com/watch?v=9F5XmZZVcRk

## Considered Options

* Жёсткая номенклатура фаз
* Приложение вне-scope + глоссарий

## Decision Outcome

Принято: вне-scope приложение; спор терминов живёт в глоссарии.

### Consequences

Reset API и S3 — пограничные темы приложения.

## Pros and Cons of the Options

### Жёсткая номенклатура фаз
* однозначность
* войны терминов — нет
### Приложение вне-scope + глоссарий
* принято: прагматизм
* терминологический долг
