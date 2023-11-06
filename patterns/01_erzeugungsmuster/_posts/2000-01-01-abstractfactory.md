---
title: Abstract Factory
permalink: /patterns/erzeugungsmuster/abstractfactory
sidebar:
    nav: erzeugungsmuster
---

Es wird eine Schnittstelle bereitgestellt, um Familien verbundener oder abhängiger Objekte zu erstellen, ohne die konkreten Klassen zu spezifizieren.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/abstractfactory/README.md), [GOF](/literature#gof), [STEMA](/literature#stema), [PK](/literature#pk)


#### Klassendiagramm

![](/images/patterns/abstractfactory/abstract_factory_cn.png)

#### Beispiel

Als Beispiel dient uns ein Szenario, in dem Daten entweder verschlüsselt oder unverschlüsselt abgelegt werden.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 1110 578">
  <image width="1110" height="578" xlink:href="/images/patterns/abstractfactory/abstract_factory_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/AbstractDataManager.java">
    <rect x="166" y="156" fill="#fff" opacity="0" width="273" height="88"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/SecureFileDataManager.java">
    <rect x="26" y="280" fill="#fff" opacity="0" width="271" height="89"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/PlainFileDataManager.java">
    <rect x="311" y="278" fill="#fff" opacity="0" width="274" height="90"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/AbstractDataReader.java">
    <rect x="752" y="36" fill="#fff" opacity="0" width="171" height="85"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/PlainFileDataReader.java">
    <rect x="649" y="158" fill="#fff" opacity="0" width="172" height="88"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/SecureFileDataReader.java">
    <rect x="857" y="158" fill="#fff" opacity="0" width="169" height="86"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/AbstractDataWriter.java">
    <rect x="753" y="279" fill="#fff" opacity="0" width="168" height="89"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/PlainFileDataWriter.java">
    <rect x="649" y="406" fill="#fff" opacity="0" width="169" height="85"></rect>
  </a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/abstractfactory/SecureFileDataWriter.java">
    <rect x="854" y="405" fill="#fff" opacity="0" width="173" height="86"></rect>
  </a>
</svg>


Das Schreiben erledigen *DataWriter*, für das Lesen sind *DataReader* zuständig.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/abstractfactory)