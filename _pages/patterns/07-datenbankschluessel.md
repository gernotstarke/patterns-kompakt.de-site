---
title: Patterns
layout: single
permalink: /patterns/datenbankschluessel
header:
  overlay_image: /images/pk_header.webp
excerpt: "**Datenbankschlüssel**"

sidebar:
  nav: datenbankschluessel
---

### [Identity Field](/patterns/datenbankschluessel/identityfield)
Eine Schlüsselklasse fasst die Spalten eines Datenbankschlüssels in einem Objekt zusammen. Damit wird die Identität zwischen Laufzeitobjekten (in-memory objects) und Datensätzen sichergestellt.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identityfield/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### [Sequence Block](/patterns/datenbankschluessel/sequenceblock)
Sequenzblock erzeugt auf performante und portable Weise Primärschlüssel für persistente Objekte.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/sequenceblock/README.md), [MARINESCU](/literature#marinescu), [PK](/literature#pk)

### [UUID](/patterns/datenbankschluessel/uuid)
UUID (aka GUID) erzeugt einen (nahezu garantiert) universell eindeutigen Schlüssel.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/uuid/README.md), [MARINESCU](/literature#marinescu), [PK](/literature#pk)

### [Hashwertschlüssel (MUHAI)](/patterns/datenbankschluessel/hashwertschluessel)
MUHAI (Mostly Unique Hashed Attributes Identifier) erzeugt einen nahezu eindeutigen Schlüssel durch das Hashen eines oder mehrerer Datensatzattribute.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/muhai/README.md), [PK](/literature#pk)

