---
title: Änderungen an Datenmodellen verfolgen
description: Hier erfahren Sie, wie Sie eine Diagnose des Adobe Campaign-Datenmodells erstellen können.
audience: developing
content-type: reference
topic-tags: about-custom-resources
feature: Data Model
role: Developer
level: Experienced
exl-id: ced9a897-47e9-4128-84fb-35660c553cd4
TQID: https://experienceleague.adobe.com/XWMP0LlTRgqEJujGETPzVXOCUvkm-Q9OXC-RvaWd-58
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 100%

---

# Änderungen an Datenmodellen verfolgen{#monitoring-data-model-changes}

Im Menü **[!UICONTROL Diagnose]** können Sie die von der Anwendung erzeugten technischen Objekte sehen und analysieren.

>[!NOTE]
>
>Die Bildschirme dieses Menüs sind schreibgeschützt.

![](assets/diagnostic.png)

Folgende Objekte sind sichtbar:

* Datenschemata
* Webseiten
* Filter
* Navigation
* Komponenten
* Batch-Aufträge

Sie können die Listenkonfiguration ändern:

* Sie können Spalten hinzufügen und entfernen.
* Sie können Spaltennamen definieren.
* Sie können die Anzeigereihenfolge der Spalten in der Liste festlegen.
* Sie können die Sortierreihenfolge der Werte in der Liste auswählen.

Sie können die Liste filtern:

* Sie können native Datenschemata, Webseiten, Filter und Navigationsobjekte ein- oder ausschließen.
* Sie können Objekte nach ihrem Namen suchen.
* Sie können Batch-Aufträge nach Status, Startdatum und Enddatum filtern.

Sie können die angezeigte Liste in einer Datei im TXT-Format mit durch Komma getrennten Werten herunterladen.

Sie können die Details des ausgewählten Objekts anzeigen.

Beispielsweise können Sie diese Funktion verwenden, um die Filterkriterien von nativen Filtern anzuzeigen. Dieses Beispiel zeigt den Code, der für die Filterkriterien eines nativen Filters angezeigt wird:

```xml
<where displayFilter="Has clicked an offer">
  <condition boolOperator="AND" enabledIf="$(offer) != ''" expr="trackingLog" internalId="1" setOperator="EXISTS">
    <condition boolOperator="AND" expr="[url/offer] = $RestKey(offer)" internalId="2"/>
    <condition boolOperator="AND" expr="[@url-id] != 1" internalId="3"/>
  </condition>
</where>
```

![](assets/diagnosis_filter_criteria.png)