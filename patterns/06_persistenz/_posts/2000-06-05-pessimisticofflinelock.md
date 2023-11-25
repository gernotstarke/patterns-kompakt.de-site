---
title: Pessimistic Offline Lock
permalink: /patterns/persistenz/pessimisticofflinelock
sidebar:
    nav: persistenz
---

Konflikte zwischen konkurrierenden Geschäftstransaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem immer nur genau eine Business-Transaktion zur gleichen Zeit auf einen Datensatz zugreifen darf.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/pessimisticofflinelock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

#### Beispiel

Im Beispiel geht es um die Bearbeitung von Kundendatensätzen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 691 509">
<image width="691" height="509" xlink:href="/images/patterns/pessimisticofflinelock/pessimistic_offline_lock_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/pessimisticofflinelock/LockManager.java">
<rect x="238" y="35" fill="#fff" opacity="0" width="240" height="114"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/pessimisticofflinelock/Customer.java">
<rect x="238" y="368" fill="#fff" opacity="0" width="241" height="115"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/pessimisticofflinelock/LockManager.java#L704">
<rect x="238" y="201" fill="#fff" opacity="0" width="240" height="115"></rect>
</a>
</svg>

Die folgende Abbildung zeigt zwei Clients, die konkurrierend die Daten zu Kunde 4711 bearbeiten.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 785 553">
<image width="785" height="553" xlink:href="/images/patterns/pessimisticofflinelock/pessimistic_offline_lock_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/pessimisticofflinelock/Customer.java">
<rect x="187" y="0" fill="#fff" opacity="0" width="90" height="553"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/pessimisticofflinelock/LockManager.java">
<rect x="315" y="0" fill="#fff" opacity="0" width="90" height="553"></rect>
</a>
</svg>

Der zweite Client *bemerkt*, dass der Kundendatensatz bereits im Zugriff durch einen anderen Client ist und bricht seinen Versuch ab.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/pessimisticofflinelock)