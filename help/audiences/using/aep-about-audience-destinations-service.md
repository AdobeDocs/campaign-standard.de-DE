---
title: Über den Audience Destinations-Dienst
description: Erfahren Sie mehr über den Audience Destination-Dienst.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e1fa546313e8d543685ef30a072ae2d97c5bf236

---


# Über den Audience Destinations-Dienst {#about-audiences}

>[!IMPORTANT]
>
>Der Audience Destinations-Dienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Nutzen Sie die [Adobe Experience Platform](https://docs.adobe.com/content/help/en/experience-platform/landing/home.html) , um zielgerichtete Audiencen auf der Grundlage großer, komplexer Datensätze zu erstellen. Die Adobe Experience Platform fasst Daten zu Profil, Verhalten und mehreren Entitäten aus Online- und Offline-Quellen zusammen, einschließlich Adobe Analytics, um Ihnen bei der Erstellung einer 360-Grad-Ansicht Ihres Kunden zu helfen und so eine effektive Verwaltung Ihrer Kundenerlebnisse zu ermöglichen.

Adobe Campaign Standard verwendet dann den Dienst **Audience Destination** , um eine Sammlung von Profilen, die als **Audiencen** bezeichnet werden, von der Adobe Experience Platform für mehrstufige und/oder Kanal-Kampagnen-Programm abzurufen.

**Audiencen** werden durch erstmalige Erstellung von **Segmenten** erstellt, bei denen es sich im Wesentlichen um einen Regelsatz handelt, der auf praktisch jeder Variablen (z. B. Profil-, Ereignis-, Multi-Entitäts-Daten) innerhalb eines Kundenprofils von Adobe Experience Platform basiert, um eine multidimensionale Zielgruppe zu erstellen. Globale Konzepte für Unified Profil &amp; Segmentation Services werden in diesen dedizierten Dokumenten referenziert:

* [Überblick über das Echtzeit-Profil von Kunden](https://docs.adobe.com/content/help/en/experience-platform/profile/home.html)
* [Übersicht über den Segmentdienst](https://docs.adobe.com/content/help/en/experience-platform/segmentation/home.html)

Nachdem ein Segment erstellt wurde, können Sie es als Audience für einen Versand in [Campaign Standard Workflows](../../automating/using/aep-targeting-audiences.md)aktivieren. Darüber hinaus können Sie Kontextdaten aus der Adobe Experience Platform verwenden, um dynamische Inhalte zu Ihren Kampagnen zu [personalisieren](../../automating/using/aep-personalizing-campaigns.md) und hinzuzufügen.

How-to videos are also available in [this section](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html).

In diesen Abschnitten verwendete Begriffe:

* **Profil**: Profil ist ein Experience Platform-Standarddatenmodell, mit dem Verbraucherattribute definiert werden. Ein Profil kann auch ein Aggregat von Ereignis-Daten und -Attributen sein, die sich auf eine Person oder ein Gerät beziehen.

   Beispiel: &quot;John Doe ist ein 55-jähriger Mann.&quot;

* **Segment**: Ein Regelsatz, der eine Untergruppe von Profilen aus Ihrer Datenbank definiert, wobei Attribute und Ereignis-Daten verwendet werden.

   Beispiel: &quot;Männer > 50 Jahre alt.&quot;

* **Audience**: Eine Sammlung von Profilen, die Segmentregeln entsprechen.

   Beispiel: Liste von Profilen, die allen Männern über 50 Jahren in Ihrer Datenbank entsprechen.
