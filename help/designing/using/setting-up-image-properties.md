---
title: Bildeigenschaften konfigurieren
seo-title: Bildeigenschaften konfigurieren
description: Bildeigenschaften konfigurieren
seo-description: Hier erfahren Sie, wie Sie die Eigenschaften der Bilder in Ihrem Inhalt verwalten.
page-status-flag: never-activated
uuid: 1a439105-d9aa-4b30-a00d-bcf731a04e08
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: using-images
discoiquuid: 80c9c1a5-6050-443d-810a-6bb755d39dca
internal: n
snippet: y
translation-type: ht
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Bildeigenschaften konfigurieren{#setting-up-image-properties}

Bei Markierung eines Bild-Blocks können in der Palette folgende Eigenschaften konfiguriert werden:

* **Personalisierung aktivieren** ermöglicht die Anpassung der Bildquelle. Siehe [Bildquellen personalisieren](../../designing/using/personalizing-an-image-source.md)
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

