---
title: Combined Method
permalink: /patterns/verteilung/combinedmethod
sidebar:
    nav: verteilung
---

Mehrere Methodenaufrufe werden in einer neuen Methode des Komponenteninterfaces zusammengefasst, um Aufrufreihenfolgen, Transaktionssicherheit bzw. Fehlerbehandlung besser gewährleisten zu können.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/combinedmethod/README.md), [POSA4](/literature#posa4), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/combinedmethod/combined_method_dn.png)

#### Beispiel

Im Beispiel haben wir es mit einer *ProductManager*-Schnittstelle zu tun.
Produkte werden erzeugt und dann registriert.
Ursprünglich gab es nur einen Server, die gemeinsame Transaktionalität war gewährleistet.
Das hat sich zwischenzeitlich geändert.

![](/images/patterns/combinedmethod/combined_method_px.png)

*Combined Method* erledigt hier Erzeugung und Registrierung aus Sicht des Clients als eine Operation.

![](/images/patterns/combinedmethod/combined_method_dx.png)

Die Methode *combinedCreateAndRegisterProduct(...)* wird entweder vollständig erfolgreich ausgeführt oder gar nicht (keine halben Sachen).

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()