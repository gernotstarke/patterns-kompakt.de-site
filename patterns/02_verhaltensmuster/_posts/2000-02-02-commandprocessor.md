---
title: Command Processor
permalink: /patterns/verhaltensmuster/commandprocessor
sidebar:
    nav: verhaltensmuster
---

Command Processor trennt Ausführung und Management von Command-Objekten.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/commandprocessor/README.md), [POSA](/literature#posa), [PK](/literature#pk)

#### Klassendiagramm

![](/images/patterns/commandprocessor/command_processor_cn.png)

#### Beispiel

Das Beispiel zeigt einen kleinen Textprozessor.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 800 343">
<image width="800" height="343" xlink:href="/images/patterns/commandprocessor/command_processor_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/commandprocessor/InputCommandProcessor.java">
<rect x="25" y="34" fill="#fff" opacity="0" width="250" height="97"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/command/InputCommand.java">
<rect x="364" y="34" fill="#fff" opacity="0" width="253" height="100"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/command/DeleteTextCommand.java">
<rect x="221" y="198" fill="#fff" opacity="0" width="253" height="98"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/command/AppendTextCommand.java">
<rect x="520" y="196" fill="#fff" opacity="0" width="250" height="99"></rect>
</a>
</svg>

Jede Texteingabe und jede Löschoperation entspricht einem *Command*, das durch den *Command Processor* entgegengenommen und verwaltet wird.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.
#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/commandprocessor)