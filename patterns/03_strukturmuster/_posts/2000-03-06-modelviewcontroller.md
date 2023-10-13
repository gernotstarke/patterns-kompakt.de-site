---
title: Model View Controller
permalink: /patterns/strukturmuster/modelviewcontroller
sidebar:
    nav: strukturmuster
---

Die Verantwortlichkeiten beim Aufbau von Benutzerschnittstellen werden auf drei verschiedene Rollen verteilt, um die unterschiedliche Präsentation derselben Information zu erleichtern.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/modelviewcontroller/README.md), [STEMA](/literature#stema), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/modelviewcontroller/model_view_controller_cn.png)

#### Beispiel

Das Beispiel zeigt eine kleine Team-Manager-Applikation für den örtlichen Sportclub.

![](/images/patterns/modelviewcontroller/model_view_controller_cx.png)

Die implementierte Variante wird *Passive View* genannt.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()