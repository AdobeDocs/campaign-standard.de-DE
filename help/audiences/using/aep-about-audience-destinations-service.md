---
title: Über den Audience Destinations-Dienst
description: Erfahren Sie mehr über den Audience Destinations-Dienst.
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
translation-type: ht
source-git-commit: e1fa546313e8d543685ef30a072ae2d97c5bf236

---


# Über den Audience Destinations-Dienst {#about-audiences}

>[!IMPORTANT]
>
>Der Audience Destinations-Dienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Nutzen Sie [Adobe Experience Platform](https://docs.adobe.com/content/help/de-DE/experience-platform/landing/home.html), um die Erlebnisse Ihrer Kunden zu optimieren, indem Sie auf der Grundlage großer, komplexer Datensätze zielgenaue Audiences erstellen. Adobe Experience Platform fasst Profildaten, Verhaltensdaten und Daten mehrerer Entitäten über Online- und Offline-Quellen hinweg zusammen, einschließlich Adobe Analytics. So erhalten Sie eine 360-Grad-Ansicht Ihres Kunden und können Kundenerlebnisse effektiv verwalten.

Adobe Campaign Standard verwendet dann den Dienst **Audience Destinations**, um von Adobe Experience Platform für mehrstufige und/oder kanalübergreifende Kampagnenprogramme eine Kollektion von Profilen abzurufen, die als **Audiences** bezeichnet werden.

**Audiences** werden durch anfängliches Einrichten von **Segmenten** erstellt, bei denen es sich im Prinzip um einen Regelsatz handelt, der auf praktisch jeder Variablen (z. B. Profil-, Ereignis-, Multi-Entitäts-Daten) innerhalb eines Kundenprofils von Adobe Experience Platform basieren kann, um eine multidimensionale Zielgruppe zu erstellen. Allgemeine Konzepte für Unified Profile- und Segmentierungsdienste werden in diesen Dokumenten erläutert:

* [Echtzeit-Kundenprofil – Überblick ](https://docs.adobe.com/content/help/de-DE/experience-platform/profile/home.html)
* [Übersicht über den Segmentierungsdienst](https://docs.adobe.com/content/help/de-DE/experience-platform/segmentation/home.html)

Nach dem Erstellen eines Segments können Sie es als Audience für einen Versand in [Campaign Standard-Workflows](../../automating/using/aep-targeting-audiences.md) aktivieren. Darüber hinaus können Sie Kontextdaten aus Adobe Experience Platform verwenden, um Nachrichten zu [personalisieren](../../automating/using/aep-personalizing-campaigns.md) und dynamische Inhalte zu Ihren Kampagnen hinzuzufügen.

Anleitungsvideos sind auch auf [dieser Seite](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html) verfügbar.

In diesen Abschnitten verwendete Begriffe:

* **Profil**: Profil ist ein Experience Platform-Standarddatenmodell, mit dem Verbraucherattribute definiert werden. Ein Profil kann auch ein Aggregat von Ereignisdaten und -attributen sein, das sich auf eine Person oder ein Gerät bezieht.

   Beispiel: &quot;Max Mustermann ist ein 55-jähriger Mann.&quot;

* **Segment**: Ein Satz von Regeln, der eine Untergruppe von Profilen aus Ihrer Datenbank definiert, wobei Attribute und Ereignisdaten verwendet werden.

   Beispiel: &quot;Männer > 50 Jahre alt.&quot;

* **Audience**: Eine Kollektion von Profilen, die Segmentregeln entsprechen.

   Beispiel: Liste von Profilen, die allen Männern über 50 Jahren in Ihrer Datenbank entspricht.
