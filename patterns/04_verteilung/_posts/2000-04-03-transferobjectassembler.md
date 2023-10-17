---
title: Transfer Object Assembler
permalink: /patterns/verteilung/transferobjectassembler
sidebar:
    nav: verteilung
---

Transferobjekte, die Daten mehrerer Geschäftsobjekte beinhalten, werden serverseitig von einem Assembler zusammengestellt, um die Schnittstelle zum Client zu vereinfachen und die Performance zu erhöhen.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/transferobjectassembler/README.md), [J2EE](/literature#j2ee), [PK](/literature#pk)

#### Sequenzdiagramm

![](/images/patterns/transferobjectassembler/transfer_object_assembler_dn.png)

#### Beispiel

Im Beispiel kann ein Client Nicht-Zahler-Informationen abrufen.

![](/images/patterns/transferobjectassembler/transfer_object_assembler_cx.png)

Jeder Eintrag enthält Metadaten aus *CustomerEntity* und *AdressEntity* aber auch Daten aus dem DWH.
Der *GeoBadPayerInfoDtoAssembler* stellt die erforderlichen Daten vor der Übertragung zum Client zusammen.

![](/images/patterns/transferobjectassembler/transfer_object_assembler_dx.png)

Der Client bekommt konzentrierte Daten in Form von *GeoBadPayerInfoDtos*.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()