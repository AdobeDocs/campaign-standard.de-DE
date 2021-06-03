---
solution: Campaign Standard
product: campaign
title: Campaign – Aktive Profile
description: Erfahren Sie, wie Sie auf Kundenmetriken und aktive Profile zugreifen können.
feature: Profile
role: Business Practitioner
level: Intermediate
exl-id: 22516348-7695-4579-99eb-480e5b723ccc
source-git-commit: f66a4e35e1f42a3d7630556d020ce76adfea5891
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 84%

---

# Aktive Profile{#active-profiles}

Funktionale Administratoren in Campaign können auf den Bericht **[!UICONTROL Kundenmetriken]** unter **[!UICONTROL Administration > Kundenmetriken]** zugreifen.

![](assets/audience_customer_metrics.png)

Dieser Bericht wird monatlich durch den technischen Workflow **[!UICONTROL Abrechnung]** generiert und zeigt die Anzahl der **aktiven Profile** an.

Ein &quot;Profil&quot; ist ein Datensatz mit Informationen, die einen Endkunden, Interessenten oder Lead repräsentieren. Profile werden als **aktiv** angesehen, wenn sie innerhalb der letzten 12 Monate über einen beliebigen Kanal durch einen Campaign-Versand angesprochen wurden.

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Anzahl aktiver Profile. Informationen zur Anzahl der gekauften aktiven Profile finden Sie in Ihrem Lizenzvertrag.

![](assets/audience_active_profiles_list.png)



* Die Profile, die bei der Vorbereitung des Versands (z. B. durch Typologieregeln oder Quarantänemechanismus) ausgeschlossen wurden, werden nicht berücksichtigt.

* Empfänger von Transaktionsnachrichten werden für aktive Profile gezählt.

* Ein Profil, das mehrere Sendungen erhalten hat, wird nur einmal gezählt.

* Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung.

Unten auf der Seite werden die Zielgruppendimensionen mit der Anzahl der Profile aufgelistet. Empfänger von Transaktionsnachrichten sind mit der Dimension **Anonymous** verknüpft.

>[!NOTE]
>
>Als Administrator können Sie die Anzahl der in Ihren Instanzen verwendeten aktiven Profile auch direkt über das Control Panel überwachen. Weitere Informationen hierzu finden Sie in der [Control Panel-Dokumentation](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/active-profiles-monitoring.html?lang=de).

