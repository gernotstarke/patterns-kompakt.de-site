---
title: Depency Injection
permalink: /patterns/integration/dependencyinjection
sidebar:
    nav: integration
---

Es soll eine Entkopplung von nutzenden Komponenten und konfigurierten Diensten erreicht werden, bei der die Komponenten weder wissen müssen, wie die Dienste heißen, noch wie sie zu beschaffen sind.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/dependencyinjection/README.md), [DI](/literature#di), [PK](/literature#pk)


![](/images/patterns/dependencyinjection/dependency_injection_cn.png)

![](/images/patterns/dependencyinjection/dependency_injection_dn.png)

#### Beispiel

Das *PrintService*-Beispiel zeigt die 3 von *Martin Fowler* identifizierten Arten der Dependency Injection.

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 764 799">
<image width="764" height="799" xlink:href="/images/patterns/dependencyinjection/dependency_injection_cx.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/PrintServiceInjectable.java">
<rect x="403" y="121" fill="#fff" opacity="0" width="260" height="73"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/ComponentFramework.java">
<rect x="25" y="121" fill="#fff" opacity="0" width="259" height="72"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/ComponentWithInterfaceInjection.java">
<rect x="404" y="238" fill="#fff" opacity="0" width="259" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/ComponentWithSetterInjection.java">
<rect x="404" y="336" fill="#fff" opacity="0" width="259" height="73"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/Component.java">
<rect x="181" y="335" fill="#fff" opacity="0" width="140" height="73"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/ComponentWithConstructorInjection.java">
<rect x="405" y="433" fill="#fff" opacity="0" width="260" height="75"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/PrintService.java">
<rect x="404" y="557" fill="#fff" opacity="0" width="259" height="74"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/dependencyinjection/PrintServiceImpl.java">
<rect x="404" y="676" fill="#fff" opacity="0" width="258" height="72"></rect>
</a>
</svg>

Unten sehen sie ein Sequenzdiagramm der *Setter-Injection*.
Annotierte Attribute, wie sie heute häufig anzutreffen sind, fallen ebenfalls in diese Kategorie, getreu dem *Uniform Access Principle*.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/dependencyinjection)