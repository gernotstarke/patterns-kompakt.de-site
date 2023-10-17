---
title: Master-Slave
permalink: /patterns/verteilung/masterslave
sidebar:
    nav: verteilung
---

Unabhängige Teilaufgaben innerhalb einer Serviceimplementierung werden in separaten Threads ausgeführt (divide and conquer), um nicht-funktionale Anforderungen (i. d. R. Performance) besser zu erfüllen.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/masterslave/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/masterslave/master_slave_dn.png)

#### Beispiel

Im Beispiel wollen wir prüfen, ob ein String ein Palindrom ist, also z.B. aBBa.
Die Aufgabe ist sehr einfach, es muss lediglich geprüft werden, ob ein Text von links nach rechts bzw. von rechts nach links gelesen identisch aussieht.
Wenn man jedoch von UTF-8-kodierten Palindromen mit mehreren 100 Millionen Zeichen ausgeht, wird es interessant.
Bei heutigen Rechnern kann man natürlich immer noch die ganze Datei in den Speicher pumpen und naiv vergleichen. Mit *Master-Slave* geht es aber effizienter.

![](/images/patterns/masterslave/master_slave_cx.png)

Der *Master* teilt die Aufgabe in Häppchen, deren Abarbeitung *Slaves* obliegt.

![](/images/patterns/masterslave/master_slave_dx.png)

Aus den Teilergebnissen der *Slaves* leitet der *Master* das Gesamtergebnis ab.

Übrigens implementiert der *IndexedTextFileAccessor*, den der *Master* intern zur Vorbereitung nutzt, selbst ebenfalls das *Master-Slave*-Pattern.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()