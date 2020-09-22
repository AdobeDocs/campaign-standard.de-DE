---
title: Audience in einer Nachricht auswählen
description: '"Hier erhalten Sie eine schrittweise Anleitung zur Auswahl von Audiences einer E-Mail: Hauptzielgruppe und Testprofile."'
page-status-flag: never-activated
uuid: 7d8f8446-f2e0-49c1-83f6-9667b29bc228
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 158da6ff-8899-4e7b-b925-8a42c3de46a1
context-tags: deliveryCreation,wizard;delivery,audience,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e725ef966bcd6df84ed0c82e17fad65f289fd013
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 84%

---


# Audience in einer Nachricht auswählen{#selecting-an-audience-in-a-message}

In Adobe Campaign können Audiences verschiedene Arten von Profilen enthalten.

Audiences können im Zuge der Nachrichtenerstellung im Assistenten oder im Nachhinein ausgehend vom Dashboard der Nachricht bestimmt werden.

>[!NOTE]
>
>Wenn die Audience innerhalb eines Workflows erstellt und mit Zusatzdaten angereichert wurde, können Sie diese Daten nicht zur Personalisierung eines Einzelversands verwenden. Diese Daten können nur über einen in einem Workflow ausgeführten Versand verwendet werden.

1. Gehen Sie im Dashboard einer Nachricht in die Audience-Kachel,

   ![](assets/delivery_audience_definition_1.png)

   um die gewünschten Profile auszuwählen. Der sich öffnende Bildschirm zeigt zwei Tabs, die die separate Definition der anzusprechenden Populationen ermöglichen:

   * Zielgruppe
   * Testprofile

   ![](assets/delivery_audience_definition_2.png)

1. Definieren Sie die **[!UICONTROL Hauptzielgruppe]** der E-Mail. Dies ist die tatsächliche Ziel-Audience der E-Mail.

   Im Tab **[!UICONTROL Zielgruppe]** werden aus den identifizierten Profilen der Datenbank diejenigen ausgewählt, die den Versand erhalten sollen.

   Dies kann beispielsweise unter Verwendung des [Abfragetools](../../automating/using/editing-queries.md#creating-queries) geschehen.

   Wenn Sie sich im Zielgruppe-Tab befinden, zeigt die Palette der **[!UICONTROL Schnellzugriffe]** nur vordefinierte Filter und Audiences, die sich auf identifizierte Profile beziehen. Der **[!UICONTROL Explorer]**-Tab bietet Zugriff auf fortgeschrittene Konfigurationen.

   Sie haben die Möglichkeit, zuvor erstellte Audiences wiederzuverwenden und zu kombinieren, bzw. durch das Hinzufügen von Filtern weiter einzuschränken.

1. Definieren Sie die **[!UICONTROL Testprofile]**, die Sie für die E-Mail verwenden möchten. Die Testprofile erhalten Testsendungen, die Sie probeweise senden können, bevor Sie die endgültige E-Mail an die Hauptzielgruppe senden.

   Weiterführende Informationen zur Testprofil-Konfiguration finden Sie im Abschnitt [Testprofile](../../audiences/using/managing-test-profiles.md).

1. Bei Bedarf können Sie eine Kontrollgruppe auf der entsprechenden Registerkarte definieren. Auf diese Weise können Sie einige Profil aus Ihrer Zielgruppe entfernen, damit sie die Nachricht nicht erhalten. For more on this, see [Adding a control group](../../sending/using/control-group.md).

1. Sie können auch Ersatzadressen verwenden, um eine genaue Darstellung der Nachricht zu erhalten, die das Profil erhalten soll.  Weiterführende Informationen finden Sie unter [Testen von E-Mail-Nachrichten mit Zielgruppenprofilen](../../sending/using/testing-messages-using-target.md).

Nach Abschluss der Konfigurationen zeigt die Audiences-Kachel an, dass sowohl die Zielgruppe als auch Testprofile definiert wurden.

![](assets/delivery_audience_definition_3.png)

