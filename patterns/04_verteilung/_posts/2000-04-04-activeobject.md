---
title: Active Object
permalink: /patterns/verteilung/activeobject
sidebar:
    nav: verteilung
---

Active Object entkoppelt einen Methodenaufruf von der Methodenausführung. Client und Komponente werden in unterschiedlichen Threads ausgeführt und interagieren asynchron.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/activeobject/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/activeobject/active_object_dn.png)

#### Beispiel

Im Beispiel hat ein Client die Möglichkeit historische Daten zu Personen abzufragen.
Die *HistoryQueryEngine* benötigt dazu ggf. einige Zeit, weil sie verschiedene Datenquellen abklappert.

![](/images/patterns/activeobject/active_object_cx.png)

Der Client verwendet daher die Engine nicht direkt, sondern die *HistoryQueryComponent*, die sofort ein *QueryRequestFuture* zurück gibt, nachdem parallel ein Abfrageauftrag geplant wurde.–

![](/images/patterns/activeobject/active_object_dx.png)

Das Future kann der Client solange pollen, bis ein Ergebnis vorliegt oder kein Interesse mehr besteht.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()