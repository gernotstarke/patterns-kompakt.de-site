---
title: Optimistic Offline Lock
permalink: /patterns/persistenz/optimisticofflinelock
sidebar:
    nav: persistenz
---

Konflikte zwischen konkurrierenden Business-Transaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem die drohende Inkonsistenz zum Zeitpunkt des Updates entdeckt und die ausführende Transaktion abgebrochen wird (rollback).

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/optimisticofflinelock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

#### Beispiel

Im Beispiel geht es um die Bearbeitung von Kundendatensätzen.

![](/images/patterns/optimisticofflinelock/optimistic_offline_lock_cx.png)

Die folgende Abbildung zeigt zwei Clients, die konkurrierend die Daten zu Kunde 4711 bearbeiten.

![](/images/patterns/optimisticofflinelock/optimistic_offline_lock_dx.png)

Der erste Client *verliert*, weil der zweite Client zwischenzeitlich erfolgreich seine Änderung abgeschlossen hat.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()