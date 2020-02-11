---
title: Konfigurieren des E-Mail-Kanals in Adobe Campaign Standard
description: Erfahren Sie, wie Sie den E-Mail-Kanal in Adobe Campaign Standard konfigurieren.
page-status-flag: never-activated
uuid: 9fddb655-b445-41f3-9b02-5d356fc88aa1
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 3752d41f-8c59-4fad-b30f-e98e09cd74a8
context-tags: extAccountEmail,overview;emailConfig,main;ruleSet,overview;delivery,properties,open
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9163a375a4d2345e94a62e38475cb90bd203ce48

---


# E-Mail-Kanal konfigurieren{#configuring-email-channel}

## Parameter für den E-Mail-Kanal {#email-channel-parameters}

Im E-Mail-Konfigurationsfenster können Sie die Parameter für den E-Mail-Kanal definieren.

![](assets/channels_1.png)

* **Header-Parameter für ausgehende E-Mails**

   In this section, you can specify the **[!UICONTROL masks]** authorized for the sender address and the error address. Bei Angabe von mehr als einer Maske sind die Masken durch Kommata zu trennen. Hierbei handelt es sich um eine optionale Konfiguration. Wenn diese Felder ausgefüllt sind, prüft Adobe Campaign im Zuge der Nachrichtenvorbereitung, dass die in der E-Mail angegebenen Adressen gültig sind. Auf diese Weise vermeiden Sie die Verwendung von Adressen, die Probleme bei der Zustellbarkeit bereiten könnten. Absenderadressen sind auf dem Versandserver zu konfigurieren.

* **Zustellbarkeit**

   Diese Kennung wird Ihnen vom Support mitgeteilt. Sie ist für die korrekte Funktionsweise der Zustellbarkeitsberichte erforderlich.

* **Versandparameter**

   Adobe Campaign versendet Nachrichten ab dem Datum des Versandstarts. The **[!UICONTROL Message delivery duration]** field allows you to specify the duration during which the messages can be sent.

   The **[!UICONTROL Online resources validity duration]** field is used for uploaded resources, mainly for the mirror page and images. Die Gültigkeitsdauer der Ressourcen auf dieser Seite ist begrenzt, um Speicherkapazität zu sparen.

* **Weitere Zustellversuche**

   Nachrichten, die vorläufig nicht zugestellt werden können, werden automatisch für einen erneuten Versuch vorgesehen. Geben Sie in diesem Bereich an, wie viele weitere Zustellversuche am ersten Tag nach dem Versandstart unternommen werden sollen (**Anzahl weiterer Versuche**), sowie die minimale Zeitspanne zwischen zwei Versuchen (**Versuchsintervall**).

   Standardmäßig sind innerhalb der ersten 24 Stunden fünf erneute Versuche im Abstand von mindestens einer Stunde vorgesehen. One retry per day is programmed after that and until the delivery deadline, which is defined in the **[!UICONTROL Delivery parameters]** section.

* **Quarantäne-Parameter der E-Mails**

   In the **[!UICONTROL Time between two significant errors]** field, enter a value to define the time the application waits before incrementing the error counter in case of failure. Standardwert: **&quot;1d&quot;** für 1 Tag.

   Wenn der **[!UICONTROL Maximum number of errors before quarantine]** Wert erreicht wird, wird die E-Mail-Adresse in Quarantäne gestellt. Standardwert: **&quot;5&quot;**: Die Adresse wird beim sechsten Fehler unter Quarantäne gestellt. Dies bedeutet, dass der Kontakt automatisch von den nächsten Sendungen ausgeschlossen wird.

**Verwandtes Thema**:

[Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)

## E-Mail-Routing-Konten  {#email-routing-accounts}

Das **[!UICONTROL Integrated email routing]** externe Konto wird standardmäßig bereitgestellt. Es enthält die technischen Parameter, die es der Anwendung erlauben, E-Mails zu senden.

![](assets/channels_2.png)

The account type must always be set to **[!UICONTROL Routing]**, the channel to **[!UICONTROL Email]** and the delivery mode set to **[!UICONTROL Bulk delivery]**.

**Verwandtes Thema**:

[Externe Konten](../../administration/using/external-accounts.md)

## Regeln zum Umgang mit E-Mails  {#email-processing-rules}

Administratoren **[!UICONTROL Email processing rules]** können über das **[!UICONTROL Administration > Channels > Email]** Menü auf die Datei zugreifen.

In den Regeln sind die von Remote-Servern potenziell zurückgegebenen Strings enthalten, die die Qualifizierung der Fehler in **Hardbounce**, **Softbounce** oder **Ignoriert** erlauben.

Folgende Regeln sind in der Standardkonfiguration vorgesehen:

### Bounce Messages {#bounce-mails}

Wenn die Zustellung einer E-Mail fehlschlägt, gibt der Remote-Server eine Fehlermeldung an die in den Plattform-Parametern angegebene Bounce-Adresse zurück.

Adobe Campaign vergleicht den Inhalt jeder Bounce-E-Mail mit den in der Regelliste verzeichneten Strings und ordnet einen der drei Fehlertypen zu.

>[!IMPORTANT]
>
>Nach der Aktualisierung auf die erweiterte MTA werden die Absprungqualifikationen in der **[!UICONTROL Message qualification]** Kampagnentabelle nicht mehr verwendet. Bei Meldungen mit Fehlern bei synchroner Bereitstellung bestimmt die erweiterte MTA den Absprungtyp und die Qualifikation und sendet diese Informationen an Kampagne zurück. Asynchrone Absprünge werden weiterhin vom InMail-Prozess qualifiziert.
>
>Weitere Informationen zur erweiterten MTA-Datei für Adobe Campaign finden Sie in diesem [Dokument](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html).

Der Benutzer kann eigene Regeln erstellen.

>[!IMPORTANT]
>
>Beim Import eines Packages und bei der Aktualisierung von Daten durch den **Zustellbarkeit**-Workflow werden benutzerdefinierte E-Mail-Regeln überschrieben.

### E-Mail-Domain-Verwaltung {#managing-email-domains}

Domain-Verwaltungsregeln ermöglichen die Regulierung des Volumens der ausgehenden E-Mails nach Domains. Sie analysieren die Bounce Messages und blockieren falls nötig den Versand.

Der Adobe-Campaign-E-Mail-Server wendet zunächst die spezifischen Domain-Regeln an und im Anschluss jene, die den Normalfall repräsentieren (durch * gekennzeichnet). 

>[!IMPORTANT]
>
>Nach der Aktualisierung auf die erweiterte MTA erfolgt die Signatur der DKIM-E-Mail-Authentifizierung (DomainKeys Identified Mail) durch die erweiterte MTA. Das DKIM-Signieren durch die native Kampagnen-MTA wird im Rahmen des erweiterten MTA-Upgrades in der **[!UICONTROL Domain management]** Tabelle deaktiviert.
>
>Weitere Informationen zur erweiterten MTA-Datei für Adobe Campaign finden Sie in diesem [Dokument](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html).

Um eigene Domain-Verwaltungsregeln zu erstellen, sind die Angabe einer Schwelle und die Auswahl gewisser SMTP-Parameter erforderlich. Die **Schwelle** entspricht einem Prozentsatz an Fehlern, der bei Überschreiten den Versand an die betroffene Domain unterbricht.

Die **SMTP-Parameter** agieren wie die im Falle einer Blockierungsregel angewendeten Filter.

* Sie haben die Möglichkeit, gewisse Authentifizierungsnormen und Verschlüsselungsschlüssel zu aktivieren, um den Domain-Namen zu prüfen: **Sender ID**, **DomainKeys**, **DKIM**, **S/MIME**.
* **SMTP-Relais**: Zur Konfiguration der IP-Adresse und des Relais-Server-Ports für eine bestimmte Domain.

### MX-Verwaltung {#mx-management}

Jede Regel definiert eine Adressenmaske des MX. Jeder MX, dessen Name dieser Adressenmaske entspricht, kommt somit infrage. Die Maske kann die Joker &quot;*&quot; und &quot;?&quot; enthalten.

So sind die Adressen

* a.mx.yahoo.com
* b.mx.yahoo.com
* c.mx.yahoo.com

mit folgenden Masken kompatibel:

* *.yahoo.com
* ?.mx.yahoo.com

Die erste Regel, deren MX-Maske mit dem gewünschten MX kompatibel ist, wird angewendet.

>[!IMPORTANT]
>
>Nach der Aktualisierung auf die erweiterte MTA werden die **MX-Verwaltungsregeln** für Adobe Campaign nicht mehr verwendet. Die erweiterte MTA verwendet ihre eigenen MX-Regeln, die es ermöglichen, Ihren Durchsatz nach Domäne basierend auf Ihrem eigenen historischen E-Mail-Ruf und dem Echtzeit-Feedback, das von den Domänen stammt, von denen Sie E-Mails senden, anzupassen.
>
>Weitere Informationen zur erweiterten MTA-Datei für Adobe Campaign finden Sie in diesem [Dokument](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html).

Folgende Parameter stehen für jede einzelne Regel zur Verfügung:

* **[!UICONTROL Range of IDs]**: Mit dieser Option können Sie die Bereiche der Bezeichner (publicId) angeben, für die die Regel gilt. Folgende Angaben sind möglich:

   * Eine Ziffer: Die Regel wird nur für diese publicId angewendet.
   * Ein Ziffernbereich (Ziffer1-Ziffer2): Die Regel wird für alle in diesem Bereich enthaltenen publicId angewendet.
   Wenn nicht anders angegeben, wird die Regel für alle Kennungen angewendet.

* **[!UICONTROL Shared]**: Diese Option gibt an, dass die höchste Anzahl von Nachrichten pro Stunde und Verbindungen für alle MXs gilt, die mit dieser Regel verknüpft sind.
* **[!UICONTROL Maximum number of connections]**: maximale Anzahl gleichzeitiger Verbindungen zu einem MX von einer bestimmten Adresse.
* **Maximale Nachrichtenanzahl**: Maximale Anzahl an Nachrichten, die von einer Verbindung aus gesendet werden können. Bei der Übersteigung der zulässigen Höchstwerte wird die Verbindung geschlossen und eine neue hergestellt.
* **[!UICONTROL Messages per hour]**: maximale Anzahl von Nachrichten, die in einer Stunde für einen MX über eine bestimmte Adresse gesendet werden können.

>[!IMPORTANT]
>
>* Nach Änderungen in der Konfiguration muss der Versandserver (MTA) neu gestartet werden.
>* Neuerstellung und Änderungen von Verwaltungsregeln sollten erfahrenen Benutzern vorbehalten bleiben.
>



## Liste der E-Mail-Eigenschaften  {#list-of-email-properties}

Dieser Abschnitt behandelt die Liste von Parametern, die in den Eigenschaften einer E-Mail oder einer E-Mail-Vorlage verfügbar sind.

>[!NOTE]
>
>Manche Parameter sind ausschließlich über die Vorlagen verfügbar. Die Parameter, auf die Sie zugreifen können, [hängen von Ihrer Zugriffsberechtigung ab](../../administration/using/users-management.md).

To edit the properties of an email or an email template, use the **[!UICONTROL Edit properties]** button.

![](assets/delivery_options_1.png)

### Allgemeine Parameter {#general-parameters}

On the top of the email parameter screen, identify the email using the **[!UICONTROL Label]** and **[!UICONTROL ID]** fields. Diese Informationen erscheinen in der Benutzeroberfläche, sind aber für die Empfänger nicht sichtbar.

![](assets/delivery_options_2.png)

>[!IMPORTANT]
>
>Die Kennung muss eindeutig sein.

The **[!UICONTROL Brand]** field allows you to select the brand linked to the delivery. Weiterführende Informationen zur Verwendung und Konfiguration von Marken finden Sie im Abschnitt [Marken](../../administration/using/branding.md).

The **[!UICONTROL Campaign]** field allows you to enter the campaign linked to the email.

You can also add a **[!UICONTROL Description]** in the corresponding field and edit the image displayed on the email thumbnail in the lists.

### Versandparameter {#sending-parameters}

The **[!UICONTROL Send]** section is only available for email templates. Darin sind die folgenden Parameter enthalten:

#### Parameter für weitere Zustellversuche {#retries-parameters}

Nachrichten, die vorläufig nicht zugestellt werden können, werden automatisch für einen erneuten Versuch vorgesehen. This section indicates how many retries should be performed the day after the send is started ( **[!UICONTROL Max. number of retries]** ) and the minimum delay between retries ( **[!UICONTROL Retry period]** ).

Standardmäßig sind innerhalb der ersten 24 Stunden fünf erneute Versuche im Abstand von mindestens einer Stunde vorgesehen. An den folgenden Tagen und bis zum Ablauf der Versandgültigkeit, die im Bereich [Parameter für den Gültigkeitszeitraum](#validity-period-parameters) angegeben ist, wird jeweils ein Zustellversuch unternommen.

Die Anzahl weiterer Versuche kann global geändert werden (kontaktieren Sie Ihren technischen Administrator von Adobe) oder einzeln für jeden Versand oder jede Versandvorlage.

#### Parameter für E-Mail-Format  {#email-format-parameters}

Sie können das Format der zu sendenden E-Mails konfigurieren. Dabei stehen drei Optionen zur Verfügung:

* **Empfängervorlieben berücksichtigen** (Standardmodus): Das Nachrichtenformat wird auf der Grundlage der im Empfängerprofil gespeicherten Daten definiert und standardmäßig im Feld **E-Mail-Format** (@emailFormat) gespeichert. Falls ein Empfänger Nachrichten in einem bestimmten Format erhalten möchte, werden sie in diesem Format gesendet. Ohne Angabe in diesem Feld wird eine Nachricht vom Typ „Multipart-Alternative“ gesendet, wie im Anschluss erläutert.
* **E-Mail-Programm des Empfängers das beste Format wählen lassen (multipart-alternative)**: Die Meldung enthält sowohl das Text- als auch das HTML-Format. Welches Format beim Empfänger angezeigt wird, hängt von der Konfiguration des E-Mail-Programms des Empfängers ab (Multipart-Alternative).

   >[!IMPORTANT]
   >
   >Diese Option umfasst beide Versionen der Nachricht. Dies hat Auswirkungen auf den Versanddurchsatz, da die Nachricht dadurch größer wird.

* **Alle Nachrichten im Textformat senden**: Die Nachricht wird im Textformat gesendet. Das HTML-Format wird nicht gesendet und lediglich für die Mirrorseite verwendet, wenn der Empfänger auf den Link in der Nachricht klickt.

#### SMTP-Testmodus {#smtp-test-mode}

The **[!UICONTROL Enable SMTP test mode]** option allows you to test sending emails via an SMTP connection without actually sending messages.
Die Nachrichten werden verarbeitet, bis eine Verbindung mit dem SMTP-Server hergestellt wurde, sie werden aber nicht gesendet.

![](assets/smtp-test-mode.png)

Diese Option steht für E-Mails und E-Mail-Vorlagen zur Verfügung.

Wenn Sie die SMTP-Testmodus-Option für eine E-Mail-Vorlage aktivieren, ist diese Option in allen mit dieser Vorlage erstellten E-Mail-Nachrichten aktiviert.

>[!IMPORTANT]
>
>Wenn diese Option für eine E-Mail aktiviert ist, werden keine Nachrichten gesendet, bis sie deaktiviert wird.
>Im Dashboard der E-Mail oder E-Mail-Vorlage wird ein Warnhinweis angezeigt.

Weiterführende Informationen zur SMTP-Konfiguration finden Sie im Abschnitt [Liste der E-Mail-SMTP-Parameter](#list-of-email-smtp-parameters).

### Parameter für den Gültigkeitszeitraum  {#validity-period-parameters}

Im Abschnitt **[!UICONTROL Validity period]** sind folgende Parameter verfügbar:

![](assets/delivery-validity-period.png)

* **[!UICONTROL Explicitly set validity dates]**: Wenn dieses Kontrollkästchen deaktiviert ist, müssen Sie eine Dauer in die Felder **[!UICONTROL Delivery duration]** und **[!UICONTROL Resource validity limit]** eingeben. Kreuzen Sie diese Option an, wenn Sie Datum und Uhrzeit genau festlegen möchten.

   ![](assets/delivery-set-explicit-dates.png)

* **[!UICONTROL Delivery duration]**: Adobe Campaign versendet Nachrichten ab dem Datum des Versandstarts. In diesem Feld lässt sich die Dauer festlegen, innerhalb derer Nachrichten verschickt werden können.

   >[!IMPORTANT]
   >
   >Nach der Aktualisierung auf die erweiterte MTA wird der **[!UICONTROL Delivery duration]** Parameter in Ihren Kampagnenauslieferungen nur verwendet, wenn er auf 3,5 Tage oder weniger eingestellt ist. Wenn Sie einen Wert von mehr als 3,5 Tagen definieren, wird dieser nicht berücksichtigt. Alle Auswirkungen sind im Dokument [Adobe Campaign Enhanced MTA](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html) ausführlich beschrieben.

* **[!UICONTROL Resource validity duration]**: Dieses Feld wird für hochgeladene Ressourcen verwendet, hauptsächlich für die Spiegelseite und Bilder. Die Gültigkeitsdauer der Ressourcen auf dieser Seite ist begrenzt, um Speicherkapazität zu sparen.
* **[!UICONTROL Mirror page management]**: Die Spiegelseite ist eine HTML-Seite, die online über einen Webbrowser aufgerufen werden kann. Sie hat den gleichen Inhalt wie die E-Mail. Standardmäßig wird die Mirrorseite automatisch generiert, wenn der entsprechende Link in den Inhalt der E-Mail eingefügt wurde. Die Erzeugung der Seite lässt sich in diesem Feld konfigurieren:

   >[!IMPORTANT]
   >
   >Die Erstellung der Mirrorseite setzt voraus, dass für die E-Mail ein HTML-Inhalt bestimmt worden ist.

   * **[!UICONTROL Generate the mirror page if a mirror link appears in the email content]** (Standardmodus): die Spiegelseite wird generiert, wenn der Link in den E-Mail-Inhalt eingefügt wird.
   * **Mirrorseitenerzeugung forcieren**: Erstellt eine Mirrorseite, selbst wenn im Versandinhalt kein entsprechender Link enthalten ist.
   * **Keine Mirrorseite erzeugen**: Generiert keine Mirrorseite, selbst wenn in den Nachrichten der entsprechende Link enthalten ist.
   * **Über die Nachrichtenkennung zugängliche Mirrorseite erzeugen**: Diese Option ermöglicht den Zugriff auf den Inhalt der Mirrorseite (einschließlich aller Personalisierungsinformationen) über das Versandlog-Fenster.

>[!NOTE]
>
>Der **[!UICONTROL Delivery duration]** Parameter gilt nicht für Transaktionsmeldungen. Weiterführende Informationen zu Transaktionsnachrichten finden Sie in [diesem Abschnitt](../../channels/using/about-transactional-messaging.md).

### Tracking-Parameter  {#tracking-parameters}

Im Abschnitt **[!UICONTROL Tracking]** sind folgende Parameter verfügbar:

* **[!UICONTROL Activate tracking]**: ermöglicht Ihnen, die Verfolgung der Nachrichten-URL zu aktivieren/deaktivieren. Über das Symbol **[!UICONTROL Links]** in der Symbolleiste von Email Designer können Sie das Tracking der einzelnen in Nachrichten enthaltenen URLs verwalten. Siehe [Über getrackte URLs](../../designing/using/links.md#about-tracked-urls).
* **[!UICONTROL Tracking validity limit]**: können Sie die Dauer festlegen, für die die Verfolgung in den URLs aktiviert wird.
* **[!UICONTROL Substitution URL for expired URLs]**: Sie können eine URL zu einer Webseite eingeben, die nach Ablauf der Verfolgung angezeigt wird.

### Erweiterte Parameter {#advanced-parameters}

Der **[!UICONTROL Advanced parameters]** Abschnitt enthält mehrere Parameter.

Die ersten Felder dienen zur Eingabe der für die Header von E-Mail-Nachrichten erforderlichen Informationen. Hier können Sie die Antwortadresse und den Text sowie die Absenderadresse (die das Feld „Von:“ ausfüllt) verwalten. Diese Informationen können personalisiert werden.

Klicken Sie auf die Schaltfläche rechts neben dem Feld, das geändert werden soll, und fügen Sie dann das Personalisierungsfeld, den Inhaltsblock oder den dynamischen Text hinzu.

![](assets/advancedparameters.png)

Das Einfügen und Verwenden des Personalisierungsinhalts ist in der Dokumentation zum [Personalisieren von E-Mail-Inhalten](../../designing/using/personalization.md) ausführlich beschrieben.

#### Zielgruppen-Kontext  {#target-context}

Im Zielgruppen-Kontext werden die für die Zielgruppenbestimmung (im Bildschirm zur Audience-Erstellung) und die Personalisierung (Definition von Personalisierungsfeldern, im HTML-Inhaltseditor) der E-Mail verwendeten Tabellen angegeben.

#### Routing  {#routing}

In diesem Feld wird der zu verwendende Routing-Modus definiert. Hierzu wird auf ein externes Konto verwiesen. Dies kann zum Beispiel von Nutzen sein, wenn Sie ein externes Konto mit speziellen Branding-Einstellungen verwenden möchten.

>[!NOTE]
>
>Zu den externen Konten gelangen Sie über das Menü **Administration** > **Anwendungskonfiguration** > **Externe Konten**.

#### Vorbereitung  {#preparation}

Die Vorbereitung von Nachrichten ist im Abschnitt [Nachrichten validieren](../../sending/using/preparing-the-send.md) beschrieben.

* **[!UICONTROL Typology]**: vor dem Senden müssen Nachrichten vorbereitet werden, um den Inhalt und die Konfiguration zu validieren. Die in der Vorbereitungsphase anzuwendenden Validierungsregeln sind in einer **Typologie** festgelegt. Zum Beispiel betrifft die Vorbereitung für E-Mails die Validierung von Betreff, URL und Bildern etc. Wählen Sie in diesem Feld die anzuwendende Typologie aus.

   >[!NOTE]
   >
   >Typologies, which can be accessed via the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** menu, are presented in the [Typologies](../../administration/using/about-typology-rules.md) section.

* **[!UICONTROL Compute the label during delivery preparation]**: ermöglicht die Berechnung des Beschriftungswerts der E-Mail während der Vorbereitung der Nachricht mithilfe von Personalisierungsfeldern, Inhaltsblöcken und dynamischem Text.

   Sie können auch den Versandtitel mit Ereignisvariablen personalisieren, die in der Aktivität &quot;Externes Signal&quot; des Workflows deklariert wurden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../automating/using/calling-a-workflow-with-external-parameters.md).

* **[!UICONTROL Save SQL queries in the log]**: Mit dieser Option können Sie während der Vorbereitungsphase SQL-Abfrageprotokolle im Journal hinzufügen.

### Liste der E-Mail-SMTP-Parameter {#list-of-email-smtp-parameters}

Im Abschnitt **[!UICONTROL SMTP]** sind folgende Parameter verfügbar:

* **[!UICONTROL Character encoding]**: Markieren Sie das **[!UICONTROL Force encoding]** Kontrollkästchen, wenn Sie die Meldungskodierung erzwingen möchten, und wählen Sie dann die Kodierung aus, die Sie verwenden möchten.
* **[!UICONTROL Bounce mails]**: Standardmäßig werden Absprungmeldungen im Fehlereingabefeld der Plattform empfangen (definiert im **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email]** > **[!UICONTROL Configuration]** Bildschirm). To define a specific error address for an email, enter the address in the **[!UICONTROL Error address]** field.
* **[!UICONTROL Additional SMTP headers]**: mit dieser Option können Sie Ihren Nachrichten zusätzliche SMTP-Header hinzufügen. The script entered in the **[!UICONTROL Headers]** field must reference one header per line, in the form of **name:value**. Werte werden bei Bedarf automatisch verschlüsselt.

   >[!IMPORTANT]
   >
   >Das Hinzufügen zusätzlicher SMTP-Header ist eine Aufgabe für erfahrene Benutzer. Die Syntax des Skripts muss die Anforderungen für diesen Inhaltstyp (keine überflüssigen Leerzeichen, keine Leerzeilen usw.) erfüllen.

### Liste der Parameter für Zugriffsberechtigung  {#list-of-access-authorization-parameters}

Im Abschnitt **[!UICONTROL Access authorization]** sind folgende Parameter verfügbar:

* The **[!UICONTROL Organizational unit]** field allows you to restrict access to this email to certain users. Die der spezifizierten Einheit oder den übergeordneten Einheiten zugeteilten Nutzer haben Lese- und Schreibzugriff auf diese E-Mail. Der Zugriff der den untergeordneten Einheiten zugeteilten Nutzer auf diese E-Mail ist schreibgeschützt.

   >[!NOTE]
   >
   >Zur Konfiguration von Organisationseinheiten gehen Sie in das Menü **Administration** > **Benutzer &amp; Sicherheit**.

* Die **[!UICONTROL Created by]**-, **[!UICONTROL Created]**- **[!UICONTROL Modified by]** und **[!UICONTROL Last modified]** -Felder werden automatisch ausgefüllt.

## E-Mails archivieren {#archiving-emails}

Sie können Adobe Campaign so konfigurieren, dass von den von der Plattform gesendeten E-Mails eine Kopie beibehalten wird.

Adobe Campaign selbst ermöglicht zwar nicht die Verwaltung von archivierten Dateien, Sie können aber die gewünschten Nachrichten an eine bestimmte Adresse senden, wo sie mithilfe eines externen Systems verarbeitet und archiviert werden.

Wenn diese Funktion in der Versandvorlage aktiviert wird, können Sie eine exakte Kopie der gesendeten Nachrichten an eine von Ihnen bestimmte BCC-E-Mail-Adresse senden (unsichtbar für die Nachrichtenempfänger).

### Empfehlungen und Einschränkungen  {#recommendations-and-limitations}

* Hierbei handelt es sich um eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.
* Die BCC-Adresse Ihrer Wahl muss dem Adobe-Team zur Verfügung gestellt werden, das sie für Sie konfiguriert.
* Sie können nur eine einzige BCC-E-Mail-Adresse verwenden.
* Nur erfolgreich gesendete E-Mails werden berücksichtigt. Bounces werden nicht berücksichtigt.
* Aus Datenschutzgründen müssen BCC-E-Mails von einem Archivierungssystem bearbeitet werden, in dem personenbezogene Daten (PII, Personally Identifiable Information) sicher aufbewahrt werden.
* Bei der Erstellung einer neuen Versandvorlage ist E-Mail-BCC nicht standardmäßig aktiviert, selbst wenn diese Option erworben wurde. Sie muss manuell in jeder Versandvorlage aktiviert werden, in der sie verwendet werden soll.

### E-Mail-Archivierung aktivieren  {#activating-email-archiving}

E-Mail-BCC wird in der [E-Mail-Vorlage](../../start/using/marketing-activity-templates.md) über die folgende Option aktiviert:

1. Gehen Sie in den Knoten **Ressourcen** > **Vorlagen** > **Versandvorlagen**.
1. Duplizieren Sie die vordefinierte **[!UICONTROL Send via email]** Vorlage.
1. Wählen Sie die duplizierte Vorlage aus.
1. Click the **[!UICONTROL Edit properties]** button to edit the template&#39;s properties.
1. Erweitern Sie den **[!UICONTROL Send]** Abschnitt.
1. Check the **[!UICONTROL Archive emails]** box to keep a copy of all sent messages for each delivery based on this template.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>If the emails sent to the BCC address are opened and clicked through, this will be taken into account in the **[!UICONTROL Total opens]** and **[!UICONTROL Clicks]** from the send analysis, which could cause some miscalculations.
