---
title: Profile erstellen
description: Weitere Informationen zum Erstellen von Profilen mit APIs.
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
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# Profile erstellen {#creating-profiles}

Das Erstellen von Profilen wird mit einer **POST** -Anforderung in der Profilinstanz durchgeführt.

>[!CAUTION]
>
>Wenn Sie eine <b>orgUnit</b> mit dem erstellten Profil verknüpfen möchten, müssen Sie die Profilressource mit diesem Feld erweitern und nach der Veröffentlichung der Erweiterung eine POST-Anforderung am <b>ProfilAndServicesExt</b> -Endpunkt durchführen.
>
>Weitere Informationen zur Ressourcenerweiterung des Profils finden Sie in der <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">Kampagnendokumentation</a>.

<br/>

***Musteranforderung***

Beispiel-POST-Anfrage, um ein Profil mit der E-Mail "john.doe@mail.com"zu erstellen.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"email":"john.doe@mail.com"}'
```

Es wird das neu erstellte Profil mit der E-Mail-Adresse "john.doe@mail.com"zurückgegeben.

```
{
    "PKey": "<PKEY>",
    "firstName": "John",
    "lastName":"Doe",
    "birthDate": "1980-10-24",
    "email": "john.doe@mail.com",
    ...
}
```
