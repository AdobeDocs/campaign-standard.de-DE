---
title: Über die Integration von Campaign mit Experience Manager
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: ff94f69b-3036-4103-a841-6b85feb0eb7e
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 98%

---

# Über die Integration von Campaign mit Experience Manager{#integrating-with-experience-manager}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

Auf diese Weise profitieren Sie gleichermaßen von den fortgeschrittenen Funktionen zur Inhaltsgestaltung in Adobe Experience Manager und den außerordentlichen Versand- sowie Datenverwaltungsfähigkeiten von Adobe Campaign. Bitte beachten Sie, dass Sie für aus Adobe Experience Manager importierte Inhalte keine A/B-Tests durchführen können.

Adobe Campaign Standard ist mit Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 und 6.5 kompatibel. Im Folgenden finden Sie eine Übersicht der möglichen Aktionen. Weiterführende Informationen finden Sie in den Abschnitten [Konfiguration](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de) und [Vorgehensweise](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=de) zur Integration.

>[!NOTE]
>
> Adobe Campaign Standard-Vorlagen sind in Adobe Experience Manager 6.5 nicht mehr verfügbar.

## Tipps zur Verwendung der Integration von Campaign mit Experience Manager {#tips-aem}

* **Verwenden Sie eine für die Integration geeigneten Vorlage.**

  Da E-Mail-Vorlagen in Adobe Experience Manager bearbeitet werden können, wäre es naheliegend, für die Bearbeitung aller Vorlagen Adobe Experience Manager zu verwenden. Bestimmte Vorlagen sind jedoch nicht einfach zu handhaben. Kundenspezifische, individualisierte Vorlagen sind für diese Integration nicht zu empfehlen und sollten direkt in Adobe Campaign Standard bearbeitet werden.

  Weiterführende Informationen zu Vorlagen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=de).

* **Stellen Sie sicher, dass der Externalizer bei der Implementierung konfiguriert wurde.**

  Bei der Implementierung von Experience Manager muss der Externalizer für Adobe Campaign Standard konfiguriert werden, damit ein Ressourcenpfad in eine URL umgewandelt werden kann. Dies ist erforderlich, um Ihre Bilder auf der Seite sichtbar zu machen. Wenn der Externalizer nicht richtig konfiguriert ist, enthalten Ihre E-Mails fehlerhafte Bilder.

  Informationen zur Konfiguration des Externalizers finden Sie in diesem Abschnitt [page](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/externalizer.html?lang=de).

* **Organisieren Sie Ihre E-Mail-Vorlagen, um zu vermeiden, dass die falschen verwendet werden.**

  Indem Sie Vorlagen organisiert halten, stellen Sie sicher, dass diese in den ihrer Funktion entsprechenden Ordnern abgelegt werden, sodass nicht versehentlich die falschen verwendet werden. Bei der Implementierung sollten daher Pfade erstellt werden, um Vorlagen an den richtigen Speicherorten abzulegen.

  Weiterführende Informationen zu Vorlagen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=de#template-availability).

* **Vordefinierten Komponenten erleichtern Ihnen den Einstieg.**

  Die in Adobe Experience Manager für Adobe Campaign Standard vordefinierten Komponenten erleichtern Ihnen den Einstieg, wenn Ihre Vorlagen nicht komplex sind.
In Experience Manager stehen hierfür sieben vordefinierte Komponenten zur Verfügung:

   * Überschrift
   * Bild
   * Link
   * Scene7-Bildvorlage
   * Zielgerichteter Verweis
   * Text und Bild
   * Text und Personalisierung

* **HTML für E-Mails unterscheidet sich von HTML für das Web**

  Es ist wichtig zu verstehen, dass Sie für E-Mail-Vorlagen nicht dieselben Komponenten verwenden können wie für Ihre Webinhalte. Mit vordefinierten Komponenten wird sichergestellt, dass Ihre Komponenten mit E-Mail kompatibel sind.

* **Heben Sie die Verknüpfung von Inhalten mit Vorlagen auf, um die Vorlagen wiederzuverwenden.**

  Wenn Sie für die Einrichtung Ihrer E-Mails in Campaign Standard eine Experience Manager-Vorlage verwenden, darf diese Vorlage nicht mit einer anderen Kampagne verknüpft sein. Andernfalls würden Sie, wenn Sie den Inhalt in Adobe Experience Manager für die eine Kampagne ändern und aktualisieren, den Inhalt in der anderen Kampagne unbeabsichtigt beeinflussen.
Um dies zu vermeiden, können Sie die Verknüpfung der Vorlage aufheben, nachdem Sie die Vorlage verwendet haben. Wählen Sie dazu einfach die Vorlage aus und klicken Sie auf **[!UICONTROL Verknüpfung mit Adobe Experience Manager-Inhalt löschen]**.

* **Erstellen Sie mit Adobe Experience Manager verschiedene Varianten von E-Mails für Adobe Campaign Standard.**

  Mithilfe der Segmentierung ermöglicht es diese Integration, aus einer E-Mail mühelos mehrere Versionen erstellen.
Informationen zum Einrichten der Segmentierung in Adobe Experience Manager und zum Erstellen von E-Mails mit zielgerichteten Inhalten finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html?lang=de#setting-up-segmentation-in-aem).

* **Für eine erfolgreiche Synchronisierung muss der Segmentname in Experience Manager exakt mit dem Segmentnamen in Campaign übereinstimmen.**
