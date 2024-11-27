---
layout: default
title: Architektura heksagonalna (Architektura portów i adapterów)
permalink: /blog/architektura-heksagonalna-porty-i-adaptery
tags: 
- hexagonal-architecture
- ports-and-apdaters 
- achitecture
---

Hexagonal Architecture (aka Ports & Adapters)

- Separacja logiki aplikacji od zależności (agnostyczne input/output), brak "wycieku" logiki aplikacji
- Luźno powiązane komponenty komunikujące się z aplikacją poprzez `porty` (interfejsy) i `adpatery` (implementacje)
- Sygnały/komunikaty są wysyłane i odbierane poprez porty, a tłumaczone w adapterach (możliwe wiele implementacji per port, np. równoległy zapis do bazy relacyjnej i dokumentowej)
- Wytwarzanie i testowanie w izolacji (zewnętrzny serwis, bazy danych, itp)