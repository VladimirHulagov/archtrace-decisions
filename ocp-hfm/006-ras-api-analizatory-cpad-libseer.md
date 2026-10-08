---
id: "006"
status: accepted
type: decision
phase: 2
parent: "005"
cross_refs: []
created: 2026-10-08
---

# RAS API + анализаторы + CPAD-инъекция; libseer — open source

## Context and Problem Statement

Демо RAS API: анализаторы, оркестратор, инъекция ошибок через CPAD. libseer открыт сразу. Shim передаёт vendor-анализатору относящиеся к памяти CER-ы — рабочий time-series analysis, объединяющий FM и телеметрию.

**Из обсуждения на встрече:**

> «В ближайшие дни планирует завершить вызов shim, который передаёт vendor-анализатору все относящиеся к памяти CER'ы — в итоге получится рабочий time-series analysis, объединяющий FM (fault management…» — HM - Hardware Fault Management - sub-project, 2026-09-18 — youtube.com/watch?v=1BvVKTPSyyw
> «Microsoft (Drew), libseer — открытый код уже сейчас» — HM - Hardware Fault Management - sub-project, 2026-06-12 — youtube.com/watch?v=SjHYwJfsSfE

## Considered Options

* Проприетарные конвейеры вендоров
* Открытый RAS API + сменные анализаторы

## Decision Outcome

Принято: открытый API, vendor-анализаторы как плагины, libseer открыт.

### Consequences

Критика: подход «номер ошибки» не виден в потоке — требуется калибровка порогов (golden number).

## Pros and Cons of the Options

### Проприетарные конвейеры вендоров
* быстро для одного вендора
* флот гетерогенен — отвергнуто
### Открытый RAS API + сменные анализаторы
* принято: экосистема
* стандартизация анализаторов — долго
