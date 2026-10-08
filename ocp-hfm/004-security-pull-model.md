---
id: "004"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Security инжекции: pull-модель, queryable state, без auto-relock

## Context and Problem Statement

Аутентификация режима инжекции и распознаваемость: читать состояние unlocked/locked может кто угодно — проблемы безопасности нет; notifications (push) не нужны, модель pull. Автоматического relock по таймауту нет — осознанное решение; основной риск unlocked-состояния в клиентской среде — denial of service и лишние замены частей.

**Из обсуждения на встрече:**

> «Итог: читать состояние unlocked/unlocked может кто угодно — проблемы безопасности нет; notifications (push) не нужны, модель pull. Комментарий в документе закрыт» — HM - Hardware Fault Management - sub-project, 2026-09-11 — youtube.com/watch?v=WVspbnJOSnQ
> «Нет автоматического relock по таймауту — осознанное решение; важно, что состояние авторизации queryable. Основной риск unlocked-состояния в клиентской среде — denial of service и лишние замены часте…» — HM - Hardware Fault Management - sub-project, 2026-07-24 — youtube.com/watch?v=Ev4dgeaNB6E

## Considered Options

* Push-уведомления + auto-relock
* Pull-модель, состояние queryable

## Decision Outcome

Принято: pull-модель без push и без auto-relock; state queryable.

### Consequences

Ссылки на OCP secure boot, DMTF authorization, OCP attestation добавлены в документ.

## Pros and Cons of the Options

### Push-уведомления + auto-relock
* защита по умолчанию
* ложные срабатывания, DoS — отвергнуто
### Pull-модель, состояние queryable
* принято: простота, достаточно
* зависит от дисциплины опроса
