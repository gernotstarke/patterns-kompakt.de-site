---
title: Template Method
permalink: /patterns/verhaltensmuster/templatemethod
sidebar:
    nav: verhaltensmuster
---

Template Method definiert die Struktur eines Algorithmus, wobei einzelne konkrete Schritte in Unterklassen verlagert werden. Das Muster erlaubt es, bestimmte Operationen eines Algorithmus zu überschreiben, ohne des Struktur zu ändern.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/templatemethod/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/templatemethod/template_method_cn.png)

#### Beispiel

Zu sehen sind gleich zwei Beispiele.
Das einfachere Beispiel ist ein String-Codec, von dem es mehrere konkrete Ableitungen geben könnte.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 640 580">
<image width="640" height="580" xlink:href="/images/patterns/templatemethod/template_method_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/templatemethod/AbstractTemplateMethodStringCodec.java">
<rect x="27" y="36" fill="#fff" opacity="0" width="239" height="114"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/templatemethod/ExampleTemplateMethodStringCodec.java">
<rect x="27" y="196" fill="#fff" opacity="0" width="236" height="97"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/templatemethod/EchoServer.java">
<rect x="330" y="473" fill="#fff" opacity="0" width="286" height="82"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/util/AbstractConsoleServer.java">
<rect x="331" y="34" fill="#fff" opacity="0" width="285" height="191"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/util/AbstractThreadedSocketServer.java">
<rect x="331" y="266" fill="#fff" opacity="0" width="286" height="169"></rect>
</a>
</svg>

Etwas komplexer - aber auch interessanter - ist ein kleiner Echo-Server, der das Muster *Template Method* nutzt, um spezifische Schritte in konkrete Unterklassen zu verlagern.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.   
Die Ausgaben des automatisch im Hintergrund gestarteten Echo-Servers werden umgeleitet und gemeinsam mit den Ausgaben des TestCase in der Konsole angezeigt.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/templatemethod)