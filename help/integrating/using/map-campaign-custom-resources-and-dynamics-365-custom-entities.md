---
title: Benutzerdefinierte Campaign-Ressourcen und benutzerdefinierte Dynamics 365-Entitäten zuordnen
description: Erfahren Sie, wie Sie im Kontext der Integration von Adobe Campaign Standard und Microsoft Dynamics 365 Ressourcen und Entitäten zuordnen können.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: ht
source-git-commit: e11de4d4482400e62be2db076c88da5ae30d60cc
workflow-type: ht
source-wordcount: '457'
ht-degree: 100%

---


# Campaign-Ressourcen und Dynamics 365-Entitäten zuordnen

Erfahren Sie, wie Sie im Kontext der Integration von Adobe Campaign Standard und Microsoft Dynamics 365 benutzerdefinierte Ressourcen und benutzerdefinierte Entitäten zuordnen können.

>[!CAUTION]
>
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um weitere Informationen zu erhalten.

## Voraussetzungen

Die [Integration von Adobe Campaign Standard mit Microsoft Dynamics 365](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md) unterstützt benutzerdefinierte Entitäten und ermöglicht die Synchronisation von benutzerdefinierten Entitäten in Dynamics 365 mit entsprechenden benutzerdefinierten Ressourcen in Campaign.

Die neuen Daten in den benutzerdefinierten Ressourcen können für verschiedene Zwecke verwendet werden, einschließlich Segmentierung und Personalisierung.

Die Integration unterstützt sowohl verknüpfte als auch nicht verknüpfte Tabellen. Die Verknüpfung wird auf bis zu drei Ebenen unterstützt (d. h. Level1->Level2->Level3).

>[!CAUTION]
>
>Wenn ein benutzerdefinierter Ressourcendatensatz in Campaign personenbezogene Daten enthält, gelten besondere Empfehlungen. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../integrating/using/notices-and-recommendations-for-acs-and-ms-dynamics.md#privacy-linked-resources).

## Hinweise

Bei der Konfiguration benutzerdefinierter Entitätsdatenflüsse ist Folgendes zu beachten:

* Die Erstellung und Änderung von benutzerdefinierten Campaign-Ressourcen sind heikle Aufgaben, die nur von erfahrenen Benutzern durchgeführt werden können.
* Bei benutzerdefinierten Entitätsdatenflüssen muss für synchronisierte benutzerdefinierte Entitäten die Änderungsverfolgung innerhalb von Dynamics 365 aktiviert werden.
* Wenn ein übergeordneter und ein verknüpfter untergeordneter Datensatz in Dynamics 365 aufgrund der parallelen Verarbeitung der Integration nahezu zur gleichen Zeit erstellt werden, besteht eine geringe Wahrscheinlichkeit, dass ein neuer untergeordneter Datensatz vor seinem übergeordneten Datensatz in Campaign geschrieben wird.

* Wenn das übergeordnete und das untergeordnete Element in Campaign mithilfe der Option **Einfache Relation mit Kardinalität 1** verknüpft sind, bleibt der untergeordnete Datensatz ausgeblendet und kann (über die Benutzeroberfläche oder API) nicht aufgerufen werden, bis der übergeordnete Datensatz in Campaign eintrifft.

* (Angenommen, **Einfache Relation mit Kardinalität 1** wird in Campaign verwendet.) Wenn der untergeordnete Datensatz in Dynamics 365 aktualisiert oder gelöscht wird und diese Änderung in Campaign geschrieben wird, bevor der übergeordnete Datensatz in Campaign angezeigt wird (nicht wahrscheinlich, aber möglich), wird diese Aktualisierung oder Löschung nicht in Campaign verarbeitet und ein Fehler ausgegeben. Im Falle einer Aktualisierung muss der betreffende Datensatz erneut in Dynamics 365 aktualisiert werden, um den aktualisierten Datensatz zu synchronisieren. Im Falle der Löschung muss der betreffende Datensatz in Campaign gesondert behandelt werden, da in Dynamics 365 kein Datensatz mehr zum Löschen oder Aktualisieren vorhanden ist.

* Wenn Sie in eine Situation geraten, in der Sie glauben, versteckte untergeordnete Datensätze zu haben und nicht darauf zugreifen zu können, können Sie den Kardinalität-Relationstyp vorübergehend in **Einfache Relation mit Kardinalität 0 oder 1** ändern, um auf diese Datensätze zuzugreifen.

Eine umfassendere Übersicht über benutzerdefinierte Campaign-Ressourcen finden Sie [in diesem Abschnitt](../../developing/using/key-steps-to-add-a-resource.md).
