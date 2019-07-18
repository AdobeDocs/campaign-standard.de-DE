---
title: Bilder einfügen
seo-title: Bilder einfügen
description: Bilder einfügen
seo-description: Hier erfahren Sie, wie Sie Bilder zu Ihrem Inhalt hinzufügen.
page-status-flag: nie aktiviert
uuid: ac 42 b 1 d 3-50 ad -4323-b 474-1 e 50 e 468901 f
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: entwerfen
content-type: Referenz
topic-tags: using-images
discoiquuid: ede 832 ac -96 e 5-41 e 1-8390-6669 ba 30 d 4 d 8
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Bilder einfügen{#inserting-images}

Sie können Bilder in E-Mail-Nachrichten und Landingpages einfügen.

Je nach Konfiguration sind die folgenden Arten von Bildern verfügbar:

* Lokale Bilder
* Freigegebene Bilder aus Adobe Experience Cloud – siehe [Campaign und Assets Core Service verwenden](../../integrating/using/working-with-campaign-and-assets-core-service.md)/Assets On Demand
* Dynamische Bilder von Adobe Target – siehe [Campaign und Target verwenden](../../integrating/using/about-campaign-target-integration.md)

Sie können Bilder mit Adobe Creative SDK ändern, vorausgesetzt dieses ist aktiviert. Siehe [Bilder mit Adobe Creative SDK bearbeiten](../../designing/using/modifying-images-with-the-adobe-creative-sdk.md).

>[!CAUTION]
>
>Wenn Sie ein Bild direkt durch Bearbeiten der HTML-Version der E-Mail hinzufügen möchten, dürfen Sie keine **externen Dateien in einem &lt;script&gt;-Tag** der HTML-Seite aufrufen. Der Adobe-Campaign-Server erlaubt keinen Import derartiger Dateien.

## Bilder in eine E-Mail einfügen {#inserting-images-in-an-email}

1. Fügen Sie eine Strukturkomponente hinzu. Weiterführende Informationen dazu finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).
1. Fügen Sie innerhalb dieser Strukturkomponente eine Inhaltskomponente des Typs **[!UICONTROL Bild]hinzu.**

   ![](assets/des_insert_images_1.png)

1. Klicken Sie auf **[!UICONTROL Durchsuchen]**. Ziehen Sie ein Bild in den Arbeitsbereich oder wählen Sie eine Datei von Ihrer Festplatte aus.

   ![](assets/des_insert_images_2.png)

1. Wählen Sie die soeben hinzugefügte Inhaltskomponente aus.
1. Überprüfen Sie die Bildeigenschaften und passen Sie sie bei Bedarf an.

   ![](assets/des_insert_images_3.png)

## Bilder in eine Landingpage einfügen {#inserting-images-in-a-landing-page}

1. Wählen Sie im Inhalt der Landingpage einen Baustein aus, der ein Bild enthält.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Einfügen].**

   ![](assets/des_insert_images_lp_1.png)

1. Wählen Sie in der dedizierten Symbolleiste die Option **[!UICONTROL Lokales Bild].**

   ![](assets/des_insert_images_lp_2.png)

1. Datei auswählen.

   ![](assets/des_insert_images_lp_3.png)

1. Passen Sie die Bildeigenschaften nach Bedarf an.

   ![](assets/des_insert_images_lp_4.png)

