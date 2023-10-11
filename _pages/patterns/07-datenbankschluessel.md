---
title: Patterns
layout: single
permalink: /patterns/datenbankschluessel
header:
  overlay_image: /images/farb_header_patterns.png
excerpt: "**Datenbankschlüssel**"

sidebar:
  nav: datenbankschluessel
---

### [Identity Field](identityfield)
Eine Schlüsselklasse fasst die Spalten eines Datenbankschlüssels in einem Objekt zusammen. Damit wird die Identität zwischen Laufzeitobjekten (in-memory objects) und Datensätzen sichergestellt.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identityfield/README.md), PEAA, PK

### [Sequence Block](sequenceblock)
Sequenzblock erzeugt auf performante und portable Weise Primärschlüssel für persistente Objekte.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/sequenceblock/README.md), MARINESCU, PK

### [UUID](uuid)
UUID (aka GUID) erzeugt einen (nahezu garantiert) universell eindeutigen Schlüssel.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/uuid/README.md), MARINESCU, PK

### [Hashwertschlüssel (MUHAI)](hashwertschluessel)
MUHAI (Mostly Unique Hashed Attributes Identifier) erzeugt einen nahezu eindeutigen Schlüssel durch das Hashen eines oder mehrerer Datensatzattribute.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/muhai/README.md), PK

