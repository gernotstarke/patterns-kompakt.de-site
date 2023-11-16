---
title: Transfer Object Assembler
permalink: /patterns/verteilung/transferobjectassembler
sidebar:
    nav: verteilung
---

Transferobjekte, die Daten mehrerer Geschäftsobjekte beinhalten, werden serverseitig von einem Assembler zusammengestellt, um die Schnittstelle zum Client zu vereinfachen und die Performance zu erhöhen.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/transferobjectassembler/README.md), [J2EE](/literature#j2ee), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/transferobjectassembler/transfer_object_assembler_dn.png)

#### Beispiel

Im Beispiel kann ein Client Nicht-Zahler-Informationen abrufen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 591 645">
<image width="591" height="645" xlink:href="/images/patterns/transferobjectassembler/transfer_object_assembler_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/GeoBadPayerInfoDtoAssembler.java">
<rect x="25" y="123" fill="#fff" opacity="0" width="290" height="66"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/CustomerEntity.java">
<rect x="378" y="35" fill="#fff" opacity="0" width="189" height="63"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/AddressEntity.java">
<rect x="379" y="123" fill="#fff" opacity="0" width="188" height="67"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/CustomerDwhInfoEntity.java">
<rect x="379" y="217" fill="#fff" opacity="0" width="189" height="65"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/GeoBadPayerInfoDto.java">
<rect x="378" y="318" fill="#fff" opacity="0" width="189" height="304"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/CustomerService.java">
<rect x="25" y="318" fill="#fff" opacity="0" width="292" height="95"></rect>
</a>
</svg>

Jeder Eintrag enthält Metadaten aus *CustomerEntity* und *AdressEntity* aber auch Daten aus dem DWH.
Der *GeoBadPayerInfoDtoAssembler* stellt die erforderlichen Daten vor der Übertragung zum Client zusammen.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 1236 965">
<image width="1236" height="965" xlink:href="/images/patterns/transferobjectassembler/transfer_object_assembler_dx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/CustomerService.java">
<rect x="226" y="0" fill="#fff" opacity="0" width="91" height="965"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/GeoBadPayerInfoDtoAssembler.java">
<rect x="419" y="0" fill="#fff" opacity="0" width="155" height="965"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/CustomerDwhInfoEntity.java">
<rect x="635" y="0" fill="#fff" opacity="0" width="116" height="965"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/CustomerEntity.java">
<rect x="769" y="0" fill="#fff" opacity="0" width="90" height="965"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/AddressEntity.java">
<rect x="872" y="0" fill="#fff" opacity="0" width="92" height="965"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/Database.java">
<rect x="974" y="0" fill="#fff" opacity="0" width="91" height="965"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler/GeoBadPayerInfoDto.java">
<rect x="1082" y="0" fill="#fff" opacity="0" width="105" height="965"></rect>
</a>
</svg>

Der Client bekommt konzentrierte Daten in Form von *GeoBadPayerInfoDtos*.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/transferobjectassembler)