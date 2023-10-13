---
title: Data Transfer Object
permalink: /patterns/verteilung/datatransferobject
sidebar:
    nav: verteilung
---

Data Transfer Object (DTO) fasst in einer verteilten Umgebung (z. B. JEE) zu übertragende Daten in einem neuen Objekt zusammen, um die Anzahl der entfernten Methodenaufrufe zu reduzieren und somit das Netzwerk zu entlasten.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/datatransferobject/README.md), [J2EE](/literature#j2ee), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/datatransferobject/data_transfer_object_dn.png)

#### Beispiel

Im Beispiel erlaubt ein *CustomerManager* den Clients Zugriff auf *CustomerEntity*-Remote-Objekte.

![](/images/patterns/datatransferobject/data_transfer_object_px.png)

Bei direkter Verwendung der Entities durch den Client entstehen potenziell viele Netzwerkaufrufe. Daher wird ein CustomerDto eingeführt.

![](/images/patterns/datatransferobject/data_transfer_object_cx.png)

Die Daten zu einem Kunden werden nun in einem *gemeinsamen Call* übertragen.

![](/images/patterns/datatransferobject/data_transfer_object_dx.png)

Ein Client liest/schreibt die einzelnen Datenfelder lokal.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()