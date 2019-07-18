---
title: Abfrage
seo-title: Abfrage
description: Abfrage
seo-description: Eine Abfrage dient der Filterung und Extraktion einer Population, die sich aus Elementen der Adobe-Campaign-Datenbank zusammensetzt.
page-status-flag: nie aktiviert
uuid: b 3 c 629 fa -370 e -481 c-b 347-fcf 9 f 5 a 5 e 847
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: targeting-activities
discoiquuid: 8 d 46 ce 28-0101-4 f 13-865 a -2208 ed 6 d 6139
context-tags: query, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d50d486ed77cb7989df47133bb49fde3227ae3a5

---


# Abfrage{#query}

## Beschreibung {#description}

![](assets/query.png)

Eine **[!UICONTROL Abfrage]dient der Filterung und Extraktion einer Population, die sich aus Elementen der Adobe-Campaign-Datenbank zusammensetzt.** Mithilfe eines dedizierten Tabs können Sie **[!UICONTROL Zusatzdaten]für die Zielpopulation definieren.** Diese Daten werden in Zusatzspalten gespeichert und können ausschließlich für den laufenden Workflow verwendet werden.

Die Aktivität verwendet das Abfragetool, dessen Funktionsweise in einem [gesonderten Kapitel](../../automating/using/editing-queries.md#about-query-editor) behandelt wird.

## Anwendungskontext {#context-of-use}

**[!UICONTROL Abfragen]kommen in verschiedenen Kontexten zum Einsatz:**

* Segmentierung von Populationen, um beispielsweise Zielgruppen und Audiences zu definieren;
* Anreicherung von Daten beliebiger Adobe-Campaign-Tabellen;
* Export von Daten.

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Abfrage]in den Workflow-Arbeitsbereich.**
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions. ](assets/edit_darkgrey-24px.png) Die Standardkonfiguration der Aktivität sieht die Suche nach Profilen vor.
1. Wenn sich Ihre Abfrage auf eine andere als die Profil-Ressource beziehen soll, können Sie im **[!UICONTROL Eigenschaften]**-Tab der Aktivität die entsprechende **[!UICONTROL Ressource]** und eine **Zielgruppendimension[!UICONTROL auswählen]**.

   The **[!UICONTROL Resource]** allows you to refine the filters displayed in the palette whereas the **[!UICONTROL Targeting dimension]**, contextual with regard to the resource selected, corresponds to the type of population that you would like to obtain (identified profiles, deliveries, data linked to the selected resource, etc.).

   Lesen Sie diesbezüglich auch den Abschnitt [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).

1. Konfigurieren Sie im Tab **[!UICONTROL Zielgruppe]die Abfrage, indem Sie Regeln definieren und/oder kombinieren.**
1. Mithilfe eines dedizierten Tabs können Sie **[!UICONTROL Zusatzdaten]für die Zielpopulation definieren.** Diese Daten werden in Zusatzspalten gespeichert und können ausschließlich für den laufenden Workflow verwendet werden. Sie können insbesondere Daten aus Tabellen der Adobe-Campaign-Datenbank hinzufügen, die mit der Zielgruppendimension der Abfrage in Relation stehen. Lesen Sie diesbezüglich auch den Abschnitt [Daten anreichern](../../automating/using/query.md#enriching-data).

   >[!NOTE]
   >
   >Standardmäßig ist die Option **[!UICONTROL Dubletten löschen (DISTINCT)]** in **[!UICONTROL Erweiterte Optionen]des Tabs** Zusatzdaten] der Abfrage aktiviert. **[!UICONTROL ** Wenn die Aktivität **[!UICONTROL Abfrage]viele Zusatzdaten enthält (mehr als 100), ist es empfehlenswert, diese Option zur Leistungssteigerung zu deaktivieren.** Beachten Sie jedoch, dass durch die Deaktivierung dieser Option abhängig von den abgefragten Daten Dubletten entstehen können.

1. Im Tab **[!UICONTROL Transition]** können Sie mit der Option **Ausgehende Transition erzeugen]im Anschluss an eine Abfrageaktivität eine ausgehende Transition hinzufügen, selbst wenn keine Daten abgefragt werden.[!UICONTROL **

   Der Segmentcode der ausgehenden Transition kann mit einem Standardausdruck und Ereignisvariablen personalisiert werden (siehe [Aktivitäten mit Ereignisvariablen anpassen](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables)).

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Zielgruppendimensionen und Ressourcen {#targeting-dimensions-and-resources}

Mit Zielgruppendimensionen und Ressourcen können Sie definieren, auf welchen Elementen eine Abfrage basieren soll, um die Zielgruppe eines Versands zu bestimmen.

Zielgruppendimensionen werden in Zielgruppen-Mappings definiert. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/target-mappings-in-campaign.md).

### Zielgruppendimension und Ressource einer Abfrage definieren {#defining-the-targeting-dimension-and-resource-of-a-query}

Die Zielgruppendimension und die Ressourcen werden bei der Erstellung eines Workflows im Tab **[!UICONTROL Eigenschaften]der Abfrage-Aktivität definiert.**

>[!NOTE]
>
>Die Zielgruppendimension kann auch bei der Erstellung einer Audience definiert werden (siehe [diesen Abschnitt](../../audiences/using/creating-audiences.md)).

![](assets/targeting_dimension1.png)

Zielgruppendimensionen und Ressourcen sind miteinander verknüpft. Die verfügbaren Targeting-Dimensionen hängen daher von der ausgewählten Ressource ab.

For example, for the Resource **[!UICONTROL Profiles (profile)]**, the following targeting dimensions will be available:

![](assets/targeting_dimension2.png)

While for **[!UICONTROL Deliveries (delivery)]**, the list will contain the following targeting dimensions:

![](assets/targeting_dimension3.png)

Sobald die Zielgruppendimension und die Ressource festgelegt wurden, stehen in der Abfrage unterschiedliche Filter zur Verfügung.

Beispiel für verfügbare Filter für die Ressource **[!UICONTROL Profile (profile)]:**

![](assets/targeting_dimension4.png)

Beispiel für verfügbare Filter für die Ressource **[!UICONTROL Sendungen (delivery)]:**

![](assets/targeting_dimension5.png)

### Von den Zielgruppendimensionen abweichende Ressourcen verwenden {#using-resources-different-from-targeting-dimensions}

Normalerweise werden die Zielgruppendimension und die Ressource festgelegt, um Profile zu erfassen.

Manchmal kann es aber nötig sein, eine von der Zielgruppendimension abweichende Ressource zu verwenden, um einen bestimmten Datensatz in einer entfernten Tabelle zu suchen.

**Beispiel 1: Sie möchten Profile identifizieren, die im Versand mit dem Titel „Willkommen zurück!“ enthalten waren**.

* In diesem Fall möchten wir Profile erfassen. We will set the targeting dimension to **[!UICONTROL Profiles (profile)]**.
* Wir möchten die ausgewählten Profile nach dem Versandtitel filtern. Deshalb wählen wir für die Ressource **[!UICONTROL Versandlogs]**. Auf diese Weise filtern wir direkt in der Versandlog-Tabelle, wodurch die Ausführung beschleunigt wird.

![](assets/targeting_dimension6.png)

![](assets/targeting_dimension7.png)

**Beispiel 2: Sie möchten Profile identifizieren, die nicht im Versand mit dem Titel "Willkommen zurück!" enthalten waren.**

Im vorherigen Beispiel haben wir eine von der Zielgruppendimension abweichende Ressource verwendet. Dieses Vorgehen ist nur möglich, wenn Sie einen Datensatz suchen, der in der entfernten Tabelle vorhanden ist (in unserem Beispiel Versandlogs).****

Wenn wir einen Datensatz suchen, der in der entfernten Tabelle **nicht vorhanden** ist (z. B. Profile, die nicht in einem bestimmten Versand enthalten waren), müssen wir dieselbe Ressource und Zielgruppendimension verwenden, da der Datensatz nicht in der entfernten Tabelle (Versandlogs) vorhanden ist.

* In diesem Fall möchten wir Profile erfassen. We will set the targeting dimension to **[!UICONTROL Profiles (profile)]**.
* Wir möchten die ausgewählten Profile nach dem Versandtitel filtern. Es ist nicht möglich, direkt nach Versandlogs zu filtern, da wir nach einem Datensatz suchen, der nicht in der Versandlog-Tabelle vorhanden ist. Deshalb wählen wir für die Ressource **[!UICONTROL Profil (profile)]und erstellen unsere Abfrage auf der Basis der Profiltabelle.**

![](assets/targeting_dimension8.png)

![](assets/targeting_dimension9.png)

## Daten anreichern {#enriching-data}

The **[!UICONTROL Additional data]** tab of the **[!UICONTROL Query]**, **[!UICONTROL Incremental query]** and **[!UICONTROL Enrichment]** activities allows you to enrich the data targeted and transfer this data to the following workflow activities, where it can be utilized. Insbesondere die folgenden Elemente lassen sich hinzufügen:

* einfache Daten,
* Aggregate
* Kollektionen.

Im Fall von Aggregaten und Kollektionen wird automatisch ein **[!UICONTROL Alias]definiert, um komplexen Ausdrücken eine technische Kennung zuzuweisen.** Dieser Alias, der eindeutig sein muss, erlaubt es, Aggregate und Kollektionen leicht zu finden. Sie können den automatisch erzeugten Alias so anpassen, dass Sie ihm einen leicht wiederzuerkennenden Namen verleihen.

>[!NOTE]
>
>Alias müssen folgende Syntax befolgen: Nur alphanumerische Zeichen und "_" sind zulässig. Alias beachten Groß- und Kleinschreibung. Alias müssen mit dem Zeichen "@" beginnen. Das direkt auf "@" folgende Zeichen darf keine Ziffer sein. Beispiel: @myAlias_1 und @_1Alias sind korrekt; @myAlias#1 und @1Alias sind falsch.

Nach dem Hinzufügen von Zusatzdaten können Sie die zunächst von der Abfrage ausgegebenen Daten weiter einschränken, indem Sie auf Basis der definierten Zusatzdaten Bedingungen erstellen.

>[!NOTE]
>
>Standardmäßig ist die Option **[!UICONTROL Dubletten löschen (DISTINCT)]** in **[!UICONTROL Erweiterte Optionen]des Tabs** Zusatzdaten] der Abfrage aktiviert. **[!UICONTROL ** Wenn die Aktivität **[!UICONTROL Abfrage]viele Zusatzdaten enthält (mehr als 100), ist es empfehlenswert, diese Option zur Leistungssteigerung zu deaktivieren.** Beachten Sie jedoch, dass durch die Deaktivierung dieser Option abhängig von den abgefragten Daten Dubletten entstehen können.

### Einfaches Feld hinzufügen {#adding-a-simple-field}

Das Hinzufügen eines einfachen Felds als Zusatzdatenelement macht ersteres direkt in der ausgehenden Transition der Aktivität sichtbar. Dadurch lässt sich beispielsweise überprüfen, ob die aus der Abfrage hervorgehenden Daten Ihren Vorstellungen entsprechen.

1. Gehen Sie in den Tab **[!UICONTROL Zusatzdaten]und fügen Sie ein neues Element hinzu.**
1. Wählen Sie im sich öffnenden Fenster im Feld **[!UICONTROL Ausdruck]ein Feld aus der Zielgruppendimension oder aus einer mit der Zielgruppendimension in Relation stehenden Dimension aus.** Sie haben die Möglichkeit, auf Felder der Dimension bezogene Ausdrücke zu bearbeiten und Funktionen anzuwenden oder einfache Berechnungen (außer Aggregate) vorzunehmen.

   Ein **[!UICONTROL Alias]wird automatisch erstellt, wenn Sie einen Ausdruck bearbeiten, der kein einfacher XPATH ist (zum Beispiel: "Year(&lt;@birthDate&gt;)").** Dieser kann bei Bedarf angepasst werden. Wenn Sie nur ein Feld (z. B. "@age") wählen, ist es nicht erforderlich, einen **[!UICONTROL Alias zu definieren]**.

1. Verwenden Sie die Schaltfläche **[!UICONTROL Hinzufügen], um die Hinzufügung des Felds zu den Zusatzdaten zu validieren.** Im Zuge der Abfragenausführung wird in der ausgehenden Transition der Aktivität eine dem hinzugefügten Feld entsprechende zusätzliche Spalte angezeigt.

![](assets/enrichment_add_simple_field.png)

### Aggregat hinzufügen {#adding-an-aggregate}

Aggregate dienen der Berechnung von Werten, die auf Feldern der Zielgruppendimension oder auf Feldern aus mit der Zielgruppendimension in Relation stehenden Dimensionen basieren. Zum Beispiel: der Durchschnitt der von einem Profil erteilten Bestellungen.

1. Gehen Sie in den Tab **[!UICONTROL Zusatzdaten]und fügen Sie ein neues Element hinzu.**
1. Wählen Sie im sich öffnenden Fenster im Feld **[!UICONTROL Ausdruck]die Kollektion aus, die Sie zur Aggregaterstellung verwenden möchten.**

   Es wird automatisch ein **[!UICONTROL Alias]erzeugt.** Dieser kann bei Bedarf im **[!UICONTROL Zusatzdaten]-Tab der Abfrage angepasst werden.**

   Das Fenster zur Aggregatdefinition öffnet sich.

1. Definieren Sie im **[!UICONTROL Daten]-Tab ein Aggregat.** Je nach ausgewähltem Aggregat sind im Feld **[!UICONTROL Ausdruck]lediglich die Elemente verfügbar, deren Datentyp kompatibel ist.** Beispielsweise lässt sich eine Summe ausschließlich mit numerischen Daten berechnen.

   ![](assets/enrichment_add_aggregate.png)

   Es besteht die Möglichkeit, mehrere, sich auf Felder der ausgewählten Kollektion beziehende Aggregate hinzuzufügen. Stellen Sie sicher, dass die vergebenen Titel eine korrekte Unterscheidung der verschiedenen Spalten in der Detailansicht der Daten in der ausgehenden Transition ermöglichen.

   Es besteht außerdem die Möglichkeit, die automatisch für jedes Aggregat erzeugten Alias anzupassen.

   ![](assets/enrichment_add_aggregate2.png)

1. Bei Bedarf können Sie einen Filter hinzufügen, um die zu berücksichtigenden Daten zu begrenzen.

   Lesen Sie diesbezüglich auch den Abschnitt [Hinzugefügte Daten filtern](../../automating/using/query.md#filtering-added-data).

1. **[!UICONTROL Validieren]Sie die Aggregaterstellung mithilfe der entsprechenden Schaltfläche.**

>[!NOTE]
>
>Die Erstellung eines ein Aggregat enthaltenden Ausdrucks kann nicht direkt über das Feld **[!UICONTROL Ausdruck]** im Fenster **Neue Zusatzdaten]vorgenommen werden.[!UICONTROL **

### Kollektion hinzufügen {#adding-a-collection}

1. Gehen Sie in den Tab **[!UICONTROL Zusatzdaten]und fügen Sie ein neues Element hinzu.**
1. Wählen Sie im sich öffnenden Fenster im Feld **[!UICONTROL Ausdruck]die Kollektion aus, die Sie hinzufügen möchten.** Es wird automatisch ein **[!UICONTROL Alias]erzeugt.** Dieser kann bei Bedarf im **[!UICONTROL Zusatzdaten]-Tab der Abfrage angepasst werden.**
1. Bestätigen Sie die Angaben mithilfe der **[!UICONTROL Hinzufügen-Schaltfläche]**. Im sich öffnenden Fenster haben Sie die Möglichkeit, die Kollektionsdaten, die Sie anzeigen möchten, zu verfeinern.
1. Wählen Sie im **[!UICONTROL Parameter]**-Tab die Option **[!UICONTROL Kollektion]aus und definieren Sie die Anzahl an Kollektionszeilen, die hinzugefügt werden sollen. Wenn Sie beispielsweise für jedes Profil die letzten drei Bestellungen abfragen möchten, müssen Sie im Feld** Anzahl an auszugebenden Zeilen] die Ziffer "3" angeben.**[!UICONTROL **

   >[!NOTE]
   >
   >Nur Ziffern größer oder gleich 1 sind zulässig.

1. Definieren Sie im **[!UICONTROL Daten]-Tab für jede Zeile die Felder der Kollektion, die angezeigt werden sollen.**

   ![](assets/enrichment_add_collection.png)

1. Bei Bedarf können Sie einen Filter hinzufügen, um die zu berücksichtigenden Zeilen der Kollektion zu begrenzen.

   Lesen Sie diesbezüglich auch den Abschnitt [Hinzugefügte Daten filtern](../../automating/using/query.md#filtering-added-data).

1. Bei Bedarf können Sie eine Sortierung für die Daten definieren.

   Wenn Sie beispielsweise im **[!UICONTROL Parameter]-Tab angegeben haben, dass drei Zeilen ausgegeben werden sollen, und Sie die drei neuesten Bestellungen abfragen möchten, können Sie eine Sortierung in absteigender Reihenfolge für das Datumsfeld ("date") der den Transaktionen entsprechenden Kollektion definieren.**

1. Lesen Sie diesbezüglich auch den Abschnitt [Hinzugefügte Daten sortieren](../../automating/using/query.md#sorting-additional-data).
1. **[!UICONTROL Validieren]Sie die Kollektionserstellung mithilfe der entsprechenden Schaltfläche.**

### Hinzugefügte Daten filtern {#filtering-added-data}

Beim Hinzufügen von Aggregaten oder Kollektionen besteht die Möglichkeit, einen zusätzlichen Filter zu bestimmen, um die Daten, die Sie angezeigt bekommen wollen, zu begrenzen.

Wenn Sie beispielsweise nur die Zeilen einer Transaktionskollektion abrufen möchten, bei denen der Transaktionsbetrag 50 Euro übersteigt, können Sie im **[!UICONTROL Filter]-Tab für das dem Transaktionsbetrag entsprechende Feld eine Bedingung hinzufügen.**

![](assets/enrichment_filter_data.png)

### Hinzugefügte Daten sortieren {#sorting-additional-data}

Beim Hinzufügen von Aggregaten oder Kollektionen zu Daten einer Abfrage können Sie angeben, ob Sie einen Filter - in auf- bzw. absteigender Reihenfolge - anwenden möchten, der auf dem Wert des Feldes oder des definierten Ausdrucks basiert.

Wenn Sie beispielsweise für ein Profil nur die neueste Transaktion beibehalten möchten, müssen Sie im **[!UICONTROL Parameter]**-Tab im Feld **[!UICONTROL Anzahl an auszugebenden Zeilen]die Ziffer "1" angeben und mithilfe des** Sortierung]-Tabs das dem Transaktionsdatum entsprechende Feld in absteigender Reihenfolge sortieren.**[!UICONTROL **

![](assets/enrichment_sort_data.png)

### Abgefragte Daten unter Verwendung von Zusatzdaten filtern {#filtering-the-targeted-data-according-to-additional-data}

Im Zuge der Verwendung von Zusatzdaten erscheint in der **[!UICONTROL Abfrage]** ein neuer Tab namens **[!UICONTROL Ergebnis verfeinern]**. Dieser Tab ermöglicht es Ihnen, die im **[!UICONTROL Zielgruppe]-Tab enthaltenen ursprünglichen Abfrageergebnisse unter Verwendung der Zusatzdaten weiter einzuschränken.**

For example, if you have targeted all of the profiles that carried out at least one transaction and an aggregate calculating the average transaction amount carried out for each profile was added to the **[!UICONTROL Additional data]**, you can refine the population initially calculated using this average.

Fügen Sie hierzu im Tab **[!UICONTROL Ergebnis verfeinern]eine die Zusatzdaten betreffende Bedingung hinzu.**

![](assets/enrichment_output_filtering2.png)

![](assets/enrichment_output_filtering.png)

### Beispiel: E-Mail mit Zusatzdaten personalisieren {#example--personalizing-an-email-with-additional-data}

Das folgende Beispiel zeigt die Hinzufügung verschiedener Zusatzdatentypen zu einer Abfrage und die Verwendung von Zusatzdaten in Form von Personalisierungsfeldern in einer E-Mail.

Für dieses Beispiel werden diverse [benutzerdefinierte Ressourcen](../../developing/using/data-model-concepts.md) verwendet:

* Die **Profil**-Ressource wurde erweitert, um ein Feld hinzuzufügen, das die Speicherung von Treuepunkten für jedes Profil ermöglicht.
* Eine **Transaktionen**-Ressource wurde erstellt. Sie enthält alle von den in der Datenbank enthaltenen Profilen getätigten Bestellungen. Für jede Transaktion wird ihr Datum, der bestellte Artikel und sein Preis gespeichert.
* Eine **Artikel**-Ressource wurde erstellt. Sie enthält alle zum Verkauf stehenden Artikel.

Ziel ist es, eine E-Mail an all jene Profile zu senden, für die mindestens eine Transaktion gespeichert wurde. In dieser E-Mail werden den Kunden die letzte von ihnen getätigte Transaktion sowie diverse Informationen zu allen bisher erfolgten Transaktionen in Erinnerung gerufen: Anzahl an bestellten Artikeln, Gesamtbetrag, Anzahl an bereits gesammelten Treuepunkten.

Der Workflow stellt sich folgendermaßen dar:

![](assets/enrichment_example1.png)

1. Ziehen Sie eine **[!UICONTROL Abfrage]in den Arbeitsbereich, um alle Profile abzurufen, die mindestens eine Transaktion getätigt haben.**

   ![](assets/enrichment_example2.png)

   Definieren Sie im **[!UICONTROL Zusatzdaten]-Tab der Abfrage die verschiedenen Daten, die in der E-Mail angezeigt werden sollen:**

   * Treuepunkte anhand eines einfachen Felds aus der Dimension **Profile.** Lesen Sie diesbezüglich auch den Abschnitt [Einfaches Feld hinzufügen](../../automating/using/query.md#adding-a-simple-field).
   * Die Anzahl an bestellten Artikeln und der Gesamtbetrag anhand von zwei auf der Transaktionskollektion basierenden Aggregaten. Fügen Sie letztere im **[!UICONTROL Daten]**-Tab des Fensters zur Aggregatkonfiguration hinzu (Aggregate **Count** und **Sum**). Lesen Sie diesbezüglich auch den Abschnitt [Aggregat hinzufügen](../../automating/using/query.md#adding-an-aggregate).
   * Betrag, Datum und Artikel der letzten Transaktion, die anhand einer Kollektion ermittelt werden.

      Fügen Sie hierzu im **[!UICONTROL Daten]-Tab des Fensters zur Kollektionskonfiguration die verschiedenen anzuzeigenden Felder hinzu.**

      Damit nur die neueste Transaktion ausgegeben wird, ist im Feld **[!UICONTROL Anzahl an auszugebenden Zeilen]** die Ziffer "1" anzugeben und das Kollektionsfeld **Datum** im **Sortierung]-Tab in absteigender Reihenfolge zu sortieren.[!UICONTROL **

      Lesen Sie diesbezüglich auch die Abschnitte [Kollektion hinzufügen](../../automating/using/query.md#adding-a-collection) und [Hinzugefügte Daten sortieren](../../automating/using/query.md#sorting-additional-data).
   ![](assets/enrichment_example4.png)

   Wenn Sie prüfen möchten, ob die Daten korrekt in der ausgehenden Transition der Aktivität übermittelt werden, starten Sie den Workflow an dieser Stelle (bevor Sie die **[!UICONTROL E-Mail-Versand]-Aktivität anschließen) und öffnen Sie die aus der Abfrage ausgehende Transition.**

   ![](assets/enrichment_example5.png)

1. Schließen Sie nun einen **[!UICONTROL E-Mail-Versand]an.** Verwenden Sie im E-Mail-Inhalt die Personalisierungsfelder, die den in der Abfrage berechneten Daten entsprechen. Folgen Sie hierzu im Explorer der Personalisierungsfelder der Relation **[!UICONTROL Zusatzdaten (targetData)].**

   ![](assets/enrichment_example3.png)

Ihr Workflow kann nun ausgeführt werden. Die mithilfe der Abfrage abgerufenen Profile erhalten eine personalisierte E-Mail mit den ihren Transaktionen entsprechenden Daten.

## Beispiele für Abfragen {#query-samples}

### Abfrage nach einfachen Profilattributen {#targeting-on-simple-profile-attributes}

Das folgende Beispiel zeigt eine Abfrage von Männern zwischen 18 und 30 Jahren, die in London leben.

![](assets/query_sample_1.png)

### Abfrage nach E-Mail-Attributen {#targeting-on-email-attributes}

Das folgende Beispiel zeigt eine Abfrage von Profilen, deren E-Mail-Adressen-Domain "orange.co.uk" lautet.

![](assets/query_sample_emaildomain.png)

Das folgende Beispiel zeigt eine Abfrage von Profilen, deren E-Mail-Adresse vorhanden ist.

![](assets/query_sample_emailnotempty.png)

### Abfrage von Profilen, deren Geburtstag heute ist {#targeting-profiles-whose-birthday-is-today}

Das folgende Beispiel zeigt eine Abfrage von Profilen, deren Geburtstag heute ist.

1. Ziehen Sie den Filter **[!UICONTROL Geburtstag]in Ihre Abfrage.**

   ![](assets/query_sample_birthday.png)

1. Wählen Sie für den **[!UICONTROL Filtertyp]** die Option **[!UICONTROL Relativ]** und danach **Heute[!UICONTROL aus]**.

   ![](assets/query_sample_birthday2.png)

### Abfrage von Profilen, die einen bestimmten Versand geöffnet haben {#targeting-profiles-who-opened-a-specific-delivery}

Das folgende Beispiel zeigt eine Abfrage von Profilen, die den Versand mit dem Titel "Sommerzeit" geöffnet haben.

1. Ziehen Sie den Filter **[!UICONTROL Geöffnet]in Ihre Abfrage.**

   ![](assets/query_sample_opened.png)

1. Wählen Sie den entsprechenden Versand aus und danach **[!UICONTROL Bestätigen]**.

   ![](assets/query_sample_opened2.png)

### Abfrage von Profilen, für die Sendungen aus einem bestimmten Grund fehlgeschlagen sind {#targeting-profiles-for-whom-deliveries-failed-for-a-specific-reason}

Das folgende Beispiel zeigt eine Abfrage von Profilen, für die Sendungen fehlgeschlagen sind, weil ihr Posteingang voll war. Diese Abfrage steht nur Benutzern mit Administratorrechten zur Verfügung, die den Organisationseinheiten **[!UICONTROL Alle (all)]** angehören (siehe [diesen Abschnitt](../../administration/using/organizational-units.md)).

1. Wählen Sie die Ressource **[!UICONTROL Versandlogs]** aus, um Filter direkt in der Versandlogtabelle zu verwenden (siehe [Von den Zielgruppendimensionen abweichende Ressourcen verwenden](../../automating/using/query.md#using-resources-different-from-targeting-dimensions)).

   ![](assets/query_sample_failure1.png)

1. Ziehen Sie den Filter **[!UICONTROL Art des Fehlschlagens]in Ihre Abfrage.**

   ![](assets/query_sample_failure2.png)

1. Wählen Sie den entsprechenden Fehlertyp aus. In unserem Fall ist das **[!UICONTROL Postfach voll]**.

   ![](assets/query_sample_failure3.png)

### Abfrage von Profilen, die in den letzten sieben Tagen nicht kontaktiert wurden {#targeting-profiles-not-contacted-during-the-last-7-days}

Das folgende Beispiel zeigt eine Abfrage von Profilen, die in den letzten sieben Tagen nicht kontaktiert wurden.

1. Ziehen Sie den Filter **[!UICONTROL Versandlogs (logs)]in Ihre Abfrage.**

   ![](assets/query_sample_7days.png)

   Wählen Sie in der Dropdown-Liste die Option **[!UICONTROL Existiert nicht]** aus und ziehen Sie danach den Filter **Versand]in Ihre Abfrage.[!UICONTROL **

   ![](assets/query_sample_7days1.png)

1. Konfigurieren Sie den Filter wie unten beschrieben.

   ![](assets/query_sample_7days2.png)

### Abfrage von Profilen, die einen bestimmten Link angeklickt haben {#targeting-profiles-who-clicked-a-specific-link-}

1. Ziehen Sie den Filter **[!UICONTROL Trackinglogs (tracking)]in Ihre Abfrage.**

   ![](assets/query_sample_trackinglogs.png)

1. Ziehen Sie den Filter **[!UICONTROL Titel (urlLabel)]in Ihre Abfrage.**

   ![](assets/query_sample_trackinglogs2.png)

1. Geben Sie im Feld **[!UICONTROL Wert]den Titel ein, der beim Einfügen des Links in den Versand definiert wurde. Bestätigen Sie danach Ihre Eingabe.**

   ![](assets/query_sample_trackinglogs3.png)

