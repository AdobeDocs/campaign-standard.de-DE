---
title: Benutzerdefinierte Ressourcen und benutzerdefinierte Entitäten für die Kampagne zuordnen
description: Erfahren Sie, wie Sie Ressourcen und Entitäten im Kontext der Integration zwischen Adobe Campaign Standard und Microsoft Dynamics 365 zuordnen.
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
translation-type: tm+mt
source-git-commit: e11de4d4482400e62be2db076c88da5ae30d60cc
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 1%

---


# Landkarten-Kampagnen und Dynamics 365-Stellen

Erfahren Sie, wie Sie benutzerdefinierte Ressourcen und benutzerdefinierte Entitäten im Kontext der Integration zwischen Adobe Campaign Standard und Microsoft Dynamics 365 zuordnen.

>[!CAUTION]
>
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Kundenbetreuer, um weitere Informationen zu erhalten.

## Voraussetzungen

Die [Microsoft Dynamics 365-Adobe Campaign Standard-Integration](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md) unterstützt benutzerdefinierte Entitäten und ermöglicht die Synchronisierung von benutzerdefinierten Entitäten in Dynamics 365 mit entsprechenden benutzerdefinierten Ressourcen in der Kampagne.

Die neuen Daten in den benutzerdefinierten Ressourcen können für verschiedene Zwecke verwendet werden, einschließlich Segmentierung und Personalisierung.

Die Integration unterstützt sowohl verknüpfte als auch nicht verknüpfte Tabellen. Die Verknüpfung wird bis zu drei Ebenen unterstützt (d.h. Level1->Level2->Level3).

>[!CAUTION]
>
>Wenn ein benutzerdefinierter Ressourcendatensatz eine Kampagne mit personenbezogenen Daten enthält, gelten spezifische Empfehlungen. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../integrating/using/notices-and-recommendations-for-acs-and-ms-dynamics.md#privacy-linked-resources).

## Hinweise

Bei der Konfiguration benutzerdefinierter Entitätsdatenflüsse ist Folgendes zu beachten:

* Das Erstellen und Bearbeiten benutzerdefinierter Kampagnen sind sensible Vorgänge, die nur von Fachbenutzern ausgeführt werden müssen.
* Bei Datenströmen benutzerdefinierter Entitäten muss die Änderungsverfolgung in Dynamics 365 für synchronisierte benutzerdefinierte Entitäten aktiviert werden.
* Wenn ein übergeordneter und verknüpfter untergeordneter Datensatz in Dynamics 365 aufgrund der parallelen Verarbeitung der Integration nahezu gleichzeitig erstellt wird, besteht eine geringe Wahrscheinlichkeit, dass ein neuer untergeordneter Datensatz vor dem übergeordneten Datensatz in Kampagne geschrieben werden könnte.

* Wenn das übergeordnete und das untergeordnete Element mithilfe des einfachen Links **&quot;** 1 Kardinalität&quot;auf der Seite der Kampagne verknüpft sind, bleibt der untergeordnete Datensatz ausgeblendet und kann (über die Benutzeroberfläche oder API) nicht aufgerufen werden, bis der übergeordnete Datensatz in der Kampagne ankommt.

* (Angenommen, es wird ein einfacher Link **** zur Kardinalität in der Kampagne verwendet) Wenn der untergeordnete Datensatz in Dynamics 365 aktualisiert oder gelöscht wird und diese Änderung in Kampagne geschrieben wird, bevor der übergeordnete Datensatz in der Kampagne angezeigt wird (nicht wahrscheinlich, aber eine entfernte Möglichkeit), wird diese Aktualisierung oder Löschung nicht in der Kampagne verarbeitet und es wird ein Fehler ausgegeben. Im Falle einer Aktualisierung muss der betreffende Datensatz erneut in Dynamics 365 aktualisiert werden, um den aktualisierten Datensatz zu synchronisieren. Im Falle der Löschung muss der betreffende Datensatz gesondert auf der Kampagne behandelt werden, da in Dynamics 365 kein Datensatz mehr zum Löschen oder Aktualisieren vorhanden ist.

* Wenn Sie in einer Situation leben, in der Sie glauben, dass Sie versteckte Kinderdatensätze haben und keinen Zugriff darauf haben, können Sie den Kardinalität-Link-Typ vorübergehend auf **0 oder 1 Kardinalität einfach Link** ändern, um auf diese Datensätze zuzugreifen.

A more comprehensive overview of Campaign custom resources can be found [in this section](../../developing/using/key-steps-to-add-a-resource.md).
