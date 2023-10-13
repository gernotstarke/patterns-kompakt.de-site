---
title: Flyweight
permalink: /patterns/strukturmuster/flyweight
sidebar:
    nav: strukturmuster
---

Um in einem System eine sehr große Anzahl feingranularer Objekte zu verwalten, wird die gemeinsame Nutzung von Instanzen (instance sharing) eingeführt.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/flyweight/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/flyweight/flyweight_cn.png)

#### Beispiel

Im Beispiel werden Instanzen eines speziell initialisierten Zählers sehr häufig benötigt.

![](/images/patterns/flyweight/flyweight_cx.png)

Nachdem *intrinsic* und *extrinsic state* identifiziert wurden, ist es möglich, die Objekte konkurrierend zu verwenden und so die gleichzeitig im System vorhandene Anzahl Instanzen zu reduzieren.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()