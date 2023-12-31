---
title: Object Pool
permalink: /patterns/erzeugungsmuster/objectpool
sidebar:
    nav: erzeugungsmuster
---

Es wird die Wiederverwendung von Objektinstanzen ermöglicht, deren Erzeugung sehr teuer ist oder deren Anzahl beschränkt werden soll.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/objectpool/README.md), [SHTR](/literature#shtr), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/objectpool/object_pool_cn.png)

#### Sequenzdiagramm

![](/images/patterns/objectpool/object_pool_dn.png)

#### Beispiel

Neben einer abstrakten Beispielimplementierung mit künstlichem Payload finden Sie eine ThreadPool-Implementierung. Hier sind die Threads die teuren Objekte.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 556 313">
<image width="556" height="313" xlink:href="/images/patterns/objectpool/object_pool_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/objectpool/SimpleThreadPool.java">
<rect x="24" y="34" fill="#fff" opacity="0" width="232" height="92"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/objectpool/PoolThread.java">
<rect x="63" y="192" fill="#fff" opacity="0" width="158" height="93"></rect>
</a>
</svg>

Die Zeit eigener Thread-Pools in Java gehört zwar der Vergangenheit an, seit es das [Executors-Framework](https://docs.oracle.com/javase/8/docs/api/index.html?java/util/concurrent/package-summary.html) gibt.
Aber zur Veranschaulichung einer Pool-Variante taugt der Code noch.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/objectpool)