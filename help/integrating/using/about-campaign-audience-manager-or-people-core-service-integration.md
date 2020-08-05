---
title: Über die Integration von Campaign mit Audience Manager oder People Core Service
description: Durch die Integration von Audience Manager/People Core Service können Sie in den unterschiedlichen Adobe Experience Cloud-Lösungen Audiences oder Segmente freigeben.
page-status-flag: never-activated
uuid: 39e3c78e-cccd-4823-afe9-abc7f8aef034
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: bf718329-f181-46f7-80a2-b525a8dee46d
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1e790f550f6eb84954f199caeda88a8fd90dfd85
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 52%

---


# Über die Integration von Campaign mit Audience Manager oder People Core Service{#about-campaign-audience-manager-or-people-core-service-integration}

>[!CAUTION]
>
>Je nach den ausgetauschten Daten kann die Einfuhr von Audiencen in Adobe Campaign rechtlichen Beschränkungen unterliegen.

Adobe Campaign erlaubt die lösungsübergreifende Nutzung von Audiences/Segmenten in Adobe Experience Cloud. Konkret bietet die Integration von **Adobe Campaign** und **People Core Service** (auch **Profiles &amp; Audiences Core Service** genannt) oder Adobe Audience Manager folgende Möglichkeiten:

* Import von Zielgruppen/Segmenten aus den verschiedenen Adobe Experience Cloud-Lösungen in Adobe Campaign. Der Import von Zielgruppen erfolgt in Adobe Campaign ausgehend vom Menü **[!UICONTROL Audiences]**.
* Export von Audiences als freigegebene Zielgruppen/Segmente. Diese Zielgruppen können dann in den anderen von Ihnen verwendeten Adobe Experience Cloud-Lösungen genutzt werden. Der Export von Audiences erfolgt innerhalb eines Workflows mithilfe der Aktivität **[!UICONTROL Audience-Speicherung]**, welche sich an eine Zielgruppenbestimmung anschließt.

Die Integration unterstützt zwei Typen von Adobe Experience Cloud-Kennungen:

* **Visitor ID**: Dieser Kennungstyp ermöglicht die Abstimmung von Adobe Experience Cloud-Besuchern mit Profilen aus Adobe Campaign. Sobald eine Verbindung über die Adobe IMS aktiviert ist, wird der Marketing Cloud Besucher-ID-Dienst aktiviert, der das von Adobe Campaign verwendete permanente Cookie ersetzt. Auf diese Weise können Sie einen Besucher identifizieren und ihn dann mit einem Profil verknüpfen.
   <br>Eine Besucher-ID wird mit einem Profil verknüpft, sobald das Profil in einer per Adobe Campaign gesendeten E-Mail klickt:
   * Wenn das Profil bereits über eine Besucher-ID verfügt, können die Browserdaten des Profils das Profil wiederherstellen und automatisch mit der Besucher-ID verknüpfen.
   * Wenn keine Besucher-ID gefunden wird, wird eine neue ID erstellt. Diese Besucher-ID wird in den Profil-Trackinglogs gespeichert.

   Unter der Voraussetzung, dass sie denselben CNAME aufweisen, erkennen die anderen Lösungen der Adobe Marketing Cloud diese Kennung.

* **Deklarierte ID**: Mit dieser ID können Sie alle Datentypen mit Elementen aus der Adobe Campaign-Datenbank abgleichen. Es wird in Adobe Campaign als vordefinierter Abstimmschlüssel dargestellt. Beim Datenaustausch werden die Adobe Campaign-Datenbankkennungen mit Hashing versehen. Diese Hash-IDs werden dann mit den Hash-IDs der Adobe Marketing Cloud-Audience verglichen, die am Import oder Export beteiligt sind.
   <br>Diese Integration unterstützt reguläre Declared IDs, Declared IDs mit Hash-Kennung und verschlüsselte Declared IDs.

   >[!CAUTION]
   >
   >Deklarierte ID funktioniert nur mit Adobe Audience Manager. Deklarierte ID funktioniert ohne sie nicht.

   Durch die Sicherheitsfunktion können verschlüsselte Daten in Datenquellen (z. B. PII) unter Verwendung der Declared ID und der Spezifikation des Verschlüsselungsalgorithmus freigegeben werden.

   Beispielsweise können Sie durch die Möglichkeit, verschlüsselte E-Mail-Adressen oder SMS-Nummern zu entschlüsseln, auch automatisch ausgelöste Nachrichten an Ihre Benutzer senden, selbst wenn deren Profil nicht in der Adobe-Campaign-Datenbank vorhanden ist.

Im folgenden Diagramm wird beschrieben, wie diese Integration funktioniert. Hier steht AAM für Adobe Audience Manager und ACS für Adobe Campaign Standard.

![](assets/aam_diagram.png)