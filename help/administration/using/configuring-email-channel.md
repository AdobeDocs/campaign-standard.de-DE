---
solution: Campaign Standard
product: campaign
title: E-Mail-Kanal in Adobe Campaign Standard konfigurieren
description: Erfahren Sie, wie Sie den E-Mail-Kanal in Adobe Campaign Standard konfigurieren.
audience: administration
content-type: reference
topic-tags: configuring-channels
context-tags: extAccountEmail,overview;emailConfig,main;ruleSet,overview;delivery,properties,open
translation-type: tm+mt
source-git-commit: bdbba06289eef65d9e42b7d82086f8fa14e1473c
workflow-type: tm+mt
source-wordcount: '2785'
ht-degree: 82%

---


# E-Mail-Kanal konfigurieren{#configuring-email-channel}

Als Campaign-[Administrator](../../administration/using/users-management.md#functional-administrators) können Sie Einstellungen für den E-Mail-Kanal konfigurieren. Zu den erweiterten Einstellungen gehören allgemeine E-Mail-Kanal-Parameter, E-Mail-Routing-Konten, Regeln zum Umgang mit E-Mails sowie E-Mail-Eigenschaften. Auf dieser Seite erfahren Sie, wie Sie die Standardwerte der allgemeinen E-Mail- und Versandparameter bearbeiten können.

## Parameter für den E-Mail-Kanal {#email-channel-parameters}

Im E-Mail-Konfigurationsfenster können Sie die Parameter für den E-Mail-Kanal definieren. Administratoren können auf diese Konfigurationen über das Menü **[!UICONTROL Administration] > [!UICONTROL Kanäle] > [!UICONTROL E-Mail] > [!UICONTROL Konfiguration]** zugreifen.

![](assets/channels_1.png)

* **Felder für zulässige Masken**

   Im Abschnitt **[!UICONTROL Header-Parameter für ausgehende E-Mails]** werden die autorisierten E-Mail-Adressen aufgelistet, mit denen Sie E-Mails an Ihre Empfänger senden können (Absenderadresse) und diese in die Lage versetzen können, automatisierte Antworten wie asynchrone Bounces, Abwesenheitsantworten usw. (Fehleradresse) zurückzusenden. Adobe Campaign prüft während der Vorbereitung der Nachricht, ob die eingegebenen Adressen gültig sind. Auf diese Weise vermeiden Sie die Verwendung von Adressen, die Probleme bei der Zustellbarkeit bereiten könnten.
   * Sowohl Absender- als auch Fehleradressen werden von Adobe eingerichtet. Diese Felder dürfen nicht leer sein.
   * Sie können diese Felder nicht bearbeiten. Wenden Sie sich zum Aktualisieren einer Adresse an das Team der Kundenunterstützung von Adobe.
   * Um eine weitere Adresse hinzuzufügen, können Sie über das [Control Panel](https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html) eine neue Subdomain einrichten oder sich an das Team der Kundenunterstützung von Adobe wenden. Beachten Sie, dass bei Verwendung mehrerer Masken diese durch Kommas getrennt werden.
   * Es wird empfohlen, Adressen mit einem Stern wie *@yourdomain.com festzulegen: Sie können jede Adresse verwenden, die mit Ihrem Subdomain-Namen endet.

* **Zustellbarkeit**

   Die **[!UICONTROL Kennung für die Zustellbarkeitsberichte]** wird vom Team der Kundenunterstützung von Adobe bereitgestellt. Sie identifiziert jede Instanz mit einer Zustellbarkeits-ID, die in den technischen Zustellberichten verwendet wird.
   <!--The Technical Deliverability report is not accessible through the UI in ACS. It will be replaced with 250ok in the future (project starting).-->

* **Versandparameter**

   Adobe Campaign versendet Nachrichten ab dem Datum des Versandstarts.

   Im Feld **[!UICONTROL Dauer des Nachrichtenversands]** können Sie den Zeitraum angeben, in dem Nachrichten im Versand, bei denen ein temporärer Fehler oder ein Softbounce auftritt, wiederholt werden.

   >[!IMPORTANT]
   >
   >**Dieser Parameter in Campaign wird jetzt nur noch verwendet, wenn er auf 3,5 Tage oder weniger gesetzt ist.** Wenn Sie einen Wert von mehr als 3,5 Tagen definieren, wird dieser nicht berücksichtigt.

   Das Feld **[!UICONTROL Gültigkeit der Online-Ressourcen]** wird für Ressourcen verwendet, die online verfügbar sind, insbesondere für Mirrorseiten und Bilder. Die Gültigkeitsdauer der Ressourcen auf dieser Seite ist begrenzt, um Speicherkapazität zu sparen.

* **Weitere Zustellversuche**

   Nachrichten, die vorläufig nicht zugestellt werden können, werden automatisch für einen erneuten Versuch vorgesehen. Weiterführende Informationen dazu finden Sie in Abschnitt [Weitere Zustellversuche nach einem vorübergehend fehlgeschlagenen Versand](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

   >[!IMPORTANT]
   >
   >Die maximale Anzahl der auszuführenden weitere Zustellversuche und die minimale Verzögerung zwischen weiteren Zustellversuchen basieren jetzt darauf, wie gut eine IP sowohl historisch als auch aktuell in einer bestimmten Domäne läuft. Die Einstellungen **[!UICONTROL Wiederholungszeitraum]** und **[!UICONTROL Anzahl der weitere Zustellversuche]** in der Kampagne werden ignoriert.

   <!--This section indicates how many retries should be performed the day after the send is started (**Number of retries**) and the minimum delay between retries (**Retry period**). By default, five retries are scheduled for the first day with a minimum interval of one hour, spread out over the 24 hours of the day. One retry per day is programmed after that and until the delivery deadline, which is defined in the **[!UICONTROL Delivery parameters]** section.-->

* **Quarantäne-Parameter der E-Mails**

   Geben Sie im Feld **[!UICONTROL Intervall zwischen zwei signifikanten Fehlern]** einen Wert an, um die Zeit zu definieren, die die Anwendung im Falle eines Softbounce-Fehlers wartet, bevor sie den Fehlerzähler inkrementiert. Der Standardwert lautet **1d** (für einen Tag).

   Wenn der Wert **[!UICONTROL Maximale Anzahl an Fehlern vor der Quarantäne]** erreicht ist, wird die E-Mail-Adresse unter Quarantäne gestellt. Der Standardwert lautet **5**: Die Adresse wird beim fünften Fehler unter Quarantäne gestellt. Dies bedeutet, dass der Kontakt automatisch von den nächsten Sendungen ausgeschlossen wird.
   <!--Actually the way ACS works is that the address is already on the quarantine list on the first bounce, but with a different status meaning that the error count has started.-->

   Weiterführende Informationen zur Quarantäne finden Sie unter [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md).

## E-Mail-Routing-Konten           {#email-routing-accounts}

Das externe Konto **[!UICONTROL Integriertes E-Mail-Routing]** wird standardmäßig bereitgestellt. Es enthält die technischen Parameter, die es der Anwendung erlauben, E-Mails zu senden.

![](assets/channels_2.png)

Dabei ist der Kontotyp mit **[!UICONTROL Routing]**, der Kanal mit **[!UICONTROL E-Mail]** und der Versandmodus mit **[!UICONTROL Gebündelter Versand]** zu konfigurieren.

**Verwandtes Thema**:

[Externe Konten](../../administration/using/external-accounts.md)

## Regeln zum Umgang mit E-Mails            {#email-processing-rules}

Auf die **[!UICONTROL Regeln zum Umgang mit E-Mails]** können Administratoren über das Menü **[!UICONTROL Administration > Kanäle > E-Mail]** zugreifen.

>[!IMPORTANT]
>
>Die E-Mail-Domänen und die MX-Regeln werden jetzt automatisch verwaltet und können nicht mehr geändert werden.<!--by the Adobe Campaign Enhanced MTA (Message Transfer Agent)-->

* **DKIM (DomainKeys Identified Mail)** E-Mail-Authentifizierungssignatur erfolgt für alle Nachrichten mit allen Domänen. Es wird nicht mit **Sender-ID**, **DomainKeys** oder **S/MIME** signiert.
* MX-Regeln passen Ihren Durchsatz automatisch nach Domäne an, basierend auf Ihrem eigenen historischen E-Mail-Ruf und dem Echtzeit-Feedback, das von den Domänen stammt, in denen Sie E-Mails senden.

<!--Note that the email domains and the MX rules are now managed by the Adobe Campaign Enhanced MTA:
* **DKIM (DomainKeys Identified Mail)** email authentication signing is done by the Enhanced MTA for all messages with all domains. It does not sign with **Sender ID**, **DomainKeys**, or **S/MIME** unless otherwise specified at the Enhanced MTA level.
* The Enhanced MTA uses its own MX rules that allow it to customize your throughput by domain based on your own historical email reputation, and on the real-time feedback coming from the domains where you are sending emails.-->

### Bounce Messages {#bounce-mails}

Asynchrone Bounces werden weiterhin mit dem inMail-Verfahren von Campaign durch die Regel **[!UICONTROL Bounce Messages]** qualifiziert.

In den Regeln sind die von Remote-Servern potenziell zurückgegebenen Strings enthalten, die die Qualifizierung der Fehler in **Hardbounce**, **Softbounce** oder **Ignoriert** erlauben.

>[!IMPORTANT]
>
>Fehlermeldungen wegen Synchronisationsfehlers werden jetzt durch das Adobe Campaign Enhanced MTA qualifiziert, das den Absprungtyp und die Absprungberechtigung bestimmt und diese Informationen an die Kampagne zurücksendet.

Weiterführende Informationen zur Qualifizierung von Bounce Messages finden Sie in diesem [Abschnitt](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification).

<!--Because they are now managed by the Enhanced MTA, the bounce qualifications in the Campaign **[!UICONTROL Message qualification]** table are no longer used. For more on bounce mail qualification, see this [section](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification).

### Management of email domains {#managing-email-domains}

The email domains are now managed by the Adobe Campaign Enhanced MTA. The Adobe Campaign **[!UICONTROL Domain management]** rules are no longer used.

**DKIM (DomainKeys Identified Mail)** email authentication signing is done by the Enhanced MTA for all messages with all domains. It does not sign with **Sender ID**, **DomainKeys**, or **S/MIME** unless otherwise specified at the Enhanced MTA level.

### MX management {#mx-management}

The MX rules are now managed by the Adobe Campaign Enhanced MTA. The Adobe Campaign **[!UICONTROL MX management]** delivery throughput rules are no longer used.

The Enhanced MTA uses its own MX rules that allow it to customize your throughput by domain based on your own historical email reputation, and on the real-time feedback coming from the domains where you are sending emails.-->

## Liste der E-Mail-Eigenschaften            {#list-of-email-properties}

Dieser Abschnitt behandelt die Liste von Parametern, die in den Eigenschaften einer E-Mail oder einer E-Mail-Vorlage verfügbar sind.

>[!NOTE]
>
>Manche Parameter sind ausschließlich über die Vorlagen verfügbar. Die Parameter, auf die Sie zugreifen können, [hängen von Ihrer Zugriffsberechtigung ab](../../administration/using/users-management.md).

Zur Änderung der Eigenschaften einer E-Mail bzw. einer E-Mail-Vorlage verwenden Sie die Schaltfläche **[!UICONTROL Eigenschaften bearbeiten]**.

![](assets/delivery_options_1.png)

### Allgemeine Parameter {#general-parameters}

Identifizieren Sie am oberen Rand des E-Mail-Parameter-Fensters die E-Mail unter Verwendung der Felder **[!UICONTROL Titel]** und **[!UICONTROL ID]**. Diese Informationen erscheinen in der Benutzeroberfläche, sind aber für die Empfänger nicht sichtbar.

![](assets/delivery_options_2.png)

>[!IMPORTANT]
>
>Die Kennung muss eindeutig sein.

Das Feld **[!UICONTROL Marke]** dient der Auswahl der dem Versand zugeordneten Marke. Weiterführende Informationen zur Verwendung und Konfiguration von Marken finden Sie im Abschnitt [Marken](../../administration/using/branding.md).

Im Feld **[!UICONTROL Kampagne]** kann die mit der E-Mail verknüpfte Kampagne eingetragen werden.

Außerdem kann im entsprechenden Feld eine **[!UICONTROL Beschreibung]** eingetragen werden. Das Bild, das in der Miniaturansicht der E-Mail innerhalb der Listen angezeigt wird, kann ebenfalls geändert werden.

### Versandparameter {#sending-parameters}

Der Bereich **[!UICONTROL Senden]** ist nur für E-Mail-Vorlagen verfügbar. Darin sind die folgenden Parameter enthalten:

#### Parameter für weitere Zustellversuche {#retries-parameters}

Nachrichten, die vorläufig nicht zugestellt werden können, werden automatisch für einen erneuten Versuch vorgesehen. Weiterführende Informationen dazu finden Sie in Abschnitt [Weitere Zustellversuche nach einem vorübergehend fehlgeschlagenen Versand](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!IMPORTANT]
>
>Die minimale Verzögerung zwischen weiteren Zustellversuchen und die maximale Anzahl der auszuführenden weitere Zustellversuche basieren jetzt darauf, wie gut eine IP sowohl historisch als auch aktuell in einer bestimmten Domäne läuft. Der **[!UICONTROL Wiederholungszeitraum]** und **[!UICONTROL Maximal. Die Anzahl der weitere Zustellversuche]**-Einstellungen in der Kampagne wird ignoriert.

Die in Campaign eingerichtete Einstellung **Versandlaufzeit** (definiert im Bereich [Parameter für den Gültigkeitszeitraum](#validity-period-parameters)) wird **weiterhin berücksichtigt, jedoch nur für bis zu 3,5 Tage**. An diesem Punkt wird jede Nachricht in der Warteschlange für weitere Versuche aus der Warteschlange entfernt und als Bounce zurückgesendet. Weiterführende Informationen zu Versandfehlern finden Sie in [diesem Abschnitt](../../sending/using/understanding-delivery-failures.md#about-delivery-failures).

#### Parameter für E-Mail-Format            {#email-format-parameters}

Sie können das Format der zu sendenden E-Mails konfigurieren. Dabei stehen drei Optionen zur Verfügung:

* **Empfängervorlieben berücksichtigen** (Standardmodus): Das Nachrichtenformat wird auf der Grundlage der im Empfängerprofil gespeicherten Daten definiert und standardmäßig im Feld **E-Mail-Format** (@emailFormat) gespeichert. Falls ein Empfänger Nachrichten in einem bestimmten Format erhalten möchte, werden sie in diesem Format gesendet. Ohne Angabe in diesem Feld wird eine Nachricht vom Typ „Multipart-Alternative“ gesendet, wie im Anschluss erläutert.
* **E-Mail-Programm des Empfängers das beste Format wählen lassen (multipart-alternative)**: Die Meldung enthält sowohl das Text- als auch das HTML-Format. Welches Format beim Empfänger angezeigt wird, hängt von der Konfiguration des E-Mail-Programms des Empfängers ab (Multipart-Alternative).

   >[!IMPORTANT]
   >
   >Diese Option umfasst beide Versionen der Nachricht. Dies hat Auswirkungen auf den Versanddurchsatz, da die Nachricht dadurch größer wird.

* **Alle Nachrichten im Textformat senden**: Die Nachricht wird im Textformat gesendet. Das HTML-Format wird nicht gesendet und lediglich für die Mirrorseite verwendet, wenn der Empfänger auf den Link in der Nachricht klickt.

#### SMTP-Testmodus {#smtp-test-mode}

Mit der Option **[!UICONTROL SMTP-Testmodus aktivieren]** können Sie den Versand von E-Mails über eine SMTP-Verbindung testen, ohne tatsächlich Nachrichten zu senden.
Die Nachrichten werden verarbeitet, bis eine Verbindung mit dem SMTP-Server hergestellt wurde, sie werden aber nicht gesendet.

![](assets/smtp-test-mode.png)

Diese Option steht für E-Mails und E-Mail-Vorlagen zur Verfügung.

Wenn Sie die SMTP-Testmodus-Option für eine E-Mail-Vorlage aktivieren, ist diese Option in allen mit dieser Vorlage erstellten E-Mail-Nachrichten aktiviert.

>[!IMPORTANT]
>
>Wenn diese Option für eine E-Mail aktiviert ist, werden keine Nachrichten gesendet, bis sie deaktiviert wird.
>Im Dashboard der E-Mail oder E-Mail-Vorlage wird ein Warnhinweis angezeigt.

Weiterführende Informationen zur SMTP-Konfiguration finden Sie im Abschnitt [Liste der E-Mail-SMTP-Parameter](#list-of-email-smtp-parameters).

### Parameter für den Gültigkeitszeitraum            {#validity-period-parameters}

Im Abschnitt **[!UICONTROL Gültigkeitszeitraum]** sind folgende Parameter verfügbar:

![](assets/delivery-validity-period.png)

* **[!UICONTROL Gültigkeit explizit festlegen]**: Wenn diese Option nicht angekreuzt ist, müssen die Felder **[!UICONTROL Versandlaufzeit]** und **[!UICONTROL Ressourcen-Gültigkeit]** mit einer Dauer versehen werden.

   Kreuzen Sie diese Option an, wenn Sie Datum und Uhrzeit genau festlegen möchten.

   ![](assets/delivery-set-explicit-dates.png)

* **[!UICONTROL Versandlaufzeit]** / **[!UICONTROL Gültigkeitsgrenze für den Nachrichtenversand]**: Adobe Campaign versendet Nachrichten ab dem Datum des Versandstarts. In diesem Feld lässt sich die Dauer festlegen, innerhalb derer Nachrichten verschickt werden können.

   >[!IMPORTANT]
   >
   >**Sie müssen einen Wert von bis zu 3,5 Tagen definieren.** Wenn Sie einen Wert über 3,5 Tage festlegen, wird dieser nicht berücksichtigt.

* **[!UICONTROL Ressourcen-Gültigkeit]** / **[!UICONTROL Ressourcen]**: In diesem Feld wird die Gültigkeit der hochgeladenen Ressourcen (insbesondere Mirrorseite und Bilder) festgelegt. Die Gültigkeitsdauer der Ressourcen auf dieser Seite ist begrenzt, um Speicherkapazität zu sparen.
* **[!UICONTROL Verwaltung der Mirrorseite]**: Bei der Mirrorseite handelt es sich um eine HTML-Seite, auf die online über einen Webbrowser zugegriffen werden kann. Sie hat den gleichen Inhalt wie die E-Mail. Standardmäßig wird die Mirrorseite automatisch generiert, wenn der entsprechende Link in den Inhalt der E-Mail eingefügt wurde. Die Erzeugung der Seite lässt sich in diesem Feld konfigurieren:

   >[!IMPORTANT]
   >
   >Die Erstellung der Mirrorseite setzt voraus, dass für die E-Mail ein HTML-Inhalt bestimmt worden ist.

   * **[!UICONTROL Mirrorseite erzeugen, wenn der Link im E-Mail-Inhalt erscheint]** (Standardmodus): Die Mirrorseite wird erstellt, wenn der entsprechende Link in den Inhalt der E-Mail eingefügt wird.
   * **Mirrorseitenerzeugung forcieren**: Erstellt eine Mirrorseite, selbst wenn im Versandinhalt kein entsprechender Link enthalten ist.
   * **Keine Mirrorseite erzeugen**: Generiert keine Mirrorseite, selbst wenn in den Nachrichten der entsprechende Link enthalten ist.
   * **Über die Nachrichtenkennung zugängliche Mirrorseite erzeugen**: Diese Option ermöglicht den Zugriff auf den Inhalt der Mirrorseite (einschließlich aller Personalisierungsinformationen) über das Versandlog-Fenster.

>[!NOTE]
>
>Der Parameter **[!UICONTROL Versandlaufzeit]** gilt nicht für Transaktionsnachrichten. Weiterführende Informationen zu Transaktionsnachrichten finden Sie in [diesem Abschnitt](../../channels/using/getting-started-with-transactional-msg.md).

### Tracking-Parameter            {#tracking-parameters}

Im Abschnitt **[!UICONTROL Tracking]** sind folgende Parameter verfügbar:

* **[!UICONTROL Tracking aktivieren]**: Aktivierung/Deaktivierung des Trackings der in den Nachrichten enthaltenen URLs. Über das Symbol **[!UICONTROL Links]** in der Symbolleiste von Email Designer können Sie das Tracking der einzelnen in Nachrichten enthaltenen URLs verwalten. Siehe [Über getrackte URLs](../../designing/using/links.md#about-tracked-urls).
* **[!UICONTROL Ablaufdatum des Trackings]**: Festlegung der Dauer, für die das URL-Tracking aktiv sein soll.
* **[!UICONTROL Ersatz-URL für abgelaufene URLs]**: Hier kann die URL für eine Webseite eingetragen werden, die nach dem Ablauf des Trackings angezeigt wird.

### Erweiterte Parameter {#advanced-parameters}

Der Abschnitt **[!UICONTROL Erweiterte Parameter]** enthält folgende Informationen:

Die ersten Felder dienen zur Eingabe der für die Header von E-Mail-Nachrichten erforderlichen Informationen. Hier können Sie die Antwortadresse und den Text sowie die Absenderadresse (die das Feld „Von:“ ausfüllt) verwalten. Diese Informationen können personalisiert werden.

Klicken Sie auf die Schaltfläche rechts neben dem Feld, das geändert werden soll, und fügen Sie dann das Personalisierungsfeld, den Inhaltsblock oder den dynamischen Text hinzu.

![](assets/advancedparameters.png)

Das Einfügen und Verwenden des Personalisierungsinhalts ist in der Dokumentation zum [Personalisieren von E-Mail-Inhalten](../../designing/using/personalization.md) ausführlich beschrieben.

#### Zielgruppen-Kontext            {#target-context}

Im Zielgruppen-Kontext werden die für die Zielgruppenbestimmung (im Bildschirm zur Audience-Erstellung) und die Personalisierung (Definition von Personalisierungsfeldern, im HTML-Inhaltseditor) der E-Mail verwendeten Tabellen angegeben.

#### Routing            {#routing}

In diesem Feld wird der zu verwendende Routing-Modus definiert. Hierzu wird auf ein externes Konto verwiesen. Dies kann zum Beispiel von Nutzen sein, wenn Sie ein externes Konto mit speziellen Branding-Einstellungen verwenden möchten.

>[!NOTE]
>
>Zu den externen Konten gelangen Sie über das Menü **Administration** > **Anwendungskonfiguration** > **Externe Konten**.

#### Vorbereitung            {#preparation}

Die Vorbereitung von Nachrichten ist im Abschnitt [Nachrichten validieren](../../sending/using/preparing-the-send.md) beschrieben.

* **[!UICONTROL Typologie]**: Vor jedem Versand müssen Nachrichten insofern vorbereitet werden, als ihr Inhalt und ihre Konfiguration zu validieren sind. Die in der Vorbereitungsphase anzuwendenden Validierungsregeln sind in einer **Typologie** festgelegt. Zum Beispiel betrifft die Vorbereitung für E-Mails die Validierung von Betreff, URL und Bildern etc. Wählen Sie in diesem Feld die anzuwendende Typologie aus.

   >[!NOTE]
   >
   >Typologien, zu denen Sie über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Typologien]** gelangen, werden [in diesem Abschnitt](../../sending/using/about-typology-rules.md) beschrieben.

* **[!UICONTROL Titel während der Versandvorbereitung berechnen]**: Ermöglicht die Berechnung des Titelwerts der E-Mail während der Nachrichtenvorbereitung mithilfe von Personalisierungsfeldern, Inhaltsbausteinen und dynamischem Text.

   Sie können auch den Versandtitel mit Ereignisvariablen personalisieren, die in der Aktivität &quot;Externes Signal&quot; des Workflows deklariert wurden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../automating/using/calling-a-workflow-with-external-parameters.md).

* **[!UICONTROL SQL-Abfragen im Protokoll speichern]**: Bei dieser Option werden in der Vorbereitungsphase SQL-Abfragelogs im Protokoll gespeichert.

#### Testversandeinstellungen {#proof-settings}

In diesem Abschnitt können Sie das Standardpräfix konfigurieren, das in der Betreffzeile des Testversands verwendet werden soll. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/sending-proofs.md).

### Liste der E-Mail-SMTP-Parameter {#list-of-email-smtp-parameters}

Im Abschnitt **[!UICONTROL SMTP]** sind folgende Parameter verfügbar:

* **[!UICONTROL Zeichenkodierung]**: Aktivieren Sie die Option **[!UICONTROL Kodierung erzwingen]**, wenn Sie die Nachrichtenkodierung erzwingen möchten, und wählen Sie dann die gewünschte Kodierungsmethode aus.
* **[!UICONTROL Bounce Messages]**: Bounce Messages werden standardmäßig in der Fehler-Inbox der Plattform empfangen (definiert unter **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail]** > **[!UICONTROL Konfiguration).]** Um eine bestimmte Fehleradresse für eine E-Mail zu definieren, geben Sie die jeweilige Adresse im Feld **[!UICONTROL Fehleradresse]** ein.
* **[!UICONTROL Zusätzliche SMTP-Header]**: Mit dieser Option können Sie Ihren Nachrichten zusätzliche SMTP-Header hinzufügen. Das im Feld **[!UICONTROL Header]** eingegebene Skript muss pro Zeile auf einen einzelnen Header (im Format **Name:Wert**) verweisen. Werte werden bei Bedarf automatisch verschlüsselt.

   >[!IMPORTANT]
   >
   >Das Hinzufügen zusätzlicher SMTP-Header ist eine Aufgabe für erfahrene Benutzer. Die Syntax des Skripts muss die Anforderungen für diesen Inhaltstyp (keine überflüssigen Leerzeichen, keine Leerzeilen usw.) erfüllen.

### Liste der Parameter für Zugriffsberechtigung            {#list-of-access-authorization-parameters}

Im Abschnitt **[!UICONTROL Zugriffsberechtigungen]** sind folgende Parameter verfügbar:

* Das Feld **[!UICONTROL Organisationseinheit]** ermöglicht es, den Zugang für diese E-Mail auf bestimmte Nutzer zu begrenzen. Die der spezifizierten Einheit oder den übergeordneten Einheiten zugeteilten Nutzer haben Lese- und Schreibzugriff auf diese E-Mail. Der Zugriff der den untergeordneten Einheiten zugeteilten Nutzer auf diese E-Mail ist schreibgeschützt.

   >[!NOTE]
   >
   >Zur Konfiguration von Organisationseinheiten gehen Sie in das Menü **Administration** > **Benutzer &amp; Sicherheit**.

* Die Felder **[!UICONTROL Erstellt von]**, **[!UICONTROL Erstellt am]**, **[!UICONTROL Geändert von]** und **[!UICONTROL Geändert am]** werden automatisch ausgefüllt.

## Alte Einstellungen {#legacy-settings}

Wenn Sie die neueste Version der Kampagne nicht ausführen, gelten die unten beschriebenen Parameter und UI-Abschnitte weiterhin für Sie.****

### Weitere Zustellversuche {#legacy-retries}

Die **[!UICONTROL Weitere Zustellversuche]**-Einstellungen im [Konfigurationsmenü](#email-channel-parameters) und in den [Sendetsparameter](#retries-parameters) der E-Mail-Eigenschaften geben an, wie viele weitere Zustellversuche am Tag nach dem Start des Versands ausgeführt werden sollen (**[!UICONTROL Anzahl der weitere Zustellversuche]** / **[!UICONTROL Max. Anzahl der weitere Zustellversuche]**) und die minimale Verzögerung zwischen den weiteren Zustellversuchen (**[!UICONTROL Wiederholungszeitraum]**).

Die Anzahl der weitere Zustellversuche kann global geändert werden (wenden Sie sich an Ihren technischen Adobe-Administrator) oder für jeden Versand oder jede Versandvorlage.

Standardmäßig sind innerhalb der ersten 24 Stunden fünf erneute Versuche im Abstand von mindestens einer Stunde vorgesehen. Danach wird eine Wiederholungszeit pro Tag bis zum Versand-Termin programmiert, der global im Bereich **[!UICONTROL Versand-Parameter]** des Menüs **[!UICONTROL Configuration]** oder im Abschnitt **[!UICONTROL Gültigkeitsdauer]** auf Versand-Ebene definiert wird (siehe unten den Abschnitt [Versand-Dauer](#legacy-delivery-duration)).

### Versandlaufzeit {#legacy-delivery-duration}

Mit dem Parameter **[!UICONTROL Dauer des Message-Versands]** im [Konfigurationsmenü](#email-channel-parameters) können Sie den Zeitraum angeben, in dem alle Meldungen im Versand, bei denen ein vorübergehender Fehler oder ein Soft-Absprung auftritt, erneut versucht werden.

Mit der Gültigkeit **[!UICONTROL Dauer des Versands]** oder **[!UICONTROL für das Senden von Nachrichten]** im Abschnitt [Gültigkeitszeitparameter](#validity-period-parameters) können Sie die Dauer angeben, während der die Nachrichten gesendet werden können.

### Regeln zum Umgang mit E-Mails            {#legacy-email-processing-rules}

Die Regeln **[!UICONTROL MX management]**, **[!UICONTROL Absprung-Mails]** und **[!UICONTROL Domänenverwaltung]** können von Administratoren über **[!UICONTROL Administration > Kanal > E-Mail > E-Mail-Verarbeitungsregeln]** [Menü](#email-processing-rules) aufgerufen und geändert werden.

### Bounce-Message-Qualifizierung  {#legacy-bounce-mail-qualification}

Der Zugriff auf die unterschiedlichen Bounce Messages und ihre jeweiligen Fehlertypen und -ursachen erfolgt über das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm. Verwenden Sie dann die Schaltflächen **[!UICONTROL Administration > Kanäle > Quarantänen > Nachrichtenqualifizierung]**.

Folgende Qualifikationsstatus von Bounces treten auf:

* **[!UICONTROL Zu qualifizieren]**: Die Bounce Message konnte nicht qualifiziert werden. Die Qualifikation muss dem Zustellbarkeitsteam unterbreitet werden, um die korrekte Steuerung der Zustellbarkeit der Plattform zu gewährleisten. Nicht qualifizierte Bounce Messages werden nicht zur Anreicherung der E-Mail-Regeln herangezogen.
* **[!UICONTROL Beibehalten]**: Die Bounce Message wurde qualifiziert und wird vom Workflow **Zustellbarkeit** verwendet, um mit den existierenden E-Mail-Regeln verglichen zu werden und eventuell die Liste zu ergänzen.
* **[!UICONTROL Ignorieren]**: Die Bounce Message wurde qualifiziert, wird jedoch nicht vom Workflow **Zustellbarkeit** verwendet. Sie wird somit nicht an die Client-Instanzen weitergeleitet.

<!--Bounces are qualified through the **[!UICONTROL Bounce mails]** processing rule. For more on accessing this rule, refer to this [section](#legacy-bounce-mail-qualification).-->

### Ausgelieferter Indikator-Berichte {#legacy-delivered-status-report}

In der **[!UICONTROL Zusammenfassungs]**-Ansicht der einzelnen Meldungen steigt der **[!UICONTROL Ausgelieferte]**-Prozentwert während der Gültigkeitsdauer des Versands schrittweise an, da die weichen und festen Absprünge zurückgemeldet werden.

An jedem weiteren Tag der Gültigkeitsdauer des Versands werden die Meldungen mit &quot;Weich abschneidend&quot;als **[!UICONTROL Fehlgeschlagen]** nach dem ersten Tag des Versands angezeigt.
