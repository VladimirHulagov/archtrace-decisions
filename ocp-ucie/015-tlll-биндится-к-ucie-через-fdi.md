---
id: "015"
title: "TLLL биндится к UCIe через FDI"
status: accepted
type: decision
phase: 4
parent: "011"
cross_refs: []
created: 2026-10-05
---

## Контекст

Универсальная схема: любой протокол (CHI + AXI + AHB конкурентно на одном линке, через type ID/стримы, всё с кредитами) биндится к TLLL, TLLL — к любому FDI. Основа — вклад Ventana (Universal TLL, FDI binding для UCIe raw streaming mode, не RDI); в 2.0 скопирован почти целиком; по предложению Cliff (OCP) переименован в TLLL. Переиспользуются управление и ECC/FEC UCIe (CRC-retry в raw streaming нет). Биндинг к BoW Flexi: 4-битная команда, 3 бита данных, ECC + опциональный continue; заголовок ~7 бит против 32 у LLP — Flexi сейчас эффективнее.


**Из обсуждения в чате:**

> «Идея «универсального transaction link layer»: любой протокол биндится к TLLL, TLLL биндится к любому FDI... Решено назвать его TLLL — youtube.com/watch?v=XWbFNW_jMzc» — Tai/Atai + Jeff, Link Layer, 2026-09-08


## Решение

TLLL = универсальный transaction link layer поверх FDI (UCIe raw streaming); протоколы маппятся на bus-интерфейсы SoC через type ID/стримы.

## Последствия

Открытые вопросы: «wide Flexi» (>32 бит, padding single-granule TLP), обобщение time- vs frame-делимитации (Jeff — обобщить, Brian — фундаментально разные); LSI-спеку изучить на конвергенцию (Jeff скептичен: «продукт, ищущий стандартизацию»).

