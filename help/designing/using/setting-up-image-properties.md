---
title: Bildeigenschaften konfigurieren
seo-title: Bildeigenschaften konfigurieren
description: Bildeigenschaften konfigurieren
seo-description: Hier erfahren Sie, wie Sie die Eigenschaften der Bilder in Ihrem Inhalt verwalten.
page-status-flag: nie aktiviert
uuid: 1 a 439105-d 9 aa -4 b 30-a 00 d-bcf 731 a 04 e 08
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: entwerfen
content-type: Referenz
topic-tags: using-images
discoiquuid: 80 c 9 c 1 a 5-6050-443 d -810 a -6 bb 555 d 39 dca
internal: n
snippet: y
translation-type: tm+mt
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

