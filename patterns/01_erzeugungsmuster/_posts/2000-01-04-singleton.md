---
title: Singleton
permalink: /patterns/erzeugungsmuster/singleton
sidebar:
    nav: erzeugungsmuster
---

Singleton stellt sicher, dass nur genau eine Instanz einer Klasse erzeugt wird.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/singleton/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/singleton/singleton_dn.png)

#### Beispiel

Sie finden zwei Implementierungen eines *Tracers*, der hier einfachheitshalber nur die Aufgabe hat, Zeilen in eine Datei zu schreiben.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 505 169">
<image width="505" height="169" xlink:href="/images/patterns/singleton/singleton_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/singleton/Tracer.java">
<rect x="25" y="34" fill="#fff" opacity="0" width="211" height="86"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/singleton/Tracer2.java">
<rect x="266" y="34" fill="#fff" opacity="0" width="212" height="87"></rect>
</a>
</svg>

Beide Implementierungen leisten dasselbe, nutzen jedoch verschiedene Wege zur Sicherstellung der Singleton-Eigenschaften.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus. Beachten Sie auch die Hinweise im Quellcode.

![](/images/patterns/singleton/singleton_photo.png)

Das Foto zeigt anschaulich die wichtigsten Eigenschaften von Singleton:

* Einfach zu verstehen
* Zu genießen in kleinen Mengen, Übermaß nicht empfohlen
* Manchmal die einzige Lösung
* Wie bei [Daniel Defoe](https://de.wikipedia.org/wiki/Daniel_Defoe) wird nur allzu gern bei den Details geschlampt

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/singleton)