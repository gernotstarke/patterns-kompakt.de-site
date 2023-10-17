---
title: Depency Injection
permalink: /patterns/integration/dependencyinjection
sidebar:
    nav: integration
---

Es soll eine Entkopplung von nutzenden Komponenten und konfigurierten Diensten erreicht werden, bei der die Komponenten weder wissen müssen, wie die Dienste heißen, noch wie sie zu beschaffen sind.

> siehe: [GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/dependencyinjection/README.md), [DI](/literature#di), [PK](/literature#pk)


![](/images/patterns/dependencyinjection/dependency_injection_cn.png)

![](/images/patterns/dependencyinjection/dependency_injection_dn.png)

#### Beispiel

Das *PrintService*-Beispiel zeigt die 3 von *Martin Fowler* identifizierten Arten der Dependency Injection.

![](/images/patterns/dependencyinjection/dependency_injection_cx.png)

Unten sehen sie ein Sequenzdiagramm der *Setter-Injection*.
Annotierte Attribute, wie sie heute häufig anzutreffen sind, fallen ebenfalls in diese Kategorie, getreu dem *Uniform Access Principle*.

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [JavaDoc (API mit Quelltext online verlinkt)]()