---
title: Decorator
permalink: /patterns/strukturmuster/decorator
sidebar:
    nav: strukturmuster
---

Decorator fügt einer Komponente dynamisch neue Funktionalität hinzu, ohne die Komponente selbst zu ändern.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/decorator/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/decorator/decorator_cn.png)

#### Beispiel

Im Beispiel wird eine zufällig erscheinende Seriennummer (z.B. für Gutscheine) benötigt.
Doppelte müssen vermieden werden. Eine Tabelle mit allen bereits vergebenen Zahlen kommt nicht in Frage.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 707 342">
<image width="707" height="342" xlink:href="/images/patterns/decorator/decorator_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/decorator/NumberSequence.java">
<rect x="248" y="35" fill="#fff" opacity="0" width="162" height="92"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/decorator/SimpleNumberSequence.java">
<rect x="25" y="181" fill="#fff" opacity="0" width="282" height="114"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/decorator/ShufflingSequenceDecorator.java">
<rect x="346" y="180" fill="#fff" opacity="0" width="283" height="117"></rect>
</a>
</svg>

Zur Verfügung steht nur eine einfache Sequenz. Ein *ShufflingSequenceDecorator* wird quasi darüber gestülpt und stellt eine geeignet verwürfelte Zahl bereit.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 851 432">
<image width="851" height="432" xlink:href="/images/patterns/decorator/decorator_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/decorator/SimpleNumberSequence.java">
<rect x="132" y="0" fill="#fff" opacity="0" width="262" height="432"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/decorator/ShufflingSequenceDecorator.java">
<rect x="430" y="0" fill="#fff" opacity="0" width="256" height="432"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/util/OrbOfConfusion.java">
<rect x="733" y="0" fill="#fff" opacity="0" width="92" height="432"></rect>
</a>
</svg>

Für die bijektive Abbildung nutzt der Decorator intern die [*Kugel der Verwirrung (OrbOfConfusion)*](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/util/OrbOfConfusion.java).
  
![](/images/patterns/decorator/decorator_orb_of_confusion.png)




Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG oder TRACE in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/decorator)