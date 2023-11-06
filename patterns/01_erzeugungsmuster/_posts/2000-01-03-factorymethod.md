---
title: Factory Method
permalink: /patterns/erzeugungsmuster/factorymethod
sidebar:
    nav: erzeugungsmuster
---


Es wird eine Schnittstelle für die Erzeugung von Objekten definiert. Die Entscheidung, welche konkrete Klasse zu instanziieren, zu konfigurieren und schließlich zurückzugeben ist, wird konkreten (Unter-)Klassen überlassen, die diese Schnittstelle implementieren.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/factorymethod/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/factorymethod/factory_method_cn.png)

#### Beispiel

Im Beispiel betrachten wir eine Shop-Software, die sowohl von *Moron Store Worldwide* als auch von *Mrs. Freakly* genutzt wird, die einen (sehr erfolgreichen) Tante-Emma-Laden in Chicago betreibt.
In beiden Fällen werden Gutscheine für die Kunden benötigt.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 762 547">
<image width="762" height="547" xlink:href="/images/patterns/factorymethod/factory_method_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/factorymethod/AbstractVoucherCreator.java">
<rect x="24" y="35" fill="#fff" opacity="0" width="290" height="94"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/factorymethod/AbstractVoucher.java">
<rect x="524" y="35" fill="#fff" opacity="0" width="210" height="164"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/factorymethod/MoronStoreVoucherCreator.java">
<rect x="96" y="259" fill="#fff" opacity="0" width="290" height="97"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/factorymethod/MoronStoreVoucher.java">
<rect x="483" y="261" fill="#fff" opacity="0" width="196" height="93"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/factorymethod/FreakliesShopVoucherCreator.java">
<rect x="26" y="403" fill="#fff" opacity="0" width="288" height="97"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/factorymethod/FreakliesShopVoucher.java">
<rect x="538" y="404" fill="#fff" opacity="0" width="196" height="94"></rect>
</a>
</svg>

Da sich die Gutscheine und ihre Erzeugung recht stark unterscheiden, wurde das *Factory Method*-pattern eingesetzt.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/factorymethod)