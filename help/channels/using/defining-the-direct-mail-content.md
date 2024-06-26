---
title: Briefpost-Inhalt definieren
description: Hier erfahren Sie, wie Sie den Inhalt für Ihren Briefpostversand definieren.
audience: channels
content-type: reference
topic-tags: direct-mail
context-tags: delivery,directMailContent,back
feature: Direct Mail
role: User
level: Intermediate
exl-id: 0a4c45ea-acc2-424f-8596-73376e344172
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '356'
ht-degree: 100%

---

# Briefpostinhalt definieren{#defining-the-direct-mail-content}

Sie können den Inhalt entweder im letzten Bildschirm des Erstellungsassistenten oder durch Klicken auf den Bereich **Inhalt** im Versand-Dashboard festlegen.

![](assets/direct_mail_6.png)

Der Bildschirm für die Definition von **[!UICONTROL Inhalt]** ist nur für den Briefpost-Kanal verfügbar. Er ist in vier Tabs unterteilt: **[!UICONTROL Auszug]**, **[!UICONTROL Dateistruktur]**, **[!UICONTROL Header]** und **[!UICONTROL Footer]**.

![](assets/direct_mail_11.png)

## Extraktion definieren {#defining-the-extraction}

1. Definieren Sie zunächst den Namen der Extraktionsdatei. Klicken Sie auf die Schaltfläche rechts neben dem Feld **[!UICONTROL Ausgabedatei]** und geben Sie den gewünschten Titel ein. Sie können Personalisierungsfelder, Inhaltsbausteine und dynamischen Text verwenden (siehe [Inhalte erstellen](../../designing/using/personalization.md#example-email-personalization)). Beispielsweise können Sie den Titel mit der Versandkennung oder dem Extraktionsdatum versehen.

   ![](assets/direct_mail_12.png)

1. Fügen Sie mithilfe der Schaltflächen **[!UICONTROL +]** oder **[!UICONTROL Element hinzufügen]** eine Ausgabespalte hinzu. In den **[!UICONTROL Ausgabespalten]** können Sie festlegen, welche Profilinformationen (Spalten) in die Ausgabedatei exportiert werden.

   >[!IMPORTANT]
   >
   >Achten Sie darauf, dass Ihre Profile eine Anschrift enthalten, da diese Information für den Briefpost-Dienstleister wesentlich ist. Beachten Sie außerdem, dass in der Profilinformation die Option **[!UICONTROL Anschrift angegeben]** aktiviert ist. Siehe [Empfehlungen](../../channels/using/about-direct-mail.md#recommendations).

   ![](assets/direct_mail_13.png)

1. Erstellen Sie so viele Spalten wie nötig. Klicken Sie zur Bearbeitung der Spalten auf deren Ausdruck oder Titel.

>[!NOTE]
>
>Weiterführende Informationen zur Definition von Ausgabespalten finden Sie im Abschnitt zur Workflow-Aktivität [Dateiextraktion](../../automating/using/extract-file.md).

## Dateistruktur definieren      {#defining-the-file-structure}

Im **Dateistruktur**-Tab können Sie das Ausgabe-, Datums- und Zahlenformat der zu exportierenden Datei konfigurieren.

![](assets/direct_mail_14.png)

>[!NOTE]
>
>Die verfügbaren Optionen finden Sie im Abschnitt zur Workflow-Aktivität [Dateiextraktion](../../automating/using/extract-file.md).

## Kopf- und Fußzeile definieren      {#defining-the-header-and-footer}

Hin und wieder müssen Sie vielleicht Informationen am Beginn oder am Ende der Extraktionsdatei hinzufügen. Verwenden Sie dazu die Tabs **[!UICONTROL Kopfzeile]** und **[!UICONTROL Fußzeile]** im Konfigurationsbildschirm **[!UICONTROL Inhalt]**.

![](assets/direct_mail_7.png)

So können Sie beispielsweise bei Briefpost die Absenderinformationen im Header der Datei einfügen. Footer und Header können mit den für den Versand verfügbaren Informationen personalisiert werden. Lesen Sie diesbezüglich den Abschnitt [Inhalte erstellen](../../designing/using/personalization.md#example-email-personalization).

Die Absenderadresse wird im Bereich **[!UICONTROL Senden]** der Briefposteigenschaften oder auf Vorlagenebene definiert.

![](assets/direct_mail_24.png)
