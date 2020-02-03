---
title: Info zur Campaign-Experience Manager-Integration
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5c1a540475b7d93c18c957243ee2a403b8154aa3

---


# Info zur Campaign-Experience Manager-Integration{#integrating-with-experience-manager}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

Auf diese Weise profitieren Sie gleichermaßen von den fortgeschrittenen Funktionen zur Inhaltsgestaltung in Adobe Experience Manager und den außerordentlichen Versand- sowie Datenverwaltungskapazitäten Adobe Campaigns. Beachten Sie, dass Sie keine A/B-Tests für Inhalte durchführen können, die aus Adobe Experience Manager importiert wurden.

Adobe Campaign Standard ist mit Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 und 6.5 kompatibel. Die folgenden Abschnitte enthalten eine Übersicht über die Aktionen, die Sie ausführen können. Weiterführende Informationen finden Sie in den Abschnitten [Konfiguration](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html) und [Vorgehensweise](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/campaign.html).

>[!NOTE]
>
> Adobe Campaign Standard-Vorlagen sind in Adobe Experience Manager 6.5 nicht mehr verfügbar.

## Tipps zur Verwendung der Campaign-Experience Manager-Integration {#tips-aem}

* **Erkennen der Vorlage für die Integration**

   Da E-Mail-Vorlagen in Adobe Experience Manager bearbeitet werden können, ist es möglicherweise einfacher, eine beliebige Vorlage in Adobe Experience Manager zu bearbeiten. Bestimmte Vorlagen sind jedoch nicht einfach einzuordnen. Für diese Integration werden benutzerdefinierte, kundenspezifische Vorlagen nicht empfohlen und sollten direkt in Adobe Campaign Standard bearbeitet werden.

   For more information on templates, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html).

* **Stellen Sie sicher, dass Externalizer während der Implementierung konfiguriert wurde.**

   Durch die Konfiguration des Externalisierers während der Implementierung von Experience Manager für Adobe Campaign Standard ist es möglich, einen Ressourcenpfad in eine URL umzuwandeln. Dadurch können Sie Ihre Bilder auf der Seite sichtbar machen. Wenn der Externalizer nicht richtig konfiguriert ist, enthalten Ihre E-Mails beschädigte Bilder.

   To learn how to configure the Externalizer, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/externalizer.html)

* **Organisieren Sie Ihre E-Mail-Vorlagen, um Missbrauch zu vermeiden.**

   Durch die Organisation der Vorlagen wird sichergestellt, dass die entsprechenden Vorlagen in den entsprechenden Ordnern vorhanden sind und nicht versehentlich die falschen ausgewählt werden. Während der Implementierung sollten Pfade erstellt werden, um Vorlagen an den richtigen Stellen zu speichern.

   For more information on templates, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html#template-availability)

* **Schneller Einstieg in vordefinierte Komponenten.**

   Vordefinierte Komponenten in Adobe Experience Manager für Adobe Campaign Standard helfen Ihnen beim schnellen Einstieg, wenn Ihre Vorlagen nicht komplex sind.
Es gibt sieben sofort einsetzbare Komponenten in Experience Manager, die Sie verwenden können:
   1. Überschrift
   1. Bild
   1. Link
   1. Scene7-Bildvorlage
   1. Targeting-Referenz
   1. Text und Bild
   1. Text und Personalisierung

* **HTML für E-Mails unterscheidet sich von HTML für Web**

   Es ist wichtig zu verstehen, dass Sie nicht dieselben Komponenten verwenden können, die in Ihren Webinhalten für E-Mail-Vorlagen verwendet werden. Die Verwendung von vordefinierten Komponenten stellt sicher, dass Ihre Komponenten mit E-Mail kompatibel sind.

* **Heben Sie die Verknüpfung von Inhalten mit Vorlagen auf und verwenden Sie sie wieder und wieder.**

   Beim Einrichten Ihrer E-Mails in Campaign Standard und Auswählen einer Experience Manager-Vorlage können Sie nur eine E-Mail auswählen, die noch nicht mit einer anderen Kampagne verknüpft wurde. Andernfalls können Sie, wenn Sie den Inhalt in Adobe Experience Manager für eine Kampagne ändern und aktualisieren, den Inhalt in der anderen Kampagne unbeabsichtigt beeinflussen.
Um dies zu vermeiden, können Sie die Verknüpfung der Vorlage aufheben, sobald Sie die Vorlage verwendet haben. Sie müssen nur die Vorlage auswählen und auf Link mit Adobe Experience Manager-Inhalt **[!UICONTROL löschen klicken]**.

* **Verwenden Sie Adobe Experience Manager, um verschiedene E-Mails für Adobe Campaign Standard zu erstellen.**

   Mit dieser Integration können Sie eine E-Mail mit der Segmentierung problemlos in mehrere Versionen umwandeln.
Informationen zum Einrichten der Segmentierung in Adobe Experience Manager und zum Erstellen von E-Mails mit zielgerichteten Inhalten finden Sie auf dieser [Seite](https://docs.adobe.com/help/en/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem).

* **Für eine erfolgreiche Synchronisierung muss der Segmentname in Experience Manager exakt mit dem Segmentnamen in Campaign übereinstimmen.**