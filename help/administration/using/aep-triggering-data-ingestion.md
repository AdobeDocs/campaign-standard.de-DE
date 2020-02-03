---
title: Auslösen der Datenerfassung über APIs
description: Erfahren Sie, wie die Datenerfassung über APIs ausgelöst wird.
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 67223cf8eed46e2431c03674bd837262e37c7473

---


# Auslösen der Datenerfassung über APIs {#triggering-data-ingestion-apis}

>[!IMPORTANT]
>
>Der Campaign Standard-Datendienst befindet sich derzeit in der Betaphase, die möglicherweise ohne Vorankündigung häufig aktualisiert wird. Kunden müssen auf Azurblau gehostet werden (derzeit nur in der Beta-Version für Nordamerika), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Zugriff haben möchten.

Mit Adobe Campaign Standard können Sie die sofortige Erfassung von Datenzuordnungen über APIs auslösen und den Status Ihrer Erfassungsanforderungen abrufen.

Auf dieser Seite wird beschrieben, wie Sie den Erfassungsstatus Ihrer Datenzuordnungen auslösen und abrufen. Globale Informationen zu Campaign Standard-APIs finden Sie in [diesem Abschnitt](../../api/using/about-campaign-standard-apis.md).

## Voraussetzungen {#prerequisites}

Bevor Sie die APIs verwenden, muss die Datenzuordnung zunächst in der Benutzeroberfläche von Campaign Standard konfiguriert und veröffentlicht worden sein. Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Zuordnungsdefinition](../../administration/using/aep-mapping-definition.md)
* [Aktivierung zuordnen](../../administration/using/aep-mapping-activation.md)

Nachdem die Datenzuordnung erstellt wurde, müssen Sie die Ausführung beenden, damit Sie sie jederzeit aus den APIs auslösen können. Gehen Sie dazu wie folgt vor:

1. Gehen Sie in Campaign Standard zum Menü **[!UICONTROL Administration]**>**[!UICONTROL  Entwicklung]** > **[!UICONTROL Plattform]**>**[!UICONTROL  Status des Datenexports in Plattform]** .

1. Doppelklicken Sie auf die Datenzuordnung, um sie zu öffnen, und klicken Sie dann auf die Schaltfläche **[!UICONTROL Stopp]**.

   ![](assets/aep_datamapping_stop.png)

1. Speichern Sie Ihre Änderungen

Die Ausführung der Datenzuordnung wird jetzt beendet. Sie können Campaign Standard-APIs verwenden, um sie manuell auszulösen.

## Starten der sofortigen Erfassung der Datenzuordnung {#starting-immediate-ingestion}

Die sofortige Erfassung einer XDM-Zuordnung zur Adobe Experience Platform wird mit einem POST-Vorgang ausgelöst:

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest`

>[!NOTE]
>
>Um den ingest POST API-Aufruf ausführen zu können, muss der Benutzer über eine **SQL-Funktion** verfügen, die von einem Campaign Standard-Administrator bereitgestellt werden kann, indem er unter JS Script ausgeführt wird:
>
>`var sqlRoleObj = REST.head.roleBase.sql.get();
REST.head.securityGroup.Administrators.roles.post(sqlRoleObj);`

Der POST-Vorgang gibt Informationen zum erstellten Anforderungsstatus zurück:

* Anfrage erfolgreich für die XDM-Zuordnung gesendet:

```
{
"requestId": <value>,
"info": "Ingestion request submitted successfully for the Mapping ID: <value>",
"status":"Success"
}
```

* Anfrage, die bereits für die XDM-Zuordnung ausgeführt wird:

```
{
"requestId": <value>,
"info": "Ingestion request already in progress for the Mapping ID: <value>",
"status":"In Progress"
}
```

* Anforderung fehlgeschlagen, da die XDM-Zuordnung nicht veröffentlicht wurde oder beendet wurde:

```
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not stopped",
"status": "Failed"
}
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not published",
"status": "Failed"
}
```

## Abrufen des Status einer Erfassungsanforderung {#retrieving-status}

Der Status einer Erfassungsanforderung kann mit einem GET-Vorgang und der gewünschten Anforderungs-ID in den Parametern abgerufen werden:

```
GET https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest
{"requestId"="<value>"}
```

>[!NOTE]
Ausführliche Informationen zum Status der XDM-Zuordnungsanforderung und der zugehörigen Aufträge finden Sie in der Benutzeroberfläche von Campaign Standard im Menü &quot; **!UICONTROL [Status des Datenexports in Plattform]** &quot;(siehe Aktivierung[der ](../../administration/using/aep-mapping-activation.md)Zuordnung).

Der GET-Vorgang gibt die folgenden Informationen zurück:

* **batchId**: Dieses Feld wird nur ausgefüllt, wenn nach der Stapelvorbereitung und dem Hochladen ein Fehler aufgetreten ist.
* **Info**: die XDM-Zuordnungs-ID,
* **numRecords**: die Anzahl der erfassten Datensätze (nur Erfolgsstatus),
* **Status**: der Erfassungsanforderungsstatus (Erfolg/Fehlgeschlagen/Wird ausgeführt)

Mögliche Antworten auf den GET-Vorgang sind:

* Anfrage erfolgreich aufnehmen:

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. ",
   "numRecords": 15,
   "requestId": 3520,
   "status": "Success"
   }
   ````

* Die Erfassungsanforderung schlug mit 0 Datensatz fehl:

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. ACP-880056 Failed to fetch the record from the database.",
   "numRecords": 0,
   "requestId": 3520,
   "status": "Failed"
   }
   ```

* Anfrage konnte nicht erfasst werden, wobei ein Datensatz unter einem Stapel hochgeladen wurde:

   ````
   {
   "batchId": "<value>",
   "info": "Mapping Id: <value>. ACP-880096 Sync Job failed to upload. Please check the error in the Platform UI.",
   "numRecords": 0,
   "requestId": <value>,
   "status": "Failed"
   }
   ```
   
* Anforderung nach dem Erfassen einiger Datensätze abgebrochen haben (dies kann in Crash-Szenarien passieren):

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. Ingestion request aborted due to some issue with data ingestion service. Please submit a new request",
   "numRecords": 0,
   "requestId": <value>,
   "status": "Aborted"
   }
   ```

* Anfrage wird verarbeitet (beim Hochladen der Daten in einen Stapel oder bei der Vorbereitung des Stapels auf die Anforderung):

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>.",
   "numRecords": 0,
   "requestId": <value>,
   "status": "In Progress"
   }
   ```
