---
title: Filterregeln
seo-title: Filterregeln
description: Filterregeln
seo-description: Mithilfe von Filterregeln können Sie die Zielgruppe Ihrer Nachrichten eingrenzen.
page-status-flag: nie aktiviert
uuid: ed 3 eea 62-3 a 47-4318-ae 22-d 82 aa 857448 f
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Administration
content-type: Referenz
topic-tags: working-with-typology-rules
discoiquuid: 7 ddaf 36 c -74 e 6-4501-b 3 eb -3 d 03 f 005 aaa 6
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Filterregeln{#filtering-rules}

Mit Filterregeln können Sie einen Teil der Nachrichten-Zielgruppe anhand von in einer Abfrage definierten Kriterien ausschließen. Mögliche Kriterien sind zum Beispiel Profile in Quarantäne oder Profile, die bereits eine bestimmte Anzahl an E-Mails erhalten haben.

Sie können beispielsweise Newsletter-Anmeldungen so filtern, dass Abonnenten unter 18 Jahren keine Nachricht erhalten.

## Filterregel erstellen {#creating-a-filtering-rule}

1. Erstellen Sie eine **Filter**-Typologieregel, die auf alle Kommunikationskanäle angewendet werden kann.

   ![](assets/typology_create-rule.png)

1. Wählen Sie im Tab **[!UICONTROL Filterbedingungen]** in der Kategorie **Anmeldung]die Abonnements aus.[!UICONTROL **

   ![](assets/typology_create-rule-subscription.png)

1. Ziehen Sie im **[!UICONTROL Explorer]**-Tab des Abfrageeditors den **Abonnent]-Knoten per Drag-and-Drop in den Arbeitsbereich des Bildschirms.[!UICONTROL **

   ![](assets/typology_create-rule-subscriber.png)

1. Wählen Sie das Feld **[!UICONTROL Alter]und definieren Sie die Filterbedingungen so, dass das Mindestalter der Abonnenten 18 Jahre beträgt.**

   ![](assets/typology_create-rule-age.png)

1. Verknüpfen Sie diese Regel im **[!UICONTROL Typologien]-Tab mit einer Typologie.**

   ![](assets/typology_create-rule-typology.png)

1. Stellen Sie sicher, dass die betreffende Typologie in der Versandvorlage ausgewählt ist, die Sie verwenden möchten.

   ![](assets/typology_template.png)

   >[!NOTE]
   >
   >To access the delivery templates, select **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** in the navigation menu, which can be accessed via the Adobe Campaign logo.

Wenn diese Regel in einer Nachricht verwendet wird, werden minderjährige Abonnenten automatisch ausgeschlossen.

## Anwendbarkeit einer Filterregel einschränken {#restricting-the-applicability-of-a-filtering-rule}

Sie können die Anwendbarkeit einer Filterregel je nach zu sendender Nachricht einschränken.

1. Deaktivieren Sie hierfür im Tab **[!UICONTROL Anwendungskriterien]** der Typologieregel die Option **Regel auf alle Sendungen anwenden], die standardmäßig aktiviert ist.[!UICONTROL **

   ![](assets/typology_limit.png)

1. Verwenden Sie den Abfrageeditor, um einen Filter zu definieren. Sie können die Regel beispielsweise nur auf Nachrichten anwenden, deren Titel mit einem bestimmten Wort beginnt oder deren Kennung bestimmte Buchstaben enthält.

   ![](assets/typology_limit-rule.png)

In diesem Fall wird die Regel nur auf die Nachrichten angewendet, die den definierten Kriterien entsprechen.

## Standardmäßige Ausschlussregeln für Zustellbarkeit {#default-deliverability-exclusion-rules}

Two filtering rules are available by default: **[!UICONTROL Exclusion of addresses]** ( **[!UICONTROL addressExclusions]** ) and **[!UICONTROL Exclusion of domains]** ( **[!UICONTROL domainExclusions]** ). Während der E-Mail-Analyse vergleichen diese Regeln die E-Mail-Adressen der Empfänger mit den unzulässigen Adressen oder Domain-Namen aus einer verschlüsselten globalen Unterdrückungsliste, die in der Zustellbarkeitsinstanz verwaltet wird. Im Falle einer Übereinstimmung wird die Nachricht nicht an den jeweiligen Empfänger gesendet.

Auf diese Weise soll Blacklisting aufgrund von schädlichen Aktivitäten, insbesondere durch die Verwendung von Spamtraps, vermieden werden. Wenn beispielsweise für die Anmeldung über ein Webformular eine Spamtrap verwendet wird, wird automatisch eine Bestätigungs-E-Mail an diese Spamtrap gesendet. Als Folge davon wird Ihre Adresse automatisch auf die Blacklist gesetzt.

>[!NOTE]
>
>Die Adressen und Domain-Namen in der globalen Unterdrückungsliste sind verborgen. In den Versandanalyse-Logs wird nur die Anzahl der ausgeschlossen Empfänger angegeben.

