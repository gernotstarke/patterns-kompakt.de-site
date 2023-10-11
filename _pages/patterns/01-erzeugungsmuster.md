---
title: Patterns
layout: single
permalink: /patterns/erzeugungsmuster
header:
  overlay_image: /images/farb_header_patterns.png

excerpt: "**Erzeugungsmuster**"

sidebar:
  nav: erzeugungsmuster
---

### [Abstract Factory](abstractfactory)
Es wird eine Schnittstelle bereitgestellt, um Familien verbundener oder abhängiger Objekte zu erstellen, ohne die konkreten Klassen zu spezifizieren.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/abstractfactory/README.md), GOF, STEMA, PK

### [Builder](builder)
Die Erzeugung komplexer Objekte wird vereinfacht, indem der Konstruktionsprozess in eine spezielle Klasse verlagert wird. Er wird so von der Repräsentation getrennt und kann sehr unterschiedliche Repräsentationen zurückliefern.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/builder/README.md), GOF, STEMA, PK

### [Factory Method](factorymethod)
Es wird eine Schnittstelle für die Erzeugung von Objekten definiert. Die Entscheidung, welche konkrete Klasse zu instanziieren, zu konfigurieren und schließlich zurückzugeben ist, wird konkreten (Unter-)Klassen überlassen, die diese Schnittstelle implementieren.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/factorymethod/README.md), GOF, STEMA, PK

### [Singleton](singleton)
Singleton stellt sicher, dass nur genau eine Instanz einer Klasse erzeugt wird.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/singleton/README.md), GOF, PK

### [Object Pool](objectpool)
Es wird die Wiederverwendung von Objektinstanzen ermöglicht, deren Erzeugung sehr teuer ist oder deren Anzahl beschränkt werden soll.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/objectpool/README.md), SHTR, PK

