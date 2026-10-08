---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-05
---

# Нет стандарта control-plane между чиплетами

## Контекст


**Кросс-упоминания из других воркстримов:**

> «**2. Bruno (Cynple), SCMI over I3C — обзор спецификации:** - Контекст: system control в чипе — распределённая функция по OCP FCSA: primary system controller в primary chiplet и secondary system controllers в secondary chiplets; между ними нужны system control interfaces. FCSA называет SCMI и RPMI вариантами протокола и упоминает I3C как физический интерфейс, но не определяет транспорт SCMI/RPMI по…» — Server - OCE - Foundation Chiplet System Architecture -, 2026-08-10 — youtube.com/watch?v=YVDgs4HamqM


## Симптомы и факты

- UCIe не определяет внутриядревый транспорт и management-биндинги (→ 002, нужна надстройка доставки)
- BOW — point-to-point, маршрутизации между чиплетами нет (→ 002, нужен слой маршрутизации)
- I3C — отдельный физический уровень; два несогласованных маппинга SCMI: Rob→UCIe и Bruno→I3C (→ 006, конфликт путей)

