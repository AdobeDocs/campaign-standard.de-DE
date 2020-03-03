---
title: Best Practices für Datenmodelle in Adobe Campaign Standard
description: Erfahren Sie mehr über die Best Practices beim Entwerfen Ihres Adobe Campaign Standard-Datenmodells.
page-status-flag: never-activated
uuid: cacd563f-6936-4b3e-83e3-5d4ae31d44e8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 4e0468da-3052-4ce5-8174-45aba1f5c4ed
context-tags: cusResource,overview;eventCusResource,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d0aa1089ee744a86a95d344235feba7adb9150a4

---


# Best Practices zum Datenmodell{#data-model-best-practices}

In diesem Dokument werden die wichtigsten Empfehlungen beim Entwerfen Ihres Adobe Campaign-Datenmodells erläutert.


>[!NOTE]
>
>Informationen zum Erstellen und Ändern von Ressourcen zur Erweiterung des vordefinierten Adobe Campaign-Datenmodells finden Sie in [diesem Abschnitt](../../developing/using/key-steps-to-add-a-resource.md).
>
>You can find a data model representation of the out-of-the-box resources [here](../../developing/using/datamodel-introduction.md).

## Übersicht {#overview}

Das Adobe Campaign-System ist äußerst flexibel und kann über die ursprüngliche Implementierung hinaus erweitert werden. Obwohl die Möglichkeiten unbegrenzt sind, ist es wichtig, kluge Entscheidungen zu treffen und eine solide Grundlage für die Entwicklung Ihres Datenmodells zu schaffen.

Dieses Dokument enthält häufige Anwendungsfälle und Best Practices, um zu erfahren, wie Sie das Adobe Campaign-Tool ordnungsgemäß verwalten.

## Architektur von Datenmodellen {#data-model-architecture}

Adobe Campaign Standard ist ein leistungsfähiges kanalübergreifendes Kampagnenverwaltungssystem, das Sie bei der Abstimmung Ihrer Online- und Offlinestrategien unterstützen kann, um personalisierte Kundenerlebnisse zu erstellen.

### Kundenorientierter Ansatz {#customer-centric-approach}

Während die meisten E-Mail-Serviceanbieter Kunden über einen listenorientierten Ansatz kommunizieren, stützt sich Adobe Campaign auf eine relationale Datenbank, um eine umfassendere Ansicht der Kunden und ihrer Attribute zu nutzen.

Dieser kundenorientierte Ansatz wird im Diagramm unten dargestellt. Die **Profilressource** in Grau stellt die Hauptkundentabelle dar, um die alles erstellt wird:

![](assets/customer-centric-data-model.png)

Das Standarddatenmodell von Adobe Campaign wird in diesem [Abschnitt](../../developing/using/datamodel-introduction.md)dargestellt.

<!--You can find a datamodel representation for the out-of-the-box resources [here](../../developing/using/datamodel-introduction.md).-->

<!--### What is a customer? {#customer-definition}

If you have customer data in more than one system, you need to determine which solution will allow you to identify records as one person. This work might require rules, eventually a match and merge processes to determine the master record. This master record should be the one sent to Adobe Campaign.

While some of this data cleansing might be performed in Adobe Campaign, the recommendation is to run these processes outside and only import clean data in Adobe Campaign. You should keep Campaign as a marketing solution more than a data cleansing tool.

Be able to provide a master customer record which will be sent to Adobe Campaign.-->

### Daten für Adobe Campaign {#data-for-campaign}

Welche Daten sollten an Adobe Campaign gesendet werden? Die für Ihre Marketingaktivitäten erforderlichen Daten müssen unbedingt ermittelt werden.

>[!NOTE]
>
>Adobe Campaign ist kein Data Warehouse. Versuchen Sie daher nicht, alle möglichen Kunden und die damit verbundenen Informationen in Adobe Campaign zu importieren.

Um zu entscheiden, ob ein Attribut in Adobe Campaign erforderlich ist, stellen Sie fest, ob es in eine der folgenden Kategorien fallen würde:
* Für die **Segmentierung verwendetes Attribut**
* Für **Datenverwaltungsprozesse** verwendetes Attribut (z. B. aggregierte Berechnung)
* Für die **Personalisierung verwendetes Attribut**
* Für die **Berichterstellung** verwendetes Attribut (Berichte können auf der Grundlage von benutzerspezifischen Profildaten erstellt werden)

Wenn Sie nicht in eine dieser Kategorien fallen, benötigen Sie dieses Attribut wahrscheinlich nicht in Adobe Campaign.

### Datentypen {#data-types}

Um eine gute Architektur und Systemleistung sicherzustellen, befolgen Sie die folgenden Best Practices, um Daten in Adobe Campaign einzurichten:
* Die Länge eines Zeichenfolgenfelds sollte immer mit der Spalte definiert werden. Standardmäßig beträgt die maximale Länge in Adobe Campaign 255 Zeichen. Adobe empfiehlt jedoch, das Feld zu kürzen, wenn Sie bereits wissen, dass die Größe eine kürzere Länge nicht überschreitet.
* Es ist akzeptabel, dass ein Feld in Adobe Campaign kürzer ist als im Quellsystem, wenn Sie sicher sind, dass die Größe im Quellsystem überschätzt wurde und nicht erreicht wird. Dies könnte eine kürzere oder kleinere Ganzzahl in Adobe Campaign bedeuten.

## Konfigurieren der Datenstruktur {#configuring-data-structure}

In diesem Abschnitt werden Best Practices für die [Konfiguration der Datenstruktur](../../developing/using/configuring-the-resource-s-data-structure.md)einer Ressource beschrieben.

### Bezeichner {#identifiers}

Adobe Campaign-Ressourcen verfügen über drei IDs, und es ist möglich, einen zusätzlichen Bezeichner hinzuzufügen.

Die folgende Tabelle beschreibt diese Bezeichner und ihren Zweck.

>[!NOTE]
>
>Der Anzeigename ist der Name des Felds, das dem Benutzer über die Benutzeroberfläche von Adobe Campaign angezeigt wird. Der technische Name ist der tatsächliche Feldname in der Ressourcendefinition (und der Name der Tabellenspalte).

| Anzeigename | Technischer Name | Beschreibung | Best Practices |
|--- |--- |--- |--- |
|  | PKey | <ul><li>Der Schlüssel ist der physische Primärschlüssel einer Adobe Campaign-Tabelle.</li><li>Dieser Bezeichner ist in der Regel für eine bestimmte Adobe Campaign-Instanz eindeutig.</li><li>In Adobe Campaign Standard ist dieser Wert für den Endbenutzer nicht sichtbar.</li></ul> | <ul><li>Über das [API-System](../../api/using/about-campaign-standard-apis.md)ist es möglich, einen PKey-Wert abzurufen (ein generierter/Hash-Wert, nicht der physische Schlüssel).</li><li>Es wird nicht empfohlen, es für andere Zwecke zu verwenden, als Datensätze über API abzurufen, zu aktualisieren oder zu löschen.</li></ul> |
| ID | name oder internalName | <ul><li>Diese Informationen sind eine eindeutige Kennung eines Datensatzes in einer Tabelle. Dieser Wert kann manuell aktualisiert werden.</li><li>Dieser Bezeichner behält seinen Wert bei, wenn er in einer anderen Instanz von Adobe Campaign bereitgestellt wird. Es muss einen anderen Namen haben als der generierte Wert, der über ein Paket exportiert werden kann.</li><li>Dies ist nicht der eigentliche Primärschlüssel der Tabelle.</li></ul> | <ul><li>Verwenden Sie keine Sonderzeichen wie Leerzeichen &quot;&quot;, Halbspalte &quot;:&quot;oder Bindestrich &quot;-&quot;.</li><li>Alle diese Zeichen werden durch einen Unterstrich (_) ersetzt. Beispielsweise würden &quot;abc-def&quot;und &quot;abc:def&quot;als &quot;abc_def&quot;gespeichert und überschrieben.</li></ul> |
| Titel | label | <ul><li>Die Beschriftung ist die Geschäftskennung eines Objekts oder Datensatzes in Adobe Campaign.</li><li>Dieses Objekt erlaubt Leerzeichen und Sonderzeichen.</li><li>Sie garantiert nicht die Einzigartigkeit eines Datensatzes.</li></ul> | <ul><li>Es wird empfohlen, eine Struktur für die Objektbeschriftungen festzulegen.</li><li>Dies ist die benutzerfreundlichste Lösung zur Identifizierung eines Datensatzes oder Objekts für einen Adobe Campaign-Benutzer.</li></ul> |
| ACS-ID | acsId | <ul><li>Es kann eine zusätzliche ID generiert werden: die [ACS-ID](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).</li><li>Da der PKey nicht in der Benutzeroberfläche von Adobe Campaign verwendet werden kann, ist dies eine Lösung, um einen eindeutigen Wert zu erhalten, der beim Einfügen eines Profildatensatzes generiert wurde.</li><li>Der Wert kann nur dann automatisch generiert werden, wenn die Option in der Ressource aktiviert ist, bevor ein Datensatz in Adobe Campaign eingefügt wird.</li></ul> | <ul><li>Diese UUID kann als Abgleichschlüssel verwendet werden.</li><li>Eine automatisch generierte ACS-ID kann nicht als Referenz in einem Workflow oder in einer Paketdefinition verwendet werden.</li><li>Dieser Wert ist spezifisch für eine Adobe Campaign-Instanz.</li></ul> |

### Identifizierungsschlüssel {#keys}

Jede in Adobe Campaign erstellte Ressource muss über mindestens einen eindeutigen [Identifizierungsschlüssel](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)verfügen.

<!--Most organizations are importing records from external systems. While the physical key of a resource lies behind the PKey attribute, it is possible to determine a custom key in addition.

This custom key is the actual record primary key in the external system feeding Adobe Campaign.

When an out-of-the-box resource has both an internal auto-generated and an internal custom key, the internal key will be set as a unique index in the physical database table.-->

Beim Erstellen einer benutzerdefinierten Ressource stehen Ihnen zwei Optionen zur Verfügung:

* Eine Kombination aus automatisch generiertem Schlüssel und internem benutzerdefiniertem Schlüssel. Diese Option ist interessant, wenn Ihr Systemschlüssel ein Composite-Schlüssel oder keine Ganzzahl ist. Ganzzahlen bieten höhere Leistungen in großen Tabellen und in Verbindung mit anderen Tabellen.
* Verwendung des primären Schlüssels als Primärschlüssel des externen Systems. Diese Lösung wird in der Regel bevorzugt, da sie den Ansatz zum Importieren und Exportieren von Daten mit einem einheitlichen Schlüssel zwischen verschiedenen Systemen vereinfacht.

Identifizierungsschlüssel sollten nicht als Referenz in Workflows verwendet werden.

<!--For more on defining identification keys, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys).-->

### Indexe {#indexes}

Adobe Campaign fügt allen in einer Ressource definierten primären und internen Schlüsseln automatisch einen [Index](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes) hinzu.

* Adobe empfiehlt, zusätzliche Indizes zu definieren, da dies die Leistung verbessern kann.
* Fügen Sie jedoch nicht zu viele Indizes hinzu, da sie Speicherplatz in der Datenbank verwenden. Zahlreiche Indizes können sich auch negativ auf die Leistung auswirken.
* Wählen Sie die zu definierenden Indizes sorgfältig aus.

<!--For more on defining indexes, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes).

When you are performing an initial import with very high volumes of data insert in Adobe Campaign database, it is recommended to run that import without custom indexes at first. It will allow to accelerate the insertion process. Once you’ve completed this important import, it is possible to enable the index(es).-->

### Relationen {#links}

Die Definition von Links zu anderen Ressourcen wird in [diesem Abschnitt](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)erläutert.

* Obwohl es möglich ist, sich einer beliebigen Tabelle in einem Workflow anzuschließen, empfiehlt Adobe, allgemeine Links zwischen Ressourcen direkt in der Datenstrukturdefinition zu definieren.
* Der Link sollte entsprechend den tatsächlichen Daten in den Tabellen definiert werden. Eine falsche Definition könnte sich auf Daten auswirken, die über Links abgerufen wurden, z. B. auf eine unerwartete Duplizierung von Datensätzen.
* Benennen Sie den Link konsistent mit dem Namen der Ressource: der Linkname sollte dabei helfen zu verstehen, was die entfernte Tabelle ist.
* Benennen Sie einen Link nicht mit &quot;id&quot;als Suffix. Benennen Sie es beispielsweise &quot;transaction&quot;anstelle von &quot;transactionId&quot;.

<!--For more on defining links with other resources, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources).-->

## Leistung {#performance}

Um jederzeit eine bessere Leistung zu gewährleisten, befolgen Sie die folgenden Best Practices.

### Allgemeine Empfehlungen {#general-recommendations}

* Vermeiden Sie die Verwendung von Operationen wie &quot;CONTAINS&quot;in Abfragen. Wenn Sie wissen, worauf gefiltert werden soll, wenden Sie die gleiche Bedingung mit einem &quot;EQUAL TO&quot;oder anderen spezifischen Filteroperatoren an.
* Vermeiden Sie es, beim Erstellen von Daten in Workflows mit nicht indizierten Feldern zusammenzuarbeiten.
* Vergewissern Sie sich, dass Prozesse wie Import und Export von Geschäftszeiten ablaufen.
* Stellen Sie sicher, dass ein Zeitplan für alle täglichen Aktivitäten vorhanden ist und halten Sie sich an den Zeitplan.
* Wenn einer oder mehrere der täglichen Prozesse fehlschlagen und es obligatorisch ist, sie am selben Tag auszuführen, stellen Sie sicher, dass beim Starten des manuellen Prozesses keine Konflikte auftreten, da dies die Systemleistung beeinträchtigen könnte.
* Stellen Sie sicher, dass keine der täglichen Kampagnen während des Importvorgangs oder bei der Ausführung eines manuellen Prozesses ausgeführt wird.
* Verwenden Sie eine oder mehrere Referenztabellen, anstatt ein Feld in jeder Zeile zu duplizieren. Bei Verwendung von Schlüssel/Wert-Paaren ist es empfehlenswert, einen numerischen Schlüssel zu wählen.
* Eine kurze Zeichenfolge bleibt zulässig. Falls Referenztabellen bereits in einem externen System vorhanden sind, erleichtert die Wiederverwendung desselben die Datenintegration mit Adobe Campaign.

### 1-zu-n-Beziehungen {#one-to-many-relationships}

* Datendesign beeinflusst Benutzerfreundlichkeit und Funktionalität. Wenn Sie Ihr Datenmodell mit einer Vielzahl von 1-zu-n Beziehungen entwickeln, wird es für Benutzer schwieriger, aussagekräftige Logik in der Anwendung zu erstellen. Eine Eins-zu-viele-Filterlogik kann für nicht-technische Marketingexperten schwierig zu konstruieren und zu verstehen sein.
* Es ist gut, alle wichtigen Felder in einer Tabelle zu haben, da es für Benutzer einfacher ist, Abfragen zu erstellen. Manchmal ist es auch gut für die Leistung, einige Felder über Tabellen hinweg zu duplizieren, wenn eine Verknüpfung vermieden werden kann.
* Bestimmte integrierte Funktionen werden nicht in der Lage sein, auf 1-zu-viele Beziehungen zu verweisen, z. B. Angebotsgewichtungsformel und Lieferungen.

### Große Tabellen {#large-tables}

Im Folgenden finden Sie einige Best Practices, die beim Entwerfen Ihres Datenmodells mit großen Tabellen und komplexen Verbindungen befolgt werden sollten.

* Reduzieren Sie die Anzahl der Spalten, insbesondere durch Identifizieren der nicht verwendeten Spalten.
* Optimieren Sie die Datenmodellbeziehungen, indem Sie komplexe Verbindungen, wie z. B. Verbindungen mit mehreren Bedingungen und/oder Spalten, vermeiden.
* Verwenden Sie für Verbindungsschlüssel immer numerische Daten anstelle von Zeichenfolgen.
* Verringern Sie so viel wie möglich die Tiefe der Protokollbindung. Wenn Sie einen tieferen Verlauf benötigen, können Sie Berechnungen zusammenstellen und/oder benutzerspezifische Protokolltabellen bearbeiten, um einen größeren Verlauf zu speichern.