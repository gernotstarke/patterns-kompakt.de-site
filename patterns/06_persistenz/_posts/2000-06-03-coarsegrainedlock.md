---
title: Coarse-Grained Lock
permalink: /patterns/persistenz/coarsegrainedlock
sidebar:
    nav: persistenz
---

Es wird eine einzige Sperre für eine Menge von Objekten gesetzt, um diese gemeinsam zu sperren.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/coarsegrainedlock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/coarsegrainedlock/coarse_grained_lock_cn.png)


#### Beispiel

Im Beispiel hat ein Kunde eine Menge von Adressen und eine Menge von Bestellungen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 738 478">
<image width="738" height="478" xlink:href="/images/patterns/coarsegrainedlock/coarse_grained_lock_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/InMemoryLockManager.java">
<rect x="475" y="35" fill="#fff" opacity="0" width="234" height="115"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/Customer.java">
<rect x="133" y="211" fill="#fff" opacity="0" width="154" height="80"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/Address.java">
<rect x="44" y="343" fill="#fff" opacity="0" width="155" height="80"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/Order.java">
<rect x="222" y="343" fill="#fff" opacity="0" width="154" height="81"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/InMemoryLockManager.java#L435">
<rect x="476" y="264" fill="#fff" opacity="0" width="232" height="92"></rect>
</a>
</svg>

Die grobkörnige Sperre stellt sicher, dass immer die Gesamtheit der Entitäten zu einem Kunden gesperrt werden, wenn eines bearbeitet wird.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 804 714">
<image width="804" height="714" xlink:href="/images/patterns/coarsegrainedlock/coarse_grained_lock_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/Customer.java">
<rect x="225" y="0" fill="#fff" opacity="0" width="90" height="714"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/Address.java">
<rect x="325" y="0" fill="#fff" opacity="0" width="90" height="714"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/InMemoryLockManager.java">
<rect x="425" y="0" fill="#fff" opacity="0" width="120" height="714"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock/InMemoryLockManager.java#L435">
<rect x="609" y="0" fill="#fff" opacity="0" width="167" height="714"></rect>
</a>
</svg>

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/coarsegrainedlock)