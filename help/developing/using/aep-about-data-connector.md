---
solution: Campaign Standard
product: campaign
title: Über Adobe Experience Platform Data Connector
description: Verwalten Sie XDM-Schemata, um Ihre Campaign Standard-Daten in Adobe Experience Platform verfügbar zu machen.
audience: administration
content-type: reference
topic-tags: configuring-channels
translation-type: tm+mt
source-git-commit: 2a92600df01fd3c78a2b35c8034a2ce347e5c1d8
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 96%

---


# Über Adobe Experience Platform Data Connector {#about-aep-data-connector}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Adobe Experience Platform Data Connector hilft Bestandskunden, ihre Daten in Adobe Experience Platform verfügbar zu machen, indem XTK-Daten (in Campaign erfasste Daten) den XDM-Daten (Experience-Datenmodell) in Adobe Experience Platform zugeordnet werden.

Beachten Sie, dass der Connector **unidirektional** ist und die Daten von Adobe Campaign Standard an Adobe Experience Platform sendet. Die Daten werden nie von Adobe Experience Platform an Adobe Campaign Standard gesendet.

Adobe Experience Platform Data Connector ist für **Dateningenieure** gedacht, die mit den benutzerdefinierten Ressourcen von Adobe Campaign Standard vertraut sind und verstehen, wie das gesamte Datenschema des Kunden in Adobe Experience Platform aussehen sollte.

Die folgenden Abschnitte beschreiben die wichtigen Schritte zum Durchführen eines Daten-Mappings zwischen Campaign Standard und Adobe Experience Platform. Dies beginnt mit der Erstellung eines XDM-Schemas und eines Datensatzes.

![](assets/do-not-localize/how-to-video.png) [Funktion im Video kennenlernen](#video).

>[!NOTE]
>Sobald Adobe Experience Platform Data Connector konfiguriert und Daten erfolgreich in Adobe Experience Platform integriert wurden, müssen Sie den Datensatz aktivieren, damit die Daten in das Echtzeit-Kundenprofil aufgenommen werden.
>
>Dies kann entweder über die APIs oder die Benutzeroberfläche von Adobe Experience Platform erfolgen. Weitere Informationen finden Sie in den entsprechenden Dokumentationen:
>
>* [Datensatz für Echtzeit-Kundenprofile aktivieren](https://docs.adobe.com/content/help/de-DE/experience-platform/rtcdp/datasets/dataset.html)
>* [Datensatz für Echtzeit-Kundenprofile und Identitätsdienst mithilfe von APIs konfigurieren](https://docs.adobe.com/content/help/de-DE/experience-platform/catalog/api/getting-started.html)


## Schlüsselkonzepte {#key-concepts}

* Vordefiniertes Mapping ist nur für Felder verfügbar, die standardmäßig in Campaign Standard bereitgestellt werden. Für die Erfassung aller benutzerdefinierten Felder und Ressourcen muss jeder Kunde sein eigenes Mapping definieren.

* Adobe Experience Platform Data Connector leitet Profildaten in regelmäßigen Abständen durch die Plattform.&#x200B; Die Intervalldauer beträgt 15 Minuten. Dieser Wert kann mit [Adobe Experience Platform-APIs](https://docs.adobe.com/content/help/de-DE/experience-platform/ingestion/home.html) geändert werden.

* Der Dateningenieur kann das Mapping von Campaign zu Adobe Experience Platform veröffentlichen, ändern und anhalten.

* Jede Zielgruppendimension kann abgebildet werden. Es wird empfohlen, für alle Felder in einer Zielgruppendimension ein einziges Mapping zu verwenden.

* Alle Profilaktualisierungen, einschließlich Kanal-Opt-ins/-Opt-outs, sind Teil der Batch-Aktualisierung.

* Alle Änderungen am Adobe Campaign Standard- oder XDM-Schema müssen manuell neu abgebildet werden.&#x200B;

* Trackinglog- und Broadlog-Daten werden automatisch als Erlebnisereignisse in Adobe Experience Platform erfasst. Diese Erfassung wird in Echtzeit an Adobe Experience Platform gestreamt.

* Der Experience-Cloud-ID-Service (ECID) ist eine Gerätekennung, die standardmäßig mit Experience-Ereignissen gesendet wird.

   Es handelt sich dabei um eine eindeutige und beständige Kennung, mit der der Platform Identity Service denselben Besucher und seine Daten in verschiedenen Experience Cloud-Lösungen identifizieren kann. Weiterführende Informationen finden Sie in der Hilfe zum [Experience Cloud Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html).

   >[!NOTE]
   >
   >Hinweis: Wenn sich zwei oder mehr Profile das gleiche Gerät teilen, ist die ECID für diese beiden Profile im Unified Identity Service identisch.

## Einschränkungen {#limitations}

* Die vordefinierte Übertragung von Abonnementereignissen wird nicht unterstützt. Um Abonnementereignisse zu übertragen, können Sie ein entsprechendes XDM und einen Datensatz in Adobe Experience Platform erstellen und dann ein benutzerdefiniertes Daten-Mapping für diese Daten konfigurieren.

* In Bezug auf Datenschutzanfragen (sowohl Zugriffs- als auch Löschaktionen) müssen Kunden separate Anfragen über den [Datenschutz-Coreservice](https://docs.adobe.com/content/help/de-DE/experience-platform/privacy/home.html#how-to-use-privacy-service-to-manage-privacy-job-requests) stellen: eine für Campaign und eine für Adobe Experience Platform. Weitere Informationen hierzu finden Sie unter [Allgemeines zu Datenschutzanfragen](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#righttoaccess) und [Verwalten von Datenschutzanfragen](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#ManagingPrivacyRequests) in Campaign.

* Für jedes XDM-Feld muss die DULE-Kennzeichnung in Adobe Experience Platform erfolgen. Es liegt in der Verantwortung des Kunden, DULE-Kennzeichnungen anzuwenden.

* Beschränkungen für Marketing-Aktionen werden erst nach Anwendung der DULE-Kennzeichnungen in Adobe Experience Platform wirksam. Davor sind alle Daten für alle Arten von Marketing-Aktionen verfügbar.

* Die Batch-Vorgänge wird alle 15 Minuten ausgeführt und identifiziert die Datensätze, die sich seit dem letzten Batch geändert haben. Wenn sich alle Datensätze zum gleichen Zeitpunkt ändern, könnte bei der Erfassung aller Profile ein Leistungsengpass auftreten.

## Tutorial-Video {#video}

Dieses Video bietet einen Überblick über den Adobe Experience Platform Data Connector.

https://video.tv.adobe.com/v/27304?quality=12&amp;captions=ger

Weitere Videos zum Adobe Experience Platform Data Connector finden Sie unter [hier](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.translate.html).
