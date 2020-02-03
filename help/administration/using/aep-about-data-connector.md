---
title: Info zu Adobe Experience Platform Data Connector
description: Verwalten Sie XDM-Schemata, um Ihre Campaign Standard-Daten auf der Adobe Experience Platform verfügbar zu machen.
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
source-git-commit: 1059b840d9a2d0c89a6cbd1808b645862747a76c

---


# Info zu Adobe Experience Platform Data Connector {#about-aep-data-connector}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector befindet sich derzeit in der Betaphase, die möglicherweise ohne Vorankündigung häufig aktualisiert wird. Kunden müssen auf Azurblau gehostet werden (derzeit nur in der Beta-Version für Nordamerika), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Zugriff haben möchten.

Adobe Experience Platform Data Connector hilft bestehenden Kunden, ihre Daten auf der Adobe Experience Platform verfügbar zu machen, indem XTK-Daten (in Campaign erfasste Daten) den XDM-Daten (Experience Data Model) auf der Adobe Experience Platform zugeordnet werden.

Beachten Sie, dass der Connector **uni-direktional** ist und die Daten von Adobe Campaign Standard an Adobe Experience Platform sendet. Die Daten werden nie von der Adobe Experience Platform an Adobe Campaign Standard gesendet.

Adobe Experience Platform Data Connector ist für **Dateningenieure** gedacht, die die benutzerdefinierten Ressourcen von Adobe Campaign Standard verstehen und verstehen, wie das Datenschema des Kunden insgesamt in der Adobe Experience Platform sein sollte.

Die folgenden Abschnitte beschreiben die wichtigen Schritte zum Durchführen einer Datenzuordnung zwischen Campaign Standard und Adobe Experience Platform. Dies beginnt mit der Erstellung eines XDM-Schemas und eines Datensatzes.

>[!NOTE]
>Sobald Adobe Experience Platform Data Connector konfiguriert und Daten erfolgreich in Adobe Experience Platform integriert wurden, müssen Sie den Datensatz aktivieren, damit die Daten in das Echtzeit-Kundenprofil aufgenommen werden.
>
>Dies kann entweder über die APIs oder die Oberfläche von Adobe Experience Platform erfolgen. Weitere Informationen finden Sie in den Dokumentation:
>
>* [Datenbestand für Echtzeit-Kundenprofil aktivieren](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/data_ingestion_tutorial/data_ingestion_tutorial.md)
>* [DataSet für Echtzeit-Kundenprofil und Identitätsdienst mithilfe von APIs konfigurieren](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/unified_profile_dataset_tutorial/unified_profile_dataset_api_tutorial.md)


## Schlüsselkonzepte {#key-concepts}

* Die Out-of-the-Box-Zuordnung ist nur für Felder verfügbar, die standardmäßig in Campaign Standard bereitgestellt werden. Für die Erfassung aller benutzerdefinierten Felder und Ressourcen muss jeder Kunde seine eigene Zuordnung definieren.

* Adobe Experience Platform Data Connector leitet Profildaten in regelmäßigen Abständen durch die Plattform &#x200B; Die Intervalldauer beträgt 15 mn. Dieser Wert kann nicht geändert werden.

   >[!NOTE]
   >
   >Diese Dauer kann mit [Adobe Experience Platform-APIs](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/authenticate_to_acp_tutorial/authenticate_to_acp_tutorial.md)geändert werden.

* Der Datenentwickler kann die Zuordnung von Campaign zu Adobe Experience Platform veröffentlichen, ändern und anhalten.

* Jede Targeting-Dimension kann zugeordnet werden. Die Empfehlung besteht darin, eine einzige Zuordnung für alle Felder in einer Targeting-Dimension zu haben.

* Alle Profilaktualisierungen, einschließlich Channel-opt-ins/opt-outs, sind Teil der Batch-Aktualisierung.

* Alle Änderungen am Adobe Campaign Standard- oder XDM-Schema müssen manuell neu zugeordnet werden. &#x200B;

* Verfolgungsprotokoll und Broadlog-Daten werden automatisch als Experience Events in Adobe Experience Platform erfasst. Diese Erfassung wird in Echtzeit an Adobe Experience Platform gestreamt.

## Einschränkungen {#limitations}

* Die sofortige Übertragung von Abonnementereignissen wird nicht unterstützt. Um Abonnementereignisse zu übertragen, können Sie entsprechende XDM- und Datasets auf der Adobe Experience Platform erstellen und dann eine benutzerdefinierte Datenzuordnung für diese Daten konfigurieren.

* In Bezug auf Datenschutzanforderungen müssen Kunden separate Anforderungen für den Kampagnen-Core-Datenschutzdienst und die Adobe Experience Platform für Zugriffs- und Löschaktionen stellen.

* Für jedes XDM-Feld muss die DULE-Kennzeichnung in Adobe Experience Platform erfolgen. Dies ist die Verantwortung des Kunden, DULE-Etiketten anzuwenden.

* Beschränkungen für Marketingaktionen gelten erst, wenn DULE-Beschriftungen in Adobe Experience Platform angewendet werden. Zuvor sind alle Daten für alle Arten von Marketingaktionen verfügbar.

* Der Stapelauftrag wird alle 15 Minuten ausgeführt und identifiziert die Datensätze, die sich seit dem letzten Stapel geändert haben. Wenn sich alle Datensätze mit demselben Zeitstempel ändern, könnte ein Leistungsengpass für die Verwaltung der Erfassung aller Profile auftreten
