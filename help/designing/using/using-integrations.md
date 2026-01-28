---
title: Erstellen von E-Mails mit Adobe Campaign-Integrationen
description: Erfahren Sie, wie Sie in Email Designer E-Mails mithilfe von Adobe Campaign-Integrationen erstellen.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Intermediate
exl-id: d5c72f69-68a2-4523-956f-f265ae79b470
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: ht
source-wordcount: '706'
ht-degree: 100%

---

# E-Mail-Entwurf mit mehreren Lösungen {#multi-solution-email-design}

Adobe Campaign bietet mehrere Möglichkeiten zur Erstellung von E-Mails. So können Sie Lösungen wie Dreamweaver verwenden, um E-Mail-Inhalte zu bearbeiten und in Email Designer responsive Nachrichten zu erstellen. Außerdem können Sie Inhalte mit Adobe Experience Manager per E-Mail versenden und in Adobe Campaign Standard in Ihren E-Mails verwenden.

## Inhalt in Dreamweaver bearbeiten {#editing-content-in-dreamweaver}

Durch die Integration von Adobe Campaign Standard mit Dreamweaver kann E-Mail-Inhalt in der Benutzeroberfläche von Dreamweaver bearbeitet werden. Damit haben Sie Zugriff auf die leistungsstarken Optionen von Dreamweaver, um responsiven E-Mail-Content zu erstellen.

* **Bidirektionale Synchronisation**

  Wenn eine Änderung an einem Produkt vorgenommen wird, wird sie auch vom anderen in Echtzeit übernommen. Wenn Sie die Textfarbe in Dreamweaver verändern möchten, ist diese Änderung unmittelbar in Campaign zu sehen. Wenn Sie Code in Dreamweaver oder Campaign auswählen, ist diese Auswahl in diesen beiden Produkten identisch, da die Zeilennummern übereinstimmen. Dies ist sehr hilfreich, wenn Sie nach einer bestimmten Stelle im Code suchen.

* **Hochladen lokaler Bilder in Adobe Campaign über Dreamweaver**

  Bei der Erstellung oder Bearbeitung einer E-Mail in Dreamweaver können Sie einfach ein auf Ihrem Desktop oder lokalen PC ausgewähltes Bild verwenden. Dreamweaver hat schon immer diese Möglichkeit geboten. Jetzt wird aber die lokale Datei unmittelbar zum Adobe Campaign-Server hochgeladen, wenn Dreamweaver und Campaign verbunden sind, ohne dass Bilder manuell hochgeladen werden müssen, wenn sich der Inhalt ändert. Zusätzlich wird damit sichergestellt, dass immer die aktuellen Bilder in Campaign vorhanden sind.

* **Campaign-Personalisierung in Dreamweaver hinzufügen**

  E-Mail-Entwickler müssen jetzt nicht mehr Text wie `[[FIRSTNAME_PLACEHOLDER]]` hinzufügen und auch nicht die Syntax Ihrer Datenmodell-Tabellen nachsehen. Die Campaign-Symbolleiste in Dreamweaver stellt eine direkte Verbindung zum Datenmodell Ihrer Campaign-Instanz her. Das bedeutet, dass Sie beliebige Personalisierungsdaten von z. B. Vorname zu Adresse ziehen können. Auch direkt in Campaign erstellte Inhaltsbausteine können direkt zu Dreamweaver gezogen werden.

Diese Funktion wird im Detail im [Dreamweaver-Handbuch](https://helpx.adobe.com/de/dreamweaver/using/working-with-dreamweaver-and-campaign.html) beschrieben.

![](assets/do-not-localize/how-to-video.png) [Mehr zu dieser Funktion erfahren Sie im Video.](#video).

## Inhalt in Adobe Experience Manager bearbeiten {#editing-content-in-experience-manager}

Inhalte können in Experience Manager bearbeitet und danach für mehrere E-Mail-Nachrichten in Adobe Campaign Standard verwendet werden. In [diesem Dokument](../../integrating/using/integrating-with-experience-manager.md) erfahren Sie mehr dazu.

## Produktlisten {#product-listing}

>[!CONTEXTUALHELP]
>id="ac_product_listing"
>title="Verwenden von Produktlisten"
>abstract="Mit den Produktlisten können Sie auf eine Datenerfassung verweisen und sie im E-Mail-Inhalt anzeigen."

Mit Produktlisten können Sie auf eine oder mehrere Datenerfassungen im E-Mail-Inhalt verweisen. Diese Listen stehen für Transaktions-E-Mails zur Verfügung. Einen speziellen Abschnitt zu dieser Funktion finden Sie [hier](../../designing/using/using-product-listings.md).

## Funktionen zur E-Mail-Erstellung im Vergleich          {#email-design-options-comparison}

Adobe Campaign bietet mehrere Möglichkeiten zur Erstellung von E-Mails. In der folgenden Tabelle werden die wichtigsten Funktionen, Vorteile und Beschränkungen aufgeführt.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Email Designer<br /> </th> 
   <th> Experience Manager<br /> </th> 
   <th> Dreamweaver<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <strong>Neue E-Mail erstellen</strong><br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HTML schreiben</strong><br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Nicht unterstützt<br /> </td> 
   <td> Unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HTML aktualisieren</strong><br /> </td> 
   <td> Nur innerhalb einer HTML-Komponente<br /> </td> 
   <td> Nicht unterstützt<br /> </td> 
   <td> Unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Einfache Personalisierung</strong><br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Erweiterte Personalisierung</strong><br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Nicht unterstützt<br /> </td> 
   <td> Nicht unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Testversand/Vorschau</strong><br /> </td> 
   <td> Unterstützt<br /> </td> 
   <td> Vorschau in AEM<br /> Testversand in Campaign<br /> </td> 
   <td> Vorschau und Testversand in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Produktlisten</strong><br /> </td> 
   <td> In E-Mail-Transaktionsnachrichten unterstützt<br /> </td> 
   <td> Nicht unterstützt<br /> </td> 
   <td> Nicht unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Vorteile</strong><br /> </td> 
   <td> 
     <p>- Einfache Erstellung von E-Mails dank Drag &amp; Drop</p>
     <p>- Funktionen sind ähnlich dem alten Inhaltseditor</p>
     <p>- Wiederverwendbare Inhalte mit Fragmenten</p>
  </td> 
   <td> 
     <p>- Assets von Website können in E-Mails wiederverwendet werden</p>
     <p>- Nutzung der Funktionen von Experience Manager in E-Mail-Inhalten</p>
    </td> 
   <td> 
    <p>- Entwickler können selbst Code für eine E-Mail schreiben</p>
    <p>- Bidirektionale Synchronisation</p>
    <p>- In Dreamweaver offline bearbeiten und später synchronisieren</p>
    <p>- Bilder über Dreamweaver zu Adobe Campaign hochladen</p>
  </td> 
  </tr> 
  <tr> 
   <td> <strong>Einschränkungen</strong><br /> </td> 
   <td> 
     <p>- Kein bedingter Inhalt innerhalb von Fragmenten</p>
     <p>- Verwendung von Experience Manager-Fragmenten nicht möglich</p>
  </td> 
   <td> 
     <p>- Erweiterte Personalisierung schwierig zu implementieren</p>
     <p>- In Adobe Campaign müssen Tests gesendet werden</p>
  </td> 
   <td> Dynamische Inhalte nicht unterstützt<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Zielgruppe</strong><br /> </td> 
   <td> Marketing-Fachleute, die weiterhin die Flexibilität haben möchten, HTML-Komponenten in Kombination mit Drag-and-Drop-Funktionen zu verwenden<br /> </td> 
   <td> Marketer, die bereits Experience Manager verwenden und Standard-E-Mail-Vorlagen mit wenig Personalisierung verwenden möchten<br /> </td> 
   <td> Entwickler, die Code für E-Mail-Inhalte selbst schreiben möchten und eine direkte Integration mit Adobe Campaign wünschen<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Weitere Informationen</strong><br /> </td> 
   <td> Siehe auch <a href="../../designing/using/designing-content-in-adobe-campaign.md">Über Email Designer</a>.<br /> </td> 
   <td> Siehe auch <a href="../../integrating/using/integrating-with-experience-manager.md">Integration mit Experience Manager</a>.<br /> </td> 
   <td> Siehe auch <a href="https://helpx.adobe.com/de/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Dreamweaver und Campaign</a> und dieses <a href="#video">Video</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Anleitungsvideo {#video}

In diesem Video wird gezeigt, wie man Inhalte für Adobe Campaign Standard mit Dreamweaver erstellt und bearbeitet.

>[!VIDEO](https://video.tv.adobe.com/v/37503?quality=12&captions=ger)

Weitere Anleitungsvideos zu Campaign Standard finden Sie [hier](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=de).
