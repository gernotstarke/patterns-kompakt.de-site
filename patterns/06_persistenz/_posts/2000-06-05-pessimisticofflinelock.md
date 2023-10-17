---
title: Pessimistic Offline Lock
permalink: /patterns/persistenz/pessimisticofflinelock
sidebar:
    nav: persistenz
---

Konflikte zwischen konkurrierenden Geschäftstransaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem immer nur genau eine Business-Transaktion zur gleichen Zeit auf einen Datensatz zugreifen darf.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/pessimisticofflinelock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

#### Beispiel

Im Beispiel geht es um die Bearbeitung von Kundendatensätzen.

![](/images/patterns/pessimisticofflinelock/pessimistic_offline_lock_cx.png)

Die folgende Abbildung zeigt zwei Clients, die konkurrierend die Daten zu Kunde 4711 bearbeiten.

![](/images/patterns/pessimisticofflinelock/pessimistic_offline_lock_dx.png)

Der zweite Client *bemerkt*, dass der Kundendatensatz bereits im Zugriff durch einen anderen Client ist und bricht seinen Versuch ab.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()