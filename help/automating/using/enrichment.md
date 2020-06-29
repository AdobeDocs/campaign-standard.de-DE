---
title: Anreicherung
description: Die Anreicherungsaktivität ist eine erweiterte Aktivität, mit der Zusatzdaten definierte werden können, die in Ihrem Workflow verarbeitet werden.
page-status-flag: never-activated
uuid: 8c1693ef-1312-422c-b05d-263553113f8f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: f67c1caf-3284-4c34-a5b0-8654a95640ae
context-tags: enrichment,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 96%

---


# Anreicherung{#enrichment}

## Beschreibung {#description}

![](assets/enrichment.png)

Die Aktivität **[!UICONTROL Anreicherung]** ist eine erweiterte Aktivität, mit der Zusatzdaten zur Weiterverarbeitung in Ihrem Workflow definiert werden können.

## Anwendungskontext {#context-of-use}

Die Aktivität **[!UICONTROL Anreicherung]** wird im Allgemeinen im Anschluss an Zielgruppenbestimmungs- oder Dateiimportaktivitäten und vor Aktivitäten verwendet, die dem Zieldatenverbrauch dienen.

Diese Aktivität verfügt über mehr erweiterte Anreicherungsfunktionen als die Aktivität **[!UICONTROL Abfrage]**. Manche einfache Anreicherungsvorgänge können direkt in der [Abfrage-Aktivität](../../automating/using/query.md#enriching-data) ausgeführt werden.

Mit der Aktivität **[!UICONTROL Anreicherung]** können Sie die eingehende Transition nutzen und entsprechend der Konfiguration der Aktivität die ausgehende Transition mit Zusatzdaten ergänzen. Die Anreicherungsaktivität ermöglicht die Kombination von Daten aus mehreren Datensätzen oder die Erstellung von Relationen zu einer temporären Ressource.

**Verwandte Themen**

* [Verwendungsfall: Anreichern von Profil-Daten mit Daten in einer Datei](../../automating/using/enriching-profile-data-file.md).
* [Verwendungsfall: Senden einer E-Mail mit erweiterten Feldern](../../automating/using/sending-email-enriched-fields.md)

## Konfiguration {#configuration}

So konfigurieren Sie die Aktivität **[!UICONTROL Anreicherung]**:

1. Ziehen Sie eine **[!UICONTROL Anreicherung]** in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wenn es für die Aktivität mehrere eingehende Transitionen gibt, wählen Sie die **[!UICONTROL Hauptmenge aus]**. Zu dieser Hauptmenge werden die in dieser Aktivität konfigurierten Zusatzdaten in der ausgehenden Transition hinzugefügt.

   Wenn die Hauptmenge bereits Zusatzdaten enthält, können Sie auswählen, ob Sie diese behalten oder entfernen möchten. Wenn Sie die Option **[!UICONTROL Alle Zusatzdaten der Hauptmenge beibehalten]** deaktivieren, werden nur die in der **[!UICONTROL Anreicherung]** konfigurierten Zusatzdaten in der ausgehenden Transition behalten.

1. Wenn mehrere eingehende Transitionen vorhanden sind, definieren Sie im Tab **[!UICONTROL Erweiterte Relationen]** Relationen zwischen der Hauptmenge und den anderen eingehenden Daten. Mit der Schaltfläche **[!UICONTROL Element hinzufügen]** können Sie mehrere Relationen hinzufügen.

   Wenn Sie eine neue Relation definieren, wählen Sie die eingehenden Datensätze aus, die mit der Hauptmenge verknüpft werden sollen. Definieren Sie anschließend den Typ der Relation. Je nach eingehenden Daten und Datenmodell sind mehrere Typen von Relationen verfügbar:

   * **[!UICONTROL Einfache Relation mit Kardinalität 1]**: Jeder eingehende Datensatz wird genau einem Datensatz der Hauptmenge zugeordnet. Jeder Datensatz der Hauptmenge ist einem Datensatz der verknüpften Menge zugeordnet.
   * **[!UICONTROL Kollektionsrelation mit Kardinalität N]**: 0, 1 oder mehr (N) Datensätze der verknüpften Menge können 1 Datensatz der Hauptmenge zugeordnet werden.
   * **[!UICONTROL Einfache Relation mit Kardinalität 0 oder 1]**: Datensätze der Hauptmenge können 0 oder maximal 1 Datensatz der verknüpften Menge zugeordnet werden.

   Nachdem die **[!UICONTROL Kardinalität]** definiert ist, legen Sie ein **[!UICONTROL Abstimmkriterium]** fest. Der **[!UICONTROL Quellausdruck]** der Abstimmungskriterien kann ein Feld der Zielgruppen-Ressource, ein [Ausdruck](../../automating/using/advanced-expression-editing.md) oder ein in Anführungszeichen angegebener Wert sein.

   Definieren Sie einen **[!UICONTROL Titel]** und eine **[!UICONTROL ID]**, die später im Workflow leicht wiedererkennbar sind.

   >[!NOTE]
   >
   >Sie können nur Relationen zwischen der Hauptmenge und den anderen eingehenden Transitionen definieren, die mit der Aktivität **[!UICONTROL Anreicherung]** verknüpft sind. Verwenden Sie für einfachere Fälle, bei denen Relationen mit Datenbank-Ressourcen definiert werden sollen, die Aktivität [Abstimmung](../../automating/using/reconciliation.md).

1. Definieren Sie die Zusatzdaten im Tab **[!UICONTROL Zusatzdaten]** der Aktivität. Sie können Zusatzdaten definieren (einfache Felder, Aggregate und Kollektionen), die mit der Zielgruppendimension der Hauptmenge verknüpft sind oder auf den Relationen basieren, die im Tab **[!UICONTROL Erweiterte Relationen]** der Aktivität **[!UICONTROL Anreicherung]** erstellt wurden.

   Lesen Sie diesbezüglich auch den Abschnitt [Daten anreichern](../../automating/using/query.md#enriching-data).

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

Die Daten stehen jetzt bereit und können in den Aktivitäten nach der **[!UICONTROL Anreicherung verwendet werden]**. Diese Daten sind beispielsweise in einem E-Mail-Inhalt im Explorer der Personalisierungsfelder der Relation **[!UICONTROL Zusatzdaten (targetData)]** verfügbar.
