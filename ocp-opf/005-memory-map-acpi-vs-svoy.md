---
id: "005"
status: accepted
type: problem
phase: 3
parent: "004"
cross_refs: []
created: 2026-10-08
---

# Memory map: переиспользовать ACPI/PI или свой OpenSFI-формат

## Context and Problem Statement

Формат передачи memory map между silicon firmware и host firmware: переиспользовать отраслевой стандарт (ACPI / PI resource descriptor) или создать собственный OpenSFI-формат — решение не принято. Формат вывода stage meminit определён только набросками Tim и Mike.

**Из обсуждения на встрече:**

> «Формат передачи memory map между silicon firmware и host firmware: переиспользовать отраслевой стандарт (ACPI / PI resource descriptor) или создать собственный OpenSFI-формат — решение не принято» — OPF - Open Platform Firmware - project, 2026-08-13 — youtube.com/watch?v=lImXLYS_wuI

## Considered Options

* ACPI / PI resource descriptor
* Собственный OpenSFI-формат

## Decision Outcome

Открыто.

### Consequences

Влияет на минимализм OpenSFI (принцип: не дублировать стандарты).

## Pros and Cons of the Options

### ACPI / PI resource descriptor
* готовый стандарт
* наследие UEFI-мира
### Собственный OpenSFI-формат
* минимальный и точный
* свой формат поддерживать
