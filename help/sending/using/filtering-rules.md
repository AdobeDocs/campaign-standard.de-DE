---
title: Filterregeln
description: Mithilfe von Filterregeln können Sie die Zielgruppe Ihrer Nachrichten eingrenzen.
page-status-flag: never-activated
uuid: ed3eea62-3a47-4318-ae22-d82aa857448f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 7ddaf36c-74e6-4501-b3eb-3d03f005aaa6
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 396084934a41d103eecd6fe141c700c118000f75

---


# Filterregeln {#filtering-rules}

Mit Filterregeln können Sie einen Teil der Nachrichten-Zielgruppe anhand von in einer Abfrage definierten Kriterien ausschließen. Mögliche Kriterien sind zum Beispiel Profile in Quarantäne oder Profile, die bereits eine bestimmte Anzahl an E-Mails erhalten haben.

## StandardfilterTypologieregeln {#default-filtering-typology-rules}

Die nachstehende Tabelle enthält Informationen zu vordefinierten Filterregeln sowie zu den zugehörigen Kanälen.

| Titel | Channel | Description |
---------|----------|---------
| **[!UICONTROL Address not specified]** | Alle | Schließt die Population der Zielgruppe ohne angegebene Adresse (E-Mail, Postanschrift usw.) aus. entsprechend dem ausgewählten Kanal). |
| **[!UICONTROL Blacklisted address]** | Alle | Schließt auf der Blacklist Adressen aus. |
| **[!UICONTROL Duplicate]** | Alle | Schließt Duplikat aus, die auf dem **[!UICONTROL Address]** Populationsfeld der Zielgruppe basieren. |
| **[!UICONTROL Exclude mobile applications]** | Mobile application | Schließt App-Abonnement aus, die nicht mit der in der Nachricht definierten Mobilanwendung übereinstimmen. |
| **[!UICONTROL Exclude mobile applications for In-App]** | In-App | Schließt App-Abonnement aus, die nicht mit der in der Nachricht definierten Mobilanwendung übereinstimmen (In-App-Vorlage). |
| **[!UICONTROL Exclude mobile applications for In-App broadcast]** | In-App | Schließt App-Abonnement aus, die nicht mit der in der Nachricht definierten Mobilanwendung übereinstimmen (In-App-Broadcast-Vorlage) |
| **[!UICONTROL Exclude mobile applications for Push]** | Mobile application | Schließt App-Abonnement aus, die nicht mit der in der Nachricht definierten Mobilanwendung übereinstimmen (für Push) |
| **[!UICONTROL Quarantined address]** | Alle | Schließt isolierte Adressen aus. |
| **[!UICONTROL Target limited in size]** | Alle | Überprüft, ob die maximale Größe des Versands für die Zielgruppe erreicht wurde. Gilt für Direktversand-Versand mit aktivierter Option &quot;Versand-Deadline&quot;. |

Zusätzlich zu diesen standardmäßigen Filterregeln stehen zwei Ausschlussregeln zur Verfügung:

* **[!UICONTROL Exclusion of addresses]** ( **[!UICONTROL addressExclusions]** )
* **[!UICONTROL Exclusion of domains]** ( **[!UICONTROL domainExclusions]** ).

Während der E-Mail-Analyse vergleichen diese Regeln die E-Mail-Adressen der Empfänger mit den unzulässigen Adressen oder Domain-Namen aus einer verschlüsselten globalen Unterdrückungsliste, die in der Zustellbarkeitsinstanz verwaltet wird. Im Falle einer Übereinstimmung wird die Nachricht nicht an den jeweiligen Empfänger gesendet.

Auf diese Weise soll Blacklisting aufgrund von schädlichen Aktivitäten, insbesondere durch die Verwendung von Spamtraps, vermieden werden. Wenn beispielsweise für die Anmeldung über ein Webformular eine Spamtrap verwendet wird, wird automatisch eine Bestätigungs-E-Mail an diese Spamtrap gesendet. Als Folge davon wird Ihre Adresse automatisch auf die Blacklist gesetzt.

>[!NOTE]
>
>Die Adressen und Domain-Namen in der globalen Unterdrückungsliste sind verborgen. In den Versandanalyse-Logs wird nur die Anzahl der ausgeschlossen Empfänger angegeben.

## Filterregel erstellen  {#creating-a-filtering-rule}

Sie können Ihre eigenen Filterregeln entsprechend Ihren Anforderungen erstellen. Sie können beispielsweise die Zielgruppe von Newslettern filtern, sodass Abonnenten unter 18 Jahren keine Nachrichten erhalten.

Gehen Sie wie folgt vor, um eine Filterungs-Typologieregel zu erstellen:

1. Erstellen Sie eine neue Typologieregel. Die wichtigsten Schritte zum Erstellen von Typologieregeln sind in [diesem Abschnitt](../../sending/using/managing-typology-rules.md)beschrieben.

1. Wählen Sie den **[!UICONTROL Filtering]** Regeltyp und geben Sie dann den gewünschten Kanal an.

1. In the **[!UICONTROsL Filtering criteria]** tab, select the subscriptions in the **[!UICONTROL Subscription]** category.

   ![](assets/typology_create-rule-subscription.png)

1. In the **[!UICONTROL Explorer]** tab of the query editor, drag and drop the **[!UICONTROL Subscriber]** node into the main part of the screen.

   ![](assets/typology_create-rule-subscriber.png)

1. Select the **[!UICONTROL Age]** field and define the filtering conditions so that the age of the subscribers is 18 or above.

   ![](assets/typology_create-rule-age.png)

1. In the **[!UICONTROL Typologies]** tab, link this rule to a typology.

   ![](assets/typology_create-rule-typology.png)

1. Vergewissern Sie sich, dass die Typologie im gewünschten Versand oder in der gewünschten Versandvorlage ausgewählt ist. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/managing-typologies.md#applying-typologies-to-messages).

   ![](assets/typology_template.png)

Wenn diese Regel in einer Nachricht verwendet wird, werden minderjährige Abonnenten automatisch ausgeschlossen.

## Konfigurieren des Targeting-Kontexts von Filterregeln {#configuring-filtering-rules-targeting-context}

Mit Campaign Standard können Sie je nach den zu Zielgruppe Daten die **Targeting** - und **Filterungsdimensionen** konfigurieren.

Öffnen Sie dazu die Eigenschaften der Typologieregel und öffnen Sie den **[!UICONTROL Advanced information]** Abschnitt.

By default, filtering is carried out on the **[!UICONTROL Profiles]**. Wenn die Regel beispielsweise auf eine Mobilanwendung ausgerichtet ist, **[!UICONTROL Filtering dimension]** kann sie in **[!UICONTROL Subscriptions to an application]** geändert werden.

![](assets/typology_rule-order_2.png)

## Anwendbarkeit einer Filterregel einschränken {#restricting-the-applicability-of-a-filtering-rule}

Sie können die Anwendbarkeit einer Filterregel je nach zu sendender Nachricht einschränken.

1. Deaktivieren Sie auf der **[!UICONTROL Application criteria]** Registerkarte &quot;Typologieregel&quot;die **[!UICONTROL Apply the rule on all deliveries]** Option, die standardmäßig aktiviert ist.

   ![](assets/typology_limit.png)

1. Verwenden Sie den Abfrageeditor, um einen Filter zu definieren. Sie können die Regel beispielsweise nur auf Nachrichten anwenden, deren Titel mit einem bestimmten Wort beginnt oder deren Kennung bestimmte Buchstaben enthält.

   ![](assets/typology_limit-rule.png)

In diesem Fall wird die Regel nur auf die Nachrichten angewendet, die den definierten Kriterien entsprechen.
