---
id: "010"
title: "SCMI не покрывает чиплетные сценарии"
status: debating
type: problem
phase: 1
parent: "001"
cross_refs: []
created: 2026-10-05
---

## Контекст

После выбора транспорта группа вернулась к API (отложенному на полгода): SCMI определяет сообщения, но не функции API; нужен слой абстракции между application firmware и SCMI agent driver (агрегирующие команды без 1:1 к SCMI). Пробелы: discovery топологии (SCMI покрывает capabilities, топология собранного SiP статична — вероятно, структура данных, не runtime-обнаружение); управление линком (mainband on/off, width — в UCIe нет, в PCIe Gen 6 есть); телеметрия (точное потребление чиплета не всегда доступно, activity counters как приближение); thermal coupling matrices между чиплетами. Ограничение MCTP: 3-битный message tag = максимум 8 outstanding transactions на endpoint (возможно, не критично — тег per channel).


**Из обсуждения в чате:**

> «SCMI определяет сообщения (payload) для базовых ресурсов, но не функции API — нет C-кода; абстракционный слой может агрегировать несколько SCMI-сообщений в одну функцию — youtube.com/watch?v=2hFN5tLTrLI» — Rob (AMD), Chiplet Systems, 2026-09-16
> «у SCMI есть 10-битный token field, у MCTP message tag всего 3 бита → максимум 8 outstanding transactions на endpoint — youtube.com/watch?v=ds7T77SRzD8» — Bruno, Chiplet Systems, 2026-08-26


