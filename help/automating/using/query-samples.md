---
title: 'Beispiele für Abfragen '
description: In diesem Abschnitt wird der Anwendungsfall bei Verwendung einer Abfrageaktivität erläutert.
page-status-flag: never-activated
uuid: b3c629fa-370e-481c-b347-fcf9f5a5e847
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 8d46ce28-0101-4f13-865a-2208ed6d6139
context-tags: query,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 100%

---


# Beispiele für Abfragen   {#query-samples}

In diesem Abschnitt wird der Anwendungsfall bei Verwendung einer **[!UICONTROL Abfrageaktivität]** erläutert. Weiterführende Informationen zur Verwendung einer **[!UICONTROL Abfrageaktivität]** finden Sie in [diesem Abschnitt](../../automating/using/query.md).

## Abfrage nach einfachen Profilattributen {#targeting-on-simple-profile-attributes}

Das folgende Beispiel zeigt eine Abfrage von Männern zwischen 18 und 30 Jahren, die in London leben.

![](assets/query_sample_1.png)

## Abfrage nach E-Mail-Attributen   {#targeting-on-email-attributes}

Das folgende Beispiel zeigt eine Abfrage von Profilen, deren E-Mail-Adressen-Domain &quot;orange.co.uk&quot; lautet.

![](assets/query_sample_emaildomain.png)

Das folgende Beispiel zeigt eine Abfrage von Profilen, deren E-Mail-Adresse vorhanden ist.

![](assets/query_sample_emailnotempty.png)

## Abfrage von Profilen, deren Geburtstag heute ist   {#targeting-profiles-whose-birthday-is-today}

Das folgende Beispiel zeigt eine Abfrage von Profilen, deren Geburtstag heute ist.

1. Ziehen Sie den Filter **[!UICONTROL Geburtstag]** in Ihre Abfrage.

   ![](assets/query_sample_birthday.png)

1. Wählen Sie für den **[!UICONTROL Filtertyp]** die Option **[!UICONTROL Relativ]** und danach **[!UICONTROL Heute]** aus.

   ![](assets/query_sample_birthday2.png)

## Abfrage von Profilen, die einen bestimmten Versand geöffnet haben {#targeting-profiles-who-opened-a-specific-delivery}

Das folgende Beispiel zeigt eine Abfrage von Profilen, die den Versand mit dem Titel &quot;Sommerzeit&quot; geöffnet haben.

1. Ziehen Sie den Filter **[!UICONTROL Geöffnet]** in Ihre Abfrage.

   ![](assets/query_sample_opened.png)

1. Wählen Sie den entsprechenden Versand aus und danach **[!UICONTROL Bestätigen]**.

   ![](assets/query_sample_opened2.png)

## Abfrage von Profilen, für die Sendungen aus einem bestimmten Grund fehlgeschlagen sind {#targeting-profiles-for-whom-deliveries-failed-for-a-specific-reason}

Das folgende Beispiel zeigt eine Abfrage von Profilen, für die Sendungen fehlgeschlagen sind, weil ihr Posteingang voll war. Diese Abfrage steht nur Benutzern mit Administratorrechten zur Verfügung, die den Organisationseinheiten **[!UICONTROL Alle (all)]** angehören (siehe [diesen Abschnitt](../../administration/using/organizational-units.md)).

1. Wählen Sie die Ressource **[!UICONTROL Versandlogs]** aus, um Filter direkt in der Versandlogtabelle zu verwenden (siehe [Von den Zielgruppendimensionen abweichende Ressourcen verwenden](../../automating/using/using-resources-different-from-targeting-dimensions.md)).

   ![](assets/query_sample_failure1.png)

1. Ziehen Sie den Filter **[!UICONTROL Art des Fehlschlagens]** in Ihre Abfrage.

   ![](assets/query_sample_failure2.png)

1. Wählen Sie den entsprechenden Fehlertyp aus. In unserem Fall ist das **[!UICONTROL Postfach voll]**.

   ![](assets/query_sample_failure3.png)

## Abfrage von Profilen, die in den letzten sieben Tagen nicht kontaktiert wurden {#targeting-profiles-not-contacted-during-the-last-7-days}

Das folgende Beispiel zeigt eine Abfrage von Profilen, die in den letzten sieben Tagen nicht kontaktiert wurden.

1. Ziehen Sie den Filter **[!UICONTROL Versandlogs (logs)]** in Ihre Abfrage.

   ![](assets/query_sample_7days.png)

   Wählen Sie in der Dropdown-Liste die Option **[!UICONTROL Existiert nicht]** aus und ziehen Sie danach den Filter **[!UICONTROL Versand]** in Ihre Abfrage.

   ![](assets/query_sample_7days1.png)

1. Konfigurieren Sie den Filter wie unten beschrieben.

   ![](assets/query_sample_7days2.png)

## Abfrage von Profilen, die auf einen bestimmten Link geklickt haben   {#targeting-profiles-who-clicked-a-specific-link-}

1. Ziehen Sie den Filter **[!UICONTROL Trackinglogs (tracking)]** in Ihre Abfrage.

   ![](assets/query_sample_trackinglogs.png)

1. Ziehen Sie den Filter **[!UICONTROL Titel (urlLabel)]** in Ihre Abfrage.

   ![](assets/query_sample_trackinglogs2.png)

1. Geben Sie im Feld **[!UICONTROL Wert]** den Titel ein, der beim Einfügen des Links in den Versand definiert wurde. Bestätigen Sie danach Ihre Eingabe.

   ![](assets/query_sample_trackinglogs3.png)
