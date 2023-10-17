---
title: Coarse-Grained Lock
permalink: /patterns/persistenz/coarsegrainedlock
sidebar:
    nav: persistenz
---

Es wird eine einzige Sperre für eine Menge von Objekten gesetzt, um diese gemeinsam zu sperren.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/coarsegrainedlock/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/coarsegrainedlock/coarse_grained_lock_cn.png)


#### Beispiel

Im Beispiel hat ein Kunde eine Menge von Adressen und eine Menge von Bestellungen.

![](/images/patterns/coarsegrainedlock/coarse_grained_lock_cx.png)

Die grobkörnige Sperre stellt sicher, dass immer die Gesamtheit der Entitäten zu einem Kunden gesperrt werden, wenn eines bearbeitet wird.

![](/images/patterns/coarsegrainedlock/coarse_grained_lock_dx.png)

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()