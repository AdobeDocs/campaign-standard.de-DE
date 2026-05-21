---
title: Campaign – Aktive Profile
description: Erfahren Sie, wie Sie auf Kundenmetriken und aktive Profile zugreifen können.
feature: Profiles
role: User
level: Intermediate
exl-id: 22516348-7695-4579-99eb-480e5b723ccc
TQID: https://experienceleague.adobe.com/XKRIP6jfP3ROPWTN4moJKsBLQcRqmR3gSWZ-hi5P8I4
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 278
ht-degree: 100%

---

# Aktive Profile{#active-profiles}

Sie können auf die Details der aktiven Profile über den Bericht **[!UICONTROL Kundenmetriken]** zugreifen. Dieser Bericht ist nur für funktionale Administratoren und Administratorinnen in Campaign verfügbar. Um auf diesen Bericht zuzugreifen, klicken Sie auf das Adobe Campaign-Symbol oben links in der [Benutzeroberfläche](../../start/using/interface-description.md#advanced-menu) und gehen Sie zu **[!UICONTROL Administration > Kundenmetriken]**.

![](assets/audience_customer_metrics.png)

Dieser Bericht wird monatlich durch den technischen Workflow **[!UICONTROL Abrechnung]** generiert und zeigt die Anzahl der **aktiven Profile** an. Weitere Informationen zu technischen Workflows finden Sie auf [dieser Seite](../../administration/using/technical-workflows.md).

Ein &quot;Profil&quot; ist ein Datensatz mit Informationen, die einen Endkunden, Interessenten oder Lead repräsentieren. Profile werden als **aktiv** angesehen, wenn sie innerhalb der letzten 12 Monate über einen beliebigen Kanal durch einen Campaign-Versand angesprochen wurden.

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Anzahl aktiver Profile. Informationen zur Anzahl der gekauften aktiven Profile finden Sie in Ihrem Lizenzvertrag.

![](assets/audience_active_profiles_list.png)



* Die Profile, die bei der Vorbereitung des Versands (z. B. durch Typologieregeln oder den Quarantänemechanismus) ausgeschlossen wurden, werden nicht berücksichtigt.

* Empfänger von Transaktionsnachrichten werden als aktive Profile gezählt.

* Ein Profil, das mehrere Sendungen erhalten hat, wird nur einmal gezählt.

* Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung.

Unten auf der Seite werden die Zielgruppendimensionen mit der jeweiligen Anzahl der Profile aufgelistet. Empfänger von Transaktionsnachrichten sind mit der Dimension **Anonym** verknüpft.

>[!NOTE]
>
>Als Administrator können Sie die Anzahl der in Ihren Instanzen verwendeten aktiven Profile auch direkt über das Control Panel überwachen. Weitere Informationen hierzu finden Sie in der [Control Panel-Dokumentation](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/active-profiles-monitoring.html?lang=de).
>
