---
title: Identity Map
permalink: /patterns/persistenz/identitymap
sidebar:
    nav: persistenz
---

Eine Identity Map verwaltet Objekte, die aus einer Datenbank gelesen und möglicherweise verändert werden und stellt sicher, dass Objekte nie mehr als einmal aus der Datenbank gelesen werden.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/identitymap/README.md), [PEAA](/literature#peaa), [PK](/literature#pk)

### Klassendiagramm

![](/images/patterns/identitymap/identity_map_cn.png)

### Sequenzdiagramm

![](/images/patterns/identitymap/identity_map_dn.png)

#### Beispiel

Im Beispiel nutzen Clients einen *DataManager*, um mit Entitäten zu arbeiten.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 717 502">
<image width="717" height="502" xlink:href="/images/patterns/identitymap/identity_map_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/DataManager.java">
<rect x="29" y="36" fill="#fff" opacity="0" width="239" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/Database.java">
<rect x="345" y="36" fill="#fff" opacity="0" width="247" height="27"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/Session.java">
<rect x="345" y="83" fill="#fff" opacity="0" width="248" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/IdentityMap.java">
<rect x="346" y="220" fill="#fff" opacity="0" width="245" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/Entity.java">
<rect x="345" y="357" fill="#fff" opacity="0" width="138" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/CustomerEntity.java">
<rect x="555" y="319" fill="#fff" opacity="0" width="136" height="76"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/identitymap/AddressEntity.java">
<rect x="555" y="402" fill="#fff" opacity="0" width="137" height="75"></rect>
</a>
</svg>

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/identitymap)