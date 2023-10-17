---
title: Service Stub
permalink: /patterns/sonstige/servicestub
sidebar:
    nav: sonstige
---

Ein Service Stub, auch bekannt als "Mock Object", stellt eine (Dummy-)Implementierung eines problematischen Services bereit.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/servicestub/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/servicestub/service_stub_cn.png)

### Beispiel

Das Beispiel zeigt einen *AccountManager*, der zur Laufzeit einen *AddressValidatorService* nutzen soll, um ungültige Adressen in unserem Datenbestand zu vermeiden.
Dummerweise steht die Adressvalidierung für Testzwecke nicht zur Verfügung.


![](/images/patterns/servicestub/service_stub_cx.png)

Der *AddressValidatorServiceMock* springt in die Bresche.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()