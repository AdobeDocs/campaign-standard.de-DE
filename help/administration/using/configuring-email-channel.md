---
title: E-Mail-Kanal konfigurieren
seo-title: E-Mail-Kanal konfigurieren
description: E-Mail-Kanal konfigurieren
seo-description: Hier erfahren Sie, wie Sie den E-Mail-Kanal konfigurieren.
page-status-flag: nie aktiviert
uuid: 9 fddb 655-b 445-41 f 3-9 b 02-5 d 356 fc 88 aa 1
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Administration
content-type: Referenz
topic-tags: configuring-channels
discoiquuid: 3752 d 41 f -8 c 59-4 path-b 30 f-e 98 e 09 cd 74 a 8
context-tags: Extaccountemail, overview; Emailconfig, main; Ruleset, overview; Bereitstellung, Eigenschaften, öffnen
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4d95fe00c1958399ff4d22d5f0e7762f895b4032

---


# E-Mail-Kanal konfigurieren{#configuring-email-channel}

## Parameter für den E-Mail-Kanal {#email-channel-parameters}

Im E-Mail-Konfigurationsfenster können Sie die Parameter für den E-Mail-Kanal definieren.

![](assets/channels_1.png)

* **Header-Parameter für ausgehende E-Mails**

   In diesem Bereich können Sie **[!UICONTROL Zulässige Masken]für die Absender- und Fehleradressen definieren.** Bei Angabe von mehr als einer Maske sind die Masken durch Kommata zu trennen. Hierbei handelt es sich um eine optionale Konfiguration. Wenn diese Felder ausgefüllt sind, prüft Adobe Campaign im Zuge der Nachrichtenvorbereitung, dass die in der E-Mail angegebenen Adressen gültig sind. Auf diese Weise vermeiden Sie die Verwendung von Adressen, die Probleme bei der Zustellbarkeit bereiten könnten. Absenderadressen sind auf dem Versandserver zu konfigurieren.

* **Zustellbarkeit**

   Diese Kennung wird Ihnen vom Support mitgeteilt. Sie ist für die korrekte Funktionsweise der Zustellbarkeitsberichte erforderlich.

* **Versandparameter**

   Adobe Campaign versendet Nachrichten ab dem Datum des Versandstarts. Im Feld **[!UICONTROL Dauer des Nachrichtenversands]lässt sich die Dauer festlegen, innerhalb derer Nachrichten verschickt werden können.**

   Das Feld **[!UICONTROL Gültigkeit der Online-Ressourcen]wird für Ressourcen verwendet, die online verfügbar sind, insbesondere für Mirrorseiten und Bilder.** Die Gültigkeitsdauer der Ressourcen auf dieser Seite ist begrenzt, um Speicherkapazität zu sparen.

* **Weitere Zustellversuche**

   Nachrichten, die vorläufig nicht zugestellt werden können, werden automatisch für einen erneuten Versuch vorgesehen. Geben Sie in diesem Bereich an, wie viele weitere Zustellversuche am ersten Tag nach dem Versandstart unternommen werden sollen (**Anzahl weiterer Versuche**), sowie die minimale Zeitspanne zwischen zwei Versuchen (**Versuchsintervall**).

   Standardmäßig sind innerhalb der ersten 24 Stunden fünf erneute Versuche im Abstand von mindestens einer Stunde vorgesehen. An den folgenden Tagen und bis zum Ablauf der Versandgültigkeit, die im Bereich **[!UICONTROL Versandparameter]angegeben wird, wird jeweils ein Zustellversuch unternommen.**

* **Quarantäne-Parameter der E-Mails**

   Geben Sie im Feld **[!UICONTROL Intervall zwischen zwei signifikanten Fehlern]einen Wert an, um die Wartezeit zu definieren, bevor der Fehlerzähler im Fall eines Fehlschlagens um einen Wert erhöht wird.** Standardwert: **"1d"** für 1 Tag.

   Wenn der Wert **[!UICONTROL Maximale Anzahl an Fehlern vor der Quarantäne]erreicht ist, wird die E-Mail-Adresse unter Quarantäne gestellt.** Standardwert: **"5"**: Die Adresse wird beim sechsten Fehler unter Quarantäne gestellt. Dies bedeutet, dass der Kontakt automatisch von den nächsten Sendungen ausgeschlossen wird.

**Verwandtes Thema**:

[Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)

## E-Mail-Routing-Konten {#email-routing-accounts}

Das externe Konto **[!UICONTROL Integriertes E-Mail-Routing]wird standardmäßig bereitgestellt.** Es enthält die technischen Parameter, die es der Anwendung erlauben, E-Mails zu senden.

![](assets/channels_2.png)

Dabei ist der Kontotyp mit **[!UICONTROL Routing]**, der Kanal mit **[!UICONTROL E-Mail]** und der Versandmodus mit **Gebündelter Versand[!UICONTROL zu konfigurieren]**.

**Verwandtes Thema**:

[Externe Konten](../../administration/using/external-accounts.md)

## Regeln zum Umgang mit E-Mails {#email-processing-rules}

In den Regeln sind die von Remote-Servern potenziell zurückgegebenen Strings enthalten, die die Qualifizierung der Fehler in **Hardbounce**, **Softbounce** oder **Ignoriert** erlauben.

Folgende Regeln sind in der Standardkonfiguration vorgesehen:

**Bounce Messages**

Wenn die Zustellung einer E-Mail fehlschlägt, gibt der Remote-Server eine Fehlermeldung an die in den Plattform-Parametern angegebene Bounce-Adresse zurück. Adobe Campaign vergleicht den Inhalt jeder Bounce-E-Mail mit den in der Regelliste verzeichneten Strings und ordnet einen der drei Fehlertypen zu.

Der Benutzer kann eigene Regeln erstellen.

>[!CAUTION]
>
>Beim Import eines Packages und bei der Aktualisierung von Daten durch den **Zustellbarkeit**-Workflow werden benutzerdefinierte E-Mail-Regeln überschrieben.

**E-Mail-Domain-Verwaltung**

Domain-Verwaltungsregeln ermöglichen die Regulierung des Volumens der ausgehenden E-Mails nach Domains. Sie analysieren die Bounce Messages und blockieren falls nötig den Versand. Der Adobe-Campaign-E-Mail-Server wendet zunächst die spezifischen Domain-Regeln an und im Anschluss jene, die den Normalfall repräsentieren (durch * gekennzeichnet). Die Regeln für Hotmail und MSN sind standardmäßig in Adobe Campaign enthalten.

Um eigene Domain-Verwaltungsregeln zu erstellen, sind die Angabe einer Schwelle und die Auswahl gewisser SMTP-Parameter erforderlich. Die **Schwelle** entspricht einem Prozentsatz an Fehlern, der bei Überschreiten den Versand an die betroffene Domain unterbricht.

So wird beispielsweise der Versand drei Stunden lang unterbrochen, wenn bei einem Volumen von mindestens 300 Nachrichten die Fehlerquote 90% erreicht.

Die **SMTP-Parameter** agieren wie die im Falle einer Blockierungsregel angewendeten Filter.

* Sie haben die Möglichkeit, gewisse Authentifizierungsnormen und Verschlüsselungsschlüssel zu aktivieren, um den Domain-Namen zu prüfen: **Sender ID**, **DomainKeys**, **DKIM**, **S/MIME**.
* **SMTP-Relais**: Zur Konfiguration der IP-Adresse und des Relais-Server-Ports für eine bestimmte Domain.

**MX-Verwaltung**

Jede Regel definiert eine Adressenmaske des MX. Jeder MX, dessen Name dieser Adressenmaske entspricht, kommt somit infrage. Die Maske kann die Joker "*" und "?" enthalten.

So sind die Adressen

* a.mx.yahoo.com
* b.mx.yahoo.com
* c.mx.yahoo.com

mit folgenden Masken kompatibel:

* *.yahoo.com
* ?.mx.yahoo.com

Die erste Regel, deren MX-Maske mit dem gewünschten MX kompatibel ist, wird angewendet.

Folgende Parameter stehen für jede einzelne Regel zur Verfügung:

* **[!UICONTROL Öffentliche Kennungen]**: Diese Option ermöglicht die Angabe der von der Regel betroffenen öffentlichen Kennungen (publicId). Folgende Angaben sind möglich:

   * Eine Ziffer: Die Regel wird nur für diese publicId angewendet.
   * Ein Ziffernbereich (Ziffer1-Ziffer2): Die Regel wird für alle in diesem Bereich enthaltenen publicId angewendet.
   Wenn nicht anders angegeben, wird die Regel für alle Kennungen angewendet.

* **[!UICONTROL Freigegeben]**: Diese Option ermöglicht die Angabe, ob die Obergrenze an Nachrichten pro Stunde und an zulässigen Verbindungen für alle der Regel zugeordneten MX angewendet wird oder nicht.
* **[!UICONTROL Maximale Verbindungsanzahl]**: maximale Anzahl an simultanen Verbindungen mit einem MX von einer Adresse ausgehend.
* **Maximale Nachrichtenanzahl**: maximale Anzahl an Nachrichten, die von einer Verbindung aus gesendet werden können. Bei der Übersteigung der zulässigen Höchstwerte wird die Verbindung geschlossen und eine neue hergestellt.
* **[!UICONTROL Nachrichten pro Stunde]**: maximale Anzahl an Nachrichten, die pro Stunde ausgehend von einer Adresse an einen MX gesendet werden können.

>[!CAUTION]
>
>* Nach Änderungen in der Konfiguration muss der Versandserver (MTA) neu gestartet werden.
>* Neuerstellung und Änderungen von Verwaltungsregeln sollten erfahrenen Benutzern vorbehalten bleiben.
>



## Liste der E-Mail-Eigenschaften {#list-of-email-properties}

Dieser Abschnitt behandelt die Liste von Parametern, die in den Eigenschaften einer E-Mail oder einer [E-Mail-Vorlage](../../start/using/about-templates.md) verfügbar sind.

>[!NOTE]
>
>Manche Parameter sind ausschließlich über die Vorlagen verfügbar. Die Parameter, auf die Sie zugreifen können, [hängen von Ihrer Zugriffsberechtigung ab](../../administration/using/users-management.md).

Zur Änderung der Eigenschaften einer E-Mail bzw. einer E-Mail-Vorlage verwenden Sie die Schaltfläche **[!UICONTROL Eigenschaften bearbeiten].**

![](assets/delivery_options_1.png)

### Allgemeine Parameter {#general-parameters}

Identifizieren Sie am oberen Rand des E-Mail-Parameter-Fensters die E-Mail unter Verwendung der Felder **[!UICONTROL Titel]** und **ID[!UICONTROL .]** Diese Informationen erscheinen in der Benutzeroberfläche, sind aber für die Empfänger nicht sichtbar.

![](assets/delivery_options_2.png)

>[!CAUTION]
>
>Die Kennung muss eindeutig sein.

Das Feld **[!UICONTROL Marke]dient der Auswahl der dem Versand zugeordneten Marke.** Weiterführende Informationen zur Verwendung und Konfiguration von Marken finden Sie im Abschnitt [Marken](../../administration/using/branding.md).

Im Feld **[!UICONTROL Kampagne]kann die der E-Mail übergeordnete Kampagne eingetragen werden.**

Außerdem kann man im entsprechenden Feld eine **[!UICONTROL Beschreibung]hinzufügen und das Bild ändern, das auf der E-Mail-Karte innerhalb der Listen angezeigt wird.**

### Versandparameter {#sending-parameters}

Der Bereich **[!UICONTROL Senden]ist nur für E-Mail-Vorlagen verfügbar.** Darin sind die folgenden Parameter enthalten:

#### Parameter für weitere Zustellversuche {#retries-parameters}

Nachrichten, die vorläufig nicht zugestellt werden können, werden automatisch für einen erneuten Versuch vorgesehen. Geben Sie in diesem Bereich an, wie viele weitere Zustellversuche am ersten Tag nach dem Versandstart unternommen werden sollen (**[!UICONTROL Maximale Versuchsanzahl]**), sowie die Mindestzeitspanne zwischen zwei Versuchen (**[!UICONTROL Versuchsintervall]** ).

Standardmäßig sind innerhalb der ersten 24 Stunden fünf erneute Versuche im Abstand von mindestens einer Stunde vorgesehen. An den folgenden Tagen und bis zum Ablauf der Versandgültigkeit, die im Bereich [Parameter für den Gültigkeitszeitraum](../../administration/using/configuring-email-channel.md#validity-period-parameters) angegeben ist, wird jeweils ein Zustellversuch unternommen.

Die Anzahl weiterer Versuche kann global geändert werden (kontaktieren Sie Ihren technischen Administrator von Adobe) oder einzeln für jeden Versand oder jede Versandvorlage.

Mit der Option **[!UICONTROL SMTP-Versand testen]können Sie den Nachrichtenversand per SMTP testen.** Die Nachrichten werden verarbeitet, bis eine Verbindung mit dem SMTP-Server hergestellt wurde, sie werden aber nicht gesendet. Weiterführende Informationen zur SMTP-Konfiguration finden Sie im Abschnitt [Liste der E-Mail-SMTP-Parameter](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters).

#### Parameter für E-Mail-Format {#email-format-parameters}

Sie können das Format der zu sendenden E-Mails konfigurieren. Dabei stehen drei Optionen zur Verfügung:

* **Empfängervorlieben berücksichtigen** (Standardmodus): Das Nachrichtenformat wird auf der Grundlage der im Empfängerprofil gespeicherten Daten definiert und standardmäßig im Feld **E-Mail-Format** (@emailFormat) gespeichert. Falls ein Empfänger Nachrichten in einem bestimmten Format erhalten möchte, werden sie in diesem Format gesendet. Ohne Angabe in diesem Feld wird eine Nachricht vom Typ „Multipart-Alternative“ gesendet, wie im Anschluss erläutert.
* **E-Mail-Programm des Empfängers das beste Format wählen lassen (multipart-alternative)**: Die Meldung enthält sowohl das Text- als auch das HTML-Format. Welches Format beim Empfänger angezeigt wird, hängt von der Konfiguration des E-Mail-Programms des Empfängers ab (Multipart-Alternative).

   >[!CAUTION]
   >
   >Diese Option umfasst beide Versionen der Nachricht. Dies hat Auswirkungen auf den Versanddurchsatz, da die Nachricht dadurch größer wird.

* **Alle Nachrichten im Textformat senden**: Die Nachricht wird im Textformat gesendet. Das HTML-Format wird nicht gesendet und lediglich für die Mirrorseite verwendet, wenn der Empfänger auf den Link in der Nachricht klickt.

### Parameter für den Gültigkeitszeitraum {#validity-period-parameters}

Im Abschnitt **[!UICONTROL Gültigkeitszeitraum]sind folgende Parameter verfügbar:**

* **[!UICONTROL Gültigkeit explizit festlegen]**: Wenn diese Option nicht angekreuzt ist, müssen die Felder **[!UICONTROL Versandlaufzeit]** und **Ressourcen-Gültigkeit]mit einer Dauer versehen werden.[!UICONTROL ** Kreuzen Sie diese Option an, wenn Sie Datum und Uhrzeit genau festlegen möchten.
* **[!UICONTROL Versandlaufzeit]**: Nachrichten werden von Adobe Campaign ab dem Datum des Versandstarts versendet. In diesem Feld lässt sich die Dauer festlegen, innerhalb derer Nachrichten verschickt werden können.
* **[!UICONTROL Ressourcen-Gültigkeit]**: An dieser Stelle wird die Gültigkeit der Online-Ressourcen (vor allem Mirrorseite und Bilder) festgelegt. Die Gültigkeitsdauer der Ressourcen auf dieser Seite ist begrenzt, um Speicherkapazität zu sparen.
* **[!UICONTROL Verwaltung der Mirrorseite]**: Bei der Mirrorseite handelt es sich um eine HTML-Seite, auf die online über einen Webbrowser zugegriffen werden kann. Sie hat den gleichen Inhalt wie die E-Mail. Standardmäßig wird die Mirrorseite automatisch generiert, wenn der entsprechende Link in den Inhalt der E-Mail eingefügt wurde. Die Erzeugung der Seite lässt sich in diesem Feld konfigurieren:

   >[!CAUTION]
   >
   >Die Erstellung der Mirrorseite setzt voraus, dass für die E-Mail ein HTML-Inhalt bestimmt worden ist.

   * **[!UICONTROL Mirrorseite erzeugen, wenn der Link im E-Mail-Inhalt erscheint]** (Standardmodus): Die Mirrorseite wird erstellt, wenn der entsprechende Link in den Inhalt der E-Mail eingefügt wird.
   * **Mirrorseitenerzeugung forcieren**: Erstellt eine Mirrorseite, selbst wenn im Versandinhalt kein entsprechender Link enthalten ist.
   * **Keine Mirrorseite erzeugen**: Generiert keine Mirrorseite, selbst wenn in den Nachrichten der entsprechende Link enthalten ist.
   * **Über die Nachrichtenkennung zugängliche Mirrorseite erzeugen**: Diese Option ermöglicht den Zugriff auf den Inhalt der Mirrorseite (einschließlich aller Personalisierungsinformationen) über das Versandlog-Fenster.

>[!NOTE]
>
>Die Parameter **[!UICONTROL Gültigkeit explizit festlegen]** und **Versandlaufzeit]gelten nicht für Transaktionsnachrichten.[!UICONTROL ** Weiterführende Informationen zu Transaktionsnachrichten finden Sie in [diesem Abschnitt](../../channels/using/about-transactional-messaging.md).

### Trackingparameter {#tracking-parameters}

Im Abschnitt **[!UICONTROL Tracking]sind folgende Parameter verfügbar:**

* **[!UICONTROL Tracking aktivieren]**: Aktivierung/Deaktivierung des Trackings der in den Nachrichten enthaltenen URLs. Über das Symbol **[!UICONTROL Links]in der Symbolleiste von Email Designer können Sie das Tracking der einzelnen in Nachrichten enthaltenen URLs verwalten.** Siehe [Über getrackte URLs](../../designing/using/about-tracked-urls.md).
* **[!UICONTROL Ablaufdatum des Trackings]**: Festlegung der Dauer, für die das URL-Tracking aktiv sein soll.
* **[!UICONTROL Ersatz-URL für abgelaufene URLs]**: Hier kann die URL für eine Webseite eingetragen werden, die nach dem Ablauf des Trackings angezeigt wird.

### Erweiterte Parameter {#advanced-parameters}

Der Abschnitt **[!UICONTROL Erweiterte Parameter]enthält folgende Informationen:**

Angaben zum E-Mail-Header (Antwortadresse und Text der Antwortadresse). Diese Informationen können personalisiert werden. Öffnen Sie mithilfe der Schaltfläche rechts des entsprechenden Eingabefelds das Auswahlfenster und fügen Sie die gewünschten Personalisierungsfelder ein. Weiterführende Informationen zur Verwendung der Personalisierungsfelder finden Sie im Abschnitt [Personalisierungsfelder einfügen](../../designing/using/inserting-a-personalization-field.md).

#### Zielgruppen-Kontext {#target-context}

Im Zielgruppen-Kontext werden die für die Zielgruppenbestimmung (im Bildschirm zur Audience-Erstellung) und die Personalisierung (Definition von Personalisierungsfeldern, im HTML-Inhaltseditor) der E-Mail verwendeten Tabellen angegeben.

#### Routing {#routing}

In diesem Feld wird der zu verwendende Routing-Modus definiert. Hierzu wird auf ein externes Konto verwiesen. Dies kann zum Beispiel von Nutzen sein, wenn Sie ein externes Konto mit speziellen Branding-Einstellungen verwenden möchten.

>[!NOTE]
>
>Zu den externen Konten gelangen Sie über das Menü **Administration** &gt; **Anwendungskonfiguration** &gt; **Externe Konten**.

#### Vorbereitung {#preparation}

Die Vorbereitung von Nachrichten ist im Abschnitt [Nachrichten validieren](../../sending/using/preparing-the-send.md) beschrieben.

* **[!UICONTROL Typologie]**: Vor jedem Versand müssen Nachrichten insofern vorbereitet werden, als ihr Inhalt und ihre Konfiguration zu validieren sind. Die in der Vorbereitungsphase anzuwendenden Validierungsregeln sind in einer **Typologie** festgelegt. Zum Beispiel betrifft die Vorbereitung für E-Mails die Validierung von Betreff, URL und Bildern etc. Wählen Sie in diesem Feld die anzuwendende Typologie aus.

   >[!NOTE]
   >
   >Typologies, which can be accessed via the **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Typologies]** menu, are presented in the [Typologies](../../administration/using/about-typology-rules.md) section.

* **[!UICONTROL Die Beschriftung während der Vorbereitung der Bereitstellung berechnen]**: ermöglicht es Ihnen, den Beschriftungswert der E-Email während der Nachrichtenvorbereitung mithilfe von Personalisierungsfeldern, Inhaltsblöcken und dynamischen Text zu berechnen.

   Es ist außerdem möglich, die Bereitstellungsbeschriftung mit Ereignisvariablen zu personalisieren, die in der externen Signalaktivität des Workflows deklariert wurden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../automating/using/calling-a-workflow-with-external-parameters.md).

* **[!UICONTROL SQL-Abfragen im Protokoll speichern]**: Bei dieser Option werden in der Vorbereitungsphase SQL-Abfragelogs im Protokoll gespeichert.

### Liste der E-Mail-SMTP-Parameter {#list-of-email-smtp-parameters}

Im Abschnitt **[!UICONTROL SMTP]sind folgende Parameter verfügbar:**

* **[!UICONTROL Zeichenkodierung]**: Aktivieren Sie die Option **[!UICONTROL Kodierung erzwingen], wenn Sie die Nachrichtenkodierung erzwingen möchten, und wählen Sie dann die gewünschte Kodierungsmethode aus.**
* **[!UICONTROL Absprungmeldungen]**: standardmäßig werden die Absprungmeldungen im Infofeld der Plattform empfangen (definiert in " **[!UICONTROL Administration]** «&gt; **[!UICONTROL " Kanäle]** «&gt; **[!UICONTROL "E-Mail]** " &gt;" **[!UICONTROL Konfiguration"]** ). Um eine bestimmte Fehleradresse für eine E-Mail zu definieren, geben Sie die jeweilige Adresse im Feld **[!UICONTROL Fehleradresse]ein.**
* **[!UICONTROL Zusätzliche SMTP-Header]**: Mit dieser Option können Sie Ihren Nachrichten zusätzliche SMTP-Header hinzufügen. Das im Feld **[!UICONTROL Header]** eingegebene Skript muss pro Zeile auf einen einzelnen Header (im Format **Name:Wert**) verweisen. Werte werden bei Bedarf automatisch verschlüsselt.

   >[!CAUTION]
   >
   >Das Hinzufügen zusätzlicher SMTP-Header ist eine Aufgabe für erfahrene Benutzer. Die Syntax des Skripts muss die Anforderungen für diesen Inhaltstyp (keine überflüssigen Leerzeichen, keine Leerzeilen usw.) erfüllen.

### Liste der Parameter für Zugriffsberechtigung {#list-of-access-authorization-parameters}

Im Abschnitt **[!UICONTROL Zugriffsberechtigungen]sind folgende Parameter verfügbar:**

* Das Feld **[!UICONTROL Organisationseinheit]ermöglicht es, den Zugang für diese E-Mail auf bestimmte Nutzer zu begrenzen.** Die der spezifizierten Einheit oder den übergeordneten Einheiten zugeteilten Nutzer haben Lese- und Schreibzugriff auf diese E-Mail. Der Zugriff der den untergeordneten Einheiten zugeteilten Nutzer auf diese E-Mail ist schreibgeschützt.

   >[!NOTE]
   >
   >Zur Konfiguration von Organisationseinheiten gehen Sie in das Menü **Administration** &gt; **Benutzer &amp; Sicherheit**.

* The **[!UICONTROL Created by]**, **[!UICONTROL Created]**, **[!UICONTROL Modified by]** and **[!UICONTROL Last modified]** fields are automatically completed.

## E-Mails archivieren {#archiving-emails}

Sie können Adobe Campaign so konfigurieren, dass von den von der Plattform gesendeten E-Mails eine Kopie beibehalten wird.

Adobe Campaign selbst ermöglicht zwar nicht die Verwaltung von archivierten Dateien, Sie können aber die gewünschten Nachrichten an eine bestimmte Adresse senden, wo sie mithilfe eines externen Systems verarbeitet und archiviert werden.

Wenn diese Funktion in der Versandvorlage aktiviert wird, können Sie eine exakte Kopie der gesendeten Nachrichten an eine von Ihnen bestimmte BCC-E-Mail-Adresse senden (unsichtbar für die Nachrichtenempfänger).

### Empfehlungen und Einschränkungen {#recommendations-and-limitations}

* Hierbei handelt es sich um eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.
* Sie können nur eine einzige BCC-E-Mail-Adresse verwenden.
* Nur erfolgreich gesendete E-Mails werden berücksichtigt. Bounces werden nicht berücksichtigt.
* Aus Datenschutzgründen müssen BCC-E-Mails von einem Archivierungssystem bearbeitet werden, in dem personenbezogene Daten (PII, Personally Identifiable Information) sicher aufbewahrt werden.
* Bei der Erstellung einer neuen Versandvorlage ist E-Mail-BCC nicht standardmäßig aktiviert, selbst wenn diese Option erworben wurde. Sie muss manuell in jeder Versandvorlage aktiviert werden, in der sie verwendet werden soll.

### E-Mail-Archivierung aktivieren {#activating-email-archiving}

E-Mail-BCC wird in der [E-Mail-Vorlage](../../start/using/about-templates.md) über die folgende Option aktiviert:

1. Gehen Sie in den Knoten **Ressourcen** &gt; **Vorlagen** &gt; **Versandvorlagen**.
1. Duplizieren Sie die Standardvorlage **[!UICONTROL Per E-Mail versenden].**
1. Wählen Sie die duplizierte Vorlage aus.
1. Bearbeiten Sie mithilfe der Schaltfläche **[!UICONTROL Eigenschaften bearbeiten]die Eigenschaften Ihrer Vorlage.**
1. Maximieren Sie den Abschnitt **[!UICONTROL Senden].**
1. Aktivieren Sie die Option **[!UICONTROL E-Mails archivieren], um eine Kopie aller gesendeten, auf dieser Vorlage basierenden Nachrichten aufzubewahren.**

   ![](assets/email_archiving.png)

>[!NOTE]
>
>Wenn die an eine BCC-Adresse gesendeten E-Mails geöffnet und angeklickt werden, wird dies in **[!UICONTROL Gesamtöffnungen]** und **Klicks]der Versandanalyse berücksichtigt, was zu falschen Berechnungen führen könnte.[!UICONTROL **

