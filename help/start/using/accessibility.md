---
solution: Campaign Standard
product: campaign
title: Barrierefreiheit in Adobe Campaign Standard
description: Erfahren Sie mehr über die Unterstützung von Barrierefreiheit in Adobe Campaign Standard Workspace.
audience: designing
content-type: reference
topic-tags: accessibility
translation-type: tm+mt
source-git-commit: 6632216ce4697892ea08b32641c9c026482ca713
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 100%

---


# Barrierefreiheit in Adobe Campaign Standard {#accessibility-acs}

Erfahren Sie mehr über die Unterstützung von Barrierefreiheit in Adobe Campaign Standard Workspace.

Mit Funktionen der Barrierefreiheit sollen Produkte für Menschen mit visuellen, auditiven, kognitiven, motorischen und anderen Behinderungen nutzbar gemacht werden. Beispiele für Barrierefreiheitsfunktionen für Software-Produkte sind die Unterstützung von Bildschirmlesegeräten, Textäquivalente für Grafiken, Tastaturbefehle, die Änderung der Anzeigefarben auf hohen Kontrast usw.

Adobe Campaign Standard bietet einige Tools, die die Verwendung dieser Funktionen ermöglichen, z. B. Kontrast, Tastaturnavigation, kontextbezogene Hilfe und Responsive Resize.

## Barrierefreiheitsfunktionen {#accessibility-features}

### Kontrast {#contrast}

Es wurde versucht, in der Benutzeroberfläche von Adobe Campaign Standard genügend Kontrast bereitzustellen, um Benutzern mit Sehbehinderung oder eingeschränkter farblicher Wahrnehmungsfähigkeit ein barrierefreies Seherlebnis zu bieten.

* Die Symbole zum Anhalten und Abbrechen von Workflows wurden aktualisiert, um den Kontrast zwischen Hintergrund und Vordergrund zu verbessern.

   ![](assets/accessibility_1.png)

* Bei erfolgreichem Versand wurde großer, grüner Text angezeigt, der unzureichenden Kontrast zwischen Hintergrund und Vordergrund aufwies. Der Kontrast wurde mit einem Mindestverhältnis von 3:1 aktualisiert.

   ![](assets/accessibility_2.png)

* In Adobe Campaign Standard werden Informationen oder Hierarchie nicht allein durch Farbe, Form oder Position kommuniziert.

### Benutzeroberfläche {#user-interface}

Die Benutzeroberfläche von Adobe Campaign Standard ermöglicht die einfache Anzeige und Wiedergabe von Inhalten, u. a. durch die Trennung von Vordergrund und Hintergrund und das Hinzufügen alternativer Texte zu den verfügbaren Schaltflächen.

* Wenn der Benutzer ein erforderliches ID-Feld leer lässt, zeigt eine Grafik mit einem Fehlermeldungstext visuell an, welches Feld fehlerhaft ist.

   ![](assets/accessibility_3.png)

* Inhalte, die beim Bewegen des Mauszeigers oder beim Fokussieren angezeigt werden, können vom Benutzer verworfen werden und verdecken keine anderen Inhalte.

   ![](assets/accessibility_4.png)

* Es wurden alternative Texte für Bildschaltflächen hinzugefügt, die gelesen werden können, anstatt eine Illustration anzuzeigen.

   ![](assets/accessibility_5.png)

* Bei der Verwendung von Listen bleiben die Zellen der Datentabellenkopfzeilen in der Ecke der Tabelle nicht leer.

### Responsive Resize für mehrere Geräte erstellen {#resize-devices}

Bei der Entwicklung von Inhalten für mehrere Geräte und Plattformen ist es wichtig, ein nahtloses Erlebnis für Bildschirmgrößen mit allen mobilen und Desktop-Auflösungen zu erstellen.

Mit Adobe Campaign Standard können Sie E-Mails und Push-Benachrichtigungen auf verschiedenen Geräten entwerfen und testen, z. B.: iPhone, Android-Geräte, iPad, Android-Tablet und Desktop.

![](assets/accessibility_6.png)

## Kontextuelle Hilfe {#contextual-help}

Die kontextuelle Hilfe hilft Ihnen, die verschiedenen erforderlichen Felder und Funktionen besser zu verstehen. Sie führt Sie außerdem durch die Produktdokumentation, wo Sie weitere Informationen über die ausgewählte Funktion erhalten.

Wenn Sie eine E-Mail entwerfen, können Sie den Cursor über die Informationsschaltfläche bewegen. Eine Kurzinfo mit Beschreibungen der Funktionen und Links zur Produktdokumentation wird angezeigt.

![](assets/accessibility_7.png)

## Unterstützung für Bildschirmlupen {#screen-magnifiers}

Ein Bildschirmlesegerät liest Text, der auf dem Computer-Bildschirm angezeigt wird. Es werden auch nicht textuelle Informationen wie Schaltflächenbeschriftungen oder Bildbeschreibungen in der Anwendung gelesen, die in Tags oder Attributen zur Barrierefreiheit bereitgestellt werden.

In Adobe Campaign Standard sind Inhalte und Funktionen auch dann noch verfügbar, wenn der Benutzer die Eigenschaften für den Textabstand außer Kraft setzt.

## In Ihrer bevorzugten Sprache arbeiten {#languages}

Adobe Campaign Standard ist in verschiedenen Sprachen erhältlich: Englisch, Französisch und Deutsch.

Bitte beachten Sie, dass die Sprache bei der Installation eingerichtet wird und danach nicht mehr geändert werden kann.

## Tastaturbefehle {#shortcuts}

### Homepage {#homepage-shortcuts}

| Tastenkombination | Aktion |
|:-:|:-:|
| Tab | Durch einzelne Elemente der Benutzeroberfläche navigieren |
| Eingabe oder Leerzeichen | Ausgewähltes Element aktivieren |

### Email Designer {#email-designer-shortcuts}

| Tastenkombination | Aktion |
|:-:|:-:|
| STRG + Z | Rückgängig |
| STRG + Y | Wiederholen |

### Dynamische Berichte {#report-shortcuts}

| Tastenkombination | Aktion |
|:-:|:-:|
| STRG + O | Projekt öffnen |
| STRG + S | Speichern |
| Umschalten + STRG + S | Speichern unter |
| Alt + R | Projekt aktualisieren |
| Umschalten + STRG + V | CSV herunterladen |
| Alt + P | Drucken |
| STRG + Z | Rückgängig |
| STRG + Umschalten + Z | Wiederholen |
| Alt + B | Neues leeres Bedienfeld |
| Alt + A | Neue Freiform |
| Alt + 1 | Neue Freiform-Tabelle |
| Alt + 2 | Neue Zeile |
| Alt + 3 | Neue Leiste |
| Alt + S | Bericht jetzt senden |
| Umschalten + Alt + S | Bericht planmäßig senden |
| Umschalten + Alt + L | Terminierte Berichte |

## Weitere Informationen {#further-reading}

Adobe Campaign Standard ist bestrebt, eine wachsendes Maß an Barrierefreiheit zu gewährleisten und das Produkt so benutzerfreundlich wie möglich zu gestalten.

Wir empfehlen Ihnen, das [Adobe Accessibility Feedback-Formular](https://www.adobe.com/accessibility/feedback.html) zu verwenden, um Verbesserungsvorschläge und Probleme mit der Barrierefreiheit zu melden.

Die neuesten Verbesserungen und Funktionen finden Sie in den [Versionshinweisen zu Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/release-notes.html?lang=de#release-notes).