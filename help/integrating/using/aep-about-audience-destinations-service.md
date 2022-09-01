---
title: Über den Audience Destinations-Dienst
description: Erfahren Sie mehr über den Audience Destinations-Dienst.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 34235749-d056-4d4c-9939-7dc52f980a76
hide: true
hidefromtoc: true
source-git-commit: 26394f3f6fd9b67996c30924c376533380e8f4d6
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Über den Audience Destinations-Service {#about-audiences}

>[!IMPORTANT]
>
>Der Audience Destinations-Dienst befindet sich derzeit in der Betaversion, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaversion), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Nutzen Sie [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de), um die Erlebnisse Ihrer Kunden zu optimieren, indem Sie auf der Grundlage großer, komplexer Datensätze zielgenaue Audiences erstellen. Adobe Experience Platform fasst Profildaten, Verhaltensdaten und Daten mehrerer Entitäten über Online- und Offline-Quellen hinweg zusammen, einschließlich Adobe Analytics. So erhalten Sie eine 360-Grad-Ansicht Ihres Kunden und können Kundenerlebnisse effektiv verwalten.

Adobe Campaign Standard verwendet dann den Dienst **Audience Destinations**, um von Adobe Experience Platform für mehrstufige und/oder kanalübergreifende Kampagnenprogramme eine Sammlung von Profilen abzurufen, die als **Audiences** bezeichnet werden.

**Audiences** werden durch anfängliches Einrichten von **Segmenten** erstellt, bei denen es sich im Prinzip um einen Regelsatz handelt, der auf praktisch jeder Variablen (z. B. Profil-, Ereignis-, Multi-Entitäts-Daten) innerhalb eines Kundenprofils von Adobe Experience Platform basieren kann, um eine multidimensionale Zielgruppe zu erstellen. Allgemeine Konzepte zu Diensten für Echtzeit-Kundenprofile und Segmentierung werden in diesen Dokumenten erläutert:

* [Echtzeit-Kundenprofil – Überblick ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de)
* [Übersicht über den Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de)

Nach dem Erstellen eines Segments können Sie es als Audience für einen Versand in [Campaign Standard-Workflows](../../integrating/using/aep-targeting-audiences.md) aktivieren. Darüber hinaus können Sie Kontextdaten aus Adobe Experience Platform verwenden, um Nachrichten zu [personalisieren](../../integrating/using/aep-personalizing-campaigns.md) und dynamische Inhalte zu Ihren Kampagnen hinzuzufügen.

![](assets/do-not-localize/how-to-video.png) Anleitungsvideos sind auch auf [dieser Seite](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html?lang=de) verfügbar.

In diesen Abschnitten verwendete Begriffe:

* **Profil**: Profil ist ein Experience Platform-Standarddatenmodell, mit dem Verbraucherattribute definiert werden. Ein Profil kann auch ein Aggregat von Ereignisdaten und -attributen sein, das sich auf eine Person oder ein Gerät bezieht.

   Beispiel: &quot;Max Mustermann ist ein 55-jähriger Mann.&quot;

* **Segment**: Ein Satz von Regeln, der eine Untergruppe von Profilen aus Ihrer Datenbank definiert, wobei Attribute und Ereignisdaten verwendet werden.

   Beispiel: &quot;Männer > 50 Jahre alt.&quot;

* **Audience**: Eine Sammlung von Profilen, die Segmentregeln entsprechen.

   Beispiel: Liste von Profilen, die allen Männern über 50 Jahren in Ihrer Datenbank entspricht.
