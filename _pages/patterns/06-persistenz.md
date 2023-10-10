---
title: Patterns
layout: single
permalink: /patterns/persistenz
header:
  overlay_image: /images/farb_header_patterns.png
excerpt: "**Persistenz**"

sidebar:
  nav: persistenz
---

### [Identity Map](identitymap)
Eine Identity Map verwaltet Objekte, die aus einer Datenbank gelesen und möglicherweise verändert werden und stellt sicher, dass Objekte nie mehr als einmal aus der Datenbank gelesen werden.

> siehe: GitHub, PEAA, PK

### [Lazy Load](lazyload)
Es wird ein Objekt geliefert, das noch nicht alle benötigten Daten enthält, aber weiß, wie diese zu beschaffen sind.

> siehe: GitHub, PEAA, PK

### [Coarse-Grained Lock](coarsegrainedlock)
Es wird eine einzige Sperre für eine Menge von Objekten gesetzt, um diese gemeinsam zu Sperren.

> siehe: GitHub, PEAA, PK

### [Optimistic Offline Lock](optimisticofflinelock)
Konflikte zwischen konkurrierenden Business-Transaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem die drohende Inkonsistenz zum Zeitpunkt des Updates entdeckt und die ausführende Transaktion abgebrochen wird (rollback).

> siehe: GitHub, PEAA, PK

### [Pessimistic Offline Lock](pessimisticofflinelock)
Konflikte zwischen konkurrierenden Geschäftstransaktionen beim Zugriff auf eine Datenquelle werden behandelt, indem immer nur genau eine Business-Transaktion zur gleichen Zeit auf einen Datensatz zugreifen darf.

> siehe: GitHub, PEAA, PK

