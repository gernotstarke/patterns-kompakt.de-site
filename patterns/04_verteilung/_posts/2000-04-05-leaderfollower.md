---
title: Leader-Follower
permalink: /patterns/verteilung/leaderfollower
sidebar:
    nav: verteilung
---

Unabhängige Teilaufgaben innerhalb einer Serviceimplementierung werden in separaten Threads ausgeführt (divide and conquer), um nicht-funktionale Anforderungen (i. d. R. Performance) besser zu erfüllen.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/masterslave/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/leaderfollower/leader_follower_dn.png)

#### Beispiel

Im Beispiel wollen wir prüfen, ob ein String ein Palindrom ist, also z.B. aBBa.
Die Aufgabe ist sehr einfach, es muss lediglich geprüft werden, ob ein Text von links nach rechts bzw. von rechts nach links gelesen identisch aussieht.
Wenn man jedoch von UTF-8-kodierten Palindromen mit mehreren 100 Millionen Zeichen ausgeht, wird es interessant.
Bei heutigen Rechnern kann man natürlich immer noch die ganze Datei in den Speicher pumpen und naiv vergleichen. Mit *Leader-Follower* geht es aber effizienter.

![](/images/patterns/leaderfollower/leader_follower_cx.png)

Der *Leader* teilt die Aufgabe in Häppchen, deren Abarbeitung *Followers* obliegt.

![](/images/patterns/leaderfollower/leader_follower_dx.png)

Aus den Teilergebnissen der *Followers* leitet der *Leader* das Gesamtergebnis ab.

Übrigens implementiert der *IndexedTextFileAccessor*, den der *Leader* intern zur Vorbereitung nutzt, selbst ebenfalls das *Leader-Follower*-Pattern.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()