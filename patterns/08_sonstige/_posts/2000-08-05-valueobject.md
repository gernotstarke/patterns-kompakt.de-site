---
title: Value Object
permalink: /patterns/sonstige/valueobject
sidebar:
    nav: sonstige
---

Die Vergleichsoperation einfacher Objekte wird durch eine neue ersetzt, die auf den Attributwerten und nicht auf der Objektidentität basiert.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/valueobject/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Beispiel

Im Beispiel betreiben wir ein wenig Bruchrechnung, ganz so, wie Sie das noch aus der Schule kennen.
Ein Bruch wird dabei durch eine *Fraction*-Instanz repräsentiert. Mit diesen Instanzen können Clients rechnen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 440 316">
<image width="440" height="316" xlink:href="/images/patterns/valueobject/value_object_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/valueobject/Fraction.java">
<rect x="25" y="35" fill="#fff" opacity="0" width="218" height="254"></rect>
</a>
</svg>

Das Ergebnis einer Kalkulation drückt sich in einer neuen *Fraction*-Instanz aus.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 597 528">
<image width="597" height="528" xlink:href="/images/patterns/valueobject/value_object_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/valueobject/Fraction.java">
<rect x="194" y="0" fill="#fff" opacity="0" width="90" height="528"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/valueobject/Fraction.java">
<rect x="339" y="0" fill="#fff" opacity="0" width="90" height="528"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/valueobject/Fraction.java">
<rect x="475" y="0" fill="#fff" opacity="0" width="90" height="528"></rect>
</a>
</svg>

*Fraction*-Instanzen sind *immutable*, ihre Attribute bzw. ihr Wert ändert sich nie.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.
Beachten Sie, wie die Identität *(fraction1.equals(fraction2))* definiert ist!

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/valueobject)