---
title: Active Object
permalink: /patterns/verteilung/activeobject
sidebar:
    nav: verteilung
---

Active Object entkoppelt einen Methodenaufruf von der Methodenausführung. Client und Komponente werden in unterschiedlichen Threads ausgeführt und interagieren asynchron.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/activeobject/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/activeobject/active_object_dn.png)

#### Beispiel

Im Beispiel hat ein Client die Möglichkeit historische Daten zu Personen abzufragen.
Die *HistoryQueryEngine* benötigt dazu ggf. einige Zeit, weil sie verschiedene Datenquellen abklappert.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 703 634">
<image width="703" height="634" xlink:href="/images/patterns/activeobject/active_object_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/HistoryQueryComponent.java">
<rect x="278" y="36" fill="#fff" opacity="0" width="322" height="72"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/QueryRequestFuture.java">
<rect x="205" y="187" fill="#fff" opacity="0" width="186" height="133"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/QueryRequest.java">
<rect x="489" y="187" fill="#fff" opacity="0" width="186" height="133"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/HistoryQueryScheduler.java">
<rect x="300" y="383" fill="#fff" opacity="0" width="279" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/AbstractHistoryQueryEngine.java">
<rect x="396" y="509" fill="#fff" opacity="0" width="280" height="73"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/activeobject/HistoryQueryEngineMock.java">
<rect x="26" y="508" fill="#fff" opacity="0" width="279" height="76"></rect>
</a>
</svg>

Der Client verwendet daher die Engine nicht direkt, sondern die *HistoryQueryComponent*, die sofort ein *QueryRequestFuture* zurück gibt, nachdem parallel ein Abfrageauftrag geplant wurde.–

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 833 774">
<image width="833" height="774" xlink:href="/images/patterns/activeobject/active_object_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/HistoryQueryComponent.java">
<rect x="154" y="0" fill="#fff" opacity="0" width="129" height="774"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/QueryRequest.java">
<rect x="349" y="0" fill="#fff" opacity="0" width="96" height="774"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/QueryRequestFuture.java">
<rect x="455" y="0" fill="#fff" opacity="0" width="105" height="774"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/activeobject/HistoryQueryEngineMock.java">
<rect x="556" y="0" fill="#fff" opacity="0" width="125" height="773"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/activeobject/HistoryQueryScheduler.java">
<rect x="694" y="0" fill="#fff" opacity="0" width="115" height="774"></rect>
</a>
</svg>

Das Future kann der Client solange pollen, bis ein Ergebnis vorliegt oder kein Interesse mehr besteht.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/activeobject)