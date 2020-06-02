---
title: Erste Schritte mit Kampagne-Integrationen
description: Adobe Campaign ermöglicht die Verwendung anderer Adobe-Lösungen und die Kombination ihrer Funktionen.
page-status-flag: never-activated
uuid: 59d7cd99-a6f7-47f1-9b5c-c50e27a2bef8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: get-started-campaign-integrations
discoiquuid: 9633e9ca-3323-499b-8259-45165d59a4d0
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e89218b584f0d621ca700d4ee2a4866555d00679
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 99%

---


# Über Campaign-Integrationen{#get-started-campaign-integrations}

In diesem Abschnitt werden die funktionalen Integrationen der vorliegenden Adobe Campaign-Version mit anderen Lösungen und Diensten beschrieben.

Die Integration von Adobe Campaign mit verschiedenen Adobe Experience Cloud-Lösungen bietet Ihnen eine schlagkräftige Kombination aus bewährten Funktionen wie Nachrichtenversand und Kampagnenverwaltung mit Tools für individuell zugeschnittene, relevante Customer Journeys.

>[!NOTE]
>
> Adobe Campaign ist standardmäßig mit einem Adobe-Experience-Cloud-Konto verknüpft.

In Ihrer Arbeitsumgebung verfügen Sie unter Umständen über verschiedene Lösungen der Adobe Experience Cloud. Diese sind miteinander über Organisationen – auch Mandanten genannt – verbunden.

Eine Organisation ist die Entität, mit der ein Administrator Gruppen und Benutzer konfigurieren und Anmeldungen in der Experience Cloud steuern kann. Eine Organisation ist wie eine Unternehmensanmeldung bei allen Produkten und Lösungen, die in der Experience Cloud enthalten sind. Normalerweise besitzt eine Organisation den Namen Ihres Unternehmens. Ein Unternehmen kann jedoch über mehrere Organisationen verfügen. Weiterführende Informationen zur Verwaltung von Benutzern und Organisationen finden Sie im [Hilfeportal der Adobe Experience Cloud](https://marketing.adobe.com/resources/help/de_DE/mcloud/organizations.html).

Wenn Sie Datenflüsse von anderen Systemen mit Adobe Campaign integrieren möchten, beachten Sie unsere [API-Dokumentation](../../api/using/get-started-apis.md).

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
   <td> Experience Manager<br /> 6.1, 6.2, 6.3, 6.4, 6.5<br /> </td> 
   <td> Dient der direkten Erstellung von E-Mail-Inhalten und mit der Adobe-Campaign-Datenbank verknüpften Formularen in Adobe Experience Manager.<br /> </td> 
   <td> 
     <a href="../../integrating/using/integrating-with-experience-manager.md">Verwenden von Campaign und Experience Manager</a><br/>, <a href="https://helpx.adobe.com/de/experience-manager/6-4/sites/administering/using/campaignstandard.html">Integrieren von Experience Manager und Campaign Standard</a><br/>, <a href="https://docs.campaign.adobe.com/doc/standard/getting_started/de/ACS_AEM.html">Erstellen einer E-Mail mit Experience Manager und Campaign</a> 
    </td> 
  </tr> 
  <tr> 
   <td> Target<br /> Classic, Standard<br /> </td> 
   <td> Dient bei der Öffnung einer mit Adobe Campaign erstellten und gesendeten E-Mail dem Einfügen von durch Adobe Target dynamisch berechneten Bildern.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-target-integration.md">Verwenden von Campaign und Target</a> <br/>, <a href="https://marketing.adobe.com/resources/help/de_DE/target/a4t/c_campaign_and_target.html">Integrieren von Campaign und Target</a><br/>, <a href="https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html">Personalize Email Images in Real-Time</a> Video (Schritt 3)
    </td> 
  </tr> 
  <tr> 
   <td> Analytics<br /> Standard, Premium <br /> </td> 
   <td> Dient der Überprüfung des Erfolgs Ihres E-Mail-Versands direkt in Adobe Analytics.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-campaign-analytics-integration.md">Freigabe von Daten in Campaign mit Analytics</a><br/>, <a href="https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html">Share KPIs for integrated Campaign reporting</a> Video (Schritt 1))
    </td> 
  </tr> 
  <tr> 
   <td> Adobe Audience Manager und People Core Service (Profile &amp; Audiences)<br /> </td> 
   <td> Dient dem Austausch von Zielgruppen zwischen den verschiedenen, von Ihnen verwendeten Adobe Experience Cloud-Anwendungen.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">People Core Service (Profiles &amp; Audiences)</a><br /> </td> 
  </tr> 
  <tr> 
   <td> Assets Core Service und Assets On Demand<br /> </td> 
   <td> Dient dem Einfügen von Assets aus Ihrer Adobe-Experience-Cloud-Bibliothek in mit Adobe Campaign erstellte E-Mails und Landingpages.<br /> </td> 
   <td> <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">Assets Core Service</a> oder Assets On Demand<br /> </td> 
  </tr> 
  <tr> 
   <td> Points of Interest (Analytics for Mobile)<br /> </td> 
   <td> Ermöglicht die Erfassung von POI-Daten Ihrer Mobile-App-Abonnenten, damit Sie ihnen über Adobe Campaign personalisierte Marketing-Nachrichten senden können.<br /> </td> 
   <td> <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">Senden von standortbasierten Marketing-Nachrichten mit Campaign und POI-Daten</a> (Analytics for Mobile)<br /> </td> 
  </tr> 
  <tr> 
   <td> Experience Cloud Triggers<br /> </td> 
   <td> Ermöglicht den Versand personalisierter E-Mails über Adobe Campaign an Ihre Kunden als Reaktion auf bestimmte Verhaltensweisen, die von Adobe Analytics auf Ihrer Website beobachtet werden.<br /> </td> 
   <td> 
    <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">Verwenden von Experience Cloud Triggers in Campaign Standard</a><br/>, <a href="../../integrating/using/abandonment-triggers-use-cases.md">Anwendungsbeispiele zur Abbruchsauslösung in Campaign</a><br/>, <a href="https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html">Trigger Remarketing Messages based on Site Activity</a> Video (Schritt 2)
    </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver<br /> </td> 
   <td> Hiermit können Sie E-Mail-Inhalte in Dreamweaver bearbeiten und mit Adobe Campaign synchronisieren.<br /> </td> 
   <td> 
    Video <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html">Create personalized emails with Dreamweaver</a> <br/>, <a href="https://helpx.adobe.com/de/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Verwenden der Campaign-Erweiterung für Dreamweaver</a> 
  </td> 
  </tr> 
  <tr> 
   <td> Experience Platform SDKs<br /> </td> 
   <td> Mithilfe der Experience Platform SDKs kann eine Mobile-App-Eigenschaft automatisch in Adobe Campaign aktiviert werden.<br /> </td> 
   <td> <a href="https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html">Konfiguration einer Mobile App mithilfe von Experience Platform SDKs</a><br /> </td> 
  </tr> 
 </tbody> 
</table>

