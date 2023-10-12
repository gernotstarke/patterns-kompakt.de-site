---
title: Command Processor
permalink: /patterns/verhaltensmuster/commandprocessor
sidebar:
    nav: verhaltensmuster
---

Command Processor trennt Ausführung und Management von Command-Objekten.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/commandprocessor/README.md), [POSA](/literature#posa), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/commandprocessor/command_processor_cn.png)

#### Beispiel

Das Beispiel zeigt einen kleinen Textprozessor.

![](/images/patterns/commandprocessor/command_processor_cx.png)

Jede Texteingabe und jede Löschoperation entspricht einem *Command*, das durch den *Command Processor* entgegengenommen und verwaltet wird.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.
#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()