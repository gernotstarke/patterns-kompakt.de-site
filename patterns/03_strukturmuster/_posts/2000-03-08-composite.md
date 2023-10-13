---
title: Composite
permalink: /patterns/strukturmuster/composite
sidebar:
    nav: strukturmuster
---

Composite ermöglicht die Gleichbehandlung von Einzelelementen und Elementgruppierungen in einer verschachtelten Struktur (z.B. Baum), sodass aus Sicht des Clients keine explizite Unterscheidung notwendig ist.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/composite/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/composite/composite_cn.png)

#### Beispiel

Im Beispiel sehen Sie eine Struktur von Unternehmenselementen.

![](/images/patterns/composite/composite_cx.png)

Trotz großer Unterschiede im Detail lassen sich alle Knoten bis zu einem gewissen Grad gleich behandeln.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()