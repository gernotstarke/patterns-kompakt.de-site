---
title: Value Object
permalink: /patterns/sonstige/valueobject
sidebar:
    nav: sonstige
---

Die Vergleichsoperation einfacher Objekte wird durch eine neue ersetzt, die auf den Attributwerten und nicht auf der Objektidentität basiert.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/valueobject/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Beispiel

Im Beispiel betreiben wir ein wenig Bruchrechnung, ganz so, wie Sie das noch aus der Schule kennen.
Ein Bruch wird dabei durch eine *Fraction*-Instanz repräsentiert. Mit diesen Instanzen können Clients rechnen.

![](/images/patterns/valueobject/value_object_cx.png)

Das Ergebnis einer Kalkulation drückt sich in einer neuen *Fraction*-Instanz aus.

![](/images/patterns/valueobject/value_object_dx.png)

*Fraction*-Instanzen sind *immutable*, ihre Attribute bzw. ihr Wert ändert sich nie.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.
Beachten Sie, wie die Identität *(fraction1.equals(fraction2))* definiert ist!

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()