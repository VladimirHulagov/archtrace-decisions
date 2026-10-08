---
id: "006"
status: accepted
type: decision
phase: 2
parent: "002"
cross_refs: []
created: 2026-10-08
---

# Питание шасси: 48 В от ORv3 bus bar, ~700 А на 2U

## Context and Problem Statement

FIT (Tim, Vincent Lin): концепция питания шасси 48 В от ORv3 bus bar. Допущения: 2U-шасси, 18 HPC-модулей по ~1,8 кВт, итого ~32,4 кВт → 675 А, округлено до 700 А для дизайна bus bar clip; текущая модель — 600 А при 48 В, коннектор к шинной сети под модулями.

**Из обсуждения на встрече:**

> «Допущения: 2U-шасси, 18 HPC-модулей по ~1,8 кВт, итого ~32,4 кВт → 675 А, округлено до 700 А для дизайна bus bar clip; текущая модель — 600 А при 48 В, коннектор к шинной сети под модулями» — Server - HPC _ High Performance Computing - sub-project, 2026-09-01 — youtube.com/watch?v=OEL620Fn9h4

## Considered Options

* Питание через backplane
* 48 В bus bar (ORv3) + clip

## Decision Outcome

Принято: ORv3 bus bar, 600–700 А дизайн клипа.

### Consequences

Ровно в экосистему Open Rack V3 (тема Владимира).

## Pros and Cons of the Options

### Питание через backplane
* привычно
* потери и меди на 700А
### 48 В bus bar (ORv3) + clip
* принято: экосистема
* клип на такие токи — новый
