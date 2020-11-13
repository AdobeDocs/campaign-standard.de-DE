---
title: Endpunkte
description: Erfahren Sie mehr über die API-Endpunkte.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '243'
ht-degree: 100%

---


# Endpunkte {#endpoints}

Die verfügbaren Endpunkte für die Adobe Campaign REST-API:

* **/profileAndServices**: zur Interaktion mit vordefinierten Feldern. Erweiterte Felder können bei diesem Endpunkt nicht aufgerufen werden.
* **/profileAndServicesExt**: zur Interaktion mit benutzerdefinierten Feldern, die bei der benutzerdefinierten Ressourcenerweiterung von Profil oder Dienste hinzugefügt werden. Weiterführende Informationen zu benutzerdefinierten Ressourcen finden Sie in [diesem Abschnitt](../../api/using/custom-resources.md).
* **/&lt;transactionalAPI>**: zur Interaktion mit der API für Transaktionsnachrichten (der Name des API-Endpunkts für Transaktionsnachrichten hängt von der Konfiguration Ihrer Instanz ab). Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/managing-transactional-messages.md).
* **/workflow/execute**: zur Interaktion mit Workflows. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/controlling-a-workflow.md).
* **/privacy/privacyTool**: zur Interaktion mit der Datenschutz-API, um eine automatische Verarbeitung von Datenschutzanfragen zu ermöglichen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/creating-a-privacy-request.md).
* **/history**: zum Abrufen des Marketingverlaufs der Profile. Weitere Informationen zu integrierten Kundenprofilen in Campaign finden Sie in der [Campaign-Dokumentation](https://helpx.adobe.com/de/campaign/standard/audiences/using/integrated-customer-profile.html).

Standardmäßig stehen für die APIs **profileAndServices** und **profileAndServicesExt** folgende Hauptressourcen zur Verfügung:

* **/profile**: zur Interaktion mit Profilen aus der Campaign-Datenbank. Um einem Dienst Profile hinzuzufügen, verwenden Sie den Endpunkt **/service**. Weitere Informationen zu Profilen in Campaign finden Sie in der [Campaign-Dokumentation](https://helpx.adobe.com/de/campaign/standard/audiences/using/about-profiles.html).
* **/service**: zum Verwalten von Anmeldediensten. Weitere Informationen zu Diensten in Campaign finden Sie in der [Campaign-Dokumentation](https://helpx.adobe.com/de/campaign/standard/audiences/using/creating-a-service.html).

>[!NOTE]
>
>Alle anderen Ressourcen, die erweitert oder erstellt wurden, stehen nur über die API **ProfileAndServicesExt** zur Verfügung. Sie müssen mit der **Profil**-Ressource verknüpft sein, um aufgerufen werden zu können.
