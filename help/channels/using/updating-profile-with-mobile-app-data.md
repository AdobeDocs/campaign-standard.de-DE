---
title: Erstellung und Aktualisierung von Profilinformationen auf der Grundlage mobiler Anwendungsdaten
seo-title: Erstellung und Aktualisierung von Profilinformationen auf der Grundlage mobiler Anwendungsdaten
description: Erstellung und Aktualisierung von Profilinformationen auf der Grundlage mobiler Anwendungsdaten
seo-description: Lernen, wie Profile auf der Grundlage mobiler Anwendungsdaten erstellt und aktualisiert werden können.
page-status-flag: never-activated
uuid: 8cf74cad-b1ba-4aad-83bd-7289cb22d5f4
contentOwner: Lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: dc944c85-2059-46df-b396-676fe3617dd1
context-tags: delivery,mobileAppContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 64c7de127285ca56b6af398b0a0c3f1470756fe4

---


# Erstellung und Aktualisierung von Profilinformationen auf der Grundlage mobiler Anwendungsdaten

## Übersicht

Diese Seite beschreibt die Schritte zur Entwicklung eines Arbeitsflusses, durch den Profildaten nach einem mobilen Antrag erstellt bzw. aktualisiert werden, und zwar auf planmäßigen Basis.

* **PII** steht für "persönlich identifizierbare Informationen «. Es kann sich um Daten handeln, auch Informationen, die nicht in der Profiltabelle aus Ihrer Wahldatenbank aufgeführt sind, beispielsweise Analytics für mobile [Interessenspunkte](../../integrating/using/about-campaign-points-of-interest-data-integration.md). Die PII wird vom mobilen App Entwicker, in der Regel mit einem Marketer, definiert.
* **PII ist** eine HTTP-POST-Operation für einen Rest API in Adobe Campaign Standard von einem mobilen App.

Ziel dieses Gebrauchs ist die Erstellung oder Aktualisierung eines Wahlstandardprofils, wenn die von einem mobilen Antrag zurückkehrenden PII-Daten profilbezogene Daten enthalten.

## Voraussetzungen

Es gibt mehrere Konfigurationsschritte, um die Push-Meldungen im Wahlstandard zu ermöglichen, bevor Profile auf der Grundlage von mobilen App-Abonnements erstellt oder aktualisiert werden können:

1. [Einführung eines mobilen Antrags](../../administration/using/configuring-a-mobile-application.md)
1. [Integration des Adobe Mobile SDK mit Ihrer mobilen Anwendung](https://helpx.adobe.com/campaign/kb/integrate-mobile-sdk.html).
1. [Configure Adobe Kampagne zur Meldung von Push-Meldungen](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

## Schritt 1 - Erweiterung des Profilvermögens für Push-Meldungen/Abonnements

Um das Profil-Ressourcenprofil mit PII-Daten schaffen oder aktualisieren zu können, müssen Sie zunächst das Profil auf den gewünschten Feldern erweitern. Gehen Sie wie folgt vor:

* Angabe der PII-Felder, die von der mobilen Anwendung übermittelt werden.
* Angabe des Felds zur Nutzung zwecks Verknüpfung der PII-Daten mit den Profildaten.

![](assets/update_profile1.png)

In diesem Beispiel spiegeln die **[!UICONTROL Felder]** die PII-Daten wider, die der Mobile Antrag übermittelt hat. Der **[!UICONTROL Link zu Profilprofilen]** zeigt das Feld an, das genutzt wird, um die PII mit den Profildaten zu assoziieren, wo **cuse-CusEmail** -Karten an **@ e Post vergeben** werden.

Die Kartierung für Profildaten während der Erweiterung der **[!UICONTROL Abonnements auf eine]** Anwendungsressource ist READ-ONLY. Es wird für die Versöhnung verwendet. Das Profil muss mit den erforderlichen Daten in das System eingegeben werden, um das Profil mit den PII-Daten zu vereinbaren. In unserem Fall muss eine E-Email-Adresse für das Profil einer E-Email aus der Sammlung PII entsprechen, um die Aussöhnung zu erreichen:

* PII wird von einem mobilen App für einen Nutzer empfangen, bei dem der Vorname‚Jane, Nachname‚Doe'lautet, und E-Mail-Adresse janedoe@doe.com.
* Unabhängig davon müssen die Profile-Daten existieren (z. B. müssen die Daten manuell eingegeben oder bereits aus einer anderen Ressource stammen), wenn die E-Mail-Adresse des Profils janedoe@doe.com ist.

**Verwandte Themen:**

* [App-Abonnements-Ressource erweitern](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).
* [Schaffung oder Erweiterung einer vorhandenen Ressource](../../developing/using/key-steps-to-add-a-resource.md).

## Schritt 2 - Schaffung des Arbeitsflusses

Mithilfe eines Arbeitsflusses im Wahlstandard kann ein Verwalter Daten zwischen den Daten des appct (Subscriber) und dem Profil oder den Empfängerdaten eindeutig identifizieren und synchronisieren. Während eine workflow-basierte Aktualisierung die Profildaten in Echtzeit nicht synchronisiert, sollte sie keine unzulässigen Datenbanken oder Overhead verursachen.

Die wichtigsten Schritte zur Schaffung des Arbeitsflusses sind:

1. **[!UICONTROL Eine Aufsuchung]** oder **[!UICONTROL zusätzliche Aufsuchung]** vornehmen, um eine Liste der letzten Abonnements zu erhalten.
1. Eine **[!UICONTROL Versöhnungsmaßnahme]** zur Karte der PII-Daten mit dem Profil verwenden.
1. Lassen Sie mich einige Nachprüfungsverfahren hinzufügen.
1. Aktualisierung der **[!UICONTROL aktualisierten Daten]** zur Aktualisierung oder Erstellung des Profils mit den PII-Daten.

Bei diesen Arbeitsströmen werden folgende Anforderungen angenommen:

* Alle/alle Felder, die verlängert wurden, sollten zur Erstellung/Aktualisierung des Profilstabs verfügbar sein.
* Das Profil kann auf Felder ausgedehnt werden, die nicht nativ unterstützt werden (z. B.T-Shirt-Größe).
* Ein Feld aus dem appsubscrisubscritisch, das leer ist, sollte nicht in der Profiltabelle aktualisiert werden.
* Jedes Protokoll, das im appstellentisch aktualisiert wurde, sollte in den nächsten Arbeitsablauf aufgenommen werden.

Um den Arbeitsfluss zu gestalten, folgen die folgenden Schritte:

1. Drag und Absenkung der folgenden Tätigkeiten in den Arbeitsraum:
   1. **[!UICONTROL Starten]**
   1. **[!UICONTROL Planung]**
   1. **[!UICONTROL Inkrementelle Abfrage]**
   1. **[!UICONTROL Daten aktualisieren]**
   ![](assets/update_profile0.png)

1. Configure the **[!UICONTROL Scheduler]** activity. Im **[!UICONTROL Allgemeinen]** Labor ist die **[!UICONTROL Ausführungsfrequenz]** (z. B. "Daily"), die **[!UICONTROL Zeit]** (z. B. "1.00.00 Uhr") und **[!UICONTROL der Start]** (z. B. das heutige Datum) festzulegen.

   ![](assets/update_profile2.png)

1. Die **[!UICONTROL zusätzliche Abfragetätigkeit]** konfigurieren lassen.
   1. In der **[!UICONTROL Eigenschaft]** "Immobilien «klicken Sie die **[!UICONTROL Auswahl eines Elements]** des **[!UICONTROL Ressourcenfelds]** und wählen Sie die **[!UICONTROL Abonnements eines Antrags aus (nms: Apponptionrcp: Apponptionrcpdetail)]** Element.

      ![](assets/update_profile3.png)

   1. In **[!UICONTROL der Target]** -Tab ist der **[!UICONTROL mobile Anwendungsfilter]** abzuziehen und dann einen mobilen Anwendungsname auszuwählen.

      ![](assets/update_profile4.png)

   1. In der **[!UICONTROL verarbeiteten]** Datentransformation ist **[!UICONTROL ein Datumsfeld zu wählen]**, dann das **[!UICONTROL letzte modifizierte]** Feld (lastmodifizierfeld) als **[!UICONTROL Pfad zum Datumsfeld hinzuzufügen]**.

      ![](assets/update_profile5.png)

1. Konfiguriert die **[!UICONTROL Aktualisierung]** der Daten.
   1. In **[!UICONTROL der Identifizierungseinrichtung]** ist sicherzustellen, dass die **[!UICONTROL Dimension für die Aktualisierung]** der Felder auf "Profile (Profil)" gesetzt wird und dann die **[!UICONTROL "Base Element]** Taste «, um ein Feld als Versöhnungskriterien hinzuzufügen.

      ![](assets/update_profile_createelement.png)

   1. Im Feld **[!UICONTROL "Source «]** ist ein Feld aus dem appsubscrsiptionrcp-Tisch als Versöhnungsfeld auszuwählen. Es kann die E-Email, crmid, marketingcloudid usw. sein. In diesem Fall werden wir das Feld "E Mail (cuse CusEmail)" nutzen.
   1. Im **[!UICONTROL Bestimmungsbereich]** ist ein Feld aus der Profiltabelle auszuwählen, um die Daten vom appsubscriptionrα Tisch zu vereinbaren. Es kann die E-Email des Profils oder ein erweitertes Feld wie crmid, marketingcloudid usw. sein. In diesem Fall müssen wir das Feld "E Mail (E Email)" auswählen, um es mit dem Feld "E Mail (cuse CusEmail)" vom appsubscriptionrrtgs-Tisch zu Karten zu Karten zu Karten.

      ![](assets/update_profile7.png)

   1. In der **[!UICONTROL Felder zur Aktualisierung]** der Klippe klicken Sie die **[!UICONTROL "Base Element]** Taste «, dann Karten, die aus dem appsubscriptionrrtgs-Tisch (**[!UICONTROL Quelle]** -Feld) mit den Feldern, die Sie im Profiltisch aktualisieren möchten (**[!UICONTROL Field Field]** ), aufzeichnen.
   1. In **[!UICONTROL der aktivierten Umgebung]** ist anzugeben, ob das entsprechende Feld in der Profiltabelle nur aktualisiert wird, wenn das Ausgangsfeld einen Wert enthält. Zu diesem Zweck wird das Feld aus der Liste ausgewählt und dann hinzugefügt. "= "Ausdrucksfeld (wenn das Quellenfeld `[target/@cusEmail]` im Expressredakteur ist, sicher zu sein `[target/@cusEmail] != ''"`).

      ![](assets/update_profile8.png)

      >[!NOTE]
      >
      >In diesem Fall führt der Workflow ein UPSIS durch, da es sich jedoch auf eine Inkrementelle-Datenbank stützt, wird es nur eingefügt. Die Änderung der Query kann Auswirkungen auf die eingefügten oder aktualisierten Daten haben.
      >Darüber hinaus werden in den Feldern zur Aktualisierung von Klipp und Fach festgelegt, welche Felder unter bestimmten Bedingungen eingefügt oder aktualisiert werden. Diese Einstellungen können für jeden Antrag oder Kunden einmalig sein. Bei der Konfiguration dieser Einstellungen Vorsicht walten lassen, da es unbeabsichtigte Folgen geben kann, da die Aktualisierung des Profils auf der Grundlage von apponptionrcp-Daten die persönliche Information der Nutzer ohne Validierung ändern kann.

   1. Wenn alle Felder zur Aufnahme/Aktualisierung des Profils hinzugefügt wurden, bestätigen Sie **[!UICONTROL bitte]**.

      ![](assets/update_profile9.png)

1. Sparen Sie den Arbeitsfluss und klicken Sie mit Beginn des Workflow.

   ![](assets/update_profile10.png)
