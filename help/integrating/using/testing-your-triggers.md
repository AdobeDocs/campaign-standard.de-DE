---
title: Trigger testen
description: null
page-status-flag: never-activated
uuid: b3a6667d-e843-4ad6-817e-d91542b5f2e2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
discoiquuid: f67e69f2-09fb-4f33-b2c3-c67a060743e3
internal: n
snippet: y
translation-type: ht
source-git-commit: 6078a16c679d368dd85cecbb8b715e2de3da805a
workflow-type: ht
source-wordcount: '450'
ht-degree: 100%

---


# Trigger testen{#testing-your-triggers}

Die folgenden Tipps zur Fehlerbehebung helfen Ihnen, die häufigsten Probleme bei der gemeinsamen Verwendung von Triggers und Adobe Campaign zu beheben.

**Ist die Funktion aktiviert?**

Um zu überprüfen, ob die Integration von Triggers mit Campaign aktiviert ist, wählen Sie das Adobe Campaign-Logo in der oberen linken Ecke und danach **[!UICONTROL Marketingpläne]** > **[!UICONTROL Transaktionsnachrichten]**. Das Element **[!UICONTROL Experience Cloud Triggers]** sollte sichtbar werden.

Ist dies der Fall, fahren Sie mit dem nächsten Schritt fort.

Ist dies nicht der Fall, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Siehe [Funktion aktivieren](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**Versuchen Sie, einen Trigger zu erstellen.**

Folgen Sie dazu den Schritten im Abschnitt [In Campaign einen gemappten Trigger erstellen](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Wenn sich der Trigger erstellen lässt, fahren Sie mit dem nächsten Schritt fort. Wenn nicht, bedeutet dies, dass die Verbindung zum Trigger-Ziel fehlgeschlagen ist. Überprüfen Sie, ob Triggers in Experience Cloud (Activation Services) bereitgestellt wurde. Ist dies nicht der Fall, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Die folgenden Informationen werden benötigt:

* Experience Cloud-Unternehmensname
* Kennung der IMS-Organisation
* Analytics-Unternehmensanmeldung (kann identisch mit dem Experience Cloud-Unternehmensnamen sein)

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

Wenn dies der Fall ist, befolgen Sie diese Richtlinien:

* Überprüfen Sie den Typ der Abstimmkennung in der Campaign-Datenquelle.
* Die CustomerId-Datenquelle wird über Kundenattribute erstellt.
* Überprüfen Sie die Kennung der Datenquelle.
* Ersuchen Sie Adobe, die Campaign-Instanz nach der Konfiguration der Datenquelle neu zu starten.
* Überprüfen Sie im Trigger-Bericht Probleme beim Parsen von Triggern.

**Befindet sich der Trigger im Status &quot;ausstehend&quot;?**

Wenn nicht, fahren Sie mit dem nächsten Schritt fort. Wenn dies der Fall ist, befolgen Sie diese Richtlinien:

* Überprüfen Sie, ob die Transaktionsvorlage publiziert ist.
* Stellen Sie sicher, dass das Profil nicht auf der Blockierungsliste steht.
* Überprüfen Sie die Anwendung der Typologieregeln.
* Überprüfen Sie die Logs der Transaktionsnachricht.

**Ist die Nachricht gültig?**

Wenn die Nachricht nicht gültig ist, überprüfen Sie die folgenden Elemente:

* Validieren Sie die Transaktionsvorlage der als ungültig gekennzeichneten Trigger-Anreicherungs-Personalisierungsfelder in den verknüpften eventCusResource-Kollektionen.
* Validieren Sie das Nachrichtenformat.

