---
id: "016"
title: "MCTP 4K-пакеты против ~50% КПД link layer"
status: debating
type: paradigm
phase: 3
parent: "011"
cross_refs: []
created: 2026-10-05
---

## Контекст

MCTP-пакеты достигают ~4 КБ; текущий формат link layer даёт ~50% КПД (header/payload), что критично для firmware download. Для 2.0 нужен механизм с эффективностью >90%: выделенный bus protocol variant (биндинг «на одну страницу», MCTP packet size статичен) + механизм разбиения (continue bit / substream 4K→1K), иначе пакет монополизирует интерфейс. Дискуссия для 2.x: добавить ли сборку пакетов в link layer, чтобы протокольный слой этим не занимался. Для 1.x: либо множество low-payload message packets (sideband, 2 байта payload, ~50% — приемлемо для разовой прошивки), либо полноценный variant. Открытый вопрос 2.0: переменный размер TLP; идея Jeff с overloading message type ID возможно несовместима с текущей спекой.


**Из обсуждения в чате:**

> «MCTP-пакеты могут достигать ~4 КБ; для них нужен новый механизм с эффективностью >90%, с разбиением и сборкой пакетов на другой стороне — youtube.com/watch?v=ds7T77SRzD8» — Brian, Link Layer, 2026-08-26


