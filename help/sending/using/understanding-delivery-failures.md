---
title: Ursachen von fehlgeschlagenen Sendungen
description: Hier erfahren Sie, wie Sie Zustellprobleme in Campaign vermeiden können.
page-status-flag: never-activated
uuid: 2735aa05-7b6f-47c9-98c4-a15cc33be39d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: 38452841-4cd4-4f92-a5c3-1dfdd54ff6f4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3c45cbbb261f18252689d0fc4f332b9f45137c85

---


# Ursachen von fehlgeschlagenen Sendungen{#understanding-delivery-failures}

## Über fehlgeschlagene Sendungen {#about-delivery-failures}

Wenn einem Profil eine Nachricht nicht zugestellt werden kann, sendet der Remote-Server automatisch eine Fehlermeldung, die von der Adobe-Campaign-Plattform erfasst und qualifiziert wird, um festzustellen, ob die E-Mail-Adresse oder Telefonnummer unter Quarantäne gestellt werden soll. Siehe [Bounce-Message-Qualifizierung](#bounce-mail-qualification).

>[!NOTE]
>
>**E-Mail**-Fehlermeldungen (auch &quot;Bounces&quot; genannt) werden vom inMail-Prozess qualifiziert. **SMS**-Fehlermeldungen (auch &quot;SR&quot; für &quot;Status Report&quot; genannt) werden vom MTA-Prozess qualifiziert.

Mitteilungen können während der Versandvorbereitung auch ausgeschlossen werden, wenn eine Adresse unter Quarantäne gestellt oder ein Profil auf die Blacklist gesetzt wurde. Ausgeschlossene Mitteilungen werden im Versand-Dashboard im Tab **[!UICONTROL Ausschlusslogs]**aufgeführt (siehe[diesen Abschnitt](../../sending/using/monitoring-a-delivery.md#exclusion-logs)).

![](assets/exclusion_logs.png)

**Verwandte Themen:**

* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Blacklists in Campaign verwenden](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## Fehlgeschlagene Sendungen für eine Nachricht identifizieren {#identifying-delivery-failures-for-a-message}

Nachdem eine Nachricht gesendet wurde, können Sie im Tab **[!UICONTROL Versandlogs]**(siehe[diesen Abschnitt](../../sending/using/monitoring-a-delivery.md#sending-logs)) den Versandstatus für jedes Profil sowie den damit verbundenen Fehlschlagstyp und die Ursache einsehen (siehe[Typen und Ursachen für fehlgeschlagene Sendungen](#delivery-failure-types-and-reasons)).

![](assets/sending_logs.png)

Es steht auch ein entsprechender Bericht zur Verfügung. Dieser Bericht zeigt die Gesamtheit aller Statistiken zu bei Sendungen aufgetretenen Hard- und Softbounces und der automatischen Bounce-Verarbeitung. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/bounce-summary.md).

## Typen und Ursachen für fehlgeschlagene Sendungen {#delivery-failure-types-and-reasons}

Bei Fehlschlägen des Versands gibt es drei Typen von Fehlern:

* **Hard**: Dieser Fehlertyp tritt bei einer ungültigen Adresse auf. Fehlermeldung, die explizit eine ungültige Adresse anzeigt, beispielsweise &quot;Benutzer unbekannt&quot;.
* **Soft**: Fehler, der eventuell nur vorübergehend auftritt oder der nicht qualifiziert werden konnte, beispielsweise &quot;Ungültige Domain&quot;, &quot;Postfach voll&quot;.
* **Ignoriert**: Vorübergehender Fehler, beispielsweise &quot;Out of office&quot; oder technischer Fehler bei Absendern vom Typ &quot;Postmaster&quot;.

Mögliche Ursachen für fehlgeschlagene Sendungen sind:

* **[!UICONTROL Unbekannter Nutzer]**(Hardbounce): Die Adresse existiert nicht. An dieses Profil werden keine weiteren Zustellversuche unternommen.
* **[!UICONTROL Adresse in Quarantäne]**(Hardbounce): Die Adresse wurde unter Quarantäne gestellt.
* **[!UICONTROL Unerreichbar]**(Softbounce/Hardbounce): Ein in der Verteilungskette der Nachricht aufgetretener Fehler (Vorfall beim SMTP-Server, zeitweilig unerreichbare Domain usw.). Entsprechend dem vom Dienstleister zurückgegebenen Fehler wird die Adresse direkt unter Quarantäne gestellt oder der Zustellversuch wiederholt, bis Campaign einen Fehler empfängt, der den Quarantänestatus auslöst oder bis die Fehleranzahl 5 erreicht hat.
* **[!UICONTROL Adresse leer]**(Hardbounce): Die Adresse ist nicht definiert.
* **[!UICONTROL Postfach voll]**(Softbounce): Das Postfach eines Benutzers ist voll und kann keine Nachrichten mehr aufnehmen. Die Adresse kann aus der Quarantäne genommen werden, um einen erneuten Zustellversuch zu unternehmen. Diese Liste wird automatisch nach 30 Tagen entfernt.

   Damit die Adresse automatisch aus der Quarantäne genommen werden kann, muss der technische Workflow **[!UICONTROL Datenbankbereinigung]**gestartet sein.

* **[!UICONTROL Abgelehnt]**(Softbounce/Hardbounce): Die Adresse wurde wegen eines Sicherheits-Feedbacks unter Quarantäne gestellt, da die Nachricht als Spam gemeldet wurde. Entsprechend dem vom Dienstleister zurückgegebenen Fehler wird die Adresse direkt unter Quarantäne gestellt oder der Zustellversuch wiederholt, bis Campaign einen Fehler empfängt, der den Quarantänestatus auslöst oder bis die Fehleranzahl 5 erreicht hat.
* **[!UICONTROL Dublette]**: Die Adresse wurde in der Segmentierung bereits erkannt.
* **[!UICONTROL Undefiniert]**(Softbounce): Die Qualifikation der Adresse ist noch nicht abgeschlossen, da die Fehler noch nicht inkrementiert wurden.

   Dieser Fehlertyp tritt auf, wenn der Server eine bis dahin unbekannte Fehlernachricht sendet: Hierbei kann es sich um einen einmaligen Fehler handeln. Sollte er sich jedoch wiederholen, wird der Fehlerzähler erhöht, was die zuständigen technischen Mitarbeiter auf das Problem aufmerksam macht.

* **[!UICONTROL Fehler ignoriert]**: Die Adresse ist auf der Whitelist und erhält E-Mail-Sendungen.
* **[!UICONTROL Adresse auf der Blacklist]**: Zum Zeitpunkt des Versands war die Adresse auf der Blacklist.
* **[!UICONTROL Konto deaktiviert]**(Softbounce/Hardbounce): Wenn das Konto längere Zeit nicht abgefragt wird, kann es vom Internetanbieter geschlossen werden, was den Versand an diese Empfängeradresse unmöglich macht. Ob es sich um einen Softbounce oder Hardbounce handelt, hängt vom empfangenen Fehlertyp ab: Wenn das Konto vorübergehend wegen einer sechsmonatigen Inaktivität deaktiviert ist und wieder aktiviert werden kann, wird der Status**[!UICONTROL  Mit Fehlern]** zugewiesen und der Zustellversuch wird wiederholt. Wenn das Konto permanent deaktiviert ist, wird es sofort unter Quarantäne gestellt.
* **[!UICONTROL Nicht angemeldet]**: Mobiltelefon des Profils war bei Versand der Nachricht ausgeschaltet oder verfügte über keinen Netzempfang.
* **[!UICONTROL Ungültige Domain]**(Softbounce): Domain der E-Mail-Adresse ist fehlerhaft oder existiert nicht mehr. An dieses Profil werden wiederholte Zustellversuche unternommen, bis die Fehleranzahl 5 erreicht. Danach wird der Datensatz in den Quarantänestatus versetzt und die Zustellversuche werden eingestellt.
* **[!UICONTROL Text zu lang]**: Die Zeichenzahl der SMS-Nachricht übersteigt das Limit. Weiterführende Informationen dazu finden Sie im Abschnitt[Kodierung, Länge und Tansliteration von SMS](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).
* **[!UICONTROL Zeichen wird in der Kodierung nicht unterstützt]**: Die SMS enthält mindestens ein Zeichen, das in der Kodierung nicht unterstützt wird. Weiterführende Informationen dazu finden Sie im Abschnitt[Zeichensatztabelle - GSM-Standard](../../administration/using/configuring-sms-channel.md#table-of-characters---gsm-standard).

## Weitere Zustellversuche nach einem vorübergehend fehlgeschlagenen Versand {#retries-after-a-delivery-temporary-failure}

Wenn die Zustellung einer Nachricht wegen eines vorübergehenden Fehlers des Typs **Ignoriert** fehlschlägt, werden während der Versandlaufzeit weitere Zustellversuche unternommen. Weiterführende Informationen zu Fehlertypen finden Sie im Abschnitt [Typen und Ursachen für fehlgeschlagene Sendungen](#delivery-failure-types-and-reasons).

Gehen Sie zur Änderung der Versandlaufzeit in die erweiterten Eigenschaften des Versands oder seiner Vorlage und geben Sie im entsprechenden Feld die gewünschte Dauer ein. Weiterführende Informationen zu den erweiterten Versandeigenschaften finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md#validity-period-parameters).

Standardmäßig sind innerhalb der ersten 24 Stunden fünf Versuche im Abstand von mindestens einer Stunde vorgesehen, an den vier folgenden Tagen je ein Versuch. Die Anzahl weiterer Versuche kann global geändert werden (kontaktieren Sie Ihren technischen Administrator von Adobe) oder für jeden Versand oder jede Versandvorlage (siehe [diesen Abschnitt](../../administration/using/configuring-email-channel.md#sending-parameters)).

## Synchrone und asynchrone Fehler {#synchronous-and-asynchronous-errors}

Ein Versand kann sofort fehlschlagen (synchroner Fehler) oder zu einem späteren Zeitpunkt nach dem Versand (asynchroner Fehler).

* **Synchroner Fehler**: Der vom Adobe-Campaign-Server angesprochene Remote-Server hat sofort eine Fehlermeldung zurückgegeben. Die Nachricht kann nicht an den Server des Profils gesendet werden.
* **Asynchroner Fehler**: Eine Bounce Message oder ein Statusbericht (SR) wird vom Remote-Server verzögert zurückgesendet. Asynchrone Fehler können bis zu eine Woche nach einem Versand auftreten.

## Bounce-Message-Qualifizierung {#bounce-mail-qualification}

Fehlermeldungen wegen Lieferausfallfehlers (oder &quot;SMTP-Absprungantworten&quot;) werden von der Adobe Campaign-Plattform abgerufen und anschließend mithilfe der Datenbank für die **Zustellungsprotokollqualifikation**, **Soft** oder **Ignoriert** verarbeitet und qualifiziert ****.

<!--Delivery failure error messages (or "bounces") are picked up by the Adobe Campaign platform and qualified by the inMail process to enrich the list of email management rules.(applies to asynchronous (out-of-band) bounces)-->

Diese Liste steht nur Administratoren bereit und enthält alle von Adobe Campaign für die Qualifizierung von fehlgeschlagenen Sendungen verwendeten Regeln.

Der Zugriff auf diese Liste erfolgt über das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm. Verwenden Sie dann die Schaltflächen**[!UICONTROL  Administration > Kanäle > E-Mail > Regeln zum Umgang mit E-Mails]**.

Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../administration/using/configuring-email-channel.md#email-processing-rules).

>[!IMPORTANT]
>
>Nach der Aktualisierung auf die erweiterte MTA werden die Absprungqualifikationen in der Qualifizierungstabelle für **[!UICONTROL Kampagnenmeldungen]**nicht mehr verwendet. Bei Meldungen mit Fehlern bei synchroner Bereitstellung bestimmt die erweiterte MTA den Absprungtyp und die Qualifikation und sendet diese Informationen an Kampagne zurück. Asynchrone Absprünge werden weiterhin vom InMail-Prozess qualifiziert.
>
>Weitere Informationen zur erweiterten MTA-Datei für Adobe Campaign finden Sie in diesem [Dokument](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html).

Folgende Qualifikationsstatus von Bounces treten auf:

* **[!UICONTROL Zu qualifizieren]**: Die Bounce Message konnte nicht qualifiziert werden. Die Qualifikation muss dem Zustellbarkeitsteam unterbreitet werden, um die korrekte Steuerung der Zustellbarkeit der Plattform zu gewährleisten. Nicht qualifizierte Bounce Messages werden nicht zur Anreicherung der E-Mail-Regeln herangezogen.
* **[!UICONTROL Beibehalten]**: Die Bounce Message wurde qualifiziert und wird vom Workflow** Zustellbarkeit **verwendet, um mit den existierenden E-Mail-Regeln verglichen zu werden und eventuell die Liste zu ergänzen.
* **[!UICONTROL Ignorieren]**: Die Bounce Message wurde qualifiziert, wird jedoch nicht vom Workflow** Zustellbarkeit **verwendet. Sie wird somit nicht an die Client-Instanzen weitergeleitet.

Der Zugriff auf die unterschiedlichen Bounce Messages und ihre jeweiligen Fehlertypen und -ursachen erfolgt über das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm. Verwenden Sie dann die Schaltflächen**[!UICONTROL  Administration > Kanäle > Quarantänen > Nachrichtenqualifizierung]**.

![](assets/qualification.png)

## Zustellbarkeit von Mails durch die Anmeldung mit zweifacher Bestätigung optimieren {#optimizing-mail-deliverability-with-double-opt-in-mechanism}

Die Anmeldung mit zweifacher Bestätigung zählt zu den Best Practices beim E-Mail-Versand. Die Plattform wird dadurch vor falschen oder ungültigen E-Mail-Adressen und Spambots geschützt, wodurch Spam-Beschwerden verhindert werden.

Das Prinzip dahinter ist folgendes: Der Besucher füllt ein Formular auf einer Online-Landingpage aus, erhält dann eine E-Mail und muss den Bestätigungs-Link anklicken, um die Anmeldung abzuschließen. Erst dann wird er als ‘Profil&#39; in der Campaign-Datenbank gespeichert.

Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/setting-up-a-double-opt-in-process.md).
