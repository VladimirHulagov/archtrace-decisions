---
id: "007"
status: debating
type: paradigm
phase: 3
parent: "006"
cross_refs: []
created: 2026-10-05
---

# Thermal trip: IBI-сообщения или open-drain

## Контекст

Можно ли передавать быстрые критичные события (thermal trip — запрос отключения питания) через IBI/сообщения, или нужны дискретные сигналы. Изначальное решение — high-priority события через IBI-прерывания. Контрпредложение Jay (AMD): open-drain сеть на уровне package — все чиплеты участвуют и мгновенно получают trip; сетка датчиков с порогами полностью аппаратная, без firmware. В server-чипах обычно два сигнала: probot и thermal trip; в dual-socket перегрев одного означает близкий перегрев второго.


**Из обсуждения в чате:**

> «open-drain решение логично и на уровне package — все чиплеты участвуют в open-drain сети и мгновенно получают trip — youtube.com/watch?v=IXifDBAGtys» — Jay/Giri (AMD), Chiplet Systems, 2026-06-24

