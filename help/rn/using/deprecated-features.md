---
title: Eingestellte und entfernte Funktionen von Campaign Standard
description: Auf dieser Seite finden Sie eingestellte und entfernte Funktionen von Adobe Campaign Standard.
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
source-git-commit: f8c8dd5ec3dcff557d17e92591748cb1b6694122
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 95%

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

Kunden wird empfohlen, die Nutzung der Funktion in ihrer aktuellen Bereitstellung zu prüfen und Pläne zur Änderung ihrer Implementierung zu erstellen, um die verfügbare Alternative zu nutzen. Planen Sie Ihre Umgebung und Ihre Projektaktualisierungen entsprechend der Zielgruppen-Entfernungsversion.

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
     <p>
     <em>Geplantes Datum für die Entfernung: 30. September 2020</em></p>
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
   <td> <p>Mit Campaign-Version 19.4. wurde die Campaign-API und -Benutzeroberfläche für Zugriffs- und Löschanfragen eingestellt. Der zweistufige Löschvorgang für Profile ist nicht verfügbar. Verwenden Sie <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Privacy Core Service von Adobe</a>.</p></br>
   <p>Siehe auch <a href="https://helpx.adobe.com/de/campaign/kb/acs-privacy.html">Datenschutzverwaltung in Campaign Standard</a>.</p>
  <p> 
  <em>Version zum Entfernen von Zielgruppen: Version 20.4 der Kampagne</em></p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>E-Mail-Design –Veralteter E-Mail-Editor</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Ab Campaign-Version 19.0 wird der alte E-Mail-Editor nicht mehr unterstützt. Verwenden Sie <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">den neuen Email Designer</a>, um Ihren E-Mail-Inhalt zu erstellen und zu personalisieren. </p></br>
   <p>In <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">diesem Abschnitt</a> erfahren Sie, wie Sie Ihre E-Mail-Vorlagen für den neuen Editor anpassen.</p></br>
  <p> 
  <em>Version zum Entfernen von Zielgruppen: Version 20.4 der Kampagne</em></p>
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
   <td> <p>Ab Version 18.7 werden geografische Einheiten nicht mehr unterstützt. Organisationseinheiten und geografische Einheiten sind in Campaign identische Konzepte. Benutzer sollten ausschließlich Organisationseinheiten verwenden, um eine Hierarchie für Benutzerberechtigungen/den Datenzugriff zu erstellen. <a href="https://helpx.adobe.com/de/campaign/standard/administration/using/organizational-units.html">Mehr dazu</a>. Bitte beachten Sie, dass die Funktion ab Version 18.7 nicht mehr für neue Campaign Standard-Instanzen oder für vorhandene Instanzen ohne geografische Einheiten implementiert werden kann.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

## Entfernte Funktionen {#removed-features}

In diesem Abschnitt werden Funktionen und Leistungsmerkmale aufgelistet, die aus Campaign Standard entfernt wurden.

<table> 
 <thead> 
  <tr> 
   <th> <strong>Creative SDK für Campaign Standard</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Creative SDK wurde eingestellt. Infolgedessen ist die von Creative SDK unterstützte Bildbearbeitung in Campaign Standard-E-Mails ab Version Campaign 20.2 nicht mehr verfügbar.</p></br>
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
   <td> <p>Adobe Campaign und Adobe Experience Cloud haben mit Campaign-Version 19.2 (Frühling 2019) den Support für Microsoft Internet Explorer 11 eingestellt. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser. <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/getting-started/discovering-the-interface/compatible-browsers.html">Mehr dazu</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>
