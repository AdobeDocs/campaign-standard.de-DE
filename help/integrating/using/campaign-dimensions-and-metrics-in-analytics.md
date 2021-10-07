---
title: Campaign-Dimensionen und -Metriken in Analytics
description: Hier erhalten Sie Informationen über die in Adobe Analytics verfügbaren Dimensionen, mit denen Ihre E-Mail-Sendungen in Adobe Campaign verfolgt werden können.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 6516c71a-efa8-4778-82bb-10615378f985
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '322'
ht-degree: 100%

---

# Campaign-Dimensionen und -Metriken in Analytics{#campaign-dimensions-and-metrics-in-analytics}

Durch die Integration mit Adobe Analytics in Adobe Campaign können Sie jetzt die Wirkung Ihrer E-Mail-Sendungen direkt in Adobe Analytics verfolgen.

Unten finden Sie die in Analytics verfügbaren **[!UICONTROL Campaign-Dimensionen]**:

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Kennung der Kampagne<br /> </td> 
   <td> Interner Kampagnenname, wie er in Campaign angezeigt wird<br /> </td> 
  </tr> 
  <tr> 
   <td> Kampagnentitel<br /> </td> 
   <td> Titel der Kampagne, wie er in Campaign angezeigt wird<br /> </td> 
  </tr> 
  <tr> 
   <td> Versandkennung<br /> </td> 
   <td> Interner Name des Versands, wie er in Campaign angezeigt wird<br /> Beispiel: DM1 ist ein wiederkehrender Versand, gemäß dem jede Woche ein untergeordneter Versand erfolgt. DM2, DM3 und DM4 werden in den ersten drei Wochen gesendet. In der Dimension "Versandkennung" werden dann die Ergebnisse für jeden Versand, also DM1 bis DM4, angezeigt. <br /> </td> 
  </tr> 
  <tr> 
   <td> Versandtitel<br /> </td> 
   <td> Titel des Versands, wie er in Campaign angezeigt wird<br /> </td> 
  </tr> 
  <tr> 
   <td> Kennung des ausgeführten Versands<br /> </td> 
   <td> Interner Name des Versands, wie er in Campaign angezeigt wird Dies betrifft nur Sendungen, die in Campaign bereits ausgeführt wurden.<br /> Beispiel: DM1 ist ein wiederkehrender Versand, gemäß dem jede Woche ein untergeordneter Versand erfolgt. DM2, DM3 und DM4 werden in den ersten drei Wochen gesendet. In der Dimension "Kennung des ausgeführten Versands" werden die Ergebnisse für die ausgeführten Sendungen, nämlich die untergeordneten Sendungen DM2, DM3 und DM4, aufgeführt. <br /> </td> 
  </tr> 
  <tr> 
   <td> Titel des ausgeführten Versands<br /> </td> 
   <td> Titel des Versands, wie er in Campaign angezeigt wird. Dies betrifft nur Sendungen, die in Campaign bereits ausgeführt wurden.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Unten finden Sie die in Analytics verfügbaren **[!UICONTROL Campaign-Metriken]**:

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Haben geklickt<br /> </td> 
   <td> Die Anzahl der Klicks auf einen Inhalt in einem Versand.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Haben geöffnet<br /> </td> 
   <td> Anzahl der Öffnungen einer Nachricht in einem Versand.<br /> </td> 
  </tr> 
  <tr> 
   <td> Gesendet<br /> </td> 
   <td> Gesamtzahl der gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Rücksendungen insgesamt<br /> </td> 
   <td> Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelöffnungen<br /> </td> 
   <td> Anzahl der Empfänger, die den Versand geöffnet haben<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelklicks<br /> </td> 
   <td> Anzahl der Empfänger, die einen Inhalt in einem Versand angeklickt haben<br /> </td> 
  </tr> 
  <tr> 
   <td> Abgemeldet<br /> </td> 
   <td> Gesamtanzahl der Klicks auf den Abmelde-Link.<br /> </td> 
  </tr> 
 </tbody> 
</table>
