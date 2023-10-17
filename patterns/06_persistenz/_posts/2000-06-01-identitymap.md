---
title: Identity Map
permalink: /patterns/persistenz/identitymap
sidebar:
    nav: persistenz
---

Eine Identity Map verwaltet Objekte, die aus einer Datenbank gelesen und möglicherweise verändert werden und stellt sicher, dass Objekte nie mehr als einmal aus der Datenbank gelesen werden.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identitymap/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/identitymap/identity_map_cn.png)

### Sequenzdiagramm

![](/images/patterns/identitymap/identity_map_dn.png)

#### Beispiel

Im Beispiel nutzen Clients einen *DataManager*, um mit Entitäten zu arbeiten.

![](/images/patterns/identitymap/identity_map_cx.png)

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()