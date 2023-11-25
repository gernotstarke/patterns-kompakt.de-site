---
title: Sequence Block
permalink: /patterns/datenbankschluessel/sequenceblock
sidebar:
    nav: datenbankschluessel
---

Ein Sequenzblock erzeugt auf performante und portable Weise Primärschlüssel für persistente Objekte.

> siehe: [GitHub - ReadMe](https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/test/java/de/calamanari/pk/sequenceblock/README.md), [MARINESCU](/literature#marinescu), [PK](/literature#pk)

### Klassendiagramm

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 667 296">
<image width="667" height="296" xlink:href="/images/patterns/sequenceblock/sequence_block_cn.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/sequenceblock/SequenceBlockCache.java">
<rect x="216" y="35" fill="#fff" opacity="0" width="195" height="82"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/sequenceblock/SequenceBlock.java">
<rect x="216" y="187" fill="#fff" opacity="0" width="195" height="83"></rect>
</a>
</svg>

### Sequenzdiagramm

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 766 467">
<image width="766" height="467" xlink:href="/images/patterns/sequenceblock/sequence_block_dn.png"></image> <a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/sequenceblock/SequenceBlockCache.java">
<rect x="183" y="0" fill="#fff" opacity="0" width="112" height="467"></rect>
</a><a xlink:href="https://github.com/KarlEilebrecht/patterns-kompakt-code/blob/main/src/main/java/de/calamanari/pk/sequenceblock/SequenceBlock.java">
<rect x="466" y="0" fill="#fff" opacity="0" width="90" height="467"></rect>
</a>
</svg>

Um das Zusammenspiel im Detail beobachten zu können, setzen Sie den log-level auf DEBUG in der logback.xml und führen den zugehörigen TestCase aus.

#### Ressourcen

> * [Quellcode (Projekt zum Download)](/patterns#codebeispiele)
> * [GitHub - Sourcecode](https://github.com/KarlEilebrecht/patterns-kompakt-code/tree/main/src/main/java/de/calamanari/pk/sequenceblock)