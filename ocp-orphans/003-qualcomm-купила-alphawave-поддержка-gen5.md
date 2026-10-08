---
id: "003"
status: accepted
type: problem
phase: 1
parent: "001"
cross_refs: []
created: 2026-10-09
---

# Qualcomm купила AlphaWave — поддержка Gen5 PHY IP осложнилась (из 20/011)

## Context and Problem Statement

Работы по extended connectivity фактически встали: внешний наблюдатель (James Kelly) спрашивал «что случилось с extended connectivity, где встречи». Проблема: Qualcomm купила AlphaWave, та ушла с рынка PHY — сложно получить поддержку, хотя их Gen5 PHY IP используется.

**Из обсуждения на встрече:**

> «Работы по extended connectivity фактически встали: James Kelly у них спрашивал, «что случилось с extended connectivity, где встречи», — если разрешение на встречи не получено, восприятие со стороны…» — Server - CMS _ Composable Memory System - workstream, 2026-06-01 — youtube.com/watch?v=4mWEcGwgcDY
> «Проблема: Qualcomm купила AlphaWave, и та ушла с рынка PHY — сложно получить поддержку, хотя их Gen5 PHY IP используется» — Server - CMS _ Composable Memory System - workstream, 2026-06-01 — youtube.com/watch?v=4mWEcGwgcDY

## Considered Options

* Искать нового PHY-партнёра
* TeraSignal intelligent redriver/TIA как замена класса решений

## Decision Outcome

Экосистема сдвигается к «интеллектуальным redriver» (TeraSignal, Astera Labs) вместо полноценных PHY.

### Consequences

Риск vendor lock на redriver-вендоров; смешанная поддержка Gen5 IP.

## Pros and Cons of the Options

### Искать нового PHY-партнёра
* полноценный PHY
* долго и дорого
### TeraSignal intelligent redriver/TIA как замена класса решений
* уже «shippable part» (медь+оптика)
* не полноценный PHY
