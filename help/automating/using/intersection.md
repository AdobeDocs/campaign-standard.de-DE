---
title: Schnittmenge
seo-title: Schnittmenge
description: Schnittmenge
seo-description: Eine Schnittmenge dient der Extraktion der gemeinsamen Population aus den eingehenden Aktivitäten.
page-status-flag: nie aktiviert
uuid: a 60 f 9811-0158-44 b 3-952 b -392685 c 006 cc
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: targeting-activities
discoiquuid: 7 a 107 d 6 b-edc 3-44 c 3-bbb 7-ba 3 dec 8 e 43 f 9
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 36727e82d3aa73add6116fa2916752ff0e407d9d

---


# Schnittmenge{#intersection}

## Beschreibung {#description}

![](assets/intersection.png)

Eine **[!UICONTROL Schnittmenge]dient der Extraktion der gemeinsamen Population aus den eingehenden Aktivitäten.**

## Anwendungskontext {#context-of-use}

Die **[!UICONTROL Schnittmenge]wird insbesondere verwendet, um die Populationen der eingehenden Transitionen weiter einzugrenzen.**

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Schnittmenge]in den Workflow-Arbeitsbereich.**
1. Schließen Sie sie an Aktivitäten wie beispielsweise Abfragen an.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Wählen Sie nun den **[!UICONTROL Abstimmtyp]**:

   * **[!UICONTROL Nur die Schlüssel]** - Standardmodus; die Aktivität behält die Elemente der eingehenden Transitionen bei, die denselben Schlüssel aufweisen.
   * **[!UICONTROL Alle gemeinsamen Spalten]** - die Abstimmung erfolgt auf Basis der Spalten, die in allen eingehenden Transitionen enthalten sind. In diesem Fall ist die Hauptmenge anzugeben, die zum Spaltenvergleich herangezogen werden soll. Diese Option bietet sich insbesondere an, wenn die eingehenden Populationen unterschiedliche Zielgruppendimensionen aufweisen.
   * **[!UICONTROL Auswahl an Spalten]** - die Abstimmung erfolgt auf Basis der von Ihnen angegebenen Spalten. Wählen Sie zunächst die die Quelldaten enthaltende Hauptmenge aus und definieren Sie dann die für die Herstellung der Relation zu verwendenden Felder.

1. Kreuzen Sie die Option **[!UICONTROL Nur gemeinsame Zusatzdaten verwenden]an, wenn Sie nur die in allen eingehenden Transitionen enthaltenen Zusatzdaten beibehalten möchten.**
1. Bei Bedarf können Sie unter Verwendung von [Transitionen](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) auf erweiterte Optionen zur Ausgabepopulation zugreifen.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Unten stehende Abbildung zeigt die Schnittmenge aus zwei Abfrageaktivitäten, die alle Profile der Adobe-Campaign-Datenbank abrufen, die zwischen 18 und 27 Jahre alt sind bzw. deren E-Mail-Adresse korrekt angegeben ist.

![](assets/wkf_intersection_example.png)

