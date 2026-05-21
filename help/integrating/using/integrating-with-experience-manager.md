---
title: Über die Integration von Campaign mit Experience Manager
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: ff94f69b-3036-4103-a841-6b85feb0eb7e
TQID: https://experienceleague.adobe.com/OuQgaZgJVeL04fw3rvn5nydbp2fOSdQOVpiFhrUcEl4
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616aid: a658c786-869b-4194-a780-2594d663addaid: d5ef99fa-df0c-4153-bf94-105ad0724167
subfeature_v2: id: c3bf7e1e-1db5-4c72-9293-e2f0b1ab73d0id: df0d6518-6f49-46e2-b46e-3bcc513f553f
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 684
ht-degree: 96%

---

# Über die Integration von Campaign mit Experience Manager{#integrating-with-experience-manager}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

Auf diese Weise profitieren Sie gleichermaßen von den fortgeschrittenen Funktionen zur Inhaltsgestaltung in Adobe Experience Manager und den außerordentlichen Versand- sowie Datenverwaltungsfähigkeiten von Adobe Campaign. Bitte beachten Sie, dass Sie für aus Adobe Experience Manager importierte Inhalte keine A/B-Tests durchführen können.

Adobe Campaign Standard ist mit Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 und 6.5 kompatibel. In den folgenden Abschnitten finden Sie einen Überblick über die Aktionen, die Sie ausführen können. Weiterführende Informationen finden Sie in den Abschnitten [Konfiguration](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de) und [Vorgehensweise](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=de) zur Integration.

>[!NOTE]
>
> Adobe Campaign Standard-Vorlagen sind in Adobe Experience Manager 6.5 nicht mehr verfügbar.

## Tipps zur Verwendung der Integration von Campaign mit Experience Manager {#tips-aem}

* **Verwenden Sie eine für die Integration geeigneten Vorlage.**

  Da E-Mail-Vorlagen in Adobe Experience Manager bearbeitet werden können, wäre es naheliegend, für die Bearbeitung aller Vorlagen Adobe Experience Manager zu verwenden. Bestimmte Vorlagen sind jedoch nicht einfach zu handhaben. Kundenspezifische, individualisierte Vorlagen sind für diese Integration nicht zu empfehlen und sollten direkt in Adobe Campaign Standard bearbeitet werden.

  Weiterführende Informationen zu Vorlagen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=de).

* **Stellen Sie sicher, dass der Externalizer bei der Implementierung konfiguriert wurde.**

  Bei der Implementierung von Experience Manager muss der Externalizer für Adobe Campaign Standard konfiguriert werden, damit ein Ressourcenpfad in eine URL umgewandelt werden kann. Dies ist erforderlich, um Ihre Bilder auf der Seite sichtbar zu machen. Wenn der Externalizer nicht richtig konfiguriert ist, enthalten Ihre E-Mails fehlerhafte Bilder.

  Weiterführende Informationen zur Konfiguration des Externalizers finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/externalizer.html?lang=de).

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
