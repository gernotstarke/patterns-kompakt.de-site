---
title: Service Stub
permalink: /patterns/sonstige/servicestub
sidebar:
    nav: sonstige
---

Ein Service Stub, auch bekannt als "Mock Object", stellt eine (Dummy-)Implementierung eines problematischen Services bereit.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/servicestub/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/servicestub/service_stub_cn.png)

### Beispiel

Das Beispiel zeigt einen *AccountManager*, der zur Laufzeit einen *AddressValidatorService* nutzen soll, um ungültige Adressen in unserem Datenbestand zu vermeiden.
Dummerweise steht die Adressvalidierung für Testzwecke nicht zur Verfügung.


<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 750 375">
<image width="750" height="375" xlink:href="/images/patterns/servicestub/service_stub_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/servicestub/AccountManager.java">
<rect x="25" y="35" fill="#fff" opacity="0" width="311" height="70"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/servicestub/Account.java">
<rect x="192" y="175" fill="#fff" opacity="0" width="145" height="54"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/servicestub/adrchk/AddressValidatorService.java">
<rect x="447" y="69" fill="#fff" opacity="0" width="252" height="90"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/servicestub/AddressValidatorServiceMock.java">
<rect x="447" y="264" fill="#fff" opacity="0" width="251" height="64"></rect>
</a>
</svg>

Der *AddressValidatorServiceMock* springt in die Bresche.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/servicestub)