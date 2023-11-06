---
title: Abstract Factory
permalink: /patterns/erzeugungsmuster/abstractfactory
sidebar:
    nav: erzeugungsmuster
---

Es wird eine Schnittstelle bereitgestellt, um Familien verbundener oder abhängiger Objekte zu erstellen, ohne die konkreten Klassen zu spezifizieren.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/abstractfactory/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)


#### Klassendiagramm

![](/images/patterns/abstractfactory/abstract_factory_cn.png)

#### Beispiel

Als Beispiel dient uns ein Szenario, in dem Daten entweder verschlüsselt oder unverschlüsselt abgelegt werden.

![](/images/patterns/abstractfactory/abstract_factory_cx.png)

Das Schreiben erledigen *DataWriter*, für das Lesen sind *DataReader* zuständig.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/abstractfactory)