---
title: Testen Ihrer Trigger
description: Die folgenden Tipps zur Fehlerbehebung helfen Ihnen, die häufigsten Probleme bei der Verwendung von Triggers in Adobe Campaign zu beheben.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 66628f2a-6ed3-4b12-b2ed-9b9eec440dc3
source-git-commit: 602878233e919d01f3972167cb6d3a1acc4cfc02
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---

# Testen Ihrer Trigger{#testing-your-triggers}

Die folgenden Tipps zur Fehlerbehebung helfen Ihnen, die häufigsten Probleme bei der gemeinsamen Verwendung von Triggers und Adobe Campaign zu beheben.

**Ist die Funktion aktiviert?**

Um zu überprüfen, ob die Integration von Triggers mit Campaign aktiviert ist, wählen Sie das Adobe Campaign-Logo in der oberen linken Ecke und danach **[!UICONTROL Marketing-Pläne]** > **[!UICONTROL Transaktionsnachrichten]**. Das Element **[!UICONTROL Experience Cloud Triggers]** sollte sichtbar werden.

Ist dies der Fall, fahren Sie mit dem nächsten Schritt fort.

Ist dies nicht der Fall, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Siehe [Funktion aktivieren](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**Versuchen Sie, einen Trigger zu erstellen.**

Folgen Sie dazu den Schritten im Abschnitt [In Campaign einen gemappten Trigger erstellen](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Wenn sich der Trigger erstellen lässt, fahren Sie mit dem nächsten Schritt fort. Wenn nicht, bedeutet dies, dass die Verbindung zum Trigger-Ziel fehlgeschlagen ist. Überprüfen Sie, ob Triggers in Experience Cloud (Activation Services) bereitgestellt wurde. Ist dies nicht der Fall, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Die folgenden Informationen werden benötigt:

* Experience Cloud-Unternehmensname
* Organization ID (Organisationskennung)
* Analytics-Unternehmensanmeldung (kann identisch mit dem Experience Cloud-Unternehmensnamen sein)

**Versuchen Sie, den Trigger zu veröffentlichen.**

Folgen Sie dazu den Schritten im Abschnitt [In Campaign einen gemappten Trigger erstellen](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign).

Wenn die Veröffentlichung erfolgreich ist, fahren Sie mit dem nächsten Schritt fort. Wenn nicht, kontaktieren Sie bitte Adobe, damit Ihre Instanz neu gestartet wird und Sie den Versuch wiederholen können.

**Erstellen Sie den Trigger auf der Website.**

Folgen Sie den Schritten im Abschnitt [Transaktionsnachrichtenvorlage bearbeiten](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template), um die Transaktionsvorlage zu bearbeiten und zu veröffentlichen. Testen Sie dann die Erstellung des Triggers auf der Website.

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

* Überprüfen Sie, ob die Transaktionsvorlage veröffentlicht ist.
* Stellen Sie sicher, dass das Profil nicht auf der Blockierungsliste steht.
* Überprüfen Sie die Anwendung der Typologieregeln.
* Überprüfen Sie die Logs der Transaktionsnachricht.

**Ist die Nachricht gültig?**

Wenn die Nachricht nicht gültig ist, überprüfen Sie die folgenden Elemente:

* Validieren Sie die Transaktionsvorlage der als ungültig gekennzeichneten Trigger-Anreicherungs-Personalisierungsfelder in den verknüpften eventCusResource-Sammlungen.
* Validieren Sie das Nachrichtenformat.
