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
source-git-commit: f1db8c886e560fe3f57d589b7fc2f2c2c1656f76

---


# Ursachen von fehlgeschlagenen Sendungen{#understanding-delivery-failures}

## Über fehlgeschlagene Sendungen {#about-delivery-failures}

Wenn einem Profil eine Nachricht nicht zugestellt werden kann, sendet der Remote-Server automatisch eine Fehlermeldung, die von der Adobe-Campaign-Plattform erfasst und qualifiziert wird, um festzustellen, ob die E-Mail-Adresse oder Telefonnummer unter Quarantäne gestellt werden soll. Siehe [Bounce-Message-Qualifizierung](#bounce-mail-qualification).

>[!NOTE]
>
>**E-Mail** -Fehlermeldungen (oder &quot;Absprünge&quot;) werden durch das erweiterte MTA (synchrone Absprünge) oder den InMail-Prozess (asynchrone Absprünge) qualifiziert. **SMS**-Fehlermeldungen (auch &quot;SR&quot; für &quot;Status Report&quot; genannt) werden vom MTA-Prozess qualifiziert.

Mitteilungen können während der Versandvorbereitung auch ausgeschlossen werden, wenn eine Adresse unter Quarantäne gestellt oder ein Profil auf die Blacklist gesetzt wurde. Excluded messages are listed in the **[!UICONTROL Exclusion logs]** tab of the delivery dashboard (see [this section](../../sending/using/monitoring-a-delivery.md#exclusion-logs)).

![](assets/exclusion_logs.png)

**Verwandte Themen:**

* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Blacklists in Campaign verwenden](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## Fehlgeschlagene Sendungen für eine Nachricht identifizieren  {#identifying-delivery-failures-for-a-message}

Once a delivery is sent, the **[!UICONTROL Sending logs]** tab (see [this section](../../sending/using/monitoring-a-delivery.md#sending-logs)) allows you to view the delivery status for each profile and the associated failure type and reason (see [Delivery failure types and reasons](#delivery-failure-types-and-reasons)).

![](assets/sending_logs.png)

Es steht auch ein entsprechender Bericht zur Verfügung. Dieser Bericht zeigt die Gesamtheit aller Statistiken zu bei Sendungen aufgetretenen Hard- und Softbounces und der automatischen Bounce-Verarbeitung. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/bounce-summary.md).

## Typen und Ursachen für fehlgeschlagene Sendungen  {#delivery-failure-types-and-reasons}

Bei Fehlschlägen des Versands gibt es drei Typen von Fehlern:

* **Hard**: Dieser Fehlertyp tritt bei einer ungültigen Adresse auf. Fehlermeldung, die explizit eine ungültige Adresse anzeigt, beispielsweise &quot;Benutzer unbekannt&quot;.
* **Soft**: Fehler, der eventuell nur vorübergehend auftritt oder der nicht qualifiziert werden konnte, beispielsweise &quot;Ungültige Domain&quot;, &quot;Postfach voll&quot;.
* **Ignoriert**: Vorübergehender Fehler, beispielsweise &quot;Out of office&quot; oder technischer Fehler bei Absendern vom Typ &quot;Postmaster&quot;.

Mögliche Ursachen für fehlgeschlagene Sendungen sind:

* **[!UICONTROL User unknown]** (Harttyp): die Adresse nicht vorhanden ist. An dieses Profil werden keine weiteren Zustellversuche unternommen.
* **[!UICONTROL Quarantined address]** (Harttyp): die Adresse wurde in Quarantäne gesetzt.
* **[!UICONTROL Unreachable]** (Weich/fest): in der Meldungskette (z. B. Domäne vorübergehend unerreichbar) ist ein Versand aufgetreten. Entsprechend dem vom Provider zurückgegebenen Fehler wird die Adresse direkt unter Quarantäne gestellt oder der Zustellversuch wiederholt, bis Campaign einen Fehler empfängt, der den Quarantänestatus auslöst oder bis die Fehleranzahl 5 erreicht hat.
* **[!UICONTROL Address empty]** (Harttyp): die Adresse nicht definiert ist.
* **[!UICONTROL Mailbox full]** (Weichtyp): der Posteingang dieses Benutzers ist voll und kann keine weiteren Nachrichten akzeptieren. Die Adresse kann aus der Quarantäne genommen werden, um einen erneuten Zustellversuch zu unternehmen. Diese Liste wird automatisch nach 30 Tagen entfernt.

   In order for the address to be automatically removed from the list of quarantined addresses, the **[!UICONTROL Database cleanup]** technical workflow must be started.

* **[!UICONTROL Refused]** (Weich/fest): die Adresse wurde aufgrund einer Sicherheitsmeldung als Spam-Bericht in Quarantäne gesetzt. Entsprechend dem vom Provider zurückgegebenen Fehler wird die Adresse direkt unter Quarantäne gestellt oder der Zustellversuch wiederholt, bis Campaign einen Fehler empfängt, der den Quarantänestatus auslöst oder bis die Fehleranzahl 5 erreicht hat.
* **[!UICONTROL Duplicate]**: die Adresse wurde bereits in der Segmentierung erkannt.
* **[!UICONTROL Not defined]** (Weichtyp): die Adresse ist qualifiziert, da die Fehler noch nicht inkrementiert wurden.

   Dieser Fehlertyp tritt auf, wenn der Server eine bis dahin unbekannte Fehlermeldung sendet: Hierbei kann es sich um einen einmaligen Fehler handeln. Sollte er sich jedoch wiederholen, wird der Fehlerzähler erhöht, was die zuständigen technischen Mitarbeiter auf das Problem aufmerksam macht.

* **[!UICONTROL Error ignored]**: die Adresse ist in der Whitelist und eine E-Mail wird in jedem Fall gesendet.
* **[!UICONTROL Blacklisted address]**: die Adresse zum Zeitpunkt der Versendung auf der Blacklist war.
* **[!UICONTROL Account disabled]** (Weich/fest): Wenn der Internet Access Provider (IAP) eine längere Inaktivität feststellt, kann er das Konto des Benutzers schließen: Versände an die Adresse des Benutzers sind dann nicht mehr möglich. The Soft or Hard type depends upon the type of error received: if the account is temporarily disabled due to six months of inactivity and can still be activated, the status **[!UICONTROL Erroneous]** will be assigned and the delivery will be tried again. Wenn das Konto permanent deaktiviert ist, wird es sofort unter Quarantäne gestellt.
* **[!UICONTROL Not connected]**: das Handy des Profils beim Senden der Nachricht ausgeschaltet oder nicht mit dem Netzwerk verbunden ist.
* **[!UICONTROL Invalid domain]** (Weichtyp): Die Domäne der E-Mail-Adresse ist nicht korrekt oder nicht mehr vorhanden. An dieses Profil werden wiederholte Zustellversuche unternommen, bis die Fehleranzahl 5 erreicht. Danach wird der Datensatz in den Quarantänestatus versetzt und die Zustellversuche werden eingestellt.
* **[!UICONTROL Text too long]**: die Anzahl der Zeichen in der SMS überschreitet den Grenzwert. Weiterführende Informationen dazu finden Sie im Abschnitt [Kodierung, Länge und Tansliteration von SMS](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).
* **[!UICONTROL Character not supported by encoding]**: die SMS-Nachricht enthält ein oder mehrere Zeichen, die von der Kodierung nicht unterstützt werden. Weiterführende Informationen dazu finden Sie im Abschnitt [Zeichensatztabelle - GSM-Standard](../../administration/using/configuring-sms-channel.md#table-of-characters---gsm-standard).

## Weitere Zustellversuche nach einem vorübergehend fehlgeschlagenen Versand  {#retries-after-a-delivery-temporary-failure}

Wenn die Zustellung einer Nachricht wegen eines vorübergehenden Fehlers des Typs **Ignoriert** fehlschlägt, werden während der Versandlaufzeit weitere Zustellversuche unternommen. Weiterführende Informationen zu Fehlertypen finden Sie im Abschnitt [Typen und Ursachen für fehlgeschlagene Sendungen](#delivery-failure-types-and-reasons).

Nach der Aktualisierung auf das [Adobe Campaign Enhanced MTA](https://helpx.adobe.com/de/campaign/kb/campaign-enhanced-mta.html)werden die Einstellungen der **Weitere Zustellversuche** in der Kampagne ignoriert. Die Anzahl der weitere Zustellversuche (wie viele weitere Zustellversuche am Tag nach dem Start des Versands ausgeführt werden sollten) und die minimale Verzögerung zwischen den weiteren Zustellversuchen werden durch die erweiterte MTA verwaltet, basierend darauf, wie gut eine IP sowohl historisch als auch aktuell in einer bestimmten Domäne läuft.

Um die Dauer eines Versands zu ändern, gehen Sie zu den erweiterten Parametern des Versands oder der Versandvorlage und bearbeiten Sie das **[!UICONTROL Delivery duration]** Feld des Abschnitts &quot; [Gültigkeitsdauer](../../administration/using/configuring-email-channel.md#validity-period-parameters) &quot;.

>[!IMPORTANT]
>
>Once upgraded to the [Adobe Campaign Enhanced MTA](https://helpx.adobe.com/de/campaign/kb/campaign-enhanced-mta.html), the **[!UICONTROL Delivery duration]** parameter in your Campaign deliveries is used only if set to 3.5 days or less. Wenn Sie einen Wert von mehr als 3,5 Tagen definieren, wird dieser nicht berücksichtigt.

Wenn Sie z. B. möchten, dass weitere Zustellversuche für einen Versand nach einem Tag anhalten, können Sie die Dauer des Versands auf **1d** festlegen. Die erweiterte MTA berücksichtigt diese Einstellung, indem Sie Meldungen nach einem Tag in der Warteschlange wiederholen.

>[!NOTE]
>
>Sobald sich eine Nachricht 3,5 Tage lang in der Warteschlange der erweiterten MTA befindet und die Bereitstellung fehlgeschlagen ist, wird sie beendet und ihr Status wird von **[!UICONTROL Sent]** in **[!UICONTROL Failed]** den [Versandlogs](../../sending/using/monitoring-a-delivery.md#delivery-logs)aktualisiert.

<!--The default configuration allows five retries at one-hour intervals, followed by one retry per day for four days. The number of retries can be changed globally (contact your Adobe technical administrator) or for each delivery or delivery template (see [this section](../../administration/using/configuring-email-channel.md#sending-parameters)).-->

## Synchrone und asynchrone Fehler  {#synchronous-and-asynchronous-errors}

Ein Versand kann sofort fehlschlagen (synchroner Fehler) oder zu einem späteren Zeitpunkt nach dem Versand (asynchroner Fehler).

* **Synchroner Fehler**: Der vom Adobe-Campaign-Server angesprochene Remote-Server hat sofort eine Fehlermeldung zurückgegeben. Die Nachricht kann nicht an den Server des Profils gesendet werden.
* **Asynchroner Fehler**: Eine Bounce Message oder ein Statusbericht (SR) wird vom Remote-Server verzögert zurückgesendet. Asynchrone Fehler können bis zu eine Woche nach einem Versand auftreten.

## Bounce-Message-Qualifizierung  {#bounce-mail-qualification}

<!--Delivery failure error messages (or "SMTP bounce responses") are picked up by the Adobe Campaign platform and then processed and qualified as **Hard**, **Soft**, or **Ignored** using the **[!UICONTROL Delivery log qualification]** database.

//Delivery failure error messages (or "bounces") are picked up by the Adobe Campaign platform and qualified by the inMail process to enrich the list of email management rules.(applies to asynchronous (out-of-band) bounces)

This list is available to administrators only and contains all the rules used by Adobe Campaign to qualify delivery failures.-->

>[!IMPORTANT]
>
>Once upgraded to the Enhanced MTA, the bounce qualifications in the Campaign **[!UICONTROL Message qualification]** table are no longer used.

Bei Fehlermeldungen, bei denen der synchrone Versand fehlgeschlagen ist, bestimmt der erweiterte MTA den Bounce-Typ und die Qualifizierung und sendet diese Informationen an Campaign zurück. Weitere Informationen zum Adobe Campaign Enhanced MTA finden Sie in diesem [Dokument](https://helpx.adobe.com/de/campaign/kb/campaign-enhanced-mta.html).

Asynchrone Absprünge sind nach wie vor durch den InMail-Prozess durch die **[!UICONTROL Inbound email]** Regeln qualifiziert. Um auf diese Regeln zuzugreifen, klicken Sie auf das **[!UICONTROL Adobe Campaign]** Logo oben links, wählen Sie dann aus **[!UICONTROL Administration > Channels > Email > Email processing rules]** und wählen Sie **[!UICONTROL Bounce mails]**. For more on this rule, refer to this [section](../../administration/using/configuring-email-channel.md#email-processing-rules).

<!--Bounces can have the following qualification statuses:

* **[!UICONTROL To qualify]**: the bounce mail needs to be qualified. Qualification must be done by the Deliverability team to ensure that the platform deliverability functions correctly. As long as it is not qualified, the bounce mail is not used to enrich the list of email processing rules.
* **[!UICONTROL Keep]**: the bounce mail was qualified and will be used by the **Update for deliverability** workflow to be compared to existing email processing rules and enrich the list.
* **[!UICONTROL Ignore]**: the bounce mail was qualified but will not be used by the **Update for deliverability** workflow. So it will not be sent to the client instances.

To list the various bounces and their associated error types et reasons, click the **[!UICONTROL Adobe Campaign]** logo, in the top left, then select **[!UICONTROL Administration > Channels > Quarantines > Message qualification]**.

![](assets/qualification.png)-->

## Zustellbarkeit von Mails durch die Anmeldung mit zweifacher Bestätigung optimieren {#optimizing-mail-deliverability-with-double-opt-in-mechanism}

Die Anmeldung mit zweifacher Bestätigung zählt zu den Best Practices beim E-Mail-Versand. Die Plattform wird dadurch vor falschen oder ungültigen E-Mail-Adressen und Spambots geschützt, wodurch Spam-Beschwerden verhindert werden.

Das Prinzip dahinter ist folgendes: Der Besucher füllt ein Formular auf einer Online-Landingpage aus, erhält dann eine E-Mail und muss den Bestätigungs-Link anklicken, um die Anmeldung abzuschließen. Erst dann wird er als ‘Profil&#39; in der Campaign-Datenbank gespeichert.

Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/setting-up-a-double-opt-in-process.md).
