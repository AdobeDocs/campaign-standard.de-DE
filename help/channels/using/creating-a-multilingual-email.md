---
title: Mehrsprachige E-Mail erstellen
description: Führen Sie diese Schritte aus, um eine mehrsprachige E-Mail an Empfänger mit unterschiedlichen bevorzugten Sprachen zu senden.
page-status-flag: never-activated
uuid: e90f4ec8-14e3-4304-b5fc-bce0ba08a4ef
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: 79231445-1d51-499a-adcf-0c0f6db1cfa3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# Mehrsprachige E-Mail erstellen{#creating-a-multilingual-email}

Sie können eine mehrsprachige E-Mail an Profile mit unterschiedlichen bevorzugten Sprachen senden: Jedes Profil erhält eine E-Mail-Variante in der bevorzugten Sprache.

Überprüfen Sie zunächst, ob eine mehrsprachige E-Mail-Vorlage verfügbar ist. Ist dies nicht der Fall, erfahren Sie in [diesem Abschnitt](../../channels/using/multilingual-messages-template.md), wie Sie eine erstellen können.

Die Audience besteht aus Profilen, in denen die bevorzugte Sprache angegeben ist.

1. Erstellen Sie eine neue E-Mail basierend auf einer [mehrsprachigen Vorlage](../../channels/using/multilingual-messages-template.md).

   ![](assets/multi_create1.png)

1. Definieren Sie die allgemeinen Eigenschaften sowie die Ziel-Audience der E-Mail auf die gleiche Weise wie für eine Standard-E-Mail. Lesen Sie diesbezüglich auch den Abschnitt [Erstellung von Audiences](../../audiences/using/creating-audiences.md).
1. Definieren Sie die Optionen der Variante im vierten Schritt des Erstellungsassistenten. If the [multilingual template](../../channels/using/multilingual-messages-template.md) already contains all the right parameters, you can directly click on the **[!UICONTROL Create]** button.

   ![](assets/multi_create4.png)

   Fügen Sie bei Bedarf Varianten mithilfe der **[!UICONTROL Add an element]** Schaltfläche hinzu. **[!UICONTROL Default]** Variante darf nicht gelöscht werden. When set to **[!UICONTROL default]**, [the profile&#39;s preferred language](../../audiences/using/creating-profiles.md) is used to choose the variant. You can also set the **[!UICONTROL Default]** variant to any other language.

1. Bestätigen Sie die Erstellung der E-Mail: Daraufhin wird das Dashboard der E-Mail angezeigt.
1. Definieren Sie den E-Mail-Inhalt für jede Variante. Je nach zuvor ausgewählter Vorlage können Sie verschiedene Betreffe, verschiedene Absendernamen oder verschiedene Inhalte angeben. Über die Dropdown-Liste können Sie zwischen den verschiedenen Varianten hin und her wechseln. Lesen Sie für weiterführende Informationen den Abschnitt [Inhaltseditor](../../designing/using/designing-content-in-adobe-campaign.md).

   ![](assets/multi_selectcontent.png)

1. Testen und validieren Sie Ihre Nachricht. Weiterführende Informationen finden Sie im Abschnitt [Testversand durchführen](../../sending/using/sending-proofs.md).
1. Planen Sie den Versand mit der **[!UICONTROL Send after confirmation option]**.
1. Nachdem Ihre E-Mail gesendet wurde, können Sie Protokolle und Berichte aufrufen, um den Erfolg Ihrer Kampagne zu messen. Weiterführende Informationen zum Reporting finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md).

**Verwandtes Thema:**

* [Mehrsprachige Zielgruppen mit einem einzigen Workflow ansprechen](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Engageyourcustomersateverystep)
