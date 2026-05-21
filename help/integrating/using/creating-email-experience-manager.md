---
title: E-Mail-Inhalt in Adobe Experience Manager erstellen
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 72b99864-d9d9-4cf4-be06-dc5719a2e4f2
TQID: https://experienceleague.adobe.com/EP76tPp3-TEsjgg91-p7dFhtHScLS0O2YOqUb2kun3E
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616a
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 567
ht-degree: 95%

---

# Adobe Experience Manager-Inhalte in eine Adobe Campaign-E-Mail importieren {#creating-email-aem}

Mithilfe dieses Dokuments lernen Sie, in Adobe Experience Manager E-Mail-Inhalte zu erstellen und zu verwalten und diese anschließend für Ihre Marketing-Kampagnen zu verwenden, indem Sie sie in Ihre Adobe Campaign Standard-E-Mails importieren.

Folgende Voraussetzungen müssen erfüllt sein:

* Zugriff auf eine AEM-Instanz, die für die Integration konfiguriert ist.
* Zugriff auf eine Adobe Campaign-Instanz, die für die Integration konfiguriert ist.
* Adobe Campaign-E-Mail-Vorlage, die für die Aufnahme eines AEM-Inhalts konfiguriert ist.

## In Adobe Experience Manager auf E-Mails zugreifen {#email-content-aem}

Melden Sie sich bei Ihrer Adobe Experience Manager-Authoring-Instanz an, und greifen Sie über Ihre Website auf den Ordner mit den E-Mail-Inhalten zu.

>[!VIDEO](https://video.tv.adobe.com/v/29996)

## Neue E-Mail-Inhalte in Adobe Experience Manager erstellen {#creating-email-content-aem}

Es stehen verschiedene Vorlagen für Adobe Campaign zur Verfügung. Verwenden Sie eine dieser Vorlagen, da sie vordefinierte Komponenten enthalten, die von Adobe Campaign unterstützt werden.

Standardmäßig stehen zwei vordefinierte Vorlagen zur Erstellung von E-Mail-Inhalten für Adobe Campaign zur Verfügung.

* **[!UICONTROL Adobe Campaign-E]** Mail: Diese Vorlage enthält Standardinhalte, die Sie personalisieren können. Sie können zwischen Adobe Campaign-E-Mail (AC6.1) und Adobe Campaign-E-Mail (ACS) wählen.
* **[!UICONTROL Importtool-Seite]**: Diese Vorlage ermöglicht Ihnen den Import einer ZIP-Datei, die wiederum eine HTML-Datei enthält, deren Inhalt sich anschließend personalisieren lässt.

1. Erstellen Sie eine neue **[!UICONTROL Seite]** in Adobe Experience Manager.

1. Wählen Sie die **[!UICONTROL Adobe Campaign-E-Mail]**-Vorlage aus. Die einzelnen Schritte finden Sie im folgenden Video.

   >[!VIDEO](https://video.tv.adobe.com/v/29997)

1. Öffnen Sie Ihren neuen E-Mail-Inhalt.

1. Legen Sie in den **[!UICONTROL Seiteneigenschaften]****[!UICONTROL Adobe Campaign]** als **[!UICONTROL Cloud Service-Konfiguration]** fest. Dies ermöglicht die Kommunikation zwischen Ihrem Inhalt und Ihrer Adobe Campaign-Instanz.

   Sehen Sie sich für weiterführende Informationen das folgende Video an:

   >[!VIDEO](https://video.tv.adobe.com/v/29999)

## E-Mails bearbeiten und senden {#editing-email-aem}

Sie können den E-Mail-Inhalt bearbeiten, indem Sie Komponenten und Elemente hinzufügen. Personalisierungsfelder können verwendet werden, um in Adobe Campaign mithilfe Empfängerdaten eine relevantere Nachricht bereitzustellen.

So erstellen Sie E-Mail-Inhalt in Adobe Experience Manager:

1. Bearbeiten Sie den Betreff und die **[!UICONTROL Klartextversion]** Ihrer E-Mail im über den Sidekick verfügbaren Menü **[!UICONTROL Seiteneigenschaften]** > **[!UICONTROL E-Mail]**.

1. Fügen Sie **[!UICONTROL Personalisierungsfelder]** über die Komponente **[!UICONTROL Text und Personalisierung]** hinzu. Jede Komponente entspricht einer bestimmten Nutzung: Einfügen von Bildern, Hinzufügen der Personalisierung usw.

   Sehen Sie sich für weiterführende Informationen das folgende Video an:

   >[!VIDEO](https://video.tv.adobe.com/v/29998)

1. Wählen Sie im Tab **[!UICONTROL Workflow]** den Validierungs-Workflow **[!UICONTROL Für Adobe Campaign genehmigen]** aus. Sie können in Adobe Campaign nur E-Mails senden, deren Inhalt validiert wurde.

So senden Sie Ihre E-Mail in Adobe Campaign Standard:

1. Nach der Definition des Inhalts und der Versandparameter können Sie eine E-Mail basierend auf einer AEM-spezifischen E-Mail-Vorlage in Adobe Campaign Standard erstellen.

   +++ Erfahren Sie mehr über AEM-spezifische Vorlagen.

   1. Wählen Sie im erweiterten Menü **[!UICONTROL Ressourcen]** die Option `>` **[!UICONTROL Vorlagen]** `>` **[!UICONTROL Versandvorlagen]** aus.

      ![](assets/aem_templates_1.png)

   1. Duplizieren oder wählen Sie eine der Versandvorlagen aus.

   1. Wählen Sie in den **[!UICONTROL Eigenschaften]** der Vorlage im Dropdown-Menü **[!UICONTROL Inhalt]** **[!UICONTROL „Adobe Experience Manager“ als Inhaltsmodus]** und dann Ihr Adobe Experience Manager-Konto aus.

      ![](assets/aem_templates_2.png)

   +++

   ![](assets/aem_send_1.png)

1. Füllen Sie die Eigenschaften Ihrer E-Mail aus und klicken Sie auf **[!UICONTROL Erstellen]**, um Ihren AEM-Inhalt auswählen zu können.

1. Rufen Sie den **[!UICONTROL Inhaltsbaustein]** auf.

   ![](assets/aem_send_2.png)

1. Klicken Sie im Menü **[!UICONTROL Inhalt aus Adobe Experience Manager verwenden]** auf **[!UICONTROL AEM-Inhalt verknüpfen]**.

   Wählen Sie dann den Inhalt aus, den Sie in Ihrer E-Mail verwenden möchten.

   ![](assets/aem_send_3.png)

1. Passen Sie Ihre E-Mail weiter an, indem Sie im Dashboard zusätzliche Parameter wie Zielgruppen und Ausführungsplanung angeben. Nach der Konfiguration können Sie nun den E-Mail-Versand durchführen. [Weitere Informationen](../../sending/using/confirming-the-send.md)

