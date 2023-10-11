---
title: Patterns
layout: single
permalink: /patterns/verteilung
header:
  overlay_image: /images/farb_header_patterns.png
excerpt: "**Verteilung**"

sidebar:
  nav: verteilung
---

### [Combined Method](combinedmethod)
Mehrere Methodenaufrufe werden in einer neuen Methode des Komponenteninterfaces zusammengefasst, um Aufrufreihenfolgen, Transaktionssicherheit bzw. Fehlerbehandlung besser gewährleisten zu können.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/combinedmethod/README.md), POSA4, PK

### [Data Transfer Object](datatransferobject)
Data Transfer Object (DTO) fasst in einer verteilten Umgebung (z. B. JEE) zu übertragende Daten in einem neuen Objekt zusammen, um die Anzahl der entfernten Methodenaufrufe zu reduzieren und somit das Netzwerk zu entlasten.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/datatransferobject/README.md), J2EE, PK

### [Transfer Object Assembler](transferobjectassembler)
Transferobjekte, die Daten mehrerer Geschäftsobjekte beinhalten, werden serverseitig von einem Assembler zusammengestellt, um die Schnittstelle zum Client zu vereinfachen und die Performance zu erhöhen.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/transferobjectassembler/README.md), J2EE, PK

### [Active Object](activeobject)
Active Object entkoppelt einen Methodenaufruf von der Methodenausführung. Client und Komponente werden in unterschiedlichen Threads ausgeführt und interagieren asynchron.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/activeobject/README.md), POSA4, PK

### [Master-Slave](masterslave)
Unabhängige Teilaufgaben innerhalb einer Serviceimplementierung werden in separaten Threads ausgeführt (divide and conquer), um nicht-funktionale Anforderungen (i. d. R. Performance) besser zu erfüllen.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/masterslave/README.md), POSA4, PK

