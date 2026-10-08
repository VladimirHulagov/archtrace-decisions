---
id: "007"
status: accepted
type: decision
phase: 3
parent: "006"
cross_refs: []
created: 2026-10-08
---

# Severity — отдельная колонка с маппингом на SEP-уровни

## Context and Problem Statement

Severity mapping: аппаратные типы ошибок и severity — разные колонки, но итоговая severity должна маппиться на SEP/seeker severities; в некоторых случаях (полное отключение питания) SEP-события нет вовсе.

**Из обсуждения на встрече:**

> «Решено: аппаратные типы ошибок и severity — разные колонки, но итоговая severity должна маппиться на SEP/seeker severities; в некоторых случаях (полное отключение питания) SEP-события нет вовсе» — HM - Hardware Fault Management - sub-project, 2026-05-08 — youtube.com/watch?v=NXq7Of3EOv0

## Considered Options

* Единое поле hardware-type→severity
* Раздельные колонки + маппинг

## Decision Outcome

Принято: раздельные колонки, маппинг на SEP-словарь.

### Consequences

Словарь severities согласуется с FMFM (Drew, cross-workstream).

## Pros and Cons of the Options

### Единое поле hardware-type→severity
* компактно
* теряет информацию — отвергнуто
### Раздельные колонки + маппинг
* принято: гибкость
* больше полей в записях
