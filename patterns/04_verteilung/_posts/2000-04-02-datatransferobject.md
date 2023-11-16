---
title: Data Transfer Object
permalink: /patterns/verteilung/datatransferobject
sidebar:
    nav: verteilung
---

Data Transfer Object (DTO) fasst in einer verteilten Umgebung (z. B. JEE) zu übertragende Daten in einem neuen Objekt zusammen, um die Anzahl der entfernten Methodenaufrufe zu reduzieren und somit das Netzwerk zu entlasten.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/datatransferobject/README.md), [J2EE](/literature#j2ee), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/datatransferobject/data_transfer_object_dn.png)

#### Beispiel

Im Beispiel erlaubt ein *CustomerManager* den Clients Zugriff auf *CustomerEntity*-Remote-Objekte.

![](/images/patterns/datatransferobject/data_transfer_object_px.png)

Bei direkter Verwendung der Entities durch den Client entstehen potenziell viele Netzwerkaufrufe. Daher wird ein CustomerDto eingeführt.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 703 455">
<image width="703" height="455" xlink:href="/images/patterns/datatransferobject/data_transfer_object_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/Customer.java">
<rect x="25" y="36" fill="#fff" opacity="0" width="159" height="208"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/CustomerRemote.java">
<rect x="237" y="35" fill="#fff" opacity="0" width="172" height="59"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/CustomerDto.java">
<rect x="237" y="183" fill="#fff" opacity="0" width="171" height="61"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/CustomerManager.java">
<rect x="352" y="308" fill="#fff" opacity="0" width="321" height="97"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/server/CustomerManagerServer.java">
<rect x="502" y="183" fill="#fff" opacity="0" width="171" height="60"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/server/CustomerEntity.java">
<rect x="503" y="34" fill="#fff" opacity="0" width="171" height="59"></rect>
</a>
</svg>

Die Daten zu einem Kunden werden nun in einem *gemeinsamen Call* übertragen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 711 602">
<image width="711" height="602" xlink:href="/images/patterns/datatransferobject/data_transfer_object_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/server/CustomerManagerServer.java">
<rect x="193" y="0" fill="#fff" opacity="0" width="134" height="602"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/server/CustomerEntity.java">
<rect x="425" y="0" fill="#fff" opacity="0" width="90" height="602"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject/CustomerDto.java">
<rect x="587" y="0" fill="#fff" opacity="0" width="92" height="602"></rect>
</a>
</svg>

Ein Client liest/schreibt die einzelnen Datenfelder lokal.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/datatransferobject)