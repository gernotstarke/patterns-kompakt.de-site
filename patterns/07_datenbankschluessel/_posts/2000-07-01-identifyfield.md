---
title: Identity Field
permalink: /patterns/datenbankschluessel/identityfield
sidebar:
    nav: datenbankschluessel
---

Eine Schlüsselklasse fasst die Spalten eines Datenbankschlüssels in einem Objekt zusammen. Damit wird die Identität zwischen Laufzeitobjekten (in-memory objects) und Datensätzen sichergestellt.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identityfield/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

#### Beispiel

Das abstrakte Beispiel zeigt eine Entität (Tabelle T_ENTITY) mit einem zweiteiligen Primärschlüssel (*PK_FIELD1* und *PK_FIELD2*).
Die zugehörige *Entity* refenziert einen *CompoundKey* in ihrem *IdentityField* **id**.

![](/images/patterns/identityfield/identity_field_cx.png)

Hier sehen sie den dynamischen Ablauf:

![](/images/patterns/identityfield/identity_field_dx.png)

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()