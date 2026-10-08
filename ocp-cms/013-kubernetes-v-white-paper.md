---
id: "013"
status: accepted
type: decision
phase: 2
parent: "001"
cross_refs: []
created: 2026-10-08
---

# Kubernetes-плагин и код — в white paper Orchestration (гл. 6–7)

## Context and Problem Statement

Вклад (код + архитектурный документ) идёт в workstream для интеграции в white paper «CMS Memory Fabric Orchestration Architecture 1.0» — в главу 7 и раздел про Kubernetes plugin в главу 6. Изменения по Kubernetes лучше лягут в готовящийся документ по software requirements.

**Из обсуждения на встрече:**

> «Итог: вклад (код + архитектурный документ) пойдёт в workstream для интеграции в white paper «CMS Memory Fabric Orchestration Architecture 1.0» — в главу 7 и раздел про Kubernetes plugin в главу 6» — Server - CMS _ Composable Memory System - workstream, 2026-05-08 — youtube.com/watch?v=C6fHdFZ5Mrk
> «Hongjin (Samsung): его рекомендация — изменения по Kubernetes лучше лягут в готовящийся документ по software requirements (software orchestration), но решение за группой» — Server - CMS _ Composable Memory System - workstream, 2026-05-29 — youtube.com/watch?v=83IRt6qwBvs

## Considered Options

* Отдельный документ по K8s-интеграции
* Влить в white paper Orchestration

## Decision Outcome

Влито в главы 6–7 white paper 1.0.

### Consequences

Ревизия white paper до OCP Global (вклад Samsung); ревью по email за неделю.

## Pros and Cons of the Options

### Отдельный документ по K8s-интеграции
* гибкость
* дробит документацию
### Влить в white paper Orchestration
* принято: единая архитектура 1.0
* сроки привязаны к саммиту
