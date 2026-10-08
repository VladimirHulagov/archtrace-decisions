---
id: "001"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-05
---

# Интеграция HPM/SCM без кастомного BMC

## Контекст


**Кросс-упоминания из других воркстримов:**

> «OCP Open Platform Firmware (EDK2, OpenBMC как референс); Arm SBSA и SBBR; чиплетный SOC по FCS (Foundation Chiplet System Architecture); межчиплетный интерфейс — UCIe. - Конфигурация узла: свой HPM, один Arm Neoverse CPU; 12 слотов DDR5 до 8400 MT/s на узел; 96 линий PCIe Gen 6 с CXL 3.0; BMC — ASPEED AST2600 (заменяем партнёром); 21" 1U форм-фактор, совместимый с OCP 3.0 rack. - Открытая часть —…» — Server - project, 2026-09-23 — youtube.com/watch?v=Ucah5MpA2A0
> «Существует PLDM-спека о хендшейке BIOS↔BMC — возможно, её стоит расширить. - Итог: передавать всё собранное BIOS'ом по стандартному каналу; это пересекается с телеметрией и требует единообразия между вендорами (по аналогии с consistent format в EPCA/UCPI). Аллисон сверит с уже сделанным DCSCM-спецификацией out-of-band конфигурации, чтобы не дублировать Redfish (Redfish «слишком поздно — нужен ребу…» — OPF - Open Platform Firmware - project, 2026-06-04 — youtube.com/watch?v=1zooRC-rWcA


