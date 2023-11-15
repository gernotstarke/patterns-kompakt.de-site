---
title: Composite
permalink: /patterns/strukturmuster/composite
sidebar:
    nav: strukturmuster
---

Composite ermöglicht die Gleichbehandlung von Einzelelementen und Elementgruppierungen in einer verschachtelten Struktur (z.B. Baum), sodass aus Sicht des Clients keine explizite Unterscheidung notwendig ist.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/composite/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/composite/composite_cn.png)

#### Beispiel

Im Beispiel sehen Sie eine Struktur von Unternehmenselementen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 799 494">
<image width="799" height="494" xlink:href="/images/patterns/composite/composite_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite/EnterpriseNode.java">
<rect x="276" y="35" fill="#fff" opacity="0" width="184" height="89"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite/StaffMember.java">
<rect x="26" y="180" fill="#fff" opacity="0" width="295" height="153"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite/AbstractEnterpriseUnit.java">
<rect x="415" y="180" fill="#fff" opacity="0" width="297" height="152"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite/Holding.java">
<rect x="362" y="375" fill="#fff" opacity="0" width="110" height="70"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite/Division.java">
<rect x="509" y="376" fill="#fff" opacity="0" width="111" height="69"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite/Company.java">
<rect x="654" y="375" fill="#fff" opacity="0" width="112" height="71"></rect>
</a>
</svg>

Trotz großer Unterschiede im Detail lassen sich alle Knoten bis zu einem gewissen Grad gleich behandeln.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/composite)