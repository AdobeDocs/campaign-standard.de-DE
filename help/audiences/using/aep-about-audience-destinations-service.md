---
title: Informationen zum Dienst Zielgruppenziele
description: Erfahren Sie mehr über den Dienst Zielgruppenziele.
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
source-git-commit: ff3b41589f47e7697a69bb68824aefd4d9036793

---


# Informationen zum Dienst Zielgruppenziele {#about-audiences}

>[!IMPORTANT]
>
>Der Zielgruppen-Zieldienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azurblau gehostet werden (derzeit nur in der Beta-Version für Nordamerika), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Zugriff haben möchten.

Nutzen Sie die [Adobe Experience Platform](https://www.adobe.io/apis/experienceplatform/home.html) (AEP), um zielgerichtete Zielgruppen auf Basis großer, komplexer Datensätze zu erstellen. Die Adobe Experience Platform fasst Profil-, Verhaltens- und Mehrentitäts-Daten aus Online- und Offlinequellen zusammen, einschließlich Adobe Analytics, um Ihnen bei der Erstellung einer 360-Grad-Ansicht Ihres Kunden zu helfen und so eine effektive Verwaltung Ihrer Kundenerlebnisse zu ermöglichen.

Adobe Campaign Standard verwendet dann den Dienst **Zielgruppenziele** , um eine Sammlung von Profilen, **Zielgruppen** genannt, von AEP für mehrstufige und/oder kanalübergreifende Kampagnenprogramme abzurufen.

**Zielgruppen** werden durch erstmaliges Erstellen von **Segmenten** erstellt, bei denen es sich im Wesentlichen um einen Regelsatz handelt, der auf praktisch jeder beliebigen Variablen (z. B. Profil-, Ereignis-, Multi-Entitäts-Daten) innerhalb eines Kundenprofils von AEP basiert, um ein multidimensionales Ziel zu erstellen. Globale Konzepte für Unified Profile &amp; Segmentation Services können in [diesen dedizierten Dokumenten](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation.html)referenziert werden.

Nachdem ein Segment erstellt wurde, können Sie es als Zielgruppe für eine Bereitstellung in den [Campaign Standard-Arbeitsabläufen](../../automating/using/aep-targeting-audiences.md)aktivieren. Darüber hinaus können Sie Kontextdaten aus der Adobe Experience Platform verwenden, um Ihre Kampagnen zu [personalisieren](../../automating/using/aep-personalizing-campaigns.md) und gegebenenfalls dynamische Inhalte hinzuzufügen.

Demovideos sind auch in [diesem Abschnitt](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html)verfügbar.

In diesen Abschnitten verwendete Begriffe:

* **Profil**: Profile ist ein Experience Platform-Standarddatenmodell, das zur Definition von Attributen von Verbrauchern verwendet wird. Ein Profil kann auch eine Aggregation von Ereignisdaten und -attributen für eine Person und ein Gerät sein.

   Beispiel: &quot;John Doe ist ein 55-jähriger Mann.&quot;

* **Segment**: Ein Regelsatz, der eine Untergruppe von Profilen aus Ihrer Datenbank definiert, wobei Attribute und Ereignisdaten verwendet werden.

   Beispiel: &quot;Männer > 50 Jahre alt.&quot;

* **Zielgruppe**: Eine Sammlung von Profilen, die Segmentregeln entsprechen.

   Beispiel: Liste der Profile aller über 50-Jährigen in Ihrer Datenbank.
