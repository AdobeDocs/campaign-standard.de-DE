---
title: Mapping-Aktivierung
description: Erfahren Sie, wie Sie Ihr Daten-Mapping aktivieren
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
source-git-commit: c2ed4b3c85ceef3b604a8f68d924c7e5d9fad900

---


# Mapping-Aktivierung {#mapping-activation}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Nach Abschluss der Mapping-Definition können Sie das Mapping veröffentlichen. Nach der Freigabe wird die Datenreplikation zwischen Campaign Standard und Adobe Experience Platform automatisch gestartet. At any time, you can stop the replication by clicking on the **[!UICONTROL Stop]** button.

Je nach Ihren Mapping-Änderungen können Sie festlegen, alle Ihre Datensätze erneut an die Adobe Experience Platform zu senden.

![](assets/aep_publishmapping.png)

Auf der Freigabekachel können Sie auf das Publikationslog und die Exportprotokolle zugreifen.

![](assets/aep_publog.png)

In the **[!UICONTROL Export jobs]** tab, you can monitor the export job for the published mapping.

![](assets/aep_jobstatus.png)

Wenn Sie alle Datenexportaufträge überwachen möchten, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** Menü.

![](assets/aep_statusmapping.png)

Status des Datenerfassungsvorgangs:

* **[!UICONTROL Created]**: Es wird ein Datenerfassungsauftrag erstellt und die Datenerfassung wird ausgeführt.
* **[!UICONTROL Failed]**: Ein Datenerfassungsauftrag ist fehlgeschlagen. Das Feld „Grund“ beschreibt den Grund des Fehlschlagens. Fehler können vorübergehend oder dauerhaft sein. Bei vorübergehenden Fehlern wird nach einem konfigurierten Intervall ein neuer Erfassungsvorgang erstellt. Als ersten Schritt zur Fehlerbehebung können Benutzer das Feld „Grund“ des Fehlers überprüfen. Wenn der Grund einen Benutzer zur Adobe Experience Platform-Benutzeroberfläche weiterleitet, kann sich der Benutzer dort anmelden und den Batch-Status im Datensatz prüfen, um den genauen Fehlergrund zu ermitteln.
* **[!UICONTROL Uploaded]**: Zuerst wird ein Stapel in Adobe Experience Platform erstellt, und dann werden Daten in den Stapel aufgenommen. Das Feld „Batch-ID“ zeigt die Batch-ID für den Batch in Adobe Experience Platform an. Adobe Experience Platform führt auch eine Nachvalidierung für den Batch durch. Der Batch wird zuerst als hochgeladen markiert, bis Adobe Experience Platform den Nachvalidierungsschritt abgeschlossen hat. Ein Vorgang fragt nach dem Hochladen weiterhin den Batch-Status von der Adobe Experience Platform ab. Ein Batch kann in Adobe Experience Platform bei der Validierung entweder den Status „Fehlgeschlagen“ oder „Erfolgreich abgeschlossen“ erhalten.
* **[!UICONTROL Success]**: Nach dem Hochladen eines Stapels auf die Adobe Experience Platform wird der Status des Auftrags (nach der Überprüfung in der Plattform) nach einem konfigurierten Intervall überprüft. Der Status „Erfolgreich abgeschlossen“ kennzeichnet eine erfolgreiche Datenerfassung in Adobe Experience Platform.
