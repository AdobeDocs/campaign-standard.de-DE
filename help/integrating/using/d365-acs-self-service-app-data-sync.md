---
title: Daten zwischen Kampagne und Microsoft Dynamics synchronisieren
description: Daten zwischen Kampagne und Dynamik synchronisieren
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: 6be7a20cde8fcaee73972b8919765ea631f2f1ee
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---


# Daten synchronisieren

Sie können Tabellen von Microsoft Dynamics 365 mit Kampagne- und Kampagne-Marketingmetriken zu Microsoft Dynamics 365 synchronisieren. Die Synchronisierung wird über drei dedizierte Technischen Workflows durchgeführt: **[!UICONTROL Microsoft Dynamics 365 zu Kampagne]**, **[!UICONTROL Kampagne zu Microsoft Dynamics 365]**, **[!UICONTROL Opt-In/Out]**. Lesen Sie diesen Abschnitt zu [Weitere Informationen](../../integrating/using/d365-acs-self-service-app-workflows.md).

>[!IMPORTANT]
>Sie müssen den Arbeitsablauf **[!UICONTROL Microsoft Dynamics 365 an Kampagne]** anhalten/Beginn haben, damit Ihre Änderungen berücksichtigt werden. [Mehr dazu](../../integrating/using/d365-acs-self-service-app-workflows.md)


## Tabellen von Microsoft Dynamics 365 zur Kampagne zuordnen

Die Seite **[!UICONTROL Microsoft Dynamics 365 to Kampagne]** zeigt eine Liste von Entitäten in Microsoft Dynamics 365 und die benutzerdefinierten Ressourcen in Adobe Campaign, mit denen sie synchronisiert werden. Sie können neue Zuordnungen hinzufügen, vorhandene Zuordnungen bearbeiten oder löschen.

![](assets/d365-to-acs-ui-page-ingress-top.png)

In der folgenden Tabelle sind die einzelnen Spalten beschrieben:

* **[!UICONTROL MICROSOFT DYNAMICS 365 TABELLE]**: Diese Spalte gibt an, welche Entität in Microsoft Dynamics 365 die Datenquelle für die Zuordnung sein wird.

* **[!UICONTROL KAMPAGNE TABELLE]**: Diese Spalte gibt an, welche Ressource in Adobe Campaign das Ziel der Daten für die Zuordnung sein wird.

* **[!UICONTROL AKTIONEN]**: Folgende mögliche Aktionen sind aufgeführt:

   * Klicken Sie auf das Symbol **[!UICONTROL Bearbeiten]**, um diese Zuordnung zu bearbeiten.

   * Verwenden Sie das Symbol **[!UICONTROL Löschen]**, um eine Tabellenzuordnung zu löschen.

   * Klicken Sie auf das Symbol **[!UICONTROL Daten erneut abspielen]**, um alle Daten in der Tabelle Microsoft Dynamics 365 erneut zu synchronisieren. Normalerweise synchronisiert die Integrationsanwendung nur die Daten in Microsoft Dynamics 365, die kürzlich geändert wurden.  In einigen Fällen (z. B. wenn Sie eine Änderung vorgenommen oder einen Fehler begangen haben) möchten Sie jedoch möglicherweise, dass alle Daten erneut synchronisiert werden.  In diesen Fällen klicken Sie auf diese Schaltfläche und beim nächsten Beenden/Beginn des Arbeitsablaufs **[!UICONTROL Microsoft Dynamics 365 zu Kampagne]** werden Ihre Daten zu synchronisieren Beginn.

      Wenn Sie auf die Schaltfläche **[!UICONTROL Daten erneut abspielen]** klicken und die Prüfungen erfolgreich sind, wird das Symbol deaktiviert: Es zeigt an, dass die Daten für dieses Tabellenzuordnungspaar mit der nächsten Ausführung des Arbeitsablaufs **[!UICONTROL Microsoft Dynamics 365 zu Kampagne]** erneut synchronisiert werden.

      Sie können die Daten nicht erneut abspielen, wenn die folgenden Werte zutreffen:

      * Wenn die Backlog-Metrik 2.000.000 (oder mehr) Elemente enthält, die mit dem Arbeitsablauf **[!UICONTROL Microsoft Dynamics 365 zu Kampagne]** verknüpft sind (angezeigt auf der Seite **[!UICONTROL Workflows]**)
      * Wenn in der Tabelle Microsoft Dynamics 365 2.000.000 oder mehr Datensätze vorhanden sind

      Die Anzahl der Datensätze, die neu synchronisiert werden müssen, ist unterschiedlich. Wenn Sie eine große Anzahl von Datensätzen haben, kann es einige Zeit dauern, den Synchronisierungsprozess abzuschließen. Lesen Sie die Metrik **[!UICONTROL Backlog]** auf der Seite **[!UICONTROL Workflows]**, während die Integrationsanwendung den Synchronisierungsprozess abschließt.

      >[!IMPORTANT]
      >
      > Es wird dringend empfohlen, den Integrationsarbeitsablauf zu beenden, wenn Änderungen an Adobe Campaign Standard oder Microsoft Dynamics 365 veröffentlicht werden. Zu den anwendbaren Änderungen gehören: Aktualisierungen von Ressourcen/Entitäten (und den zugehörigen Feldern), Links, Identifizierungsspalten usw. die derzeit von der Integration verwendet werden.




## Neues Mapping erstellen {#add-a-new-mapping}

Gehen Sie wie folgt vor, um eine neue Zuordnung zu erstellen:

1. Klicken Sie auf der Seite **[!UICONTROL Microsoft Dynamics 365 to Kampagne]** auf die Schaltfläche **[!UICONTROL Hinzufügen Neue Zuordnung]**.

1. Verwenden Sie die Dropdown-Listen, um Microsoft Dynamics 365 und Kampagne Tabellen für die Zuordnung auszuwählen.
Die meisten anderen Eingaben auf der Seite hängen davon ab, welche Tabellen Sie auswählen.

   ![](assets/d365-to-acs-ui-page-ingress-choose-tables.png)

   >[!NOTE]
   >Sie können die einzelnen Tabellen nicht mehr als einmal zuordnen. Daher werden Sie bemerken, dass die Dropdownauswahl keine Tabellen enthält, die bereits zugeordnet wurden.

1. Klicken Sie zur Bestätigung auf **[!UICONTROL OK]**: Die Anwendung benötigt einen kurzen Moment, um die mit den ausgewählten Tabellen verknüpften Feldinformationen zu lesen.

Anschließend können Sie mit der Zuordnungskonfiguration fortfahren. [Mehr dazu](#new-mapping-settings)

>[!IMPORTANT]
>
>Sie können die Tabellen auf dieser Seite nur auswählen, wenn Sie die Zuordnung zum ersten Mal hinzufügen. Vergewissern Sie sich, dass Sie die richtigen Tabellen ausgewählt haben, bevor Sie auf die Schaltfläche **[!UICONTROL Speichern]** klicken: Nach dem Speichern sind die Tabellenauswahlfelder **schreibgeschützt**.

### Bearbeiten einer vorhandenen Zuordnung

Wenn Sie eine vorhandene Zuordnung bearbeiten, sehen Sie, dass die Tabellenauswahl nicht bearbeitbar ist.

![](assets/d365-to-acs-ui-page-ingress-table-read-only.png)

Dies geschieht standardmäßig, weil die weiter unten auf der Seite angezeigten Eingaben auf den mit diesen Tabellen verknüpften Feldern basieren. Wenn Sie die Tabellen ändern, sind alle mit diesen Tabellen verknüpften Felder ungültig.  Wenn Sie die Tabelle ändern möchten, der Sie zuordnen möchten, müssen Sie zur vorherigen Seite zurückkehren, die zu ändernde Zuordnung löschen und eine neue Zuordnung hinzufügen.

### Konfigurieren einer einzelnen Tabellenzuordnung {#new-mapping-settings}

In diesem Abschnitt erfahren Sie, wie Sie eine **single** Zuordnung einer Microsoft Dynamics 365-Tabelle zu einer Adobe Campaign-Tabelle konfigurieren.

Sie können die folgenden Einstellungen definieren:

* **[!UICONTROL Tabellen]**: In diesem Abschnitt werden der Name der Microsoft Dynamics 365-Tabelle und die Kampagne, der sie zugeordnet werden, Liste.
* **[!UICONTROL Feldzuordnungen]**: Weitere Informationen in  [diesem Abschnitt](#field-mappings)
* **[!UICONTROL Feldersetzungen]**: Weitere Informationen in  [diesem Abschnitt](#field-replacements)
* **[!UICONTROL Filter]**: Weitere Informationen in  [diesem Abschnitt](#filters)
* **[!UICONTROL Erweiterte Einstellungen]**: Weitere Informationen in  [diesem Abschnitt](#advanced-settings)

### Feldzuordnungen {#field-mappings}

#### Primär Keys

Wenn Sie eine neue Microsoft Dynamics 365-Kampagne zur Tabellenzuordnung hinzufügen, müssen Sie das ID-Feld identifizieren.

![](assets/d365-to-acs-ui-page-ingress-mappings-first-key.png)

Der Microsoft Dynamics 365-Primärschlüssel ist schreibgeschützt, da die Anwendung ihn erkennt.

Zur Kampagne müssen Sie festlegen, welches Feld der eindeutige Schlüssel sein soll. Sie muss als benutzerdefinierte Ressource [CRM-ID](../../developing/using/uc-calling-resource-id-key.md) konfiguriert sein und darf keine Duplikat enthalten.

>[!NOTE]
>
>Sie können das ID-Feld in der Tabelle nur dann auswählen, wenn Sie **[!UICONTROL Hinzufügen Neue Zuordnung]** ausgewählt haben. Wenn Sie auf die Schaltfläche &quot;Bearbeiten&quot;klicken, um eine vorhandene Tabellenzuordnung zu bearbeiten, ist das ID-Feld schreibgeschützt.

Die primären Schlüssel sind immer die ersten Feldnamen, die im Abschnitt **[!UICONTROL Feldzuordnungen]** aufgeführt werden. Zur Erinnerung: Das folgende Symbol wird rechts angezeigt, um Sie daran zu erinnern, dass es sich hierbei um die Hauptschlüssel handelt.

![](assets/d365-to-acs-icon-primary-key.png)

#### hinzufügen anderen Feldzuordnungen

Im Abschnitt **[!UICONTROL Feldzuordnungen]** können Sie andere Feldzuordnungen als die &quot;Primär Keys&quot;hinzufügen. Um eine neue Feldzuordnung von Microsoft Dynamics 365 zu Adobe Campaign hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Hinzufügen neue Feldzuordnung]**.

Wählen Sie in den Listen die Felder Microsoft Dynamics 365 und Kampagne aus:

![](assets/d365-to-acs-ui-page-ingress-new-field-mapping.png)

Diese Listen enthalten die Feldnamen, die mit den Microsoft Dynamics 365 und den Kampagnen verknüpft sind, die Sie oben auf der Seite ausgewählt haben.

Mit dem Umschalter **[!UICONTROL Updates anwenden]** können Sie steuern, ob Updates auf dieses Feld von Microsoft Dynamics 365 auf die Kampagne übertragen werden:
* Wenn ![](assets/d365-to-acs-icon-switch-on.png) eingeschaltet wird, werden Updates der Werte in Microsoft Dynamics 365 an Adobe Campaign weitergegeben, sobald die Updates vorgenommen werden.

* Wenn Sie ![](assets/d365-to-acs-icon-switch-off.png) ausschalten, wird der Wert beim Laden (oder Wiedergeben) der Daten weitergegeben, inkrementelle Aktualisierungen des Felds in Microsoft Dynamics 365 werden jedoch nicht weitergegeben.

>[!NOTE]
>
>Klicken Sie auf die Spaltenüberschrift **[!UICONTROL Updates anwenden]**, um **alle** der Switches zu aktivieren oder zu deaktivieren.


Wenn Sie Feldwerte auswählen, wird der Datentyp unter den Dropdown-Menüs angezeigt.   Dies ist bei der Zuordnung von Werten aus einem Feld zum anderen zu beachten.

![](assets/d365-to-acs-ui-page-ingress-mappings-fields-selected.png)

>[!NOTE]
>
> Es ist nicht möglich, mehrere Microsoft Dynamics 365-Kampagnen einem Feld zuzuordnen.

### Feldersetzungen {#field-replacements}

Verwenden Sie die Schaltfläche **[!UICONTROL Hinzufügen Ersetzen eines neuen Felds]**, um ein neues Feld zu definieren.

Mit den Feldersetzungen können Sie Folgendes identifizieren:

* einem Feldnamen Microsoft Dynamics 365 (der oben im Abschnitt Feldzuordnungen hinzugefügt wurde),
* einem vorhandenen Wert (der in Microsoft Dynamics 365 vorhanden ist) und
* ein neuer Wert zum Schreiben in Adobe Campaign

Eine Dropdown-Liste wird für picklist-, Auflistung- und boolesche Werte bereitgestellt. Ein Textfeld wird für andere Zeichenfolgen- und numerische Typen verwendet.

### Filter {#filters}

Verwenden Sie die Schaltfläche **[!UICONTROL Hinzufügen Neuer Filter]**, um auszuwählen, welche Microsoft Dynamics 365-Datensätze in die Kampagne übertragen werden sollen. Sie können ein Feld auswählen, das mit einem Datensatz verknüpft ist, um Filtern hinzuzufügen (der Feldname muss nicht den Feldzuordnungen hinzugefügt werden).

Sie geben einen Filter an, indem Sie die folgenden Informationen ausfüllen:

* Feldname für Microsoft Dynamics 365
* einen Vergleichswert und
* ein Wert (aus Microsoft Dynamics 365)
Wenn der Feldname, der Feldvergleich und der Wert für einen bestimmten Datensatz &quot;true&quot;ergibt, wird der Datensatz an Adobe Campaign weitergegeben.

Sie können festlegen, wie diese Filter bewertet werden, indem Sie die Eingabe mit der Bezeichnung **[!UICONTROL Wählen Sie den Filtervergleichsoperator]**.  Wenn Sie **und** wählen, müssen alle Filter &quot;true&quot;sein, damit ein Datensatz in die Kampagne übertragen wird. Wenn Sie **oder** wählen, wird der Datensatz propagiert, wenn einer von ihnen &quot;true&quot;ergibt.

Die Option **[!UICONTROL Möchten Sie Datensätze in Adobe Campaign Standard löschen, die aus Microsoft Dynamics 365 herausgefiltert werden?]** steuert, ob aus der Kampagne gefilterte Datensätze gelöscht werden sollen. Wenn Sie **Nein** auswählen, bleiben die Datensätze im Adobe Campaign. Wählen Sie **Ja**, um sie durch die Integrationslogik zu löschen.

>[!NOTE]
>
> Wenn keine Filter hinzugefügt werden, werden alle geänderten Datensätze an Adobe Campaign weitergegeben.


### Erweiterte Einstellungen {#advanced-settings}

Beim Konfigurieren einer Zuordnung können Sie die folgenden zusätzlichen Optionen einrichten:

* Setzen Sie die Option **[!UICONTROL Löschvorgänge in Microsoft Dynamics 365 auf Kampagne anwenden?]** Option  **Ja**, wenn Sie Löschungen, die in Microsoft Dynamics 365 auftreten, an das entsprechende Feld in Adobe Campaign weiterleiten möchten (basierend auf der Feldnamenzuordnung). Wählen Sie **Nein**, um Löschungen in Microsoft Dynamics 365 zu ignorieren.

* Legen Sie die &quot;**[!UICONTROL Technische Werte in Microsoft Dynamics 365&quot;-Auswahllisten fest?]** auf  **** Noif (Noif), wenn Sie den mit einer Microsoft Dynamics 365-Auswahlliste verknüpften Anzeigewert auf die Kampagne übertragen möchten. Wählen Sie **Ja**, um den technischen Wert zu propagieren.

## Synchronisieren von Kampagne Marketing-Ereignissen mit Microsoft Dynamics 365

Auf der Seite **[!UICONTROL Kampagne zu Microsoft Dynamics 365]** können Sie erkennen, welche E-Mail-Marketing-Ereignis von Adobe Campaign zu Microsoft Dynamics 365 zugeordnet werden.

Die vier Metriken, die Sie steuern können, sind: **Sendet**, **Klicks**, **Öffnet** und **Absprünge**.

![](assets/d365-to-acs-ui-page-workflows-egress.png)

Wählen Sie **Ja** aus, um zu bestätigen, dass Ereignis dieses Typs zu Microsoft Dynamics 365 laufen sollen.

Klicken Sie [hier](../../integrating/using/d365-acs-self-service-app-workflows.md), um weitere Informationen zu diesen E-Mail-Ereignissen zu erhalten.

## Opt-in/out-Arbeitsablauf {#opt-in-out-wf}

Mit dem Arbeitsablauf **Ausschluss/Ausschluss** können Sie den Fluss der Opt-in/out-Informationen zwischen Microsoft Dynamics 365 und Adobe Campaign identifizieren. Dabei wird davon ausgegangen, dass die Daten mit der Microsoft Dynamics 365-Entität &quot;contact&quot;und der Adobe Campaign-Ressource &quot;Profil&quot;verknüpft sind.

Weitere Informationen zur Opt-out-Verwaltung finden Sie in [diesem Abschnitt](../../integrating/using/d365-acs-notices-and-recommendations.md#opt-out).

Denken Sie daran, dass Sie auf &quot;Speichern&quot;klicken müssen, um Ihre Auswahl zu speichern. Denken Sie auch daran, dass Sie den Workflow **Kampagne zu Microsoft Dynamics 365** beenden und dann auf &quot;Abspielen&quot;klicken müssen, um die Änderungen zu übernehmen.

![](assets/d365-to-acs-ui-page-workflows-optinout-disabled.png)

### Opt-in/Out-Synchronisierungsrichtung

Nachstehend finden Sie die Liste der verfügbaren Optionen zum Synchronisieren von Daten:

* **[!UICONTROL Deaktiviert]**: Wenn diese Option aktiviert ist, werden keine Opt-in/out-Informationen zwischen Adobe Campaign und Microsoft Dynamics 365 verschoben.

* **[!UICONTROL Unidirektional (Microsoft Dynamics 365 zur Kampagne)]**: Diese Option wird verwendet, um die Option zum Ein-/Ausstieg von Microsoft Dynamics 365 auf Adobe Campaign zu übertragen. In der Integrationsanwendung können Sie den Fluss in diesem Bildschirm nicht konfigurieren. Klicken Sie stattdessen auf die Schaltfläche **[!UICONTROL Speichern]** und navigieren Sie zum Arbeitsablauf **[!UICONTROL Microsoft Dynamics 365 zu Kampagne]**. In diesem Arbeitsablauf können Sie die Zuordnung von Kontakten/Profil-Tabellen bearbeiten, um herauszufinden, wie die Ausschluss-/Abmeldefelder zugeordnet werden sollen.

* **[!UICONTROL Unidirektional (Kampagne zu Microsoft Dynamics 365)]**: Diese Option macht den  **** Zuordnungsabschnitt sichtbar. Mithilfe dieser Eingaben können Sie festlegen, welche Adobe Campaign-Felder Daten zu welchen Feldern in Microsoft Dynamics 365 zuordnen. Das bedeutet, wenn Sie einen Wert in Microsoft Dynamics 365 manuell aktualisieren, wird dieser Wert durch den Adobe Campaign-Wert überschrieben, wenn er sich ändert.

* **[!UICONTROL Bidirektional]**: Diese Option macht den  **** Zuordnungsabschnitt sichtbar. Diese Paare identifizieren, welche Felder in Microsoft Dynamics 365 und Adobe Campaign sich gegenseitig zuordnen. [Weitere Informationen](../../integrating/using/d365-acs-notices-and-recommendations.md).

### Zuordnungen

Dieser Abschnitt gilt nur, wenn für das Feld für die Synchronisierungsrichtung die Einstellung **[!UICONTROL Eindeutig (Kampagne auf Microsoft Dynamics 365)]** oder **[!UICONTROL Bidirektional]** festgelegt ist. Sie können festlegen, welche Felder in Microsoft Dynamics 365 den Eingaben in Adobe Campaign zugeordnet werden.

Die Feldnamen von Microsoft Dynamics 365 umfassen alle Feldnamen vom Typ **boolean**.

Die Feldnamen des Adobe Campaigns sind ein fester Satz von Werten, die für die Ein-/Ausschlussoption spezifisch sind. Die Feldnamen des Adobe Campaigns sind ein fester Satz von Werten, die für die Ein-/Ausschlussoption spezifisch sind. **Der Wertesatz in dieser Liste kann nicht geändert** werden.
