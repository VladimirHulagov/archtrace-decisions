---
id: "003"
status: accepted
type: problem
phase: 2
parent: "002"
cross_refs: []
created: 2026-10-08
---

# GPU + нейроморфное ускорение: нет общей памяти

## Context and Problem Statement

Презентация «GPU + neuromorphic acceleration working together»: проблема взаимодействия — нет общей памяти между GPU и нейроморфным железом, нужен memory manager/оркестратор; gateway потребляет энергию, противореча главному преимуществу нейроморфики (энергоэффективности).

**Из обсуждения на встрече:**

> «Проблемы, не раскрытые в paper: нет общей памяти между GPU и нейроморфным железом — нужен memory manager/оркестратор; сам gateway потребляет энергию, что противоречит главному преимуществу нейроморф» — Server - AI HW SW CoDesign - sub-project, 2026-09-18 — youtube.com/watch?v=G9_sGvS2xgg

## Considered Options

* Gateway-мост с копированием
* Общая память через memory manager/оркестратор

## Decision Outcome

Открыто: направление — общий memory manager; gateway-энергия признаётся контр-аргументом.

### Consequences

Пересечение с CMS (pooled CXL-память) как потенциальная инфраструктура.

## Pros and Cons of the Options

### Gateway-мост с копированием
* просто
* энергия gateway против преимуществ
### Общая память через memory manager/оркестратор
* энергоэффективно
* сложная координация
