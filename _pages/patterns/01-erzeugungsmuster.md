---
title: Patterns
layout: single
permalink: /patterns/erzeugungsmuster
header:
  overlay_image: /images/pk_header.webp

excerpt: "**Erzeugungsmuster**"

sidebar:
  nav: erzeugungsmuster
---

### [Abstract Factory](/patterns/erzeugungsmuster/abstractfactory)
Es wird eine Schnittstelle bereitgestellt, um Familien verbundener oder abhängiger Objekte zu erstellen, ohne die konkreten Klassen zu spezifizieren.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/abstractfactory/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

### [Builder](/patterns/erzeugungsmuster/builder)
Die Erzeugung komplexer Objekte wird vereinfacht, indem der Konstruktionsprozess in eine spezielle Klasse verlagert wird. Er wird so von der Repräsentation getrennt und kann sehr unterschiedliche Repräsentationen zurückliefern.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/builder/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

### [Factory Method](/patterns/erzeugungsmuster/factorymethod)
Es wird eine Schnittstelle für die Erzeugung von Objekten definiert. Die Entscheidung, welche konkrete Klasse zu instanziieren, zu konfigurieren und schließlich zurückzugeben ist, wird konkreten (Unter-)Klassen überlassen, die diese Schnittstelle implementieren.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/factorymethod/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

### [Singleton](/patterns/erzeugungsmuster/singleton)
Singleton stellt sicher, dass nur genau eine Instanz einer Klasse erzeugt wird.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/singleton/README.md), [GOF](/literature#gof), [PK](/literature#pk)

### [Object Pool](/patterns/erzeugungsmuster/objectpool)
Es wird die Wiederverwendung von Objektinstanzen ermöglicht, deren Erzeugung sehr teuer ist oder deren Anzahl beschränkt werden soll.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/objectpool/README.md), [SHTR](/literature#shtr), [PK](/literature#pk)

