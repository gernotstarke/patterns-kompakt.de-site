---
title: Optimistic Offline Lock
permalink: /patterns/persistenz/optimisticofflinelock
sidebar:
    nav: persistenz
---

Konflikte zwischen konkurrierenden Business-Transaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem die drohende Inkonsistenz zum Zeitpunkt des Updates entdeckt und die ausführende Transaktion abgebrochen wird (rollback).

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/optimisticofflinelock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

#### Beispiel

Im Beispiel geht es um die Bearbeitung von Kundendatensätzen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 700 302">
<image width="700" height="302" xlink:href="/images/patterns/optimisticofflinelock/optimistic_offline_lock_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/optimisticofflinelock/DataManager.java">
<rect x="236" y="36" fill="#fff" opacity="0" width="216" height="78"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/optimisticofflinelock/Customer.java">
<rect x="235" y="172" fill="#fff" opacity="0" width="218" height="80"></rect>
</a>
</svg>

Die folgende Abbildung zeigt zwei Clients, die konkurrierend die Daten zu Kunde 4711 bearbeiten.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 832 793">
<image width="832" height="793" xlink:href="/images/patterns/optimisticofflinelock/optimistic_offline_lock_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/optimisticofflinelock/DataManager.java">
<rect x="219" y="0" fill="#fff" opacity="0" width="90" height="793"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/optimisticofflinelock/Customer.java">
<rect x="325" y="0" fill="#fff" opacity="0" width="90" height="793"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/optimisticofflinelock/Customer.java">
<rect x="430" y="0" fill="#fff" opacity="0" width="90" height="793"></rect>
</a>
</svg>

Der erste Client *verliert*, weil der zweite Client zwischenzeitlich erfolgreich seine Änderung abgeschlossen hat.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/optimisticofflinelock)