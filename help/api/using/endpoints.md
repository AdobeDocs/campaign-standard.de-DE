---
title: Endpunkte
description: Erfahren Sie mehr über die APIs-Endpunkte.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f251e4b5187aa09f65a5d8d6215f208a09cd9159

---


# Endpunkte {#endpoints}

Die verfügbaren Endpunkte für die Adobe Campaign REST API:

* **/profileAndServices**: interagieren Sie mit vordefinierten Feldern. Erweiterte Felder können mit diesem Endpunkt nicht aufgerufen werden.
* **/profileAndServicesExt**: interagieren Sie mit benutzerdefinierten Feldern, die während der Profile- oder Services-Erweiterung hinzugefügt werden. For more on custom resources, refer to [this section](../../api/using/custom-resources.md).
* **/&lt;transactionalAPI&gt;**: Interagieren Sie mit der API für Transaktionsmeldungen (der Name des API-Endpunkts für Transaktionsmeldungen hängt von Ihrer Instanzkonfiguration ab). Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/managing-transactional-messages.md).
* **/workflow/execute**: mit Workflows interagieren. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/controlling-a-workflow.md).
* **/privacy/privacyTool**: Interagieren Sie mit der Datenschutz-API, um den automatischen Prozess von Datenschutzanforderungen zu ermöglichen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/creating-a-privacy-request.md).
* **/history**: den Marketing-Verlauf der Profile abrufen. Weitere Informationen zu integrierten Kundenprofilen in Campaign finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/audiences/using/integrated-customer-profile.html).

Standardmäßig stehen für die **profileAndServices** - und **profileAndServicesExt** -APIs folgende Hauptressourcen zur Verfügung:

* **/profile**: mit Profilen aus der Campaign-Datenbank interagieren. Um einem Dienst Profile hinzuzufügen, verwenden Sie den **/Dienst** -Endpunkt. Weitere Informationen zu Profilen in Campaign finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/audiences/using/about-profiles.html).
* **/service**: Abonnementdienste verwalten. Weitere Informationen zu Diensten in Campaign finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/audiences/using/creating-a-service.html).

>[!NOTE]
>
>Alle anderen Ressourcen, die erweitert oder erstellt wurden, stehen nur über die **ProfileAndServicesExt** -API zur Verfügung. Sie müssen mit der **Profilressource** verknüpft sein, um zugänglich zu sein.
