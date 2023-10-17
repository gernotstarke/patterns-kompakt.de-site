---
title: Patterns
layout: single
permalink: /patterns/persistenz
header:
  overlay_image: /images/pk_header.webp
excerpt: "**Persistenz**"

sidebar:
  nav: persistenz
---

### [Identity Map](/patterns/persistenz/identitymap)
Eine Identity Map verwaltet Objekte, die aus einer Datenbank gelesen und möglicherweise verändert werden und stellt sicher, dass Objekte nie mehr als einmal aus der Datenbank gelesen werden.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identitymap/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### [Lazy Load](/patterns/persistenz/lazyload)
Es wird ein Objekt geliefert, das noch nicht alle benötigten Daten enthält, aber weiß, wie diese zu beschaffen sind.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/lazyload/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### [Coarse-Grained Lock](/patterns/persistenz/coarsegrainedlock)
Es wird eine einzige Sperre für eine Menge von Objekten gesetzt, um diese gemeinsam zu sperren.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/coarsegrainedlock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### [Optimistic Offline Lock](/patterns/persistenz/optimisticofflinelock)
Konflikte zwischen konkurrierenden Business-Transaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem die drohende Inkonsistenz zum Zeitpunkt des Updates entdeckt und die ausführende Transaktion abgebrochen wird (rollback).

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/optimisticofflinelock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### [Pessimistic Offline Lock](/patterns/persistenz/pessimisticofflinelock)
Konflikte zwischen konkurrierenden Geschäftstransaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem immer nur genau eine Business-Transaktion zur gleichen Zeit auf einen Datensatz zugreifen darf.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/pessimisticofflinelock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

