---
title: Null-Object
permalink: /patterns/sonstige/nullobject
sidebar:
    nav: sonstige
---

Es wird eine Klasse definiert, die "nichts" tut - wobei das "Nichts" fachlich ist.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/nullobject/README.md), [UNCLEBOB](/literature#unclebob), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/nullobject/null_object_cn.png)

### Beispiel

m Beispiel gibt der *HostNameDataProvider* eine *HostNameData*-Instanz zurück, die dem Client die Namen zu jedem Zweck auflisten soll.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 586 457">
<image width="586" height="457" xlink:href="/images/patterns/nullobject/null_object_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/HostNameDataProvider.java">
<rect x="182" y="340" fill="#fff" opacity="0" width="240" height="69"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/ConcreteHostNameData.java">
<rect x="388" y="173" fill="#fff" opacity="0" width="171" height="90"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/HostNameDataNullObject.java">
<rect x="182" y="173" fill="#fff" opacity="0" width="171" height="90"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/HostNameData.java">
<rect x="289" y="35" fill="#fff" opacity="0" width="172" height="89"></rect>
</a>
</svg>

Wird nichts gefunden, vermeidet der *HostNameDataProvider* die Rückgabe von *null*.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 700 445">
<image width="700" height="445" xlink:href="/images/patterns/nullobject/null_object_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/HostNameDataProvider.java">
<rect x="192" y="0" fill="#fff" opacity="0" width="131" height="445"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/ConcreteHostNameData.java">
<rect x="370" y="0" fill="#fff" opacity="0" width="124" height="445"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject/HostNameDataNullObject.java">
<rect x="537" y="3" fill="#fff" opacity="0" width="138" height="442"></rect>
</a>
</svg>

Stattdessen erhält der Client ein *HostNameDataNullObject*, mit dem er normal arbeiten kann.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/nullobject)