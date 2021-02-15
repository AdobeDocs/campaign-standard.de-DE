---
solution: Campaign Standard
product: campaign
title: Eingestellte und entfernte Funktionen von Campaign Standard
description: Auf dieser Seite finden Sie eingestellte und entfernte Funktionen von Adobe Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-deprecated-features
translation-type: tm+mt
source-git-commit: becaf20fefb6fce05db0824baa69670f810966dc
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 100%

---


# Eingestellte und entfernte Funktionen {#deprecated-and-removed-features}

Adobe evaluiert laufend die Funktionen seiner Produkte, um ältere Funktionen durch neuere Alternativen zu ersetzen. Auf diese Weise kann der Kundennutzen unter sorgfältiger Berücksichtigung der Abwärtskompatibilität verbessert werden.

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
   <th> <strong>Prädiktive Betreffzeile</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Ab dem 15. Dezember 2020 wird die Funktionalität der prädiktiven Betreffzeile nicht mehr unterstützt.</p><br/>
   <p>Wir empfehlen Ihnen, die KI-gestützten E-Mail-Funktionen zu nutzen, um Öffnungsraten, optimale Sendezeiten und voraussichtliche Abwanderungszahlen anhand historischer Interaktionsmetriken zu analysieren und vorherzusagen. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/preparing-and-testing-messages/predictive.html?lang=de">Mehr dazu</a></p></br>
     <p>
     <em>Geplantes Datum für die Entfernung: April 2021.</em></p>
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
   <td> <p> Ab Campaign-Version 20.1 wird SDK v4 nicht mehr unterstützt. <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">Mehr dazu</a>.</p><br/>
   <p>Das <a href="https://aep-sdks.gitbook.io/docs/">Adobe Experience Platform Mobile SDK</a> (früher als v5 bezeichnet) unterstützt ausschließlich kommende Adobe Experience Cloud-Funktionen.</p>
   <p><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-mobile/sdkv4-migration.html?lang=de">Auf dieser Seite</a> erfahren Sie, wie Sie vom SDK v4 zum Adobe Experience Platform Mobile SDK migrieren.</p></br>
     <p>
     <em>Target-Entfernungsdatum: 31. August 2021</em></p>
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
   <td> <p>Mit Campaign-Version 19.4. wurde die Campaign-API und -Benutzeroberfläche für Zugriffs- und Löschanfragen eingestellt. Der zweistufige Löschvorgang für Profile ist nicht verfügbar. Verwenden Sie <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Privacy Coreservice von Adobe</a>.</p></br>
   <p>Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=de-DE">Verwalten von Datenschutzanfragen</a>.</p>
  <p> 
  <em>Geplantes Datum für die Entfernung: April 2021.</em></p>
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
   <td> <p>Ab Version 19.0 von Campaign wird der alte E-Mail-Editor nicht mehr unterstützt. Verwenden Sie den <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html?lang=de-DE">E-Mail-Designer von Campaign</a>, um Ihre E-Mail-Inhalte zu erstellen und zu personalisieren. </p></br>
   <p>In <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/building-email-content/using-existing-content.html?lang=de-DE">diesem Abschnitt</a> erfahren Sie, wie Sie Ihre E-Mail-Vorlagen für den neuen Editor anpassen.</p></br>
  <p> 
  <em>Target-Entfernungsdatum: Ende 2021</em></p>
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
   <th> <strong>Neigungsbewertung mit Experience Cloud Triggers</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Die <b>Neigungsbewertung </b> wurde in Adobe Experience Cloud Triggers eingestellt. Infolgedessen wurde diese Option aus Adobe Campaign Standard entfernt. Um veraltete Werte der Neigungsbewertung in den Anreicherungsschemas zu vermeiden, empfehlen wir, die Schemas zu aktualisieren, um die neuesten Änderungen abzurufen und vorhandene Triggers erneut zu veröffentlichen. Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html?lang=de-DE">Trigger in Campaign veröffentlichen</a>.
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
   <td> <p>[!DNL Adobe Creative SDK] wurde eingestellt. Infolgedessen ist die von [!DNL Creative SDK] unterstützte Bildbearbeitung in Campaign Standard-E-Mails ab Campaign 20.2 nicht mehr verfügbar.</p></br>
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
   <td> <p>Adobe Campaign und Adobe Experience Cloud haben mit Campaign-Version 19.2 (Frühling 2019) den Support für Microsoft Internet Explorer 11 eingestellt. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser. <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/about-configuration-guidelines.html?lang=de-DE">Mehr dazu</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>
