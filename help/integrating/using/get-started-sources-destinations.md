---
title: Erste Schritte mit Quellen und Zielen
description: Weitere Informationen zu Adobe Experience Platform-Quellen und -Zielen.
audience: integrating
content-type: reference
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: ba6205fa-dbcf-497a-882f-f15c00f12e68
TQID: https://experienceleague.adobe.com/r1rASYXuo-xeKH80eZVYG-jUhxy93GuTa8CIDyouSNY
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616a
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 100%

---

# Erste Schritte mit Quellen und Zielen {#rtcdp}

## Über Quellen und Ziele

Mit Adobe Experience Platform können Sie Daten zwischen Campaign Standard und der Adobe Echtzeit-Kundendatenplattform (RTCDP) austauschen. Auf diese Weise können Sie Adobe Experience Platform-Zielgruppen in Ihren Campaign-Workflows auswählen und dann Daten, die sich auf diese Zielgruppen beziehen, wie Sendungen, Öffnungen und Klicks, an Adobe Real-Time Customer Data Platform zurücksenden.

* Mit **Zielen** können Sie Adobe Experience Platform-Zielgruppen in Campaign Standard aufnehmen. Auf diese Weise können Sie bekannte und unbekannte Daten für Ihre Marketing-Kampagnen aktivieren.
* Mit **Quellen** exportieren Sie Campaign Standard-Daten (z. B. Sendungen, Öffnungen, Klicks) nach Adobe Experience Platform. Auf diese Weise können Sie Daten, die Sie aus unterschiedlichen Quellen erfassen, an einem Ort zusammenfassen und die daraus gewonnenen Erkenntnisse nutzen.


>[!IMPORTANT]
>
>Beachten Sie bei dieser Integration die Einschränkungen für die SFTP-Datenspeicherung, für die Datenbank-Datenspeicherung und für aktive Profile gemäß Ihrem Adobe Campaign-Vertrag.

Eine detaillierte Übersicht über die Adobe Echtzeit-Kundendatenplattform, Ziele und Quellen finden Sie auf diesen Seiten:

* [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de)
* [Dokumentation zu Zielen](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html?lang=de)
* [Dokumentation zu Quellen](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=de)

## Campaign Standard mit Adobe Experience Platform verbinden

Um Daten zwischen Adobe Experience Platform und Campaign Standard austauschen zu können, müssen Sie zunächst Adobe Campaign als **Ziel** und in Adobe Experience Platform Ihren AWS-S3- oder Azure-Blob-Speicherort als **Quelle** verbinden.

Nachdem die Connectoren konfiguriert wurden, können Sie mithilfe von Workflows einen Datenimport oder -export in Campaign Standard einrichten.

![](assets/rtcdp-schema.png)

Weitere Informationen zum Einrichten dieser Import- und Exportprozesse finden Sie in den folgenden Abschnitten:

* [Adobe Experience Platform-Zielgruppen in Campaign aufnehmen](../../integrating/using/ingest-aep-data.md)
* [Daten von Campaign nach Adobe Experience Platform exportieren](../../integrating/using/export-campaign-data.md)
