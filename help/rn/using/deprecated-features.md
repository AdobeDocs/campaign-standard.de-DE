---
title: Eingestellte und entfernte Funktionen von Campaign Standard
description: Auf dieser Seite finden Sie eingestellte und entfernte Funktionen von Adobe Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: 03797137-c01c-48dc-b25b-8e72741abb04
source-git-commit: 6b683ccd93e10f78ff643eed9f374a794c085cb1
workflow-type: ht
source-wordcount: '882'
ht-degree: 100%

---

# Eingestellte und entfernte Funktionen {#deprecated-and-removed-features}

Adobe wertet laufend die Funktionen seiner Produkte aus, um ältere Funktionen durch neuere Alternativen zu ersetzen. Auf diese Weise kann der Kundennutzen unter sorgfältiger Berücksichtigung der Abwärtskompatibilität verbessert werden.

Bei der Mitteilung einer bevorstehenden Entfernung/Ersetzung von Campaign Standard-Funktionen gelten die folgenden Regeln:

* Zuerst wird die Entfernung der Funktion angekündigt. Auch wenn nicht mehr unterstützte Funktionen für bestehende Benutzer weiterhin verfügbar sind, werden sie weder weiter verbessert noch dokumentiert.
* Die eingestellten Funktionen werden frühestens in der folgenden Version entfernt. Das tatsächliche Zieldatum für die Entfernung wird auf dieser Seite angegeben.

Durch dieses Vorgehen erhält der Kunde mindestens einen Versionszyklus Zeit, um seine Implementierung an eine neue Version oder einen Nachfolger einer eingestellten Funktion anzupassen, bevor sie tatsächlich entfernt wird.

>[!NOTE]
>Die Versionen und neuen Funktionen von Adobe Campaign Standard sind in den [Versionshinweisen](../../rn/using/release-notes.md) aufgeführt.


## Eingestellte Funktionen {#deprecated-features}

In diesem Abschnitt werden Funktionen aufgeführt, die bei den aktuellen Campaign Standard-Versionen als eingestellt gekennzeichnet wurden.

Im Allgemeinen werden Funktionen, die in einer zukünftigen Version entfernt werden sollen, zuerst als eingestellt gekennzeichnet, wobei eine Alternative bereitgestellt wird. Diese Funktionen sind für neue Campaign Standard-Kunden entweder nicht mehr verfügbar oder sollten für keine neue Implementierung verwendet werden. Sie werden auch aus der Produktdokumentation entfernt.

Kunden wird empfohlen, die Nutzung der Funktion in ihrer aktuellen Bereitstellung zu prüfen und Pläne zur Änderung ihrer Implementierung zu erstellen, um die verfügbare Alternative zu nutzen. Achten Sie auf die geplante Version für die Entfernung, um Ihre Umgebungs- und Projektaktualisierungen zu planen.



<table> 
 <thead> 
  <tr> 
   <th> <strong>SDK V4 für Mobile Apps</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Die Unterstützung für die SDKs der Adobe Experience Platform Mobile-Version 4 wurde am 31. August 2021 eingestellt. Wenn Sie immer noch diese ältere Version des SDK in Adobe Campaign Standard verwenden, müssen Sie Ihre Implementierung mit Adobe Experience Platform SDK <strong>vor Ende Juni 2024</strong> aktualisieren. </p></br>
   <p>Lesen Sie <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-mobile/sdkv4-migration.html?lang=de">diesen Artikel</a>, um zu erfahren, wie Sie Ihre Implementierung anpassen und auf das neueste Experience Platform SDK umsteigen können.</p></br>
   <p><strong>Achtung</strong>: Das SDK V4 wird in Campaign Standard ab Ende Juni 2024 nicht mehr unterstützt.</p>
  </td> 
  </tr> 
 </tbody> 
</table>




<table> 
 <thead> 
  <tr> 
   <th> <strong>E-Mail-Design – Veralteter E-Mail-Editor</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Ab Version 19.0 von Campaign wird der alte E-Mail-Editor nicht mehr unterstützt. Verwenden Sie den <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html?lang=de">E-Mail-Designer von Campaign</a>, um Ihre E-Mail-Inhalte zu erstellen und zu personalisieren. </p></br>
   <p>In <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/building-email-content/using-existing-content.html?lang=de">diesem Abschnitt</a> erfahren Sie, wie Sie Ihre E-Mail-Vorlagen für den neuen Editor anpassen.</p></br>
  </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Benutzer &amp; Sicherheit – Geografische Einheiten</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Ab Campaign-Version 18.7 werden geografische Einheiten nicht mehr unterstützt. Organisationseinheiten und geografische Einheiten sind in Campaign identische Konzepte. Benutzer sollten ausschließlich Organisationseinheiten verwenden, um eine Hierarchie für Benutzerberechtigungen/den Datenzugriff zu erstellen. <a href="https://helpx.adobe.com/de/campaign/standard/administration/using/organizational-units.html">Mehr dazu</a>. Bitte beachten Sie, dass die Funktion ab Version 18.7 nicht mehr für neue Campaign Standard-Instanzen oder für vorhandene Instanzen ohne geografische Einheiten implementiert werden kann.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## Entfernte Funktionen {#removed-features}

In diesem Abschnitt werden Funktionen und Leistungsmerkmale aufgelistet, die aus Campaign Standard entfernt wurden.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Integration mit Audience Destinations Service</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Ab Version 21.3 von Campaign Standard wird die Integration mit Audience Destinations Service nicht mehr unterstützt.  Sie wurde jetzt entfernt.</p>
   <p>Bei neuen Implementierungen können Sie Audience Destinations Service nicht mehr in Adobe Campaign Standard integrieren. Sie können Campaign und Adobe Experience Platform jedoch über Quellen und Ziele integrieren. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/aep-sources-destinations/get-started-sources-destinations.html?lang=de">Weitere Informationen</a>.</p>
     </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Integration mit Adobe Experience Platform Data Connector</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Ab Campaign Standard-Version 21.3 wird die Integration mit Adobe Experience Platform Data Connector nicht mehr unterstützt.  Sie wurde jetzt entfernt.</p>
   <p>Bei einer neuen Implementierung können Sie den Adobe Experience Platform Data Connector nicht mehr in Adobe Campaign Standard integrieren. Sie können Campaign und Adobe Experience Platform jedoch über Quellen und Ziele integrieren. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/aep-sources-destinations/get-started-sources-destinations.html?lang=de">Weitere Informationen</a>.</p>
     </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Push-Benachrichtigungen mit SDK v4</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Ab Campaign-Version 20.1 wird SDK v4 nicht mehr unterstützt. Es wurde jetzt entfernt. <a href="https://experienceleague.adobe.com/docs/discontinued/using/mobile-services.html?lang=de">Weitere Informationen</a>.</p><br/>
   <p>Das <a href="https://developer.adobe.com/client-sdks/documentation/">Adobe Experience Platform Mobile-SDK</a> (früher als v5 bezeichnet) unterstützt ausschließlich künftige Adobe Experience Cloud-Funktionen.</p>
   <p>Nach dem 31. August 2021 können Kunden die SDKs der Version 4 weiterhin herunterladen und verwenden. Es wird jedoch kein Support durch die Kundenunterstützung und kein Zugriff auf Foren mehr bereitgestellt.</p>
   <p><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-mobile/sdkv4-migration.html?lang=de">Auf dieser Seite</a> erfahren Sie, wie Sie vom SDK v4 zum Adobe Experience Platform Mobile SDK migrieren.</p></br>
     </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Datenschutzanfragen – Campaign-API und -Benutzeroberfläche</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Mit Campaign-Version 21.2. wurde die Campaign-API und -Benutzeroberfläche für Zugriffs- und Löschanfragen eingestellt. Das zweistufige Löschen von Profilen ist nicht mehr verfügbar. Verwenden Sie <a href="https://developer.adobe.com/experience-platform-apis/references/privacy-service">Privacy Core Service von Adobe</a>.</p></br>
   <p>Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=de">Verwalten von Datenschutzanfragen</a>.</p>
  </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
 <tr> 
   <th> <strong>Prädiktive Betreffzeile</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Ab April 2021 wird die Funktion der prädiktiven Betreffzeile eingestellt.</p><br/>
   <p>Wir empfehlen Ihnen, die KI-gestützten E-Mail-Funktionen zu nutzen, um Öffnungsraten, optimale Sendezeiten und voraussichtliche Abwanderungszahlen anhand historischer Interaktionsmetriken zu analysieren und vorherzusagen. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/preparing-and-testing-messages/predictive.html?lang=de">Mehr dazu</a></p></br>
     </td> 
  </tr> 
  </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Neigungsbewertung mit Experience Cloud Triggers</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Die <b>Neigungsbewertung </b> wurde in Adobe Experience Cloud Triggers eingestellt. Infolgedessen wurde diese Option aus Adobe Campaign Standard entfernt. Um veraltete Werte der Neigungsbewertung in den Anreicherungsschemas zu vermeiden, empfehlen wir, die Schemas zu aktualisieren, um die neuesten Änderungen abzurufen und vorhandene Triggers erneut zu veröffentlichen. Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html?lang=de">Trigger in Campaign veröffentlichen</a>.
</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Creative SDK für Campaign Standard</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>[!DNL Adobe Creative SDK] wurde eingestellt. Infolgedessen ist die Bildbearbeitung mit [!DNL Creative SDK] in Campaign Standard-E-Mails ab der Version Campaign 20.2 nicht mehr verfügbar.</p></br>
   </td> 
  </tr> 
 </tbody> 
</table>

## Ende der Kompatibilität {#end-of-compatibility}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Microsoft Internet Explorer 11</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Campaign und Adobe Experience Cloud haben mit Campaign-Version 19.2 (Frühling 2019) den Support für Microsoft Internet Explorer 11 eingestellt. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/about-configuration-guidelines.html?lang=de">Mehr dazu</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>
