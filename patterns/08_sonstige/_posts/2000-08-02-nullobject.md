---
title: Null-Object
permalink: /patterns/sonstige/nullobject
sidebar:
    nav: sonstige
---

Es wird eine Klasse definiert, die "nichts" tut - wobei das "Nichts" fachlich ist.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/nullobject/README.md), [UNCLEBOB](/literature#unclebob), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/nullobject/null_object_cn.png)

### Beispiel

m Beispiel gibt der *HostNameDataProvider* eine *HostNameData*-Instanz zurück, die dem Client die Namen zu jedem Zweck auflisten soll.

![](/images/patterns/nullobject/null_object_cx.png)

Wird nichts gefunden, vermeidet der *HostNameDataProvider* die Rückgabe von *null*.

![](/images/patterns/nullobject/null_object_dx.png)

Stattdessen erhält der Client ein *HostNameDataNullObject*, mit dem er normal arbeiten kann.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.



#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()