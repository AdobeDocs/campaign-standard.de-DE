---
title: API-Zugriff einrichten
description: Erfahren Sie, wie Sie den Zugriff auf Campaign Standard-APIs einrichten.
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
source-git-commit: c0c0be79613f99a15676343d8ce10d335baf968a

---


# API-Zugriff einrichten {#setting-up-api-access}

Der Zugriff auf die Adobe Campaign Standard-API erfolgt wie folgt: Jeder dieser Schritte wird in der [Adobe IO-Dokumentation](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)beschrieben.

>[!CAUTION]
>
>Um Zertifikate in Adobe IO zu verwalten, vergewissern Sie sich, dass Sie über <b>Systemadministrator</b> -Rechte für das Unternehmen oder ein <a href="https://helpx.adobe.com/enterprise/using/manage-developers.html">Entwicklerkonto</a> in der Admin-Konsole verfügen.

1. **Überprüfen Sie, ob Sie über ein digitales Zertifikat** verfügen, oder erstellen Sie bei Bedarf ein Zertifikat. Die mit dem Zertifikat bereitgestellten öffentlichen und privaten Schlüssel werden in den folgenden Schritten benötigt.
1. **Erstellen Sie eine neue Integration in Adobe Campaign Service** in Adobe IO und konfigurieren Sie sie. Ihre Anmeldeinformationen werden dann generiert (API-Schlüssel, Client-geheim...).
1. **Erstellen Sie ein JSON-Web-Token (JWT)** aus den zuvor erstellten Anmeldeinformationen und signieren Sie es mit Ihrem privaten Schlüssel. Die JWT kodiert alle Identitäts- und Sicherheitsinformationen, die Adobe zum Überprüfen Ihrer Identität und zum Erteilen des Zugriffs auf die API benötigt.
1. **Tauschen Sie Ihre JWT über eine POST-Anforderung gegen ein Zugriffstoken** aus. Dieses Zugriffstoken muss in jeder Kopfzeile Ihrer API-Anforderungen verwendet werden.

Um eine sichere Service-to-Service-Adobe-API-Sitzung einzurichten, muss jede Anforderung an einen Adobe-Dienst die unten stehenden Informationen in den Autorisierungs-Header aufnehmen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

* **&lt;ORGANISATION&gt;**: Dies ist Ihre persönliche Organisations-ID, eine Organisations-ID wird von Adobe für jede Ihrer Instanzen bereitgestellt:

   * &lt;ORGANISATION&gt;: Ihre Produktionsinstanz,
   * &lt;ORGANISATION-mkt-stage&gt;: Ihre Stage-Instanz.
   Wenden Sie sich an Ihren Administrator oder Ihren technischen Ansprechpartner bei Adobe, um Ihren Organisations-ID-Wert abzurufen. Sie können sie auch beim Erstellen einer neuen Integration in die Adobe-E/A-Datei in der Liste der Lizenzen abrufen (siehe <a href="https://www.adobe.io/authentication.html">Adobe IO-Dokumentation</a>).

* **&lt;ACCESS_TOKEN&gt;**: Ihr persönliches Zugriffstoken, das beim Austausch Ihres JSON-Webtokens über eine POST-Anforderung abgerufen wurde.

* **&lt;API_KEY&gt;**: Ihren persönlichen API-Schlüssel. Sie wird in Adobe I/O bereitgestellt, nachdem eine neue Integration in Adobe Campaign Service erstellt wurde.

   ![ALT-Text](assets/tenant.png)
