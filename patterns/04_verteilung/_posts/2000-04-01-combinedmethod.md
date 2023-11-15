---
title: Combined Method
permalink: /patterns/verteilung/combinedmethod
sidebar:
    nav: verteilung
---

Mehrere Methodenaufrufe werden in einer neuen Methode des Komponenteninterfaces zusammengefasst, um Aufrufreihenfolgen, Transaktionssicherheit bzw. Fehlerbehandlung besser gewährleisten zu können.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/combinedmethod/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/combinedmethod/combined_method_dn.png)

#### Beispiel

Im Beispiel haben wir es mit einer *ProductManager*-Schnittstelle zu tun.
Produkte werden erzeugt und dann registriert.
Ursprünglich gab es nur einen Server, die gemeinsame Transaktionalität war gewährleistet.
Das hat sich zwischenzeitlich geändert.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 559 284">
<image width="559" height="284" xlink:href="/images/patterns/combinedmethod/combined_method_px.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/combinedmethod/ProductManager.java">
<rect x="352" y="80" fill="#fff" opacity="0" width="113" height="63"></rect>
</a>
</svg>

*Combined Method* erledigt hier Erzeugung und Registrierung aus Sicht des Clients als eine Operation.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 683 318">
<image width="683" height="318" xlink:href="/images/patterns/combinedmethod/combined_method_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/combinedmethod/Product.java">
<rect x="208" y="0" fill="#fff" opacity="0" width="92" height="318"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/combinedmethod/ProductManagerServer.java">
<rect x="395" y="0" fill="#fff" opacity="0" width="138" height="318"></rect>
</a>
</svg>

Die Methode *combinedCreateAndRegisterProduct(...)* wird entweder vollständig erfolgreich ausgeführt oder gar nicht (keine halben Sachen).

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/combinedmethod)