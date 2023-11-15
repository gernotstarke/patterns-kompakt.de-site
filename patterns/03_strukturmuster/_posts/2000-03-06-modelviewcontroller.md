---
title: Model View Controller
permalink: /patterns/strukturmuster/modelviewcontroller
sidebar:
    nav: strukturmuster
---

Die Verantwortlichkeiten beim Aufbau von Benutzerschnittstellen werden auf drei verschiedene Rollen verteilt, um die unterschiedliche Präsentation derselben Information zu erleichtern.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/modelviewcontroller/README.md), [STEMA](/literature#stema), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/modelviewcontroller/model_view_controller_cn.png)

#### Beispiel

Das Beispiel zeigt eine kleine Team-Manager-Applikation für den örtlichen Sportclub.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 651 398">
<image width="651" height="398" xlink:href="/images/patterns/modelviewcontroller/model_view_controller_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/modelviewcontroller/TeamView.java">
<rect x="25" y="223" fill="#fff" opacity="0" width="184" height="40"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/modelviewcontroller/TeamController.java">
<rect x="281" y="224" fill="#fff" opacity="0" width="183" height="40"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/modelviewcontroller/TeamModel.java">
<rect x="152" y="318" fill="#fff" opacity="0" width="185" height="40"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/modelviewcontroller/TeamModel.java#L141">
<rect x="459" y="107" fill="#fff" opacity="0" width="167" height="55"></rect>
</a>
</svg>

Die implementierte Variante wird *Passive View* genannt.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/modelviewcontroller)