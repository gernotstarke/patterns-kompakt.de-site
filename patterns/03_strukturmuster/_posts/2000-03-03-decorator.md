---
title: Decorator
permalink: /patterns/strukturmuster/decorator
sidebar:
    nav: strukturmuster
---

Decorator fügt einer Komponente dynamisch neue Funktionalität hinzu, ohne die Komponente selbst zu ändern.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/decorator/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/decorator/decorator_cn.png)

#### Beispiel

Im Beispiel wird eine zufällig erscheinende Seriennummer (z.B. für Gutscheine) benötigt.
Doppelte müssen vermieden werden. Eine Tabelle mit allen bereits vergebenen Zahlen kommt nicht in Frage.

![](/images/patterns/decorator/decorator_cx.png)

Zur Verfügung steht nur eine einfache Sequenz. Ein ShufflingSequenceDecorator wird quasi darüber gestülpt und stellt eine geeignet verwürfelte Zahl bereit.

![](/images/patterns/decorator/decorator_dx.png)

Für die bijektive Abbildung nutzt der Decorator intern die Kugel der Verwirrung (OrbOfConfusion).

![](/images/patterns/decorator/decorator_orb_of_confusion.png)

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG oder TRACE in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()