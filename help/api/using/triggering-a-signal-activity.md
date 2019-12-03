---
title: Auslösen einer Signalaktivität
description: Erfahren Sie, wie Sie eine Signalaktivität mit APIs auslösen.
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


# Auslösen einer Signalaktivität {#triggering-a-signal-activity}

In einem Adobe Campaign Standard-Arbeitsablauf kann es eine oder mehrere **externe Signalaktivitäten** geben. Bei diesen Aktivitäten handelt es sich um "Listener", die auf die Auslösung warten.

Mit den Kampagnenstandard-APIs können Sie eine **Aktivität für externe Signale** auslösen, um einen Workflow aufzurufen. Der API-Aufruf kann Parameter enthalten, die in die Ereignisvariablen des Workflows eingebunden werden (Zielgruppenname für Target, zu importierender Dateiname, Teil des Nachrichteninhalts usw.). Auf diese Weise lassen sich Ihre automatisch durchgeführten Campaign-Prozesse einfach mit einem externen Datensystem integrieren.

>[!NOTE]
>
>Externe Signalaktivitäten können nicht öfter als alle 10 Minuten ausgelöst werden und der Ziel-Workflow muss bereits ausgeführt werden.

Gehen Sie wie folgt vor, um einen Workflow auszulösen:

1. Führen Sie im Workflow eine **GET** -Anforderung durch, um die URL des Auslösers für externe Signalaktivität abzurufen.

   `GET https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>`

1. Führen Sie eine **POST** -Anforderung an die zurückgegebene URL aus, um die Signalaktivität auszulösen, wobei der Parameter **"source"** in der Nutzlast enthalten ist. Dieses Attribut ist obligatorisch. Sie können die auslösende Anforderungsquelle angeben.

Wenn Sie den Workflow mit Parametern aufrufen möchten, fügen Sie sie mit dem Attribut **"parameters"** in die Nutzlast ein. Die Syntax besteht aus dem Namen des Parameters gefolgt vom Wert (die folgenden Typen werden unterstützt: **Zeichenfolge**, **Nummer**, **Boolescher Wert** und **Datum/Uhrzeit**).

```
  -X POST <TRIGGER_URL>
  -H 'Authorization: Bearer <ACCESS_TOKEN>' \
  -H 'Cache-Control: no-cache' \
  -H 'X-Api-Key: <API_KEY>' \
  -H 'Content-Type: application/json;charset=utf-8' \
  -H 'Content-Length:79' \
  -i
  -d {
  -d    "source":"<SOURCE>",
  -d    "parameters":{
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>",  
  -d      "<PARAMETER_NAME":"<PARAMETER_VALUE>"
  -d    }
  -d }
```

>[!NOTE]
>
>Stellen Sie beim Hinzufügen eines Parameters zur Payload sicher, dass seine **Namen** - und **Typwerte** mit den in der Aktivität "Externes Signal"deklarierten Informationen übereinstimmen. Darüber hinaus sollte die Nutzdatengröße 64 Ko nicht überschreiten.

<br/>

***Musteranforderung***

Führen Sie eine GET-Anforderung für den Workflow durch.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die Workflow-Signalaktivität und die zugehörige Auslöser-URL zurück.

```
{
"PKey": "<PKEY>",
"activities": {
  "activity": {
    "signal1": {
      ...
      "trigger": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<PKEY>/activities/activity/<PKEY>/trigger/"
        },
        ...
      }
    }
  }
}
```

Um eine Signalaktivität auszulösen, führen Sie eine POST-Anforderung an die Auslöser-URL mit der "Quelle"durch. Fügen Sie die Attribute "Parameter"hinzu, wenn Sie den Workflow mit Parametern aufrufen möchten.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<PKEY>/activities/activity/<PKEY>/trigger \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{
-d "source":"API",
-d "parameters":{
-d    "audience":"audience",
-d    "email":"anna.varney@mail.com",
-d    "template":"05",
-d    "contentURL":"http://www.adobe.com",
-d    "test":"true",
-d    "segmentCode":"my segment",
-d    "attribute":"2019-04-03 08:17:19.100Z"}
-d  }'
```

<!-- + réponse -->

Wenn einer der Parameter nicht in der Aktivität "Externes Signal"deklariert ist, gibt die POST-Anforderung den unten stehenden Fehler zurück, der angibt, welcher Parameter fehlt.

```
RST-360011 An error has occurred - please contact your administrator.
'contentURL' parameter isn't defined in signal activity.
XTK-170006 Unable to parse expression 'HandleTrigger(@name, $(source), $({parameters}))'.
RST-360000 Error while assessing 'HandleTrigger(@name, $(source), $({parameters}))' expression ('xtk:workflow:execution/activities/signal/trigger' resource)
```
