---
title: Service Stub
permalink: /patterns/sonstige/servicestub
sidebar:
    nav: sonstige
---


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