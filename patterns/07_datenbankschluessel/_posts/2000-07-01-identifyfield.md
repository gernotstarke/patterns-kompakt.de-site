---
title: Identity Field
permalink: /patterns/datenbankschluessel/identityfield
sidebar:
    nav: datenbankschluessel
---

Eine Schlüsselklasse fasst die Spalten eines Datenbankschlüssels in einem Objekt zusammen. Damit wird die Identität zwischen Laufzeitobjekten (in-memory objects) und Datensätzen sichergestellt.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identityfield/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

#### Beispiel

Das abstrakte Beispiel zeigt eine Entität (Tabelle T_ENTITY) mit einem zweiteiligen Primärschlüssel (*PK_FIELD1* und *PK_FIELD2*).
Die zugehörige *Entity* refenziert einen *CompoundKey* in ihrem *IdentityField* **id**.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 482 498">
<image width="482" height="498" xlink:href="/images/patterns/identityfield/identity_field_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/Entity.java">
<rect x="279" y="241" fill="#fff" opacity="0" width="116" height="71"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/DataManager.java">
<rect x="25" y="240" fill="#fff" opacity="0" width="117" height="71"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/CompoundKey.java">
<rect x="215" y="35" fill="#fff" opacity="0" width="243" height="146"></rect>
</a>
</svg>

Hier sehen sie den dynamischen Ablauf:

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 815 778">
<image width="815" height="778" xlink:href="/images/patterns/identityfield/identity_field_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/DataManager.java">
<rect x="168" y="0" fill="#fff" opacity="0" width="90" height="778"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/Entity.java">
<rect x="305" y="0" fill="#fff" opacity="0" width="59" height="778"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/CompoundKey.java">
<rect x="389" y="0" fill="#fff" opacity="0" width="90" height="778"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/Entity.java">
<rect x="520" y="0" fill="#fff" opacity="0" width="51" height="778"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/CompoundKey.java">
<rect x="600" y="0" fill="#fff" opacity="0" width="90" height="778"></rect>
</a>
</svg>

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identityfield/)