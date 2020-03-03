---
title: E-Mail-Inhalt in Adobe Experience Manager erstellen
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9efce905cd767013a22afb2a4d642e42b6616ef1

---


# Importieren von Adobe Experience Manager-Inhalten in eine Adobe Campaign-E-Mail {#creating-email-aem}

Mithilfe dieses Dokuments lernen Sie, in   Adobe Experience Manager   E-Mail-Inhalte zu erstellen und zu verwalten und diese anschließend für Ihre Marketingkampagnen zu verwenden, indem Sie sie in   Ihre Adobe Campaign Standard-E-Mails importieren.

Folgende Voraussetzungen müssen erfüllt sein:

* Zugriff auf eine AEM-Instanz, die für die Integration konfiguriert ist.
* Zugriff auf eine Adobe Campaign-Instanz, die für die Integration konfiguriert ist.
* Adobe Campaign-E-Mail-Vorlage, die für die Aufnahme eines AEM-Inhalts konfiguriert ist.

## Zugriff auf E-Mails in Adobe Experience Manager {#email-content-aem}

Melden Sie sich bei Ihrer Adobe Experience Manager-Authoring-Instanz an und navigieren Sie zu Ihrer Site, um auf den Ordner mit Ihren E-Mail-Inhalten zuzugreifen.

>[!VIDEO](https://video.tv.adobe.com/v/29996)

## Creating new email content in Adobe Experience Manager {#creating-email-content-aem}

Es stehen verschiedene Vorlagen für Adobe Campaign zur Verfügung. Sie müssen eine dieser Vorlagen verwenden, da sie vordefinierte Komponenten enthalten, die von Adobe Campaign unterstützt werden.

Standardmäßig stehen zwei vordefinierte Vorlagen zur Erstellung von E-Mail-Inhalten für Adobe Campaign zur Verfügung.

* **[!UICONTROL Adobe Campaign Email]**: Diese Vorlage enthält einen Standardinhalt, den Sie personalisieren können. Sie können zwischen Adobe Campaign E-Mail (AC6.1) und Adobe Campaign E-Mail (ACS) wählen.
* **[!UICONTROL Importer Page]**: Diese Vorlage ermöglicht Ihnen den Import einer ZIP-Datei, die wiederum eine HTML-Datei enthält, deren Inhalt sich anschließend personalisieren lässt.

1. Erstellen Sie in Adobe Experience Manager eine neue Version **[!UICONTROL Page]**.

1. Select the **[!UICONTROL Adobe Campaign Email]** template. Die einzelnen Schritte finden Sie im folgenden Video.
   >[!VIDEO](https://video.tv.adobe.com/v/29997)

1. Öffnen Sie Ihren neuen E-Mail-Inhalt.

1. Legen Sie im **[!UICONTROL Page properties]** Feld **[!UICONTROL Adobe Campaign]** als **[!UICONTROL Cloud Service Configuration]**. Dies ermöglicht die Kommunikation zwischen Ihrem Inhalt und Ihrer Adobe Campaign-Instanz.

   Sehen Sie sich für weiterführende Informationen das folgende Video an:

   >[!VIDEO](https://video.tv.adobe.com/v/29999)

## Bearbeiten und Senden einer E-Mail {#editing-email-aem}

Sie können den E-Mail-Inhalt bearbeiten, indem Sie Komponenten und Elemente hinzufügen. Personalisierungsfelder können verwendet werden, um eine relevantere Nachricht basierend auf den Daten der Empfänger in Adobe Campaign bereitzustellen.

So erstellen Sie E-Mail-Inhalt in Adobe Experience Manager:

1. Bearbeiten Sie den Betreff und die **[!UICONTROL Plain text]** Version Ihrer E-Mail, indem Sie auf die Registerkarte **[!UICONTROL Page properties]** > **[!UICONTROL Email]** > des Sidekick zugreifen.

1. Fügen Sie **[!UICONTROL Personalization fields]** über die **[!UICONTROL Text & Personalization]** Komponente hinzu. Jede Komponente entspricht einer bestimmten Nutzung: Einfügen von Bildern, Hinzufügen der Personalisierung usw.

   Sehen Sie sich für weiterführende Informationen das folgende Video an:
   >[!VIDEO](https://video.tv.adobe.com/v/29998)

1. Wählen Sie auf der **[!UICONTROL Workflow]** Registerkarte den **[!UICONTROL Approve for Adobe Campaign]** Überprüfungsarbeitsablauf aus. Sie können in Adobe Campaign keine E-Mail senden, wenn ein nicht genehmigter Inhalt verwendet wird.

1. Sobald die Parameter für Inhalt und Senden definiert sind, können Sie die E-Mail in Adobe Campaign Standard genehmigen, vorbereiten und senden.

   Sehen Sie sich für weiterführende Informationen das folgende Video an:

   >[!VIDEO](https://video.tv.adobe.com/v/23721)
