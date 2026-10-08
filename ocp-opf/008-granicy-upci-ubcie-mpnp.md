---
id: "008"
status: accepted
type: decision
phase: 2
parent: "003"
cross_refs: []
created: 2026-10-08
---

# Границы спецификаций: UPCI/UBCIE независимо от OpenSFI

## Context and Problem Statement

Разделение спецификаций: UPCI/UBCIE остаётся независимой от OpenSFI, при этом выравнивается и с MPNP — вопрос границ спецификаций активный, но без формальных решений (формат — к следующим неделям).

**Из обсуждения на встрече:**

> «Разделение спецификаций: UPCI/UBCIE остаётся независимой от OpenSFI, при этом выравнивается и с MPNP — вопрос границ спецификаций активный, но без формальных решений (формат — к следующим неделям)» — OPF - Open Platform Firmware - project, 2026-07-02 — youtube.com/watch?v=ULmJUYBCVfg

## Considered Options

* Влить UPCI в OpenSFI
* Независимые спеки с выравниванием

## Decision Outcome

Принято: независимость + выравнивание границ.

### Consequences

Требует дисциплины cross-references между документами.

## Pros and Cons of the Options

### Влить UPCI в OpenSFI
* единый документ
* большой монолит
### Независимые спеки с выравниванием
* принято: модульность
* риск рассинхрона
