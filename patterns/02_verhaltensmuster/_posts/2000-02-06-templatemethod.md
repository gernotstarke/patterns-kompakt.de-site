---
title: Template Method
permalink: /patterns/verhaltensmuster/templatemethod
sidebar:
    nav: verhaltensmuster
---

Template Method definiert die Struktur eines Algorithmus, wobei einzelne konkrete Schritte in Unterklassen verlagert werden. Das Muster erlaubt es, bestimmte Operationen eines Algorithmus zu überschreiben, ohne des Struktur zu ändern.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/templatemethod/README.md), [GOF](/literature#gof), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/templatemethod/template_method_cn.png)

#### Beispiel

Zu sehen sind gleich zwei Beispiele.
Das einfachere Beispiel ist ein String-Codec, von dem es mehrere konkrete Ableitungen geben könnte.

![](/images/patterns/templatemethod/template_method_cx.png)

Etwas komplexer - aber auch interessanter - ist ein kleiner Echo-Server, der das Muster *Template Method* nutzt, um spezifische Schritte in konkrete Unterklassen zu verlagern.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.   
Die Ausgaben des automatisch im Hintergrund gestarteten Echo-Servers werden umgeleitet und gemeinsam mit den Ausgaben des TestCase in der Konsole angezeigt.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()