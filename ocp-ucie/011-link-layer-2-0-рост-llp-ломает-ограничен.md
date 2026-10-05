---
id: "011"
title: "Link layer 2.0: рост LLP ломает ограничения 1.x"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-05
---

## Контекст

Спека transaction link layer (TLLL, в прошлом Universal TLL — вклад Ventana) готовит 2.0: снятие ограничения «один TOP-тип на LOP» ради роста размера LLP порождает каскад вопросов по кредитованию (messages, virtual wires, credit returns), форматам сообщений и размеру LLP. Цель — PHY-агностичность: три file layer binding (BoW, UCIe/FDI, BoW Flexi), реорганизация «un-bowify» (BoW становится главой, а не всей спекой). ECC решён: без новых типов пакетов, reserved биты RX игнорирует при отсутствии поддержки (вариант новых типов — «слишком много усилий», возврат возможен в 2.1).


**Из обсуждения в чате:**

> «Интегрирует прошлогодние proposals в документ 2.0, чтобы выявить проблемы до финального решения; ни одно предложение ещё не утверждено — youtube.com/watch?v=9V9t7xtYA-0» — Ведущий Link Layer, 2026-04-23
> «ECC: для систем без поддержки решено не вводить новые типы пакетов — биты ECC остаются reserved, RX просто игнорирует — youtube.com/watch?v=0nYUpyDnTQk» — Ведущий Link Layer, 2026-05-07


