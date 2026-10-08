---
id: "007"
status: accepted
type: problem
phase: 1
parent: null
cross_refs: []
created: 2026-10-08
---

# Дефицит PCIe/CXL-портов на AI-платформах

## Context and Problem Statement

Пул памяти требует вывода PCIe из сервера, но AI-платформы физически не имеют свободных портов. Ключевой конфликт: «value proposition CXL+GPU понятна» vs «тактически сегодня нет покупаемой платформы» — Pankaj требовал конкретики «здесь и сейчас», Mitch/Muhammad отвечали про PoC.

**Из обсуждения на встрече:**

> «Ключевой конфликт встречи: «value proposition CXL+GPU понятна» vs «тактически сегодня нет покупаемой платформы» — Pankaj требовал конкретики «здесь и сейчас», Mitch/Muhammad отвечали про PoC и ближа…» — Server - CMS _ Composable Memory System - workstream, 2026-09-25 — youtube.com/watch?v=UFU4ExnzhfM

## Considered Options

* Ждать платформ с портами
* Extended connectivity: вывести PCIe через массовый коннектор

## Decision Outcome

Направление — extended connectivity поверх массовых коннекторов (см. 008); платформа-дефицит признан блокером so what-аргументации.

### Consequences

Каждое решение CMS обязано показывать use case и заказчика (OCP marketplace), не только future-proofing.

## Pros and Cons of the Options

### Ждать платформ с портами
* нулевые усилия
* тема теряет момент
### Extended connectivity: вывести PCIe через массовый коннектор
* драйвер подпроекта CMA
* нужен protocol-agnostic подход
