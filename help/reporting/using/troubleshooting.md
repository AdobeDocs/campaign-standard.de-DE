---
title: Problembehebung
seo-title: Problembehebung
description: Problembehebung
seo-description: Hier finden Sie häufig gestellte Fragen zu dynamischen Berichten.
page-status-flag: nie aktiviert
uuid: a 84 a 18 bd -4 e 33-466 e-a 6 ce-d 7008 fe 12746
contentOwner: gezählt
products: SG_ CAMPAIGN/STANDARD
audience: Berichterstellung
content-type: Referenz
topic-tags: Fehlerbehebung
discoiquuid: bbb 41 c 38-12 c 1-4625-85 d 5-69627 e 2 f 4 b 39
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e0cbdfecde495d7c9f8bfa33dd5ee8598cdfe60a

---


# Problembehebung{#troubleshooting}

In diesem Abschnitt finden Sie häufig gestellte Fragen zu dynamischen Berichten.

## For Unique opens and Unique clicks, the count in the aggregate row is not matching the ones in individual rows {#unique-open-clicks-no-match}

Dies ist ein erwartetes Verhalten.
Wir können das folgende Beispiel verwenden, um dieses Verhalten zu erläutern.

Eine E-Email wird an Profile P 1 und P 2 gesendet.

P 1 öffnet die E-Mail am ersten Tag zweimal und dann am zweiten Tag.

P 2 öffnet die E-Email einmal am ersten Tag und öffnet sie nicht in den folgenden Tagen erneut.
Im Folgenden finden Sie eine visuelle Darstellung der Interaktion der Profile mit der gesendeten E-Mail:

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>Day</strong> <br /> </th> 
   <th align="center"> <strong>Öffnungen</strong> <br /> </th> 
   <th align="center"> <strong>Einzelöffnungen</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> Day 1<br /> </td> 
   <td align="center"> 2 + 1 = 3<br /> </td> 
   <td align="center"> 1 + 1 = 2<br /> </td> 
  </tr> 
  <tr> 
   <td align="center"> Day 2<br /> </td> 
   <td align="center"> 3 + 0 = 3<br /> </td> 
   <td align="center"> 1 + 0 = 1<br /> </td> 
  </tr>
 </tbody> 
</table>

To understand the overall number of unique opens, we need to sum up the row counts of **[!UICONTROL Unique Opens]** which gives us the value 3. Da die E-Email jedoch nur auf 2 Profile ausgerichtet wurde, sollte die offene Rate 150% anzeigen.

To not obtain percentage higher than 100, the definition of **[!UICONTROL Unique Opens]** is maintained to be the number of unique broadlogs that were opened. In diesem Fall, wenn P 1 die E-Email am Tag 1 und Tag 2 geöffnet hat, ist seine einzigartige Öffnung weiterhin 1.

Dies ergibt die folgende Tabelle:

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>Day</strong> <br /> </th> 
   <th align="center"> <strong>Öffnungen</strong> <br /> </th> 
   <th align="center"> <strong>Einzelöffnungen</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> Day 1<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 2<br /> </td>
  </tr> 
  <tr> 
   <td align="center"> Day 2<br /> </td> 
   <td align="center"> 3<br /> </td> 
   <td align="center"> 2<br /> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Eindeutige Zahlen basieren auf einer HLL-basierten Skizze. Dies kann bei großen Zahlen zu leichten Ungenauigkeiten führen.

## Open counts do not match the Database count {#open-counts-no-match-database}

This may be due to the fact that, heuristics are used in Dynamic reporting to track opens even when we can't track the **[!UICONTROL Open]** action.

For example, if a user has disabled images on their client and click on a link in the email, the **[!UICONTROL Open]** may not be tracked by the database but the **[!UICONTROL Click]** will.

Therefore, the **[!UICONTROL Open]** tracking logs counts may not have the same count in the database.

Such occurrences are added as **"an email click implies an email open"**.

>[!NOTE]
>
>Da eindeutige Zähler auf einer HLL-basierten Skizze basieren, können kleinere Inkonsistenzen zwischen den Zählungen aufgetreten sein.

## Wie werden wiederkehrende/Transaktionslieferungen berechnet?

Bei wiederkehrenden und Transaktionsbasierten Lieferungen werden die Zählungen sowohl der übergeordneten als auch der untergeordneten Auslieferung zugeordnet.

We can take the example of a recurring delivery named **R1** set to run every day on day 1 (RC1), day 2 (RC2) and day 3 (RC3).

Nehmen wir an, dass nur eine Person alle untergeordneten Lieferungen mehrmals geöffnet hat. In this case, the individual recurring child deliveries will show the **[!UICONTROL Open]** count as 1 for each.

However, since the same person clicked on all the deliveries, the parent recurring delivery will also have **[!UICONTROL Unique open]** as 1.

After the Adobe Campaign Standard 19.2.1 release, the definition of **Unique counts** is changed from **Number of unique persons interacting with the delivery** to **Number of unique messages interacted**.

Vor der Adobe Campaign Standard 19.2.1-Version wurden folgende Berichte angezeigt:

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>Versand</strong> <br /> </th> 
   <th align="center"> <strong>Gesendet</strong> <br /> </th> 
   <th align="center"> <strong>Zugestellt</strong> <br /> </th>
   <th align="center"> <strong>Öffnungen</strong> <br /> </th> 
   <th align="center"> <strong>Einzelöffnungen</strong> <br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong>R1<br/> </td> 
   <td align="center"> <strong>100<br/> </td> 
   <td align="center"> <strong>90<br/> </td> 
   <td align="center"> <strong>10<br/> </td> 
   <td align="center"> <strong>1<br/> </td> 
  </tr> 
  <tr> 
   <td align="center"> RC1<br/> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
    <tr> 
   <td align="center"> RC2<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 30<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
    <tr> 
   <td align="center"> RC3<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
 </tbody> 
</table>

Nach der Adobe Campaign Standard 19.2.1-Version sehen die Berichte wie folgt aus:

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>Versand</strong> <br /> </th> 
   <th align="center"> <strong>Gesendet</strong> <br /> </th> 
   <th align="center"> <strong>Zugestellt</strong> <br /> </th>
   <th align="center"> <strong>Öffnungen</strong> <br /> </th> 
   <th align="center"> <strong>Einzelöffnungen</strong> <br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong>R1<br/> </td> 
   <td align="center"> <strong>100<br/> </td> 
   <td align="center"> <strong>90<br/> </td> 
   <td align="center"> <strong>10<br/> </td> 
   <td align="center"> <strong>3<br/> </td> 
  </tr> 
  <tr> 
   <td align="center"> RC1<br/> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
    <tr> 
   <td align="center"> RC2<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 30<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
    <tr> 
   <td align="center"> RC3<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
 </tbody> 
</table>

## What is the colors' signification in my reports' table? {#reports-color-signification}

In Ihren Berichten angezeigte Farben werden randomisiert und können nicht personalisiert werden. Sie stellen eine Fortschrittsleiste dar und werden angezeigt, damit Sie den in Ihren Berichten erreichten Höchstwert besser hervorheben können.

Im folgenden Beispiel hat die Zelle die gleiche Farbe, da ihr Wert 100% beträgt.

![](assets/troubleshooting_1.png)

If you change the **Conditional formatting** to custom, when the value reaches the upper limit the cell will get greener. Wenn es jedoch den unteren Grenzwert erreicht, wird er erreicht.

For example, here, we set the **Upper limit** to 500 and **Lower limit** to 0.

![](assets/troubleshooting_2.png)