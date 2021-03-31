---
solution: Campaign Standard
product: campaign
title: Endpunkte
description: Erfahren Sie mehr über die API-Endpunkte.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Erfahren
translation-type: ht
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: ht
source-wordcount: '247'
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
