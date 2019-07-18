---
title: Trigger testen
seo-title: Trigger testen
description: Trigger testen
seo-description: null
page-status-flag: nie aktiviert
uuid: b 3 a 6667 d-e 843-4 ad 6-817 e-d 91542 b 5 f 2 e 2
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-trigger
discoiquuid: f 67 e 69 f 2-09 fb -4 f 33-b 2 c 3-c 67 a 060743 e 3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Trigger testen{#testing-your-triggers}

Die folgenden Tipps zur Fehlerbehebung helfen Ihnen, die häufigsten Probleme bei der gemeinsamen Verwendung von Triggers und Adobe Campaign zu beheben.

**Ist die Funktion aktiviert?**

To check if the Triggers - Campaign integration is activated, click the Adobe Campaign logo, in the top left corner, then select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]**. Das Element **[!UICONTROL Experience Cloud Triggers]sollte sichtbar werden.**

Ist dies der Fall, fahren Sie mit dem nächsten Schritt fort.

Ist dies nicht der Fall, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Siehe [Funktion aktivieren](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**Versuchen Sie, einen Trigger zu erstellen.**

Folgen Sie dazu den Schritten im Abschnitt [In Campaign einen gemappten Trigger erstellen](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Wenn sich der Trigger erstellen lässt, fahren Sie mit dem nächsten Schritt fort. Wenn nicht, bedeutet dies, dass die Verbindung zum Trigger-Ziel fehlgeschlagen ist. Überprüfen Sie, ob Triggers in Experience Cloud (Activation Services) bereitgestellt wurde. Ist dies nicht der Fall, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Die folgenden Informationen werden benötigt:

* Marketing Cloud-Unternehmensname
* Kennung der IMS-Organisation
* Analytics-Unternehmensanmeldung (kann identisch mit dem Marketing Cloud-Unternehmensnamen sein)

**Versuchen Sie, den Trigger zu publizieren.**

Folgen Sie dazu den Schritten im Abschnitt [In Campaign einen gemappten Trigger erstellen](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Wenn die Publikation erfolgreich ist, fahren Sie mit dem nächsten Schritt fort. Wenn nicht, kontaktieren Sie bitte Adobe, damit Ihre Instanz neu gestartet wird und Sie den Versuch wiederholen können.

**Erstellen Sie den Trigger auf der Website.**

Folgen Sie den Schritten im Abschnitt [Transaktionsnachrichtenvorlage bearbeiten](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template), um die Transaktionsvorlage zu bearbeiten und zu publizieren. Testen Sie dann die Erstellung des Triggers auf der Website.

Wenn der Trigger von Analytics empfangen wird, fahren Sie mit dem nächsten Schritt fort. Wenn nicht, überprüfen Sie Folgendes:

* Triggers ist für Analytics aktiviert.
* Die Website verwendet MCID und Analytics ist in DTM aktiviert.
* Bei der Erstellung von Triggern wird die korrekte Analytics Report Suite verwendet.

**Wird der Trigger von Campaign empfangen?**

Wenn nicht, überprüfen Sie, ob der von der Pipeline kommende Trigger empfangen wurde.

Wenn nicht, kontaktieren Sie Adobe, um die Konfiguration des Pipeline-Ziels zu überprüfen.

Wenn er empfangen wurde, folgen Sie diesen Schritten:

* Überprüfen Sie den Typ der Abstimmkennung in der Campaign-Datenquelle.
* Die CustomerId-Datenquelle wird über Kundenattribute erstellt.
* Überprüfen Sie die Kennung der Datenquelle.
* Ersuchen Sie Adobe, die Campaign-Instanz nach der Konfiguration der Datenquelle neu zu starten.
* Überprüfen Sie im Trigger-Bericht Probleme beim Parsen von Triggern.

**Befindet sich der Trigger im Status "ausstehend"?**

Wenn nicht, fahren Sie mit dem nächsten Schritt fort. Wenn ja, folgen Sie diesen Schritten:

* Überprüfen Sie, ob die Transaktionsvorlage publiziert ist.
* Wenn die propensityScore-Schwelle für Campaign aktiviert ist, überprüfen Sie in der Pipeline die Auswertung für den Trigger.
* Stellen Sie sicher, dass das Profil nicht auf der Blacklist steht.
* Überprüfen Sie die Anwendung der Typologieregeln.
* Überprüfen Sie die Logs der Transaktionsnachricht.

**Ist die Nachricht gültig?**

Wenn die Nachricht nicht gültig ist, überprüfen Sie die folgenden Elemente:

* Validieren Sie die Transaktionsvorlage der als ungültig gekennzeichneten Trigger-Anreicherungs-Personalisierungsfelder in den verknüpften eventCusResource-Kollektionen.
* Validieren Sie das Nachrichtenformat.

