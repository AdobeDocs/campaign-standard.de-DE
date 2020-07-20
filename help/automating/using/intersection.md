---
title: Schnittmenge
description: Eine Schnittmenge dient der Extraktion der gemeinsamen Population aus den eingehenden Aktivitäten.
page-status-flag: never-activated
uuid: a60f9811-0158-44b3-952b-392685c006cc
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 7a107d6b-edc3-44c3-bbb7-ba3dec8e43f9
internal: n
snippet: y
translation-type: ht
source-git-commit: 21faea89b3b38f3e667ed6c4de0be6d07f0b7197
workflow-type: ht
source-wordcount: '304'
ht-degree: 100%

---


# Schnittmenge{#intersection}

## Beschreibung {#description}

![](assets/intersection.png)

Eine **[!UICONTROL Schnittmenge]** dient der Extraktion der gemeinsamen Population aus den eingehenden Aktivitäten.

## Anwendungskontext {#context-of-use}

Die **[!UICONTROL Schnittmenge]** wird insbesondere verwendet, um die Populationen der eingehenden Transitionen weiter einzugrenzen.

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Schnittmenge]** in den Workflow-Arbeitsbereich.
1. Schließen Sie sie an Aktivitäten wie beispielsweise Abfragen an.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wählen Sie nun den **[!UICONTROL Abstimmtyp]**:

   * **[!UICONTROL Nur die Schlüssel]** – Standardmodus; die Aktivität behält die Elemente der eingehenden Transitionen bei, die denselben Schlüssel aufweisen.
   * **[!UICONTROL Alle gemeinsamen Spalten]** – die Abstimmung erfolgt auf Basis der Spalten, die in allen eingehenden Transitionen enthalten sind. In diesem Fall ist die Hauptmenge anzugeben, die zum Spaltenvergleich herangezogen werden soll. Diese Option bietet sich insbesondere an, wenn die eingehenden Populationen unterschiedliche Zielgruppendimensionen aufweisen.
   * **[!UICONTROL Auswahl an Spalten]** – die Abstimmung erfolgt auf Basis der von Ihnen angegebenen Spalten. Wählen Sie zunächst die die Quelldaten enthaltende Hauptmenge aus und definieren Sie dann die für die Herstellung der Relation zu verwendenden Felder.

1. Kreuzen Sie die Option **[!UICONTROL Nur gemeinsame Zusatzdaten verwenden]** an, wenn Sie nur die in allen eingehenden Transitionen enthaltenen Zusatzdaten beibehalten möchten.
1. Bei Bedarf können Sie unter Verwendung von [Transitionen](../../automating/using/activity-properties.md) auf erweiterte Optionen zur Ausgabepopulation zugreifen.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Unten stehende Abbildung zeigt die Schnittmenge aus zwei Abfrageaktivitäten, die alle Profile der Adobe-Campaign-Datenbank abrufen, die zwischen 18 und 27 Jahre alt sind bzw. deren E-Mail-Adresse korrekt angegeben ist.

![](assets/wkf_intersection_example.png)

