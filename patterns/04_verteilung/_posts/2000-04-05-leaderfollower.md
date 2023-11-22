---
title: Leader-Follower
permalink: /patterns/verteilung/leaderfollower
sidebar:
    nav: verteilung
---

Unabhängige Teilaufgaben innerhalb einer Serviceimplementierung werden in separaten Threads ausgeführt (divide and conquer), um nicht-funktionale Anforderungen (i. d. R. Performance) besser zu erfüllen.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/leaderfollower/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/leaderfollower/leader_follower_dn.png)

#### Beispiel

Im Beispiel wollen wir prüfen, ob ein String ein Palindrom ist, also z.B. aBBa.
Die Aufgabe ist sehr einfach, es muss lediglich geprüft werden, ob ein Text von links nach rechts bzw. von rechts nach links gelesen identisch aussieht.
Wenn man jedoch von UTF-8-kodierten Palindromen mit mehreren 100 Millionen Zeichen ausgeht, wird es interessant.
Bei heutigen Rechnern kann man natürlich immer noch die ganze Datei in den Speicher pumpen und naiv vergleichen. Mit *Leader-Follower* geht es aber effizienter.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 1122 762">
<image width="1122" height="762" xlink:href="/images/patterns/leaderfollower/leader_follower_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckLeader.java">
<rect x="384" y="41" fill="#fff" opacity="0" width="495" height="103"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckFuture.java">
<rect x="692" y="291" fill="#fff" opacity="0" width="391" height="233"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckResult.java">
<rect x="35" y="291" fill="#fff" opacity="0" width="326" height="162"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckFollowerTask.java">
<rect x="385" y="615" fill="#fff" opacity="0" width="494" height="101"></rect>
</a>
</svg>

Der *Leader* teilt die Aufgabe in Häppchen, deren Abarbeitung *Followers* obliegt.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 1122 783">
<image width="1122" height="783" xlink:href="/images/patterns/leaderfollower/leader_follower_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckLeader.java">
<rect x="223" y="0" fill="#fff" opacity="0" width="141" height="783"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckFuture.java">
<rect x="470" y="0" fill="#fff" opacity="0" width="126" height="783"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckFollowerTask.java">
<rect x="751" y="0" fill="#fff" opacity="0" width="143" height="783"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/leaderfollower/PalindromeCheckResult.java">
<rect x="945" y="0" fill="#fff" opacity="0" width="124" height="783"></rect>
</a>
</svg>

Aus den Teilergebnissen der *Followers* leitet der *Leader* das Gesamtergebnis ab.

Übrigens implementiert der *IndexedTextFileAccessor*, den der *Leader* intern zur Vorbereitung nutzt, selbst ebenfalls das *Leader-Follower*-Pattern.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/leaderfollower)