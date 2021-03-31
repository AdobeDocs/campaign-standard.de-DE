---
solution: Campaign Standard
product: campaign
title: Steuern eines Workflows
description: Erfahren Sie, wie Sie mit APIs einen Workflow steuern können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Erfahren
translation-type: ht
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: ht
source-wordcount: '100'
ht-degree: 100%

---


# Steuern eines Workflows {#controlling-a-workflow}

Sie können einen Workflow direkt über die REST-API steuern, indem Sie eine POST-Anfrage mit der Workflow-Kennung und dem erforderlichen Ausführungsbefehl verwenden:

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands`

>[!CAUTION]
>
>Wenn die Workflow-Kennung in Adobe Campaign geändert wird, funktioniert die API-Anfrage nicht mehr.

Zum Steuern eines Workflows stehen vier Ausführungsbefehle zur Verfügung:

* Starten
* Aussetzen
* Fortsetzen
* Anhalten

Weiterführende Informationen zu den Ausführungsbefehlen finden Sie in der [Campaign-Dokumentation](https://docs.adobe.com/content/help/de-DE/campaign-standard/using/managing-processes-and-data/executing-a-workflow/about-workflow-execution.html).

<br/>

***Beispielanfragen***

* Workflow starten

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -i
   -d '{"method":"start"}'
   ```

   <!-- + réponse -->

* Workflow anhalten

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/workflow/execution/<workflowID>/commands \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -i
   -d '{"method":"stop"}'
   ```

   <!-- + réponse -->
