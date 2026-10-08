---
id: "009"
status: accepted
type: decision
phase: 3
parent: "008"
cross_refs: []
created: 2026-10-08
---

# Точка подключения оптики: CEM-слот vs MCIO — спор открыт

## Context and Problem Statement

Базовая точка подключения оптики: CEM-слот (определён PCI-SIG, но дорогая активная карта) vs MCIO от DCMHS (новая OCP-работа, коннектор «в середине» платы). Microsoft хочет карты и сервер DCMHS для тестирования с приобретённым набором кабелей.

**Из обсуждения на встрече:**

> «Базовая точка подключения оптики: CEM-слот (определён PCI-SIG, но дорогая активная карта) vs MCIO от DCMHS (новая OCP-работа, коннектор «в середине» платы). Спор не закрыт; решение за командой» — Server - CMS _ Composable Memory System - workstream, 2026-05-22 — youtube.com/watch?v=1k2S0661Gkw
> «Итог: договорились добавить вариант MCIO в список работ; Microsoft хочет получить такие карты и сервер DCMHS для тестирования с приобретённым набором кабелей» — Server - CMS _ Composable Memory System - workstream, 2026-05-22 — youtube.com/watch?v=1k2S0661Gkw

## Considered Options

* CEM-слот (PCI-SIG)
* MCIO (DCMHS)

## Decision Outcome

MCIO добавлен в список работ параллельно CEM; выбор за данными вендоров о реально отгружаемых объёмах.

### Consequences

Решение блокирует финальную редакцию 2.0; влияет на совместимость с DC-MHS платформами.

## Pros and Cons of the Options

### CEM-слот (PCI-SIG)
* стандарт готов
* дорогая активная карта
### MCIO (DCMHS)
* дешевле, «в середине» платы
* новая OCP-работа — сроки
