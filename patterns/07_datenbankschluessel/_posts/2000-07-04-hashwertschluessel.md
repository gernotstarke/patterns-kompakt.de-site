---
title: Hashwertschlüssel (MUHAI)
permalink: /patterns/datenbankschluessel/hashwertschluessel
sidebar:
    nav: datenbankschluessel
---

MUHAI (Mostly Unique Hashed Attributes Identifier) erzeugt einen nahezu eindeutigen Schlüssel durch das Hashen eines oder mehrerer Datensatzattribute.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/muhai/README.md), [PK](/literature#pk)

### Beispiel

Die Firma Multiglom Smart Business, Anbieter der Web Shop Suite WANNAWEB, möchte die Analysefunktionen der Software erweitern. Anstatt die Abfragen direkt auf den Tabellen des Shops laufen zu lassen, wurde ein neues DWH-Schema ergänzt, das regelmäßig aktualisiert wird. Jeden Tag sollen einige Millionen Sätze aus unterschiedlichen Quellen importiert werden.  

Während man für andere Daten jeweils einen Record-Identifikator gefunden hat, der als PK genutzt werden kann, steht das Team bei einem Import vor einem Problem. Der logische Key eines Datensatzes besteht aus einer Komposition mehrerer Felder.

![](/images/patterns/muhai/muhai_dx.png)

Würde man diesen Key als Composite-PK definieren, gäbe es einerseits erhebliche Performance-Probleme, und andererseits wäre der Umgang mit den Composite-Keys bei Abfragen eine ziemliche Qual.

Um das Problem zu lösen, wird zunächst ein kryptographischer Hashwert (hier SHA1) über die Attributwerte gebildet, die den Datensatz identifizieren. Ein Teil des Hashes (z.B. die ersten 64 bits) wird in einen INT64-Bit-Integer-Wert konvertiert.

![](/images/patterns/muhai/muhai_cx.png)

![](/images/patterns/muhai/muhai_ex.png)

Nun haben die Keys in der Datenbank den Typ INT64 und sind sowohl für Maschine als auch Mensch gut verträglich. Die Kollisionswahrscheinlichkeit ist sehr niedrig, Kollisionen können aber prinzipiell auftreten. MUHAIs eignen sich daher für alle Szenarien, in denen wenige Kollisionen irrelevant sind oder bei denen man (durch Simulation aller möglichen Keys) vorab garantieren kann, dass keine Kollisionen auftreten werden.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus. Ein kleines Toolkit erlaubt zudem, mehrere Milliarden von Schlüsseln zu generieren und auf Kollisionen hin zu prüfen. Eine Implementierung der Schätzfunktion aus dem Buch finden Sie dort auch.

### Das Bloom-Filter-Experiment

Basierend auf dem gleichen Prinzip der Ausnutzung besonderer Eigenschaften kryptographischer Hashes habe ich einen experimentellen generischen [One-Hashing Bloom Filter (OHBF)](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/ohbf/README.md) implementiert. Dabei wurde die MUHAI-Hashing-Implementierung wiederverwendet.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()