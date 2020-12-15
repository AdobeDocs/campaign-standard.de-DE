---
solution: Campaign Standard
product: campaign
title: Barrierefreiheit in Adobe Campaign Standard
description: Erfahren Sie mehr über die Unterstützung von Barrierefreiheit in Adobe Campaign Standard Workspace.
audience: designing
content-type: reference
topic-tags: accessibility
translation-type: tm+mt
source-git-commit: 6ea28c457b1024dab315b60281adaee56eb80cd0
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 45%

---


# Barrierefreiheit in Adobe Campaign Standard {#accessibility-acs}

Erfahren Sie mehr über die Unterstützung von Barrierefreiheit in Adobe Campaign Standard Workspace.

Mit Funktionen der Barrierefreiheit sollen Produkte für Menschen mit visuellen, auditiven, kognitiven, motorischen und anderen Behinderungen nutzbar gemacht werden. Beispiele für Barrierefreiheitsfunktionen für Softwareprodukte sind semantisch strukturierte Inhalte, Unterstützung von Bildschirmlesehilfen, Entsprechungen für Grafiken, Tastaturbefehle usw.

Adobe Campaign Standard bietet Funktionen, die die Verwendung von Kontrast, Beschriftungen, strukturierten Inhalten, Tastaturnavigation und kontextbezogener Hilfe erleichtern.

## Barrierefreiheitsfunktionen {#accessibility-features}

### Kontrast und Farbe {#contrast}

Die Adobe Campaign Standard-Benutzeroberfläche ist bestrebt, einen ausreichenden Kontrast in der Anwendung zu gewährleisten, um eine barrierefreie Anzeige für Benutzer mit Sehschwäche oder Farbmangel zu gewährleisten.

* Große Texte und Überschriften wurden verbessert, um ein Kontrastverhältnis von 3:1 zu erreichen.

   ![](assets/accessibility_2.png)

* Der Hilfeinhalt und der Text in der Anwendung wurden aktualisiert, um ein Kontrastverhältnis von 4,5:1 zu erreichen.

* Die Symbole zum Anhalten und Abbrechen von Workflows wurden aktualisiert, um den Kontrast zwischen Hintergrund- und Vordergrundfarben zu verbessern.

   ![](assets/accessibility_1.png)

* Farbe, Form und Position sind nicht die einzigen Methoden, mit denen Informationen oder Hierarchien in der Anwendung kommuniziert werden können.

### Benutzeroberfläche {#user-interface}

Die Adobe Campaign Standard-Benutzeroberfläche erleichtert allen Benutzern die Interaktion mit Inhalten, indem sie visuellen Elementen alternative Texte hinzufügen und die semantische Struktur verwenden, um Informationen sowohl visuell als auch programmatisch zu vermitteln.

* Wenn der Benutzer ein erforderliches ID-Feld leer lässt, zeigt eine Grafik visuell an, welches Feld mit Fehlermeldungstext fehlerhaft ist und dass dieselben Informationen programmgesteuert an Benutzer mit Hilfstechnologien wie Bildschirmlesehilfen weitergeleitet werden.

   ![](assets/accessibility_3.png)

* Inhalte, die beim Bewegen des Mauszeigers oder beim Fokussieren angezeigt werden, können vom Benutzer verworfen werden und verdecken keine anderen Inhalte.

   ![](assets/accessibility_4.png)

* Es wurden alternative Texte für Bild- und barrierefreie Namen für Schaltflächen hinzugefügt, die mit Hilfstechnologien vorgelesen werden können, anstatt sich lediglich auf visuelle Hinweise zur Identifizierung von Elementen zu verlassen.

<!--
### Create responsive resize for multiple devices {#resize-devices}

When designing for multiple devices and platforms, it's important to create a seamless experience for screen sizes across mobile and desktop resolutions.

Adobe Campaign Standard allows you to design and test emails and push notifications on different devices such as: iPhone, Android devices, iPad, Android tablet and desktop.

![](assets/accessibility_6.png)
-->

## Kontextuelle Hilfe {#contextual-help}

Mithilfe der kontextbezogenen Hilfe können Sie die verschiedenen erforderlichen Felder und Funktionen besser verstehen. Sie führt Sie außerdem durch die Produktdokumentation, wo Sie weitere Informationen über die ausgewählte Funktion erhalten.

Beim Entwerfen einer E-Mail können Sie auf eine QuickInfo zugreifen, die Beschreibungen der Funktionen und Links zur Produktdokumentation enthält.

![](assets/accessibility_7.png)

## Unterstützung für Hilfstechnologie {#screen-magnifiers}

Wir sind bestrebt, die Adobe Campaign Standard-Anwendung durch verschiedene Hilfstechnologien so nutzbar wie möglich zu machen, unter anderem durch modifizierte Tastaturen, Bildschirmvergrößerungssoftware, Bildschirmlesehilfen, Spracherkennungssoftware und andere Hilfsmittel.

## In Ihrer bevorzugten Sprache arbeiten {#languages}

Adobe Campaign Standard ist in verschiedenen Sprachen erhältlich: Englisch, Französisch und Deutsch.

Bitte beachten Sie, dass die Sprache bei der Installation eingerichtet wurde und danach nicht mehr geändert werden kann.

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