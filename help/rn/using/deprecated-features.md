---
title: Funktionen von Campaign Standard veraltet und entfernt
description: Diese Seite listet nicht mehr unterstützte und entfernte Funktionen von Adobe Campaign Standard auf.
page-status-flag: never-activated
uuid: null
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-deprecated-features
discoiquuid: null
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 490908e5fe0810c0a07c73fef5040ddb42983019

---


# Eingestellte und entfernte Funktionen {#deprecated-and-removed-features}

Adobe bewertet die Produktfunktionen ständig, um ältere Funktionen zu identifizieren, die durch modernere Alternativen ersetzt werden sollten, um den Gesamtwert der Kunden zu verbessern, wobei stets die Abwärtskompatibilität zu berücksichtigen ist.

Für die Mitteilung der bevorstehenden Entfernung/Ersetzung von Campaign Standard-Funktionen gelten die folgenden Regeln:

* Die Ankündigung der Vernichtung kommt an erster Stelle. Auch wenn nicht mehr unterstützte Funktionen für bestehende Benutzer verfügbar sein können, werden sie weder weiter verbessert noch dokumentiert.
* Die veralteten Funktionen werden frühestens in der folgenden Version entfernt. Das tatsächliche Zieldatum für die Entfernung wird auf dieser Seite angegeben.

Durch diesen Prozess erhalten Kunden mindestens einen Versionszyklus, um ihre Implementierung an eine neue Version oder einen Nachfolger einer nicht mehr unterstützten Funktion anzupassen, bevor sie die Implementierung tatsächlich entfernen.

>[!NOTE]
>Die Versionen und neuen Funktionen von Adobe Campaign Standard sind in den [Versionshinweisen](../../rn/using/release-notes.md)aufgeführt.


## Veraltete Funktionen {#deprecated-features}

Dieser Abschnitt listet Funktionen auf, die mit den neuesten Kampagnen Standard-Versionen als veraltet markiert wurden.

Im Allgemeinen werden Funktionen, die in einer zukünftigen Version entfernt werden sollen, zuerst auf &quot;Veraltet&quot;eingestellt, wobei eine Alternative bereitgestellt wird. Diese Funktionen sind für neue Campaign Standard-Kunden entweder nicht mehr verfügbar oder sollten für keine neue Implementierung verwendet werden. Sie werden auch aus der Produktdokumentation entfernt.

Kunden wird empfohlen, zu prüfen, ob sie die Funktion/Funktion in ihrer aktuellen Bereitstellung nutzen, und Pläne zur Änderung ihrer Implementierung zu erstellen, um die verfügbare Alternative zu nutzen. Planen Sie Ihre Umgebung und Ihre Projektaktualisierungen entsprechend dem Zielentfernungsdatum.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Push-Benachrichtigungen mit SDK v4</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p> Ab Version 20.1 wird SDK v4 nicht mehr unterstützt. <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">Mehr dazu</a>.</p><br/>
   <p>Das <a href="https://aep-sdks.gitbook.io/docs/">Adobe Experience Platform Mobile SDK</a> (früher als v5 bezeichnet) unterstützt ausschließlich kommende Adobe Experience Cloud-Funktionen.</p></br>
     <p>Zielentfernungsdatum:30. September 2020</p>
     </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Creative SDK for Campaign Standard</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Creative SDK wurde abgesetzt. Demzufolge wird die Image-Edition, die auf Creative SDK basiert, in den E-Mails von Campaign Standard ab Version 20.1 nicht mehr unterstützt.</p></br>
  <p> Zielentfernungsdatum:März 2020 - Version der Kampagne 20.2</p>
   </td> 
  </tr> 
 </tbody> 
</table>
<table> 
 <thead> 
  <tr> 
   <th> <strong>Datenschutzanforderungen - Kampagnen-API und -Oberfläche</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Ab Version 19.4 von Campaign wird die Verwendung der Kampagnen-API und -Schnittstelle für den Zugriff und das Löschen von Anforderungen nicht mehr unterstützt. Verwenden Sie den <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Adobe Privacy Core Service</a>.</p></br>
   <p>Siehe auch <a href="https://helpx.adobe.com/campaign/kb/acs-privacy.html">Datenschutzverwaltung in Campaign Standard</a>.</p>
  <p> Zielentfernungsdatum: Juli 2020 - Version der Kampagne 20.5</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>E-Mail-Design - Veralteter E-Mail-Editor</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Ab der Version Campaign 19.0 wird der alte E-Mail-Editor nicht mehr unterstützt. Verwenden Sie <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">den neuen E-Mail-Designer</a> , um Ihren E-Mail-Inhalt zu erstellen und zu personalisieren. </p></br>
   <p>Lesen Sie <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">diesen Abschnitt</a> , um zu erfahren, wie Sie Ihre E-Mail-Vorlagen für den neuen Editor anpassen.</p></br>
  <p> Zielentfernungsdatum:Oktober 2020 - Version der Kampagne 20.6</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Benutzer und Sicherheit - Geografische Einheiten</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Ab Version 18.7 werden geografische Einheiten nicht mehr unterstützt. Organisatorische und geografische Einheiten sind identische Konstrukte in Campaign. Benutzer sollten nur organisatorische Einheiten verwenden, um ihre Hierarchie der Benutzerberechtigungen/des Datenzugriffs zu erstellen. <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html">Mehr dazu</a>. Bitte beachten Sie, dass neue Campaign Standard-Instanzen sowie vorhandene Instanzen ohne geografische Einheiten ab Version 18.7 nicht implementiert werden können.</p>
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
   <td> <p>Adobe Campaign und Adobe Experience Cloud haben die Unterstützung für Microsoft Internet Explorer 11 ab Frühjahr 2019 und für Campaign 19.2 eingestellt. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser. <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/getting-started/discovering-the-interface/compatible-browsers.html">Mehr dazu</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>
