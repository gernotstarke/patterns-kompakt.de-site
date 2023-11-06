---
title: Factory Method
permalink: /patterns/erzeugungsmuster/factorymethod
sidebar:
    nav: erzeugungsmuster
---


Es wird eine Schnittstelle für die Erzeugung von Objekten definiert. Die Entscheidung, welche konkrete Klasse zu instanziieren, zu konfigurieren und schließlich zurückzugeben ist, wird konkreten (Unter-)Klassen überlassen, die diese Schnittstelle implementieren.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/factorymethod/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/factorymethod/factory_method_cn.png)

#### Beispiel

Im Beispiel betrachten wir eine Shop-Software, die sowohl von *Moron Store Worldwide* als auch von *Mrs. Freakly* genutzt wird, die einen (sehr erfolgreichen) Tante-Emma-Laden in Chicago betreibt.
In beiden Fällen werden Gutscheine für die Kunden benötigt.

![](/images/patterns/factorymethod/factory_method_cx.png)

Da sich die Gutscheine und ihre Erzeugung recht stark unterscheiden, wurde das *Factory Method*-pattern eingesetzt.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/factorymethod)