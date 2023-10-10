---
title: Patterns
layout: single
permalink: /patterns
header:
  overlay_image: /images/farb_header_patterns.png
excerpt: "**Online-Material zu Patterns kompakt**"

sidebar:
  nav: patterns
---

Hier möchten wir unseren Lesern weitere Diagramme, Beispielszenarien und [Codebeispiele](#codebeispiele) zur Verfügung stellen, für die im Buch kein Raum ist.

Das Material ist nach dem Motto *einsteigen und losfahren* aufgebaut. Nur selten gibt es Abhängigkeiten zwischen den Beispielen, so dass Sie sich auf ein Pattern konzentrieren können.
Ganz bewusst haben wir jeweils ein anderes Szenario als im Buch gewählt.
Das soll Ihnen die Möglichkeit geben, das Muster noch einmal aus einem anderen Blickwinkel zu betrachten.

Jedes Pattern ist lauffähig in Form eines Testcases. Spielen Sie mit den Log-Leveln, oder führen Sie weitere Debug-Ausgaben ein, wenn Ihnen etwas unklar sein sollte. Denken Sie auch ruhig mal darüber nach, ob das jeweils demonstrierte Pattern in dem Szenario der Weißheit letzter Schluss ist, oder ob ein anderes vielleicht besser passen würde!

Wir laden Sie zum Ausprobieren, Experimentieren und Kritisieren ein. Berichten Sie uns von Ihren Erfahrungen und wo Sie Entwurfsmuster bereits erfolgreich anwenden konnten.

Viel Erfolg und vor allem Spaß bei Ihrer Arbeit!



<h2 id="codebeispiele"> Code-Beispiele </h2>

Neben der Möglichkeit, sich die API der Klassen mit verlinktem Source-Code online anzuschauen, können Sie das Projekt mit den Codebeispielen hier herunterladen:

[Download pk-examples.zip](/downloads/pk-examples.zip)  

*Ältere Versionen*:

* [Download pk-examples_j6.zip](/downloads/pk-examples_j6.zip) (2012, JDK 6)
* [Download pk-examples_j7.zip](/downloads/pk-examples_j7.zip) (2014, JDK 7)
* [Download pk-examples_j11.zip](/downloads/pk-examples_j11.zip) (2019, JDK 11) 


Es hat sich zum Standard entwickelt, viele Basisfunktionaliäten mit Bibliotheken abzudecken, die als externe Dependencies deklariert und aus Repositories geladen werden.
Bis einschließlich Java 7 haben wir noch versucht, ohne solche zusätzlichen Abhängigkeiten auszukommen, weil das für Neulinge die Hürden erhöht, Beispiele einfach mal auszuprobieren.

Mittlerweile wird ein solcher Insel-Entwicklungsansatz aber immer schwieriger (verschlanktes JDK) und ist zunehmend fragwürdig, weil er einfach *Best Practices* widerspricht.
Daher sind die Code-Beispiele jetzt als Maven-Projekt umgesetzt und setzen neben dem JDK 15 eine funktionierende Maven-Installation voraus.

Neben dem Archiv mit den Sourcen benötigen Sie:
* Java Platform (JDK) 15 (z.B. OpenJDK)
* Apache Maven (3.6.3 oder neuer) 

Zu empfehlen ist eine IDE wie [Eclipse](https://www.eclipse.org/).   
Wir haben außerdem [SonarLint](https://www.sonarsource.com/products/sonarlint/) im Einsatz.



<i class="fa-solid fa-globe orange-text fa-xl"></i>  
Documentation on this page is in German. However, I have documented each demonstrated pattern as well in English language using [Markdown](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
All comments in the source code are anyway in English language.

The git-repository (and thus the English markdown documentation) can be found [on GitHub](https://github.com/KarlEilebrecht/patterns-kompakt-code).



## Das Letzte
Kennen Sie die *Pattern-Wette des Teufels*?
Die Legende besagt, dass der Teufel (bildet sich 666 Stunden pro Tag weiter) irgendwann feststellte, dass es bei Entwurfsmustern viele Details zu beachten gibt. *"Details klingt gut"*, grinste er, *"da stecke ich drin!"*
Seitdem erscheint er vielen Entwicklern im Traum *"Wetten, dass Du es nicht schaffst, das folgende Pattern in Deinem aktuellen Projekt einzusetzen? Falls doch, sollst Du berühmt werden, anderfalls wird das Projekt mein sein!"*  

Diese Wette gewinnt fast immer der Teufel - *so oder so ...*