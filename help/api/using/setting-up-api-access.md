---
title: Einrichten von API-Zugriff
description: Erfahren Sie, wie Sie Zugriff auf Campaign Standard-APIs einrichten können.
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
source-git-commit: b0e69280912ee70e6f53efd24782474395c57f74
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Einrichten von API-Zugriff {#setting-up-api-access}

Der Zugriff auf Adobe Campaign Standard-APIs lässt sich mit den folgenden Schritten einrichten: Jeder dieser Schritte wird in der [Adobe I/O-Dokumentation](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md) beschrieben.

>[!IMPORTANT]
>
>Wenn Sie in Adobe I/O Zertifikate verwalten möchten, vergewissern Sie sich, dass Sie in der Admin Console über <b>Systemadministrator</b> -Rechte für das Unternehmen oder ein [Entwicklerkonto](https://helpx.adobe.com/de/enterprise/using/manage-developers.html) verfügen.</a>

1. **Überprüfen Sie, ob Sie ein digitales Zertifikat haben**, oder erstellen Sie bei Bedarf eines. Die mit dem Zertifikat bereitgestellten öffentlichen und privaten Schlüssel werden in den folgenden Schritten benötigt.
1. **Erstellen Sie eine neue Integration mit Adobe Campaign Service** in Adobe I/O und konfigurieren Sie sie. Dann werden Ihre Zugangsdaten generiert (API-Schlüssel, Client-Geheimnis...).
1. **Erstellen Sie einen JSON-Web-Token (JWT)** aus den zuvor erstellten Anmeldedaten und signieren Sie ihn mit Ihrem privaten Schlüssel. Der JWT kodiert alle Identitäts- und Sicherheitsdaten, die Adobe zum Überprüfen Ihrer Identität und zum Erteilen des Zugriffs auf die API benötigt.
1. **Tauschen Sie Ihr JWT über eine POST-Anfrage gegen einen Zugriffstoken** aus. Dieser Zugriffstoken muss in allen Kopfzeilen Ihrer API-Anfragen verwendet werden.

Um eine sichere Service-to-Service-Adobe I/O-API-Sitzung herzustellen, muss jede Anfrage an einen Adobe-Dienst folgende Informationen in der Autorisierungskopfzeile umfassen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

* **&lt;ORGANIZATION>**: Dies ist Ihre persönliche Organisationskennung; von Adobe erhalten Sie für jede Ihrer Instanzen eine Organisationskennung:

   * &lt;ORGANIZATION>: Ihre Produktionsinstanz,
   * &lt;ORGANIZATION-mkt-stage>: Ihre Staging-Instanz.

   Wenden Sie sich an Ihren Administrator oder Ihren technischen Ansprechpartner bei Adobe, um den Wert Ihrer Organisationskennung zu erhalten. Sie können sie auch beim Erstellen einer neuen Integration in Adobe I/O abrufen, und zwar in der Lizenzliste (siehe <a href="https://www.adobe.io/authentication.html">Adobe I/O-Dokumentation</a>).

* **&lt;ACCESS_TOKEN>**: Ihr persönlicher Zugriffstoken, der beim Austausch Ihres JSON-Web-Token über eine POST-Anfrage abgerufen wurde.

* **&lt;API_KEY>**: Ihr persönlicher API-Schlüssel. Er wird in Adobe I/O bereitgestellt, nachdem eine neue Integration mit Adobe Campaign Service erstellt wurde.

   ![Alternativtext](assets/tenant.png)

## Fehlerbehebung

Wenn bei der AdobeIO-Integration der folgende Fehler angezeigt wird:

```
{ 
"code": 502, 
"message": "Oops. Something went wrong. Check your URI and try again." 
}
```


Wenden Sie sich an Ihren Administrator oder Ihren technischen Ansprechpartner für die Adobe, um zu prüfen, ob der CNAME-Parameter korrekt erstellt wurde.