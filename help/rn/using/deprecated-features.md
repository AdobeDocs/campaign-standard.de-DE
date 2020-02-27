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
source-git-commit: 6ffbf03a7eb4fc1b5bfbd523c0c5342d41cfd211

---


# Funktionen von Campaign Standard veraltet und entfernt {#deprecated-and-removed-features}

Adobe bewertet die Produktfunktionen ständig, um ältere Funktionen zu identifizieren, die durch modernere Alternativen ersetzt werden sollten, um den Gesamtwert der Kunden zu verbessern, wobei stets die Abwärtskompatibilität zu berücksichtigen ist.

Für die Mitteilung der bevorstehenden Entfernung/Ersetzung von Campaign Standard-Funktionen gelten die folgenden Regeln:

* Die Ankündigung der Vernichtung kommt an erster Stelle. Auch wenn nicht mehr unterstützte Funktionen für bestehende Benutzer verfügbar sein können, werden sie weder weiter verbessert noch dokumentiert.
* Die veralteten Funktionen werden frühestens in der folgenden Version entfernt. Das tatsächliche Zieldatum für die Entfernung wird auf dieser Seite angegeben.

Durch diesen Prozess erhalten Kunden mindestens einen Versionszyklus, um ihre Implementierung an eine neue Version oder einen Nachfolger einer nicht mehr unterstützten Funktion anzupassen, bevor sie die Implementierung tatsächlich entfernen.

>[!NOTE]
>Die Versionen und neuen Funktionen von Adobe Campaign Standard sind in den [Versionshinweisen](../../rn/using/release-notes.md)aufgeführt.


## Veraltete Funktionen {#deprecated-features}

Dieser Abschnitt listet Funktionen auf, die mit den neuesten Kampagnen Standard-Versionen als veraltet markiert wurden. Im Allgemeinen werden Funktionen, die in einer zukünftigen Version entfernt werden sollen, zuerst auf &quot;Veraltet&quot;eingestellt, wobei eine Alternative bereitgestellt wird. Diese Funktionen sind für neue Campaign Standard-Kunden entweder nicht mehr verfügbar oder sollten für keine neue Implementierung verwendet werden. Sie werden auch aus der Produktdokumentation entfernt.

Kunden wird empfohlen, zu prüfen, ob sie die Funktion/Funktion in ihrer aktuellen Bereitstellung nutzen, und Pläne zur Änderung ihrer Implementierung zu erstellen, um die verfügbare Alternative zu nutzen. Planen Sie Ihre Umgebung und Ihre Projektaktualisierungen entsprechend dem Zielentfernungsdatum.

<table> 
 <thead> 
  <tr> 
   <th> Version<br /> </th> 
   <th> Funktionen<br /> </th> 
   <th> Replacement<br /> </th> 
    <th> Target-Entfernungsdatum<br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 20.1<br /> </td> 
   <td> Push-Benachrichtigungen<br /> </td> 
    <td> Das <a href="https://aep-sdks.gitbook.io/docs/version-4-sdk-end-of-support-faq">Adobe Experience Platform Mobile SDK</a> (früher als v5 bezeichnet) unterstützt ausschließlich kommende Adobe Experience Cloud-Funktionen. <br /> </td> 
    <td> September 30, 2020<br /> </td> 
  </tr> 
  <tr> 
   <td> 20.1<br /> </td> 
   <td> Creative SDK for Campaign Standard<br /> </td> 
  <td> Adobe Creative SDK wurde abgesetzt. Infolgedessen wird die Image-Edition, die auf Creative SDK basiert, in den E-Mails von Campaign Standard jetzt nicht mehr unterstützt.<br /> </td>
  <td> März 2020 - Version der Kampagne 20.2<br /> </td> 
  </tr> 
  <tr> 
   <td> 19.4<br /> </td> 
   <td> Datenschutzanforderungen - Kampagnen-API und -Oberfläche<br /> </td>
    <td> Die Campaign-API und -Schnittstelle für Zugriffs- und Löschanfragen wurde eingestellt. Verwenden Sie den Datenschutz-Core-Dienst. <a href="https://www.adobe.io/apis/experiencecloud/gdpr.html">Mehr dazu</a>. Siehe auch <a href="https://helpx.adobe.com/campaign/kb/acs-privacy.html">Datenschutzverwaltung in Campaign Standard</a>.<br /> </td>
    <td>  Juli 2020 - Version der Kampagne 20.5<br /> </td> 
  </tr>
  <tr> 
   <td> 19.0<br /> </td> 
   <td> E-Mail-Design - Veralteter E-Mail-Editor<br /> </td>
    <td> Der veraltete E-Mail-Editor ist jetzt veraltet. Verwenden Sie den neuen E-Mail-Designer, um E-Mail-Inhalte zu erstellen und zu personalisieren. <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/designing-content-in-adobe-campaign.html">Mehr dazu</a>. Lesen Sie <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/designing-content/building-email-content/using-existing-content.html">diesen Abschnitt</a> , um zu erfahren, wie Sie Ihre E-Mail-Vorlagen für den neuen Editor anpassen.<br /> </td>
    <td> Oktober 2020 - Version der Kampagne 20.6<br /> </td> 
  </tr>
  <tr> 
   <td> 18.7<br /> </td> 
   <td> Benutzer und Sicherheit - Geografische Einheiten<br /> </td>
    <td> Organisatorische und geografische Einheiten sind identische Konstrukte in Campaign. Benutzer sollten nur organisatorische Einheiten verwenden, um ihre Hierarchie der Benutzerberechtigungen/des Datenzugriffs zu erstellen. <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html">Mehr dazu</a>. Please note that new Campaign Standard instances, as well as existing instances with no geographical units created, cannot have this capability implemented starting 18.7 release.<br /> </td>
    <td> K. A.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Ende der Kompatibilität {#end-of-compatibility}

<table> 
 <thead> 
  <tr> 
   <th> Version<br /> </th> 
   <th> Funktionen<br /> </th> 
   <th> Replacement<br /> </th> 
 </tr> 
 </thead> 
 <tbody>
<tr> 
   <td> 19.2<br /> </td> 
   <td> Datenschutzanforderungen - Kampagnen-API und -Oberfläche<br /> </td>
    <td> Adobe Campaign und Adobe Experience Cloud haben die Unterstützung für Microsoft Internet Explorer 11 ab Frühjahr 2019 und für Campaign 19.2 eingestellt. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser.  <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/getting-started/discovering-the-interface/compatible-browsers.html">Mehr dazu</a>.<br /> </td>
    <td><br /> </td> 
  </tr>
  </tbody> 
</table>
