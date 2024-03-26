---
title: Erste Schritte mit Campaign-Integrationen
description: Verwenden Sie andere Lösungen von Adobe und kombinieren Sie ihre verschiedenen Funktionen mit Campaign.
audience: integrating
content-type: reference
topic-tags: get-started-campaign-integrations
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: ecf88c7d-6729-4b3a-85c4-60427bb57442
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 100%

---

# Über Campaign-Integrationen{#get-started-campaign-integrations}

In diesem Abschnitt werden die funktionalen Integrationen der vorliegenden Adobe Campaign-Version mit anderen Lösungen und Diensten beschrieben.

Die Integration von Adobe Campaign mit verschiedenen Adobe Experience Cloud-Lösungen bietet Ihnen eine schlagkräftige Kombination aus bewährten Funktionen wie Nachrichtenversand und Kampagnenverwaltung mit Tools für individuell zugeschnittene, relevante Customer Journeys.

>[!NOTE]
>
> Adobe Campaign ist standardmäßig mit einem Adobe-Experience-Cloud-Konto verknüpft.

In Ihrer Arbeitsumgebung verfügen Sie unter Umständen über verschiedene Lösungen der Adobe Experience Cloud. Diese sind miteinander über Organisationen – auch Mandanten genannt – verbunden.

Eine Organisation ist die Entität, mit der ein Administrator Gruppen und Benutzer konfigurieren und Anmeldungen in der Experience Cloud steuern kann. Eine Organisation ist wie eine Unternehmensanmeldung bei allen Produkten und Lösungen, die in der Experience Cloud enthalten sind. Normalerweise besitzt eine Organisation den Namen Ihres Unternehmens. Ein Unternehmen kann jedoch über mehrere Organisationen verfügen. Weiterführende Informationen zur Verwaltung von Benutzern und Organisationen finden Sie im [Hilfeportal der Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html?lang=de).

Wenn Sie Datenflüsse von anderen Systemen mit Adobe Campaign integrieren möchten, beachten Sie unsere [API-Dokumentation](../../api/using/get-started-apis.md).

>[!NOTE]
>
>Adobe Campaign Standard kann auch eine Verbindung zu Microsoft Dynamics 365 herstellen: Diese Integration ermöglicht die Synchronisierung aller verfügbaren Kontaktdaten im CRM-System, sodass alle relevanten Kontaktdaten für Kampagnenaktivitäten verfügbar sind. Weiterführende Informationen dazu finden Sie im Abschnitt zur [Verwendung von Campaign und Dynamics 365](../../integrating/using/d365-acs-get-started.md).


<table> 
 <thead> 
  <tr> 
   <th> Lösung<br /> </th> 
   <th> Anwendungsbeispiel<br /> </th> 
   <th> Siehe Abschnitt<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Adobe Experience Manager<br /> </td> 
   <td> Dient der direkten Erstellung von E-Mail-Inhalten und mit der Adobe-Campaign-Datenbank verknüpften Formularen in Adobe Experience Manager.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">Verwenden von Campaign und Experience Manager</a>, <a href="https://helpx.adobe.com/de/experience-manager/6-4/sites/administering/using/campaignstandard.html">Integrieren von Experience Manager und Campaign Standard</a>, <a href="https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de">Erstellen einer E-Mail mit Experience Manager und Campaign</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Target<br /> </td> 
   <td> Ermöglicht Ihnen, durch Adobe Target dynamisch berechnete Bilder einzufügen, wenn eine mit Adobe Campaign erstellte und gesendete E-Mail geöffnet wird.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">Verwenden von Campaign und Target</a>, <a href="https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=de">Integrieren von Campaign und Target</a>, <a href="https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html">E-Mail-Bilder in Echtzeit personalisieren</a> Video (Schritt 3)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Analytics<br /> </td> 
   <td> Dient der Überprüfung des Erfolgs Ihres E-Mail-Versands direkt in Adobe Analytics.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Freigabe von Campaign-Daten für Analytics</a> <a href="https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html">Freigabe von KPIs für integriertes Campaign-Reporting</a> Video (Schritt 1)
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager und People Core Service (Profile &amp; Audiences)<br /> </td> 
   <td> Dient dem Austausch von Audiences zwischen den verschiedenen, von Ihnen verwendeten Adobe Experience Cloud-Anwendungen.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">People Core Service (Profiles &amp; Audiences)</a><br /> </td> 
  </tr> 
   <tr> 
   <td> Adobe Echtzeit-Kundendatenplattform (RTCDP)<br /> </td> 
   <td> Die Integration zwischen Adobe Campaign und Adobe Echtzeit-Kundendatenplattform (RTCDP) ermöglicht das Freigeben von Segmentdaten und das Importieren von Audiences in Adobe Campaign.</td>
   <td><a href="../../integrating/using/get-started-sources-destinations.md">Erste Schritte mit Quellen und Zielen</a></td>
  </tr> 
  <tr> 
   <td> Adobe Assets Core Service und Assets On Demand<br /> </td> 
   <td> Dient dem Einfügen von Assets aus Ihrer Adobe-Experience-Cloud-Bibliothek in mit Adobe Campaign erstellte E-Mails und Landingpages.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">Assets Core Service</a> oder Assets On Demand<br /> </td> 
  </tr> 
  <tr> 
   <td> Points of Interest (Analytics for Mobile)<br /> </td> 
   <td> Ermöglicht die Erfassung von POI-Daten Ihrer Mobile-App-Abonnenten, damit Sie ihnen über Adobe Campaign personalisierte Marketing-Nachrichten senden können.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">Senden von standortbasierten Marketing-Nachrichten mit Campaign und POI-Daten</a> (Analytics for Mobile)<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Experience Cloud Triggers<br /> </td> 
   <td> Ermöglicht den Versand personalisierter E-Mails über Adobe Campaign an Ihre Kunden als Reaktion auf bestimmte Verhaltensweisen, die von Adobe Analytics auf Ihrer Website beobachtet werden.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Verwenden von Experience Cloud Triggers in Campaign Standard</a>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">Anwendungsbeispiele zur Abbruchsauslösung in Campaign</a>, <a href="https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html">Trigger Remarketing Messages based on Site Activity</a> Video (Schritt 2)
    </td> 
  </tr> 
    <tr> 
   <td> Adobe Journey Orchestration<br /> </td> 
   <td> Ermöglicht den Versand von E-Mails, Push-Benachrichtigungen und SMS unter Verwendung der Transaktionsnachrichten-Funktionen von Adobe Campaign Standard im Kontext von Adobe Journey Orchestration durch eine vorkonfigurierte Aktion.<br /> </td> 
   <td> <a href="https://experienceleague.adobe.com/docs/journeys/using/action-journeys/working-with-adobe-campaign.html?lang=de">Arbeiten mit Adobe Journey Orchestration und Adobe Campaign Standard</a><br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Dreamweaver<br /> </td> 
   <td> Hiermit können Sie E-Mail-Inhalte in Dreamweaver bearbeiten und mit Adobe Campaign synchronisieren.<br /> </td> 
   <td> 
    Video <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html?lang=de">Personalisierte E-Mails mit Dreamweaver erstellen</a>, <a href="https://helpx.adobe.com/de/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Verwenden der Campaign-Erweiterung für Dreamweaver</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Adobe Experience Platform-SDKs<br /> </td> 
   <td> Mithilfe der Experience Platform SDKs kann eine Mobile-App-Eigenschaft automatisch in Adobe Campaign aktiviert werden.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html">Konfiguration einer Mobile App mithilfe von Experience Platform SDKs</a><br /> </td> 
  </tr> 
 </tbody> 
</table>
