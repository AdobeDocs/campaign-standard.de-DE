---
title: Bilder verwenden
description: Erfahren Sie, wie Sie Bilder in E-Mails mit Email Designer verwalten.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: ht
source-git-commit: 7e300de836a74372e411b5b1d584851fac77aafe

---


# Bilder verwenden {#images}

## Bilder einfügen{#inserting-images}

Sie können Bilder in E-Mail-Nachrichten und Landingpages einfügen.

Je nach Konfiguration sind die folgenden Arten von Bildern verfügbar:

* Lokale Bilder
* Freigegebene Bilder aus Adobe Experience Cloud – siehe [Campaign und Assets Core Service verwenden](../../integrating/using/working-with-campaign-and-assets-core-service.md)/Assets On Demand
* Dynamische Bilder von Adobe Target – siehe [Campaign und Target verwenden](../../integrating/using/about-campaign-target-integration.md)

Sie können Bilder mit Adobe Creative SDK ändern, vorausgesetzt dieses ist aktiviert. Siehe [Bilder mit Adobe Creative SDK bearbeiten](#modifying-images-with-the-adobe-creative-sdk).

>[!CAUTION]
>
>Wenn Sie ein Bild direkt durch Bearbeiten der HTML-Version der E-Mail hinzufügen möchten, dürfen Sie keine **externen Dateien in einem &lt;script>-Tag** der HTML-Seite aufrufen. Der Adobe-Campaign-Server erlaubt keinen Import derartiger Dateien.

### Bilder in eine E-Mail einfügen  {#inserting-images-in-an-email}

1. Fügen Sie eine Strukturkomponente hinzu. Weiterführende Informationen dazu finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Fügen Sie innerhalb dieser Strukturkomponente eine Inhaltskomponente des Typs **[!UICONTROL Bild]**hinzu.

   ![](assets/des_insert_images_1.png)

1. Klicken Sie auf **[!UICONTROL Durchsuchen]**. Ziehen Sie ein Bild in den Arbeitsbereich oder wählen Sie eine Datei von Ihrer Festplatte aus.

   ![](assets/des_insert_images_2.png)

1. Wählen Sie die soeben hinzugefügte Inhaltskomponente aus.
1. Überprüfen Sie die Bildeigenschaften und passen Sie sie bei Bedarf an.

   ![](assets/des_insert_images_3.png)

## Bildeigenschaften konfigurieren{#setting-up-image-properties}

Bei Markierung eines Bild-Blocks können in der Palette folgende Eigenschaften konfiguriert werden:

* **Personalisierung aktivieren** ermöglicht die Anpassung der Bildquelle. Siehe [Bildquellen personalisieren](../../designing/using/personalization.md#personalizing-an-image-source)
* Mit der Option **Bildtitel** können Sie einen Titel für das Bild festlegen.
* **Alternativtext** (E-Mail) oder **Legende** (Landingpage) fügt dem Bild einen Text hinzu, der z. B. dann angezeigt wird, wenn das Bild nicht geladen werden kann (entspricht dem **alt**-Tag im HTML-Code).
* Bei der Bearbeitung einer E-Mail ermöglicht **Stil** die Spezifikation der Größe, des Hintergrunds und der Rahmen des Bildes.
* Bei der Bearbeitung einer Landingpage ermöglicht **Dimensionen** die Spezifikation der Bildgröße und der Pixel.

Der Editor unterstützt **alle Bildarten**, deren Format mit den gängigen Browsern kompatibel ist. Um kompatibel zu sein, sind **Flash-Animationen** wie folgt in HTML-Seiten einzufügen:

```
<object type="application/x-shockwave-flash" data="http://www.mydomain.com/flash/your_animation.swf" width="200" height="400">
 <param name="movie" value="http://www.mydomain.com/flash/your_animation.swf" />
 <param name="quality" value="high" />
 <param name="play" value="true"/>
 <param name="loop" value="true"/> 
</object>
```

## Bilder mit Adobe Creative SDK bearbeiten{#modifying-images-with-the-adobe-creative-sdk}

Die weitreichenden Funktionen des Adobe Creative SDK erlauben Ihnen, Bilder direkt im Inhaltseditor während der Bearbeitung von E-Mails oder Landingpages zu bearbeiten.

Mit den leistungsfähigen, umfassenden Bildbearbeitungsfunktionen des Bildeditors können Sie u. a. Bilder bearbeiten, Effekte, Rahmen, originelle Sticker und attraktive Überblendungen hinzufügen sowie unterhaltsame Funktionen wie Tilt/Shift und Color Splash und die Profibildanpassung verwenden.

Um Bilder mit Adobe Creative SDK zu bearbeiten, gehen Sie folgendermaßen vor:

1. Wählen Sie ein Bild aus.
1. Klicken Sie in der Symbolleiste auf das Symbol für Creative Cloud.

   ![](assets/des_creative_sdk_icon.png)

1. Wählen Sie das gewünschte Tool über die Symbole am oberen Fensterrand aus, um das Bild zu bearbeiten.

   ![](assets/email_designer_ccsdktoolbar.png)

1. Klicken Sie nach Abschluss der Änderungen auf **[!UICONTROL Speichern]**. Das aktualisierte Bild wird auf dem Adobe-Campaign-Server gespeichert und kann nun verwendet werden.

>[!NOTE]
Die im Bildeditor verfügbaren Tools können nicht angepasst werden.
