---
title: Flyweight
permalink: /patterns/strukturmuster/flyweight
sidebar:
    nav: strukturmuster
---

Um in einem System eine sehr große Anzahl feingranularer Objekte zu verwalten, wird die gemeinsame Nutzung von Instanzen (instance sharing) eingeführt.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/flyweight/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/flyweight/flyweight_cn.png)

#### Beispiel

Im Beispiel werden Instanzen eines speziell initialisierten Zählers sehr häufig benötigt.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 692 554">
<image width="692" height="554" xlink:href="/images/patterns/flyweight/flyweight_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/flyweight/CounterFlyweightFactory.java">
<rect x="27" y="192" fill="#fff" opacity="0" width="266" height="76"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/flyweight/CounterFlyweightCarryingItem.java">
<rect x="400" y="35" fill="#fff" opacity="0" width="266" height="50"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/flyweight/CounterFlyweight.java">
<rect x="402" y="190" fill="#fff" opacity="0" width="266" height="76"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/flyweight/ConcreteCounterFlyweight.java">
<rect x="399" y="324" fill="#fff" opacity="0" width="267" height="75"></rect>
</a><a xlink:href="#">
<rect x="0" y="0" fill="#fff" opacity="0" width="100" height="100"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/flyweight/UnsharedConcreteCounterFlyweight.java">
<rect x="399" y="454" fill="#fff" opacity="0" width="267" height="75"></rect>
</a>
</svg>

Nachdem *intrinsic* und *extrinsic state* identifiziert wurden, ist es möglich, die Objekte konkurrierend zu verwenden und so die gleichzeitig im System vorhandene Anzahl Instanzen zu reduzieren.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/flyweight)